# Component Database (CDB) — Functionality Summary

## About

The Component Database (CDB) is a web-based tool developed at Argonne National Laboratory to document, organize, and track components used in the MBA accelerator. It serves as a centralized repository connecting component documentation, physical inventory, and machine design planning.

This ANL project's code is managed in the [GitHub repository](https://github.com/AdvancedPhotonSource/ComponentDB).

---

## Three Core Domains

The CDB is built around three interrelated domains.

- **Component Catalog** — Functions like a reference library. Each entry represents a unique component type (custom-fabricated or commercial) with metadata including name, model number, description, technical system, function, vendor sources, images, and custom properties.

- **Component Inventory** — Tracks physical instances of catalog items, each assigned a unique QR ID code for real-world identification. Includes location tracking down to the room, cabinet, or shelf level.

- **Design Library** — Allows users to group components into assemblies (e.g., a PLC chassis with I/O modules, or a BPM processing system), enabling a full hierarchical Bill of Materials for the machine.

---

## Properties System

Since different components require different metadata, CDB uses a flexible properties system. Key characteristics include:

- Any number of properties can be attached to components, instances, or designs
- Properties support **handlers** — smart logic that integrates with external systems:
  - **PDMLink** — Engineering drawings
  - **eTraveler** — Inspection forms
  - **PARIS** — Purchase requisitions
  - **ICMS** — Document management
  - **EDP** and **AMOS** — External order and collection management
- Properties can be static or **dynamic** (varying per instance)
- All value changes are logged historically

---

## Logging

Every domain supports log entries for recording changes, maintenance events, and other lifecycle information. Logs can include:

- A text entry
- A topic classification
- File attachments

---

## Portal Interface

The CDB portal (`cdb.aps.anl.gov`) is accessible on the APS intranet or VPN. Users can browse without logging in, but editing requires an account. Key interface features include:

- Filterable and sortable list views
- Row expansion for quick access to properties and logs
- Customizable columns (including property value columns)
- Export to PDF or Excel
- Consistent detail page panels (Details, Gallery, Logs, and Properties) across all domains, all editable in-place for users with appropriate permissions
- A separate development **sandbox** environment available for training purposes

---

## External Integrations

The CDB connects to several external tools, making it a central hub for component lifecycle management across the project:

| System | Purpose |
|---|---|
| PDMLink | Engineering drawings |
| eTraveler | Inspection workflows |
| PARIS | Procurement / purchase requisitions |
| ICMS | Document management |
| EDP | External collections |
| AMOS | Maintenance orders |