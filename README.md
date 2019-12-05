# gh-actions-samples

The purpose of this repo is to answer questions one might have about github actions, through examples. After you have seen the examples in this repo, you may want to also run them which is why **anyone can test the actions by creating an issue that contains the action file's name (without the extension)**.

Each action will run when it detects an issue with it's name was created. It does this through the help of the [`issues`](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/events-that-trigger-workflows#issues-event-issues) event.

---

# Ready:question: [Go:bangbang:](#I-want-to)
<br/>

## I want to...
- :speaking_head: [Pass a parameter to a step...](#passing-parameters)

## Passing Parameters...
- :outbox_tray: [Using an environment variable...](https://github.com/smac89/gh-actions-samples#creating-environment-variables)

## Creating environment variables
:speech_balloon: There are two ways to create [environment variables](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/using-environment-variables#about-environment-variables):

- :information_source: By using the env keyword on the _entire workflow_, a _job_ or a _step_. See [`env`](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/workflow-syntax-for-github-actions#env). ***Note: This variable CAN be used in the same place where it was created***
- :information_source: Through Github Actions [`set-env`](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/development-tools-for-github-actions#set-an-environment-variable-set-env). This will create an environment variable that can be used by all subsequent steps. ***Note: Variables created this way CANNOT be used in the same step where they were created, however following steps can see that variable***
  - :running_woman: **See [`step_param_from_env.yml`](https://github.com/smac89/gh-actions-samples/blob/898cfc848d9a0aa073416ea615ce880ed7488c0e/.github/workflows/step_param_from_env.yml#L17)**
