
# OFRescue Boston

### OrangeFox Recovery 12.1 - Rescue Center GUI

OFRescue Boston is an informational touchscreen rescue interface project for the:

- **Device:** Motorola Moto G Stylus 5G 2024
- **Model:** XT2419-1
- **Codename:** Boston
- **Recovery target:** OrangeFox Recovery 12.1
- **Interface:** Android recovery touchscreen GUI

---

## Project Goals

OFRescue aims to provide a simple, organized recovery interface with:

1. Device Information
2. Bootloop Diagnostics
3. Partition Backup Guidance
4. Recovery Builder Status
5. Safe navigation through recovery tools

## Safety First

OFRescue is designed around a safety-first approach.

The current GUI pages are informational. They do not independently perform:

- Partition flashing
- Partition formatting
- Data wiping
- Bootloader unlocking
- Backup operations
- Restore operations

Always verify the device model, partition layout, firmware package, and recovery compatibility before performing recovery operations.

**Never assume a source ZIP is a flashable recovery image.**

## Repository Structure

```text
OFRescue/
├── .github/
│   └── workflows/
│       ├── ofrescue.yml
│       └── Recovery Build.yml
├── gui/
│   └── theme/
│       └── portrait_hdpi/
│           └── pages/
│               ├── advanced.xml
│               └── ofrescue.xml
└── README.md
```

## Source Validation

The OFRescue Source Package workflow:

- Checks required GUI files.
- Parses available XML files.
- Checks required OFRescue page names.
- Creates a downloadable source ZIP.
- Uploads the ZIP as a GitHub Actions artifact.

The source package is not a recovery image or installer.

## Building Recovery

The separate Recovery Build workflow is intended for recovery image compilation.

A successful build requires:

- A compatible OrangeFox manifest.
- A working Boston device tree.
- Compatible kernel and vendor configuration.
- Correct recovery build configuration.
- Successful compilation and device testing.

Build settings must be verified against the actual device tree before attempting a device-specific build.

## Development Status

| Component | Status |
|---|---|
| OFRescue home page | Source created |
| Device information page | Informational |
| Bootloop diagnostics | Checklist only |
| Backup guidance | Informational |
| Recovery builder page | Status information only |
| XML validation workflow | Implemented |
| Source ZIP packaging | Implemented |
| Boston recovery integration | Requires testing |
| Hardware validation | Not yet verified |

## Contributing

Contributions are welcome.

Please verify XML syntax, OrangeFox compatibility, device-specific configuration, and safety behavior before submitting changes.

## Credits

Thanks to the OrangeFox Recovery developers, Android recovery developers, device-tree maintainers, and the open-source Android community.

---

**Project:** OFRescue Boston  
**Repository:** irvenhill777/OFRescue  
**Target:** Motorola XT2419-1 (Boston)
