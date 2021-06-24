# Board of Ethics file management

## Purpose

The Board of Ethics uses a series of interconnected PDFs to manage documents through SharePoint. This functionality is not available on the WordPress platform, and due to timeline constraints will not be able to be replicated in time for a June 14th 2021 SharePoint shutdown date. This repo facilitates the direct upload of PDFs to specific Ethics Board public folder paths, so that old PDFs will not be lost, and new PDFs can be maintained in the short term.

## How to use

1. Use the GitHub interface to upload a new file to the default (staging) branch. 
2. After a successful deploy to staging (e.g. https://staging-www.phila.gov/ethicsboard/Advisory%20Opinions/bd.op.2006-001.pdf) create Pull Request into `main`. 
3. Merge pull request to publish file(s). 


Github is a tool that allows for version management of documents. We will be utilizing this tool for handling documents for both OHR and BOE at the following links:

https://github.com/CityOfPhiladelphia/phila.gov-boe-aws-deploy/

## Upload a file
In order to upload a file, navigate to your repository home page listed above and confirm that you are in the “staging” environment as indicated by the button in the top left of the page.

![image1](https://user-images.githubusercontent.com/16737142/123292728-57298100-d4e1-11eb-90c7-39dad6bf5203.png)

After confirming the environment, simply drag and drop your file(s) onto the page, which will bring you to a “new commit” page listing the file(s) added. A commit is the breadcrumb that Github uses to track changes made to the repository. From this view, give the commit a descriptive name such as “Adding file X”. Then click the “Commit changes” button.

![image2](https://user-images.githubusercontent.com/16737142/123292799-66a8ca00-d4e1-11eb-8fcb-64a708ec61c1.png)

At this point, the commit is now confirmed in the staging environment, as indicated by the status on the home page.

![image11](https://user-images.githubusercontent.com/16737142/123294936-4843ce00-d4e3-11eb-9a1d-31e35871abe7.png)

The file(s) will now be made available at the staging url associated with your repository. Navigate to the “Merge into main” section to copy the file(s) from staging to production.

## Delete file

In order to delete a file, navigate to the file in the folder structure and click on the file link.

![image3](https://user-images.githubusercontent.com/16737142/123292850-732d2280-d4e1-11eb-9077-6e9d57220a94.png)

From this view, click the trash icon on the right. This will create a new commit to the branch. Click “Commit changes” to confirm deleting the file from the branch.

![image4](https://user-images.githubusercontent.com/16737142/123292884-7a543080-d4e1-11eb-9fb0-19475d0a1e5e.png)

After the file has been deleted, make sure to follow the instructions at “Merge into main” to apply to production.

## Modify file

Follow the instructions in “Upload file”. Rather than adding a new file, the older version of the file will be replaced with the new version. Make sure to follow the steps in “Merge into main” for the change to be reflected on the production site.

## Merge into main

In order to copy your files from staging to production, you will need to create and merge a pull request. To start, click on the “Pull requests” tab from your 
repository home page.

![image5](https://user-images.githubusercontent.com/16737142/123292926-84762f00-d4e1-11eb-877a-8d7be4ea164d.png)

From this page, click on the “new pull request” button on the top right of the page, which will bring you to the “Compare changes” page.

![image10](https://user-images.githubusercontent.com/16737142/123294660-0c106d80-d4e3-11eb-85c5-75c54237153e.png)

From here, you will set the “base” branch (the branch that will be modified), and the “compare” branch (the branch with the changes that will apply to the base branch). For this use case, set the base branch to “main” and allow the compare branch to remain “staging”. You should then see any commit messages that have not been merged below.

![image6](https://user-images.githubusercontent.com/16737142/123292985-9061f100-d4e1-11eb-9e71-7ae9c91b502a.png)

If the commit list looks accurate, click the “Create pull request” button and click it again in the 
“Open a pull request” page.

![image7](https://user-images.githubusercontent.com/16737142/123293000-9657d200-d4e1-11eb-927e-2c9769f46023.png)

At this point, a “pull request” (a request to modify one branch from another) has been created, but has not applied to the base branch. In order to apply the change, click the “Merge pull request” button.

![image8](https://user-images.githubusercontent.com/16737142/123293024-9eb00d00-d4e1-11eb-8aa6-f6cc07eb6e34.png)

Lastly, you will need to confirm the merge with the “Confirm merge” button.

![image9](https://user-images.githubusercontent.com/16737142/123293045-a374c100-d4e1-11eb-8d60-ad4ba39ef38f.png)

## Review files on staging

After adding, modifying, or deleting a file, you can confirm that your changes have been applied by reviewing in the staging phila.gov environment. For this repository, all files are uploaded at the top directory of https://staging-www.phila.gov/ethicsboard/advisory%20opinions/ or https://staging-www.phila.gov/ethicsboard/settlement%20agreements followed by the name of the file.

## Review files on production

After adding, modifying, or deleting a file, you can confirm that your changes have been applied by reviewing in the staging phila.gov environment. For this repository, all files are uploaded at the top directory of https://www.phila.gov/ethicsboard/advisory%20opinions/ or https://www.phila.gov/ethicsboard/settlement%20agreements followed by the name of the file.
