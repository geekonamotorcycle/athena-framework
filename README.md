# Athena Framework

The Athena Framework is an open source repository of reusable documentation, configuration templates, and automation tools for building modern ITSP and MSP infrastructure. It is strategy-driven, modular, and mythology-themed, named after Athena—the goddess of wisdom, planning, and skill.

This project is licensed openly to promote community participation and practical reuse. Contributions are welcome.

## Purpose

The framework provides baseline scaffolding for infrastructure documentation and system implementation. This includes:

- Hardware baseline configurations
- Operating system templates and services
- Networking layouts and rulesets
- Hypervisor deployments and best practices
- Tooling for observability, automation, and security

## Directory Structure

```text
athena-framework/
├── forge/
├── blueprints/
│   ├── hardware/
│   │   └── servers/
│   │       ├── dell/
│   │       └── qotom/
│   ├── hypervisors/
│   │   ├── broadcom-vmware/
│   │   ├── citrix-xenserver/
│   │   ├── windows-hyperv/
│   │   └── xcp-ng/
│   ├── networking/
│   │   ├── hardware/
│   │   │   ├── firewalls/
│   │   │   ├── hubs/
│   │   │   ├── routers/
│   │   │   └── switches/
│   │   └── network-operations/
│   ├── operating-systems/
│   │   ├── bsd/
│   │   │   ├── freebsd-based/
│   │   │   ├── netbsd-based/
│   │   │   └── openbsd-based/
│   │   ├── linux/
│   │   │   ├── debian-base/
│   │   │   │   ├── debian/
│   │   │   │   └── ubuntu/
│   │   │   └── red-hat-base/
│   │   │       ├── alma/
│   │   │       ├── rhel/
│   │   │       └── rocky/
│   │   └── windows/
│   │       └── server/
│   │           ├── server-2008/
│   │           ├── server-2012/
│   │           ├── server-2016/
│   │           ├── server-2019/
│   │           └── server-2025/
│   │               └── services/
│   │                   └── pki-templates/
├── relics/
├── codex/
├── oracle/
├── sentinel/
└── README.md
```

## Section Overview

### [forge/](./forge)

Tools and scripts to automate infrastructure provisioning, configuration generation, or documentation prep.

### [blueprints/](./blueprints)

The heart of the framework. Contains organized, versioned, reusable documentation and deployment templates.

### [blueprints/hardware/](./blueprints/hardware)

- [servers/dell/](./blueprints/hardware/servers/dell) – Dell-specific server templates
- [servers/qotom/](./blueprints/hardware/servers/qotom) – Qotom server and edge appliance configs

### [blueprints/hypervisors/](./blueprints/hypervisors)

- [broadcom-vmware/](./blueprints/hypervisors/broadcom-vmware)
- [citrix-xenserver/](./blueprints/hypervisors/citrix-xenserver)
- [windows-hyperv/](./blueprints/hypervisors/windows-hyperv)
- [xcp-ng/](./blueprints/hypervisors/xcp-ng)

### [blueprints/networking/](./blueprints/networking)

- [hardware/firewalls](./blueprints/networking/hardware/firewalls)
- [hardware/hubs](./blueprints/networking/hardware/hubs)
- [hardware/routers](./blueprints/networking/hardware/routers)
- [hardware/switches](./blueprints/networking/hardware/switches)
- [network-operations](./blueprints/networking/network-operations)

### [blueprints/operating-systems/](./blueprints/operating-systems)

- [bsd/freebsd-based](./blueprints/operating-systems/bsd/freebsd-based)
- [bsd/netbsd-based](./blueprints/operating-systems/bsd/netbsd-based)
- [bsd/openbsd-based](./blueprints/operating-systems/bsd/openbsd-based)
- [linux/debian-base/debian](./blueprints/operating-systems/linux/debian-base/debian)
- [linux/debian-base/ubuntu](./blueprints/operating-systems/linux/debian-base/ubuntu)
- [linux/red-hat-base/alma](./blueprints/operating-systems/linux/red-hat-base/alma)
- [linux/red-hat-base/rhel](./blueprints/operating-systems/linux/red-hat-base/rhel)
- [linux/red-hat-base/rocky](./blueprints/operating-systems/linux/red-hat-base/rocky)
- [windows/server/server-2008](./blueprints/operating-systems/windows/server/server-2008)
- [windows/server/server-2012](./blueprints/operating-systems/windows/server/server-2012)
- [windows/server/server-2016](./blueprints/operating-systems/windows/server/server-2016)
- [windows/server/server-2019](./blueprints/operating-systems/windows/server/server-2019)
- [windows/server/server-2025](./blueprints/operating-systems/windows/server/server-2025)
- [pki-templates](./blueprints/operating-systems/windows/server/server-2025/services/pki-templates)

### [codex/](./codex)

Markdown how-to guides, reference materials, and repeatable runbooks.

### [oracle/](./oracle)

Observability tooling, templates for Zabbix, Prometheus, and Grafana integration.

### [sentinel/](./sentinel)

Security-focused configurations, baselines, and hardening checklists.

### [relics/](./relics)

Deprecated or superseded templates retained for legacy support or audit history.

## Contribution Guidelines

- Use lowercase and hyphens or underscores in folder/file names. No whitespace.
- Wrap all documentation to 120 characters max.
- All sections must include README.md stubs and markdownlint compliance.
- Submit contributions with descriptions and PR titles referencing intended use.

## License

This project is dual-licensed. See [LICENSE.md](LICENSE.md) for full details.
