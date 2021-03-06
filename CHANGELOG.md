## [Whimsical-Wyvern](https://github.com/cyverse/atmosphere/milestone/10?closed=1) (as of 4/6/2017)

Features:
  - Include sentry.io error reporting for production environments
  - [application_to_provider](https://github.com/cyverse/atmosphere/pull/284) migration script
  - [iRODS transfer support](https://github.com/cyverse/atmosphere/pull/318) for application_to_provider script

Improvements:
  - Improved support for Instance Actions in v2 APIs
  - Include ext4 support for creating and mounting volumes

Bugfixes:
  - Set provider quota returns more information to allow easier triage by support staff
  - Enable LDAP Expiration information in Profile, if included in configuration

Internal:
  - A new image metrics API endpoint has been created (Staff-users only, for now)
  - Upgrade to latest requirements.txt
  - Included redeploy as an InstanceAction
  - Use ansible to create and mount volumes
  - Provide optional cloud_config options in 'deploy' section: 'volume_fs_type' and 'volume_mount_prefix'
  - Image validation is now a feature flag, configurable from settings.ENABLE_IMAGE_VALIDATION

## [Voracious-Velociraptor](https://github.com/cyverse/atmosphere/milestone/9?closed=1) (as of 2/14/2017)

Features:
  - Image validation works as intended (and deletes instance on cleanup)
  - New command `manage.py find_uuid` can help understand what object you are looking at when given a UUID without context
  - Improved sorting for image catalog
  - Include 'project' in instance launch (v2 API)

Bugfixes:
  - Instance status/activity show up as expected when in 'Networking' and 'Deploying'
  - Errors that bubble up from API are now more verbose and help users understand the problem

Internal:
  - Remove iPlant-isms from template pages
  - Fix logfile growing pains

## Undulating-Umbrellabird (as of 1/4/17)

Features:
  - move from iplantauth to django_cyverse_auth
  - Add 'user expiration' LDAP plugin and include 'is_expired' attribute in user's profile API
  - [Creation of new identities/providers now available in v2 API](https://github.com/cyverse/atmosphere/pull/222)
  - Include instance reporting as a v2 API, allow generation of XLSX and CSV files
  - Create a PluginManager to avoid code duplication between plugin validation and class loading

Bugfixes:
  - Fixed a bug that caused the image bookmark API to produce an invalid query
  - Quota foreign key has been re-assigned from IdentityMembership to Identity
  - Create router gateway when using the ExternalNetworkTopology
  - Quota can now be set "above the pre-set limits" listed in openstack.

Deprecated:
  - [./scripts/add_new_accounts.py](./scripts/add_new_accounts.py) and [./scripts/add_new_provider.py](./scripts/add_new_provider.py) will stop receiving updates after creation is moved into the GUI/API.

## Toco-Toucan

Internal Release:
  - Included in `Undulating-Umbrellabird`
