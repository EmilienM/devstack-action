[![.github/workflows/with-defaults.yml](https://github.com/EmilienM/devstack-action/actions/workflows/with-defaults.yml/badge.svg)](https://github.com/EmilienM/devstack-action/actions/workflows/with-defaults.yml)

# devstack-actions
Github actions which will install OpenStack with devstack.

Example of Github Action step:

With defaults:
```
    steps:
      - name: Deploy devstack
        uses: EmilienM/devstack-action@v0.6
```

With overrides:
```
    steps:
      - name: Deploy devstack
        uses: EmilienM/devstack-action@v0.6
        with:
          branch: stable/xena
          conf_overrides:
            CINDER_ISCSI_HELPER=tgtadm
          enabled_services: 's-account,s-container,s-object,s-proxy'
```
