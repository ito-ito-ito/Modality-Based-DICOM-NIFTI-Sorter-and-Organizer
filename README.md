# Modality-Based-DICOM-NIFTI-Sorter-and-Organizer
A pipeline that filters, sorts, and converts DICOM series into organized, compressed NIfTI files, streamlining medical imaging data for analysis.

Pipeline Overview
This script processes DICOM datasets by:

1. Filtering non-imaging DICOM files into a separate (specified) directory
2. Sorting imaging series by description and UID
3. Converting DICOM series to compressed NIfTI format
4. Organizing output into modality-specific folders

Performance Notes
- 102KB file filter significantly reduces processing time
- ThreadPoolExecutor enables concurrent I/O operations
- Compression trades processing time for storage savings
- Typical processing: 2-7 minutes per 1000 DICOM files

Error Handling
- Skipped files logged with error causes
- Modality detection failsafe prevents pipeline halts
- Validation exceptions caught without interrupting conversion

This implementation provides a robust pipeline for converting clinical DICOM datasets into analysis-ready NIfTI format while maintaining comprehensive metadata preservation. The parallel processing and smart filtering make it suitable for large-scale medical imaging datasets.
