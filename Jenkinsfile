pipeline
{
    agent any

    stages
    {
        stage('git clone')
        {
           steps{
                    echo "hellow world"
                    git credentialsId: 'e819d4b4-e0d6-4e8d-b03d-6e4148ad227c', url: 'https://github.com/mohansai25/SeleniumWithCucucumber.git'

                }

        }
        stage('mvn build')
        {
           steps{
                    sh ' mvn verify'
                    sh ' mvn compile'
                }

        }
        stage('Cucumber')
        {
           steps{
                   cucumber fileIncludePattern: '**/*.json', sortingMethod: 'ALPHABETICAL'

                }

        }

    }
}