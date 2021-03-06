# Workflow processes
Several processes are run within the workflow. We divide them for the moment into 3 main steps:

## Preprocessing [Stable]:
 - MapReads - Map reads [Stable]
 - MergeBams - Merge BAMs if multilane samples [Stable]
 - MarkDuplicates - Mark Duplicates [Stable]
 - CreateIntervals - Create Intervals [Stable]
 - RealignBams - Realign Bams as T/N pair [Stable]
 - CreateRecalibrationTable - Create Recalibration Table [Stable]
 - RecalibrateBam - Recalibreate Bam [Stable]

## Variant Calling:
 - RunHaplotypecaller - Run HaplotypeCaller for GermLine Variant Calling (Parrallelized processes) [Stable]
 - RunMutect1 - Run MuTect1 for Variant Calling (Parrallelized processes) [Stable]
 - RunMutect2 - Run MuTect2 for Variant Calling (Parrallelized processes) [Working]
 - RunFreeBayes - Run FreeBayes for Variant Calling (Parrallelized processes) [Working]
 - RunVardict - Run VarDict for Variant Calling (Parrallelized processes) [Working]
 - ConcatVCF - Merge results from HaplotypeCaller, MuTect1, MuTect2 and VarDict parrallelized processes [Stable]
 - RunStrelka - Run Strelka for Variant Calling [Stable]
 - RunManta - Run Manta for Structural Variant Calling [Need more tests]
 - RunAlleleCount - Run AlleleCount to prepare for Ascat [Stable]
 - RunConvertAlleleCounts - Run convertAlleleCounts to prepare for Ascat [Stable]
 - RunAscat - Run Ascat for CNV [Stable]

## Report and QC:
 - RunFastQC - Run FastQC for QC on fastq files [Stable]
 - RunMultiQC - Run MultiQC for report and QC [Stable]
