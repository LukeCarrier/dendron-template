---
id: ydvcBHDK9gcghuHX
title: Windows
desc: ''
updated: 1627665781202
created: 1627594346414
---


## Github Actions

The github actions for windows can be finicky and there are sometimes issues there that don't show up locally. If you are debugging a github actions windows integration test issue and need to actually run the integration test using github action, we have a specific workflow [here](https://github.com/dendronhq/dendron/blob/master/.github/workflows/ci-windows-test.yml#L1:L1) that triggers when you push to a branch matching the following pattern: `chore/windows-ci-*`

This is an example of a [pull request](https://github.com/dendronhq/dendron/pull/1060) that makes use of this

## Skipping Windows Test

In the cases when a windows tests will not pass or is flaky, an emergency option is to use the following test runner for the plugin: [runTestButSkipForWindows](https://github.com/dendronhq/dendron/blob/chore/windows-ci-hashtags/packages/plugin-core/src/test/testUtilsV3.ts#L405:L405)