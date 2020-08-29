#!groovy
node('master') {
def JobStatus = "Job Started"
def JobError = ""
echo "${JobStatus}"
try {   
	            stage("Stage 1") 
				{
					echo "Stage 1 Testing"
				}
				def PkgNUMBER = env.BUILD_NUMBER
				stage("Stage 2") 
				{
					echo "${PkgNUMBER}"
					echo "Stage 2 Completed"
				}
		JobStatus = 'Job Completed'
	}
catch(error)
	{
				JobError = error
				JobStatus = "Failed"
				echo "Error:" + ${JobError}
	}
finally
	{
				def email_body='Job status - ' + JobStatus
				Email(email_body) 
	}
}
def Email(mail_body){
    mail body: mail_body,
        from: 'atan.chatterjee@gmail.com',
        subject: 'Testing Jenkins Job Status',
        to: 'chatterji.atanu@gmail.com'
}