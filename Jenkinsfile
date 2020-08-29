
node('master') {

echo "Current workspace is ${env.WORKSPACE}"
echo "Current workspace is $WORKSPACE"

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
				 
				echo "Job status -  + ${JobStatus}"
	}
}
