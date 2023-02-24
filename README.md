# bug-renovate-poetry-python-version

## Introduction

### Observed behavior

This is a mono repo. 
Renovate uses same Python version for both projects.

### Expected behavior

Each projects use its own Python version defined in pyproject.toml.

In this case,

- api-python is using python = "3.11.x"
- hm-locust is using python = "3.10.x"

## Ticket

Opened the ticket at https://github.com/renovatebot/renovate/issues/20615

## Renovate Log

<details>
  <summary>Click to expand</summary>

  ```shell
DEBUG: No dangling containers to remove
INFO: Repository started
{
  "renovateVersion": "34.152.4"
}
DEBUG: Using localDir: /mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version
DEBUG: PackageFiles.clear() - Package files deleted
DEBUG: initRepo("Hongbo-Miao/bug-renovate-poetry-python-version")
DEBUG: Using queue: host=api.github.com, concurrency=10
DEBUG: Hongbo-Miao/bug-renovate-poetry-python-version default branch = main
DEBUG: Using app token for git init
DEBUG: RepoCacheBase.load() - expecting data of type 'string' received 'object' instead - skipping
DEBUG: Resetting npmrc
DEBUG: checkOnboarding()
DEBUG: isOnboarded()
DEBUG: findFile(renovate.json)
DEBUG: Initializing git repository into /mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version
DEBUG: Performing blobless clone
DEBUG: git clone completed
{
  "durationMs": 906
}
DEBUG: latest repository commit
{
  "latestCommit": {
    "hash": "61ed04784dcaa32656e6df5588f6796df4b1e292",
    "date": "2023-02-25T01:40:37+09:00",
    "message": "docs",
    "refs": "HEAD -> main, origin/main, origin/HEAD",
    "body": "",
    "author_name": "Hongbo Miao",
    "author_email": "3375461+Hongbo-Miao@users.noreply.github.com"
  }
}
DEBUG: findFile(renovate.json5)
DEBUG: Config file exists, fileName: renovate.json5
DEBUG: Retrieving issueList
DEBUG: Retrieved 0 issues
DEBUG: Repo is onboarded
DEBUG: Found renovate.json5 config file
DEBUG: Repository config
{
  "fileName": "renovate.json5",
  "config": {
    "extends": [
      "config:base"
    ]
  }
}
DEBUG: migrateAndValidate()
DEBUG: No config migration necessary
DEBUG: massaged config
{
  "config": {
    "extends": [
      "github>whitesource/merge-confidence:beta",
      "config:base"
    ]
  }
}
DEBUG: migrated config
{
  "config": {
    "extends": [
      "github>whitesource/merge-confidence:beta",
      "config:base"
    ]
  }
}
DEBUG: Setting hostRules from config
DEBUG: Found repo ignorePaths
{
  "ignorePaths": [
    "**/node_modules/**",
    "**/bower_components/**",
    "**/vendor/**",
    "**/examples/**",
    "**/__tests__/**",
    "**/test/**",
    "**/tests/**",
    "**/__fixtures__/**"
  ]
}
DEBUG: Using queue: host=api.github.com, concurrency=10
DEBUG: No vulnerability alerts found
DEBUG: No vulnerability alerts found
DEBUG: findIssue(Dependency Dashboard)
DEBUG: No baseBranches
DEBUG: extract()
DEBUG: Setting current branch to main
DEBUG: latest commit
{
  "branchName": "main",
  "latestCommitDate": "2023-02-25T01:40:37+09:00"
}
DEBUG: Using file match: (^|/)tasks/[^/]+\.ya?ml$ for manager ansible
DEBUG: Using file match: (^|/)requirements\.ya?ml$ for manager ansible-galaxy
DEBUG: Using file match: (^|/)galaxy\.ya?ml$ for manager ansible-galaxy
DEBUG: Using file match: (^|/)\.tool-versions$ for manager asdf
DEBUG: Using file match: azure.*pipelines?.*\.ya?ml$ for manager azure-pipelines
DEBUG: Using file match: (^|/)batect(-bundle)?\.yml$ for manager batect
DEBUG: Using file match: (^|/)batect$ for manager batect-wrapper
DEBUG: Using file match: (^|/)WORKSPACE(|\.bazel)$ for manager bazel
DEBUG: Using file match: \.bzl$ for manager bazel
DEBUG: Using file match: (^|\/)\.bazelversion$ for manager bazelisk
DEBUG: Using file match: (^|/)\.?bitbucket-pipelines\.ya?ml$ for manager bitbucket-pipelines
DEBUG: Using file match: buildkite\.ya?ml for manager buildkite
DEBUG: Using file match: \.buildkite/.+\.ya?ml$ for manager buildkite
DEBUG: Using file match: (^|/)Gemfile$ for manager bundler
DEBUG: Using file match: \.cake$ for manager cake
DEBUG: Using file match: (^|/)Cargo\.toml$ for manager cargo
DEBUG: Using file match: (^|/)\.circleci/config\.yml$ for manager circleci
DEBUG: Using file match: (^|/)cloudbuild\.ya?ml for manager cloudbuild
DEBUG: Using file match: (^|/)Podfile$ for manager cocoapods
DEBUG: Using file match: (^|/)([\w-]*)composer\.json$ for manager composer
DEBUG: Using file match: (^|/)conanfile\.(txt|py)$ for manager conan
DEBUG: Using file match: (^|/)(?:deps|bb)\.edn$ for manager deps-edn
DEBUG: Using file match: (^|/)(?:docker-)?compose[^/]*\.ya?ml$ for manager docker-compose
DEBUG: Using file match: (^|/|\.)Dockerfile$ for manager dockerfile
DEBUG: Using file match: (^|/)Dockerfile[^/]*$ for manager dockerfile
DEBUG: Using file match: (^|/)\.drone\.yml$ for manager droneci
DEBUG: Using file match: (^|/)fleet\.ya?ml for manager fleet
DEBUG: Using file match: (^|\/)flux-system\/(?:.+\/)?gotk-components\.yaml$ for manager flux
DEBUG: Using file match: (^|\/)\.fvm\/fvm_config\.json$ for manager fvm
DEBUG: Using file match: (^|/)\.gitmodules$ for manager git-submodules
DEBUG: Using file match: ^(workflow-templates|\.github\/workflows)\/[^/]+\.ya?ml$ for manager github-actions
DEBUG: Using file match: (^|\/)action\.ya?ml$ for manager github-actions
DEBUG: Using file match: \.gitlab-ci\.yml$ for manager gitlabci
DEBUG: Using file match: \.gitlab-ci\.yml$ for manager gitlabci-include
DEBUG: Using file match: (^|/)go\.mod$ for manager gomod
DEBUG: Using file match: \.gradle(\.kts)?$ for manager gradle
DEBUG: Using file match: (^|\/)gradle\.properties$ for manager gradle
DEBUG: Using file match: (^|\/)gradle\/.+\.toml$ for manager gradle
DEBUG: Using file match: \.versions\.toml$ for manager gradle
DEBUG: Using file match: (^|\/)versions.props$ for manager gradle
DEBUG: Using file match: (^|\/)versions.lock$ for manager gradle
DEBUG: Using file match: (^|/)gradle/wrapper/gradle-wrapper\.properties$ for manager gradle-wrapper
DEBUG: Using file match: (^|/)requirements\.yaml$ for manager helm-requirements
DEBUG: Using file match: (^|/)values\.yaml$ for manager helm-values
DEBUG: Using file match: (^|/)helmfile\.yaml$ for manager helmfile
DEBUG: Using file match: (^|/)Chart\.yaml$ for manager helmv3
DEBUG: Using file match: (^|/)bin/hermit$ for manager hermit
DEBUG: Using file match: ^Formula/[^/]+[.]rb$ for manager homebrew
DEBUG: Using file match: \.html?$ for manager html
DEBUG: Using file match: (^|/)plugins\.(txt|ya?ml)$ for manager jenkins
DEBUG: Using file match: (^|/)jsonnetfile\.json$ for manager jsonnet-bundler
DEBUG: Using file match: ^.+\.main\.kts$ for manager kotlin-script
DEBUG: Using file match: (^|/)kustomization\.ya?ml$ for manager kustomize
DEBUG: Using file match: (^|/)project\.clj$ for manager leiningen
DEBUG: Using file match: (^|/|\.)pom\.xml$ for manager maven
DEBUG: Using file match: ^(((\.mvn)|(\.m2))/)?settings\.xml$ for manager maven
DEBUG: Using file match: (^|\/).mvn/wrapper/maven-wrapper.properties$ for manager maven-wrapper
DEBUG: Using file match: (^|/)package\.js$ for manager meteor
DEBUG: Using file match: (^|\/)Mintfile$ for manager mint
DEBUG: Using file match: (^|/)mix\.exs$ for manager mix
DEBUG: Using file match: (^|\/)flake\.nix$ for manager nix
DEBUG: Using file match: (^|/)\.node-version$ for manager nodenv
DEBUG: Using file match: (^|/)package\.json$ for manager npm
DEBUG: Using file match: \.(?:cs|fs|vb)proj$ for manager nuget
DEBUG: Using file match: \.(?:props|targets)$ for manager nuget
DEBUG: Using file match: (^|\/)dotnet-tools\.json$ for manager nuget
DEBUG: Using file match: (^|\/)global\.json$ for manager nuget
DEBUG: Using file match: (^|/)\.nvmrc$ for manager nvm
DEBUG: Using file match: (^|/)src/main/features/.+\.json$ for manager osgi
DEBUG: Using file match: (^|/)([\w-]*)requirements\.(txt|pip)$ for manager pip_requirements
DEBUG: Using file match: (^|/)setup\.py$ for manager pip_setup
DEBUG: Using file match: (^|/)Pipfile$ for manager pipenv
DEBUG: Using file match: (^|/)pyproject\.toml$ for manager poetry
DEBUG: Using file match: (^|/)\.pre-commit-config\.yaml$ for manager pre-commit
DEBUG: Using file match: (^|/)pubspec\.ya?ml$ for manager pub
DEBUG: Using file match: (^|\/)Puppetfile$ for manager puppet
DEBUG: Using file match: (^|/)\.python-version$ for manager pyenv
DEBUG: Using file match: (^|/)\.ruby-version$ for manager ruby-version
DEBUG: Using file match: \.sbt$ for manager sbt
DEBUG: Using file match: project/[^/]*.scala$ for manager sbt
DEBUG: Using file match: (^|/)setup\.cfg$ for manager setup-cfg
DEBUG: Using file match: (^|/)Package\.swift for manager swift
DEBUG: Using file match: \.tf$ for manager terraform
DEBUG: Using file match: (^|/)\.terraform-version$ for manager terraform-version
DEBUG: Using file match: (^|/)terragrunt\.hcl$ for manager terragrunt
DEBUG: Using file match: (^|/)\.terragrunt-version$ for manager terragrunt-version
DEBUG: Using file match: \.tflint\.hcl$ for manager tflint-plugin
DEBUG: Using file match: ^\.travis\.yml$ for manager travis
DEBUG: Using file match: (^|/)\.vela\.ya?ml$ for manager velaci
DEBUG: Using file match: ^\.woodpecker(?:\/[^/]+)?\.ya?ml$ for manager woodpecker
DEBUG: Matched 2 file(s) for manager poetry: api-python/pyproject.toml, hm-locust/pyproject.toml
DEBUG: Found poetry package files
DEBUG: Found 2 package file(s)
INFO: Dependency extraction complete
{
  "baseBranch": "main",
  "stats": {
    "managers": {
      "poetry": {
        "fileCount": 2,
        "depCount": 15
      }
    },
    "total": {
      "fileCount": 2,
      "depCount": 15
    }
  }
}
DEBUG: Using queue: host=pypi.org, concurrency=10
DEBUG: PackageFiles.add() - Package file saved for base branch
{
  "baseBranch": "main"
}
DEBUG: Package releases lookups complete
{
  "baseBranch": "main"
}
DEBUG: branchifyUpgrades
DEBUG: detectSemanticCommits()
DEBUG: getCommitMessages
DEBUG: semanticCommits: detected "unknown"
DEBUG: semanticCommits: disabled
DEBUG: 2 flattened updates found: python-dotenv, python-dotenv
DEBUG: Returning 1 branch(es)
DEBUG: config.repoIsOnboarded=true
DEBUG: packageFiles with updates
{
  "baseBranch": "main",
  "config": {
    "poetry": [
      {
        "deps": [
          {
            "depName": "Flask",
            "depType": "dependencies",
            "currentValue": "2.2.3",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "2.2.3",
            "packageName": "flask",
            "versioning": "pep440",
            "depIndex": 0,
            "updates": [],
            "warnings": [],
            "registryUrl": "https://pypi.org/pypi",
            "homepage": "https://palletsprojects.com/p/flask",
            "changelogUrl": "https://flask.palletsprojects.com/changes/",
            "currentVersion": "2.2.3",
            "fixedVersion": "2.2.3"
          },
          {
            "depName": "Flask-APScheduler",
            "depType": "dependencies",
            "currentValue": "1.12.4",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "1.12.4",
            "packageName": "flask-apscheduler",
            "versioning": "pep440",
            "depIndex": 1,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/viniciuschiele/flask-apscheduler",
            "registryUrl": "https://pypi.org/pypi",
            "currentVersion": "1.12.4",
            "fixedVersion": "1.12.4"
          },
          {
            "depName": "Flask-Cors",
            "depType": "dependencies",
            "currentValue": "3.0.10",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "3.0.10",
            "packageName": "flask-cors",
            "versioning": "pep440",
            "depIndex": 2,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/corydolphin/flask-cors",
            "registryUrl": "https://pypi.org/pypi",
            "currentVersion": "3.0.10",
            "fixedVersion": "3.0.10"
          },
          {
            "depName": "confluent-kafka",
            "depType": "dependencies",
            "currentValue": "2.0.2",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "2.0.2",
            "versioning": "pep440",
            "depIndex": 3,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/confluentinc/confluent-kafka-python",
            "registryUrl": "https://pypi.org/pypi",
            "currentVersion": "2.0.2",
            "fixedVersion": "2.0.2"
          },
          {
            "depName": "flask-sock",
            "depType": "dependencies",
            "currentValue": "0.6.0",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "0.6.0",
            "versioning": "pep440",
            "depIndex": 4,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/miguelgrinberg/flask-sock",
            "registryUrl": "https://pypi.org/pypi",
            "currentVersion": "0.6.0",
            "fixedVersion": "0.6.0"
          },
          {
            "depName": "gunicorn",
            "depType": "dependencies",
            "currentValue": "20.1.0",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "20.1.0",
            "versioning": "pep440",
            "depIndex": 5,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/benoitc/gunicorn",
            "registryUrl": "https://pypi.org/pypi",
            "homepage": "https://gunicorn.org",
            "currentVersion": "20.1.0",
            "fixedVersion": "20.1.0"
          },
          {
            "depName": "python-dotenv",
            "depType": "dependencies",
            "currentValue": "0.21.1",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "0.21.1",
            "versioning": "pep440",
            "depIndex": 6,
            "updates": [
              {
                "bucket": "major",
                "newVersion": "1.0.0",
                "newValue": "1.0.0",
                "releaseTimestamp": "2023-02-24T06:46:36.000Z",
                "newMajor": 1,
                "newMinor": 0,
                "updateType": "major",
                "branchName": "renovate/python-dotenv-1.x"
              }
            ],
            "warnings": [],
            "sourceUrl": "https://github.com/theskumar/python-dotenv",
            "registryUrl": "https://pypi.org/pypi",
            "currentVersion": "0.21.1",
            "isSingleVersion": true,
            "fixedVersion": "0.21.1"
          },
          {
            "depName": "sentry-sdk",
            "depType": "dependencies",
            "currentValue": "1.15.0",
            "managerData": {
              "nestedVersion": true
            },
            "datasource": "pypi",
            "lockedVersion": "1.15.0",
            "versioning": "pep440",
            "depIndex": 7,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/getsentry/sentry-python",
            "registryUrl": "https://pypi.org/pypi",
            "changelogUrl": "https://github.com/getsentry/sentry-python/blob/master/CHANGELOG.md",
            "currentVersion": "1.15.0",
            "fixedVersion": "1.15.0"
          },
          {
            "depName": "poethepoet",
            "depType": "dev",
            "currentValue": "0.18.1",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "0.18.1",
            "versioning": "pep440",
            "depIndex": 8,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/nat-n/poethepoet",
            "registryUrl": "https://pypi.org/pypi",
            "currentVersion": "0.18.1",
            "fixedVersion": "0.18.1"
          },
          {
            "depName": "pytest",
            "depType": "dev",
            "currentValue": "7.2.1",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "7.2.1",
            "versioning": "pep440",
            "depIndex": 9,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/pytest-dev/pytest",
            "registryUrl": "https://pypi.org/pypi",
            "homepage": "https://docs.pytest.org/en/latest/",
            "changelogUrl": "https://docs.pytest.org/en/stable/changelog.html",
            "currentVersion": "7.2.1",
            "fixedVersion": "7.2.1"
          },
          {
            "depName": "pytest-cov",
            "depType": "dev",
            "currentValue": "4.0.0",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "4.0.0",
            "versioning": "pep440",
            "depIndex": 10,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/pytest-dev/pytest-cov",
            "registryUrl": "https://pypi.org/pypi",
            "changelogUrl": "https://pytest-cov.readthedocs.io/en/latest/changelog.html",
            "currentVersion": "4.0.0",
            "fixedVersion": "4.0.0"
          }
        ],
        "lockFiles": [
          "api-python/poetry.lock"
        ],
        "packageFile": "api-python/pyproject.toml",
        "constraints": {
          "python": "3.11.x"
        }
      },
      {
        "deps": [
          {
            "depName": "locust",
            "depType": "dependencies",
            "currentValue": "2.14.2",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "2.14.2",
            "versioning": "pep440",
            "depIndex": 0,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/locustio/locust",
            "registryUrl": "https://pypi.org/pypi",
            "homepage": "https://locust.io/",
            "currentVersion": "2.14.2",
            "fixedVersion": "2.14.2"
          },
          {
            "depName": "python-dotenv",
            "depType": "dependencies",
            "currentValue": "0.21.1",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "0.21.1",
            "versioning": "pep440",
            "depIndex": 1,
            "updates": [
              {
                "bucket": "major",
                "newVersion": "1.0.0",
                "newValue": "1.0.0",
                "releaseTimestamp": "2023-02-24T06:46:36.000Z",
                "newMajor": 1,
                "newMinor": 0,
                "updateType": "major",
                "branchName": "renovate/python-dotenv-1.x"
              }
            ],
            "warnings": [],
            "sourceUrl": "https://github.com/theskumar/python-dotenv",
            "registryUrl": "https://pypi.org/pypi",
            "currentVersion": "0.21.1",
            "isSingleVersion": true,
            "fixedVersion": "0.21.1"
          },
          {
            "depName": "python-magic",
            "depType": "dependencies",
            "currentValue": "0.4.27",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "0.4.27",
            "versioning": "pep440",
            "depIndex": 2,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/ahupp/python-magic",
            "registryUrl": "https://pypi.org/pypi",
            "currentVersion": "0.4.27",
            "fixedVersion": "0.4.27"
          },
          {
            "depName": "poethepoet",
            "depType": "dev",
            "currentValue": "0.18.1",
            "managerData": {
              "nestedVersion": false
            },
            "datasource": "pypi",
            "lockedVersion": "0.18.1",
            "versioning": "pep440",
            "depIndex": 3,
            "updates": [],
            "warnings": [],
            "sourceUrl": "https://github.com/nat-n/poethepoet",
            "registryUrl": "https://pypi.org/pypi",
            "currentVersion": "0.18.1",
            "fixedVersion": "0.18.1"
          }
        ],
        "lockFiles": [
          "hm-locust/poetry.lock"
        ],
        "packageFile": "hm-locust/pyproject.toml",
        "constraints": {
          "python": "3.10.x"
        }
      }
    ]
  }
}
DEBUG: detectSemanticCommits()
DEBUG: semanticCommits: returning "disabled" from cache
DEBUG: processRepo()
DEBUG: Processing 1 branch: renovate/python-dotenv-1.x
DEBUG: Calculating hourly PRs remaining
DEBUG: getPrList success
{
  "pullsTotal": 0,
  "requestsTotal": 1,
  "apiQuotaAffected": true
}
DEBUG: currentHourStart=2023-02-24T16:00:00.000+00:00
DEBUG: PR hourly limit remaining: 2
DEBUG: Calculating prConcurrentLimit (10)
DEBUG: getBranchPr(renovate/python-dotenv-1.x)
DEBUG: findPr(renovate/python-dotenv-1.x, undefined, open)
DEBUG: findPr(renovate/python-dotenv-1.x, undefined, closed)
DEBUG: 0 PRs are currently open
DEBUG: PR concurrent limit remaining: 10
DEBUG: Calculated maximum PRs remaining this run: 2
DEBUG: PullRequests limit = 2
DEBUG: Calculating hourly PRs remaining
DEBUG: currentHourStart=2023-02-24T16:00:00.000+00:00
DEBUG: PR hourly limit remaining: 2
DEBUG: Calculating branchConcurrentLimit (10)
DEBUG: 0 already existing branches found:
DEBUG: Branch concurrent limit remaining: 10
DEBUG: Calculated maximum branches remaining this run: 2
DEBUG: Branches limit = 2
DEBUG: syncBranchState()(branch="renovate/python-dotenv-1.x")
DEBUG: syncBranchState(): Branch cache not found, creating minimal branchState(branch="renovate/python-dotenv-1.x")
DEBUG: getBranchPr(renovate/python-dotenv-1.x)(branch="renovate/python-dotenv-1.x")
DEBUG: findPr(renovate/python-dotenv-1.x, undefined, open)(branch="renovate/python-dotenv-1.x")
DEBUG: findPr(renovate/python-dotenv-1.x, undefined, closed)(branch="renovate/python-dotenv-1.x")
DEBUG: branchExists=false(branch="renovate/python-dotenv-1.x")
DEBUG: dependencyDashboardCheck=undefined(branch="renovate/python-dotenv-1.x")
DEBUG: recreateClosed is false(branch="renovate/python-dotenv-1.x")
DEBUG: findPr(renovate/python-dotenv-1.x, Update dependency python-dotenv to v1, !open)(branch="renovate/python-dotenv-1.x")
DEBUG: prAlreadyExisted=false(branch="renovate/python-dotenv-1.x")
DEBUG: Checking schedule(at any time, null)(branch="renovate/python-dotenv-1.x")
DEBUG: No schedule defined(branch="renovate/python-dotenv-1.x")
DEBUG: Branch needs creating(branch="renovate/python-dotenv-1.x")
DEBUG: Using reuseExistingBranch: false(branch="renovate/python-dotenv-1.x")
DEBUG: Setting current branch to main(branch="renovate/python-dotenv-1.x")
DEBUG: latest commit(branch="renovate/python-dotenv-1.x")
{
  "branchName": "main",
  "latestCommitDate": "2023-02-25T01:40:37+09:00"
}
DEBUG: manager.getUpdatedPackageFiles() reuseExistingBranch=false(branch="renovate/python-dotenv-1.x")
DEBUG: Starting search at index 175(packageFile="hm-locust/pyproject.toml", branch="renovate/python-dotenv-1.x")
{
  "depName": "python-dotenv"
}
DEBUG: Found match at index 175(packageFile="hm-locust/pyproject.toml", branch="renovate/python-dotenv-1.x")
{
  "depName": "python-dotenv"
}
DEBUG: Contents updated(packageFile="hm-locust/pyproject.toml", branch="renovate/python-dotenv-1.x")
{
  "depName": "python-dotenv"
}
DEBUG: Value is not updated(packageFile="api-python/pyproject.toml", branch="renovate/python-dotenv-1.x")
{
  "manager": "poetry",
  "expectedValue": "1.0.0",
  "foundValue": "0.21.1"
}
DEBUG: Starting search at index 329(packageFile="api-python/pyproject.toml", branch="renovate/python-dotenv-1.x")
{
  "depName": "python-dotenv"
}
DEBUG: Found match at index 329(packageFile="api-python/pyproject.toml", branch="renovate/python-dotenv-1.x")
{
  "depName": "python-dotenv"
}
DEBUG: Contents updated(packageFile="api-python/pyproject.toml", branch="renovate/python-dotenv-1.x")
{
  "depName": "python-dotenv"
}
DEBUG: poetry.updateArtifacts(hm-locust/pyproject.toml)(branch="renovate/python-dotenv-1.x")
DEBUG: Updating hm-locust/poetry.lock(branch="renovate/python-dotenv-1.x")
DEBUG: Using python constraint from config(branch="renovate/python-dotenv-1.x")
DEBUG: Setting CONTAINERBASE_CACHE_DIR to /tmp/containerbase(branch="renovate/python-dotenv-1.x")
DEBUG: Using docker to execute(branch="renovate/python-dotenv-1.x")
{
  "image": "sidecar"
}
DEBUG: Resolved stable matching version(branch="renovate/python-dotenv-1.x")
{
  "toolName": "python",
  "constraint": "3.11.x",
  "resolvedVersion": "3.11.1"
}
DEBUG: Resolved stable matching version(branch="renovate/python-dotenv-1.x")
{
  "toolName": "poetry",
  "constraint": null,
  "resolvedVersion": "1.3.2"
}
DEBUG: containerbaseDir is separate from cacheDir(branch="renovate/python-dotenv-1.x")
DEBUG: Resolved tag constraint(branch="renovate/python-dotenv-1.x")
{
  "image": "docker.io/renovate/sidecar"
}
DEBUG: Docker image is already prefetched: docker.io/renovate/sidecar@sha256:ee4ff56091d0e5913593fdb977ff8baa652714c52b9015ba154f6293a29c342f(branch="renovate/python-dotenv-1.x")
DEBUG: Executing command(branch="renovate/python-dotenv-1.x")
{
  "command": "docker run --rm --name=renovate_sidecar --label=renovate_child -v \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\":\"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\" -v \"/tmp/renovate-cache\":\"/tmp/renovate-cache\" -v \"/tmp/containerbase\":\"/tmp/containerbase\" -e PIP_CACHE_DIR -e BUILDPACK_CACHE_DIR -e CONTAINERBASE_CACHE_DIR -w \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/hm-locust\" docker.io/renovate/sidecar bash -l -c \"install-tool python 3.11.1 && install-tool poetry 1.3.2 && poetry update --lock --no-interaction python-dotenv\""
}
DEBUG: rawExec err(branch="renovate/python-dotenv-1.x")
{
  "err": {
    "name": "ExecError",
    "cmd": "/bin/sh -c docker run --rm --name=renovate_sidecar --label=renovate_child -v \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\":\"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\" -v \"/tmp/renovate-cache\":\"/tmp/renovate-cache\" -v \"/tmp/containerbase\":\"/tmp/containerbase\" -e PIP_CACHE_DIR -e BUILDPACK_CACHE_DIR -e CONTAINERBASE_CACHE_DIR -w \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/hm-locust\" docker.io/renovate/sidecar bash -l -c \"install-tool python 3.11.1 && install-tool poetry 1.3.2 && poetry update --lock --no-interaction python-dotenv\"",
    "stderr": "The currently activated Python version 3.11.1 is not supported by the project (3.10.x).\nTrying to find and use a compatible version. \n\nPoetry was unable to find a compatible version. If you have one, you can explicitly use it via the \"env use\" command.\n",
    "stdout": "installing v2 tool python v3.11.1\nlinking tool python v3.11.1\nPython 3.11.1\npip 23.0.1 from /opt/buildpack/tools/python/3.11.1/lib/python3.11/site-packages/pip (python 3.11)\nInstalled v2 /usr/local/buildpack/tools/v2/python.sh in 24 seconds\nskip cleanup, not a docker build: f2b5ed7e935f\ninstalling v2 tool poetry v1.3.2\nlinking tool poetry v1.3.2\nPoetry (version 1.3.2)\nInstalled v2 /usr/local/buildpack/tools/v2/poetry.sh in 57 seconds\nskip cleanup, not a docker build: f2b5ed7e935f\n",
    "options": {
      "cwd": "/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/hm-locust",
      "encoding": "utf-8",
      "env": {
        "PIP_CACHE_DIR": "/tmp/renovate-cache/others/pip",
        "HOME": "/home/ubuntu",
        "PATH": "/home/ubuntu/.local/bin:/home/ubuntu/bin:/opt/buildpack/tools/python/3.9.3/bin:/home/ubuntu/.npm-global/bin:/home/ubuntu/renovateapp/node_modules/.bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
        "LC_ALL": "C.UTF-8",
        "LANG": "C.UTF-8",
        "BUILDPACK_CACHE_DIR": "/tmp/containerbase",
        "CONTAINERBASE_CACHE_DIR": "/tmp/containerbase"
      },
      "maxBuffer": 10485760,
      "timeout": 900000
    },
    "exitCode": 1,
    "message": "Command failed: docker run --rm --name=renovate_sidecar --label=renovate_child -v \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\":\"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\" -v \"/tmp/renovate-cache\":\"/tmp/renovate-cache\" -v \"/tmp/containerbase\":\"/tmp/containerbase\" -e PIP_CACHE_DIR -e BUILDPACK_CACHE_DIR -e CONTAINERBASE_CACHE_DIR -w \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/hm-locust\" docker.io/renovate/sidecar bash -l -c \"install-tool python 3.11.1 && install-tool poetry 1.3.2 && poetry update --lock --no-interaction python-dotenv\"\nThe currently activated Python version 3.11.1 is not supported by the project (3.10.x).\nTrying to find and use a compatible version. \n\nPoetry was unable to find a compatible version. If you have one, you can explicitly use it via the \"env use\" command.\n",
    "stack": "ExecError: Command failed: docker run --rm --name=renovate_sidecar --label=renovate_child -v \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\":\"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\" -v \"/tmp/renovate-cache\":\"/tmp/renovate-cache\" -v \"/tmp/containerbase\":\"/tmp/containerbase\" -e PIP_CACHE_DIR -e BUILDPACK_CACHE_DIR -e CONTAINERBASE_CACHE_DIR -w \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/hm-locust\" docker.io/renovate/sidecar bash -l -c \"install-tool python 3.11.1 && install-tool poetry 1.3.2 && poetry update --lock --no-interaction python-dotenv\"\nThe currently activated Python version 3.11.1 is not supported by the project (3.10.x).\nTrying to find and use a compatible version. \n\nPoetry was unable to find a compatible version. If you have one, you can explicitly use it via the \"env use\" command.\n\n    at ChildProcess.<anonymous> (/home/ubuntu/renovateapp/node_modules/renovate/dist/util/exec/common.js:87:24)\n    at ChildProcess.emit (node:events:525:35)\n    at ChildProcess.emit (node:domain:489:12)\n    at Process.ChildProcess._handle.onexit (node:internal/child_process:293:12)"
  }
}
DEBUG: Failed to update hm-locust/poetry.lock file(branch="renovate/python-dotenv-1.x")
{
  "err": {
    "name": "ExecError",
    "cmd": "/bin/sh -c docker run --rm --name=renovate_sidecar --label=renovate_child -v \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\":\"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\" -v \"/tmp/renovate-cache\":\"/tmp/renovate-cache\" -v \"/tmp/containerbase\":\"/tmp/containerbase\" -e PIP_CACHE_DIR -e BUILDPACK_CACHE_DIR -e CONTAINERBASE_CACHE_DIR -w \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/hm-locust\" docker.io/renovate/sidecar bash -l -c \"install-tool python 3.11.1 && install-tool poetry 1.3.2 && poetry update --lock --no-interaction python-dotenv\"",
    "stderr": "The currently activated Python version 3.11.1 is not supported by the project (3.10.x).\nTrying to find and use a compatible version. \n\nPoetry was unable to find a compatible version. If you have one, you can explicitly use it via the \"env use\" command.\n",
    "stdout": "installing v2 tool python v3.11.1\nlinking tool python v3.11.1\nPython 3.11.1\npip 23.0.1 from /opt/buildpack/tools/python/3.11.1/lib/python3.11/site-packages/pip (python 3.11)\nInstalled v2 /usr/local/buildpack/tools/v2/python.sh in 24 seconds\nskip cleanup, not a docker build: f2b5ed7e935f\ninstalling v2 tool poetry v1.3.2\nlinking tool poetry v1.3.2\nPoetry (version 1.3.2)\nInstalled v2 /usr/local/buildpack/tools/v2/poetry.sh in 57 seconds\nskip cleanup, not a docker build: f2b5ed7e935f\n",
    "options": {
      "cwd": "/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/hm-locust",
      "encoding": "utf-8",
      "env": {
        "PIP_CACHE_DIR": "/tmp/renovate-cache/others/pip",
        "HOME": "/home/ubuntu",
        "PATH": "/home/ubuntu/.local/bin:/home/ubuntu/bin:/opt/buildpack/tools/python/3.9.3/bin:/home/ubuntu/.npm-global/bin:/home/ubuntu/renovateapp/node_modules/.bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
        "LC_ALL": "C.UTF-8",
        "LANG": "C.UTF-8",
        "BUILDPACK_CACHE_DIR": "/tmp/containerbase",
        "CONTAINERBASE_CACHE_DIR": "/tmp/containerbase"
      },
      "maxBuffer": 10485760,
      "timeout": 900000
    },
    "exitCode": 1,
    "message": "Command failed: docker run --rm --name=renovate_sidecar --label=renovate_child -v \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\":\"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\" -v \"/tmp/renovate-cache\":\"/tmp/renovate-cache\" -v \"/tmp/containerbase\":\"/tmp/containerbase\" -e PIP_CACHE_DIR -e BUILDPACK_CACHE_DIR -e CONTAINERBASE_CACHE_DIR -w \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/hm-locust\" docker.io/renovate/sidecar bash -l -c \"install-tool python 3.11.1 && install-tool poetry 1.3.2 && poetry update --lock --no-interaction python-dotenv\"\nThe currently activated Python version 3.11.1 is not supported by the project (3.10.x).\nTrying to find and use a compatible version. \n\nPoetry was unable to find a compatible version. If you have one, you can explicitly use it via the \"env use\" command.\n",
    "stack": "ExecError: Command failed: docker run --rm --name=renovate_sidecar --label=renovate_child -v \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\":\"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\" -v \"/tmp/renovate-cache\":\"/tmp/renovate-cache\" -v \"/tmp/containerbase\":\"/tmp/containerbase\" -e PIP_CACHE_DIR -e BUILDPACK_CACHE_DIR -e CONTAINERBASE_CACHE_DIR -w \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/hm-locust\" docker.io/renovate/sidecar bash -l -c \"install-tool python 3.11.1 && install-tool poetry 1.3.2 && poetry update --lock --no-interaction python-dotenv\"\nThe currently activated Python version 3.11.1 is not supported by the project (3.10.x).\nTrying to find and use a compatible version. \n\nPoetry was unable to find a compatible version. If you have one, you can explicitly use it via the \"env use\" command.\n\n    at ChildProcess.<anonymous> (/home/ubuntu/renovateapp/node_modules/renovate/dist/util/exec/common.js:87:24)\n    at ChildProcess.emit (node:events:525:35)\n    at ChildProcess.emit (node:domain:489:12)\n    at Process.ChildProcess._handle.onexit (node:internal/child_process:293:12)"
  }
}
DEBUG: poetry.updateArtifacts(api-python/pyproject.toml)(branch="renovate/python-dotenv-1.x")
DEBUG: Updating api-python/poetry.lock(branch="renovate/python-dotenv-1.x")
DEBUG: Using python constraint from config(branch="renovate/python-dotenv-1.x")
DEBUG: Setting CONTAINERBASE_CACHE_DIR to /tmp/containerbase(branch="renovate/python-dotenv-1.x")
DEBUG: Using docker to execute(branch="renovate/python-dotenv-1.x")
{
  "image": "sidecar"
}
DEBUG: Resolved stable matching version(branch="renovate/python-dotenv-1.x")
{
  "toolName": "python",
  "constraint": "3.11.x",
  "resolvedVersion": "3.11.1"
}
DEBUG: Resolved stable matching version(branch="renovate/python-dotenv-1.x")
{
  "toolName": "poetry",
  "constraint": null,
  "resolvedVersion": "1.3.2"
}
DEBUG: containerbaseDir is separate from cacheDir(branch="renovate/python-dotenv-1.x")
DEBUG: Resolved tag constraint(branch="renovate/python-dotenv-1.x")
{
  "image": "docker.io/renovate/sidecar"
}
DEBUG: Docker image is already prefetched: docker.io/renovate/sidecar@sha256:ee4ff56091d0e5913593fdb977ff8baa652714c52b9015ba154f6293a29c342f(branch="renovate/python-dotenv-1.x")
DEBUG: Executing command(branch="renovate/python-dotenv-1.x")
{
  "command": "docker run --rm --name=renovate_sidecar --label=renovate_child -v \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\":\"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version\" -v \"/tmp/renovate-cache\":\"/tmp/renovate-cache\" -v \"/tmp/containerbase\":\"/tmp/containerbase\" -e PIP_CACHE_DIR -e BUILDPACK_CACHE_DIR -e CONTAINERBASE_CACHE_DIR -w \"/mnt/renovate/gh/Hongbo-Miao/bug-renovate-poetry-python-version/api-python\" docker.io/renovate/sidecar bash -l -c \"install-tool python 3.11.1 && install-tool poetry 1.3.2 && poetry update --lock --no-interaction python-dotenv\""
}
DEBUG: exec completed(branch="renovate/python-dotenv-1.x")
{
  "durationMs": 93990,
  "stdout": "installing v2 tool python v3.11.1\nlinking tool python v3.11.1\nPython 3.11.1\npip 23.0.1 from /opt/buildpack/tools/python/3.11.1/lib/python3.11/site-packages/pip (python 3.11)\nInstalled v2 /usr/local/buildpack/tools/v2/python.sh in 28 seconds\nskip cleanup, not a docker build: 7a3a44c0202f\ninstalling v2 tool poetry v1.3.2\nlinking tool poetry v1.3.2\nPoetry (version 1.3.2)\nInstalled v2 /usr/local/buildpack/tools/v2/poetry.sh in 55 seconds\nskip cleanup, not a docker build: 7a3a44c0202f\nUpdating dependencies\nResolving dependencies...\n\nWriting lock file\n  • Installing tzdata (2022.7)\n  • Installing h11 (0.14.0)\n  • Installing markupsafe (2.1.2)\n  • Installing pytz-deprecation-shim (0.1.0.post0)\n  • Installing attrs (22.2.0)\n  • Installing click (8.1.3)\n  • Installing iniconfig (2.0.0)\n  • Installing itsdangerous (2.1.2)\n  • Installing jinja2 (3.1.2)\n  • Installing packaging (23.0)\n  • Installing pluggy (1.0.0)\n  • Updating setuptools (67.1.0 -> 67.3.2)\n  • Installing pytz (2022.7.1)\n  • Installing tzlocal (4.2)\n  • Installing six (1.16.0)\n  • Installing werkzeug (2.2.3)\n  • Installing wsproto (1.2.0)\n  • Installing apscheduler (3.10.0)\n  • Installing blinker (1.5)\n  • Installing pastel (0.2.1)\n  • Installing certifi (2022.12.7)\n  • Installing coverage (7.1.0)\n  • Installing simple-websocket (0.9.0)\n  • Installing python-dateutil (2.8.2)\n  • Installing urllib3 (1.26.14)\n  • Installing pytest (7.2.1)\n  • Installing tomli (2.0.1)\n  • Installing flask (2.2.3)\n  • Installing confluent-kafka (2.0.2)\n  • Installing flask-sock (0.6.0)\n  • Installing flask-cors (3.0.10)\n  • Installing flask-apscheduler (1.12.4)\n  • Installing pytest-cov (4.0.0)\n  • Installing poethepoet (0.18.1)\n  • Installing sentry-sdk (1.15.0)\n  • Installing gunicorn (20.1.0)\n  • Installing python-dotenv (1.0.0)\n",
  "stderr": "Creating virtualenv hm-api-python-S1coFyZ6-py3.11 in /home/ubuntu/.cache/pypoetry/virtualenvs\n"
}
DEBUG: Returning updated api-python/poetry.lock(branch="renovate/python-dotenv-1.x")
DEBUG: Updated 2 package files(branch="renovate/python-dotenv-1.x")
DEBUG: Updated 1 lock files(branch="renovate/python-dotenv-1.x")
{
  "updatedArtifacts": [
    "api-python/poetry.lock"
  ]
}
DEBUG: Branch timestamp: 2023-02-24T06:46:36.000Z(branch="renovate/python-dotenv-1.x")
DEBUG: PR is older than 2 hours, raise PR with lock file errors(branch="renovate/python-dotenv-1.x")
DEBUG: 3 file(s) to commit(branch="renovate/python-dotenv-1.x")
DEBUG: Preparing files for committing to branch renovate/python-dotenv-1.x(branch="renovate/python-dotenv-1.x")
DEBUG: Setting git author name: Renovate Bot(branch="renovate/python-dotenv-1.x")
DEBUG: Setting git author email: bot@renovateapp.com(branch="renovate/python-dotenv-1.x")
DEBUG: git commit(branch="renovate/python-dotenv-1.x")
{
  "deletedFiles": [],
  "ignoredFiles": [],
  "result": {
    "author": null,
    "branch": "renovate/python-dotenv-1.x",
    "commit": "8252fd5097b473c3b3d27fa834d0419612f782ae",
    "root": false,
    "summary": {
      "changes": 3,
      "insertions": 7,
      "deletions": 7
    }
  }
}
DEBUG: resetToCommit(61ed04784dcaa32656e6df5588f6796df4b1e292)(branch="renovate/python-dotenv-1.x")
DEBUG: Fetching branch renovate/python-dotenv-1.x(branch="renovate/python-dotenv-1.x")
INFO: Branch created(branch="renovate/python-dotenv-1.x")
{
  "commitSha": "90e17b3e7ab94e79e0ea0042a4eb4437f0968a85"
}
DEBUG: Updating status check state to failed(branch="renovate/python-dotenv-1.x")
DEBUG: Setting branch status(branch="renovate/python-dotenv-1.x")
{
  "context": "renovate/artifacts",
  "state": "red"
}
DEBUG: Ensuring PR(branch="renovate/python-dotenv-1.x")
DEBUG: There are 0 errors and 0 warnings(branch="renovate/python-dotenv-1.x")
DEBUG: getBranchPr(renovate/python-dotenv-1.x)(branch="renovate/python-dotenv-1.x")
DEBUG: findPr(renovate/python-dotenv-1.x, undefined, open)(branch="renovate/python-dotenv-1.x")
DEBUG: findPr(renovate/python-dotenv-1.x, undefined, closed)(branch="renovate/python-dotenv-1.x")
DEBUG: getPrCache()(branch="renovate/python-dotenv-1.x")
DEBUG: Forcing PR because of artifact errors(branch="renovate/python-dotenv-1.x")
DEBUG: Fetching changelog: https://github.com/theskumar/python-dotenv (0.21.1 -> 1.0.0)(branch="renovate/python-dotenv-1.x")
DEBUG: Fetching changelog: https://github.com/theskumar/python-dotenv (0.21.1 -> 1.0.0)(branch="renovate/python-dotenv-1.x")
DEBUG: Creating PR(branch="renovate/python-dotenv-1.x")
{
  "prTitle": "Update dependency python-dotenv to v1"
}
DEBUG: Creating PR(branch="renovate/python-dotenv-1.x")
{
  "title": "Update dependency python-dotenv to v1",
  "head": "Hongbo-Miao:renovate/python-dotenv-1.x",
  "base": "main",
  "draft": false
}
DEBUG: PR created(branch="renovate/python-dotenv-1.x")
{
  "pr": 1,
  "draft": false
}
DEBUG: Adding labels '' to #1(branch="renovate/python-dotenv-1.x")
INFO: PR created(branch="renovate/python-dotenv-1.x")
{
  "pr": 1,
  "prTitle": "Update dependency python-dotenv to v1"
}
DEBUG: addParticipants(pr=1)(branch="renovate/python-dotenv-1.x")
DEBUG: setPrCache()(branch="renovate/python-dotenv-1.x")
DEBUG: Created Pull Request #1(branch="renovate/python-dotenv-1.x")
WARN: artifactErrors(branch="renovate/python-dotenv-1.x")
{
  "artifactErrors": [
    {
      "lockFile": "hm-locust/poetry.lock",
      "stderr": "installing v2 tool python v3.11.1\nlinking tool python v3.11.1\nPython 3.11.1\npip 23.0.1 from /opt/buildpack/tools/python/3.11.1/lib/python3.11/site-packages/pip (python 3.11)\nInstalled v2 /usr/local/buildpack/tools/v2/python.sh in 24 seconds\nskip cleanup, not a docker build: f2b5ed7e935f\ninstalling v2 tool poetry v1.3.2\nlinking tool poetry v1.3.2\nPoetry (version 1.3.2)\nInstalled v2 /usr/local/buildpack/tools/v2/poetry.sh in 57 seconds\nskip cleanup, not a docker build: f2b5ed7e935f\n\nThe currently activated Python version 3.11.1 is not supported by the project (3.10.x).\nTrying to find and use a compatible version. \n\nPoetry was unable to find a compatible version. If you have one, you can explicitly use it via the \"env use\" command.\n"
    }
  ]
}
DEBUG: Getting comments for #1(branch="renovate/python-dotenv-1.x")
DEBUG: Found 0 comments(branch="renovate/python-dotenv-1.x")
DEBUG: Ensuring comment "⚠ Artifact update problem" in #1(branch="renovate/python-dotenv-1.x")
INFO: Comment added(branch="renovate/python-dotenv-1.x")
{
  "issueNo": 1,
  "topic": "⚠ Artifact update problem"
}
DEBUG: setBranchCommit()(branch="renovate/python-dotenv-1.x")
DEBUG: getBranchPr(renovate/python-dotenv-1.x)
DEBUG: findPr(renovate/python-dotenv-1.x, undefined, open)
DEBUG: Found PR #1
DEBUG: branch.isBehindBase(): using cached result "false"
DEBUG: isBranchConflicted(main, renovate/python-dotenv-1.x)
DEBUG: branch.isConflicted(): using cached result "false"
DEBUG: getPrCache()
DEBUG: Ensuring Dependency Dashboard
DEBUG: ensureIssue(Dependency Dashboard)
INFO: Issue created
DEBUG: Removing any stale branches
DEBUG: config.repoIsOnboarded=true
DEBUG: Branch lists
{
  "branchList": [
    "renovate/python-dotenv-1.x"
  ],
  "renovateBranches": [
    "renovate/python-dotenv-1.x"
  ]
}
DEBUG: remainingBranches=
DEBUG: No branches to clean up
DEBUG: Retrieving issueList
DEBUG: Retrieved 1 issues
DEBUG: Cleaning up Renovate refs: refs/renovate/*
DEBUG: PackageFiles.clear() - Package files deleted
DEBUG: Branch summary
{
  "baseBranches": [
    {
      "branchName": "main",
      "sha": "61ed04784dcaa32656e6df5588f6796df4b1e292"
    }
  ],
  "branches": [
    {
      "automerge": false,
      "baseBranch": "main",
      "baseBranchSha": "61ed04784dcaa32656e6df5588f6796df4b1e292",
      "branchName": "renovate/python-dotenv-1.x",
      "branchSha": "90e17b3e7ab94e79e0ea0042a4eb4437f0968a85",
      "isModified": false,
      "isPristine": true
    }
  ],
  "inactiveBranches": []
}
DEBUG: Renovate repository PR statistics
{
  "stats": {
    "total": 1,
    "open": 1,
    "closed": 0,
    "merged": 0
  }
}
DEBUG: Repository result: done, status: onboarded, enabled: true, onboarded: true
DEBUG: Repository timing splits (milliseconds)
{
  "splits": {
    "init": 4435,
    "extract": 2153,
    "lookup": 1222,
    "onboarding": 2,
    "update": 190502
  },
  "total": 200613
}
DEBUG: Package cache statistics
{
  "get": {
    "count": 17,
    "avgMs": 159,
    "medianMs": 180,
    "maxMs": 336
  },
  "set": {
    "count": 3,
    "avgMs": 59,
    "medianMs": 43,
    "maxMs": 104
  }
}
DEBUG: http statistics
{
  "urls": {
    "https://api.github.com/graphql (POST,200)": 4,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/commits/90e17b3e7ab94e79e0ea0042a4eb4437f0968a85/statuses (GET,200)": 2,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/commits/renovate/python-dotenv-1.x/status (GET,200)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/git/commits (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/git/refs (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/git/trees (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/issues (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/issues/1/comments (GET,200)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/issues/1/comments (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/pulls (GET,200)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/pulls (POST,201)": 1,
    "https://api.github.com/repos/Hongbo-Miao/bug-renovate-poetry-python-version/statuses/90e17b3e7ab94e79e0ea0042a4eb4437f0968a85 (POST,201)": 1,
    "https://api.github.com/repos/whitesource/merge-confidence/contents/beta.json (GET,200)": 1,
    "https://pypi.org/pypi/confluent-kafka/json (GET,200)": 1,
    "https://pypi.org/pypi/python-dotenv/json (GET,200)": 1
  },
  "hostStats": {
    "api.github.com": {
      "requestCount": 17,
      "requestAvgMs": 419,
      "queueAvgMs": 0
    },
    "pypi.org": {
      "requestCount": 2,
      "requestAvgMs": 596,
      "queueAvgMs": 0
    }
  },
  "totalRequests": 19
}
DEBUG: dns cache
{
  "hosts": [
    "api.github.com",
    "pypi.org"
  ]
}
INFO: Repository finished
{
  "cloned": true,
  "durationMs": 200613
}
  ```
</details>
