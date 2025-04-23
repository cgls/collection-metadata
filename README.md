# CLMS INSPIRE Metadata Repository

This repository contains metadata files compliant with the INSPIRE (Infrastructure for Spatial Information in Europe) directive for geospatial datasets. The metadata follows ISO 19115/19139 standards and is stored in XML format.

## Overview

The INSPIRE directive aims to create a European Union spatial data infrastructure for environmental policies and activities that may have an impact on the environment. This repository serves as a centralized storage location for metadata describing various geospatial datasets, ensuring they are properly documented according to INSPIRE requirements.

## Repository Structure

The repository is organized as follows:

```
inspire-metadata/
├── README.md                  # This documentation file
├── CLMS-GLOBAL/               # Copernicus Land Monitoring Service - Global
│   ├── metadata/              # INSPIRE-compliant metadata XML files
│   └── quicklooks/            # Preview images of the datasets
└── LCFM/                      # Land Cover and Forest Monitoring
    └── metadata/              # INSPIRE-compliant metadata XML files
```

Each metadata directory contains XML files that follow the ISO 19115/19139 standards and are INSPIRE-compliant, describing various geospatial datasets.

## Metadata File Format

The metadata files follow the ISO 19115/19139 standards and are encoded in XML. They include:

- **File identification**: Unique identifiers for each dataset
- **Data provider information**: Contact details for the organizations responsible
- **Dataset characteristics**: Spatial and temporal coverage, resolution
- **Distribution information**: Access mechanisms, download options
- **Data quality**: Conformance results, lineage information
- **Reference systems**: Coordinate systems used

Example metadata elements include:
- `gmd:fileIdentifier` - Unique identifier for the metadata file
- `gmd:contact` - Contact information for the metadata maintainer
- `gmd:identificationInfo` - Core information about the dataset
- `gmd:distributionInfo` - Information on how to access the dataset
- `gmd:dataQualityInfo` - Quality information and conformance statements

## Usage Guidelines

### Adding New Metadata

1. Identify the appropriate directory for your dataset type
2. ~~Use a template from the `templates/` directory if available~~
3. Generate the XML metadata file following INSPIRE requirements
4. Validate the file using the validation tool
5. Add the file to the repository with a descriptive commit message

### Updating Existing Metadata

1. Locate the metadata file that needs updating
2. Make the necessary changes while maintaining INSPIRE compliance
3. Validate the updated file
4. Commit the changes with a clear description of what was modified

### Naming Conventions

Metadata files should be named according to the following pattern:
```
clms_[dataset_name]_[version].xml
```

Example: `clms_global_ba_300m_v3_daily.xml`

## Validation

All metadata files should be validated against INSPIRE requirements before being committed. It is recommended to use the official INSPIRE Validator (https://inspire.ec.europa.eu/validator/) to ensure compliance.

Contributors are expected to validate their metadata files before submitting them to this repository. While we don't include validators directly in this repository, proper validation is still an essential step in the workflow.

## Tools and Resources

### Recommended Tools

- **INSPIRE Validator**: The official INSPIRE validation service (https://inspire.ec.europa.eu/validator/)
- **GeoNetwork**: Open-source catalog for managing geospatial metadata
- **QGIS Metadata Editor**: Plugin for creating and editing ISO metadata

### Resources

- [INSPIRE Metadata Technical Guidelines](https://inspire.ec.europa.eu/id/document/tg/metadata-iso19139)
- [ISO 19115 Information and Documentation](https://www.iso.org/standard/53798.html)
- [INSPIRE Geoportal](https://inspire-geoportal.ec.europa.eu/)

## Contributing

Contributions to this repository are welcome. Please follow these steps:

1. Fork the repository
2. Create a feature branch
3. Add or modify metadata files
4. Validate all changes
5. Submit a pull request with a clear description of your changes

## License

This metadata repository is licensed under the European Union Public License (EUPL), which is specifically designed for European public sector software and data projects. The EUPL ensures proper attribution while encouraging reuse of the metadata in alignment with European Union policies.

The datasets described by this metadata may have their own licensing terms. Please refer to the metadata itself and the dataset provider for specific licensing information regarding the actual data.
