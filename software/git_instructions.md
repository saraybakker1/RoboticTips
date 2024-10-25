Some rules to stick to when working (with multiple people) on a repository:
1. Protect the main branch to only allow for changes via pull-request (see point 2). 
2. Create a new branch (preferably named ft_<name_of_feature>) branching off to the main branch, and do a [pull-request](https://docs.github.com/en/enterprise-server@3.12/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) to merge your branch with main.
3. Add Pytests to the github pull-request using [Github actions](https://docs.github.com/en/actions/use-cases-and-examples/building-and-testing/building-and-testing-python).
   Add a pytest that runs all examples, to avoid breaking code (of others). This will also check if the dependencies can be installed.
4. Try to avoid ROS-dependencies in packages, unless explicitly needed. This will make the installation much cleaner and easier for people to use in Ubuntu20/22/Windows.
