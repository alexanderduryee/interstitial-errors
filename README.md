interstitial-errors
===================

Tool to detect interstitial errors in digitization workflows

Introduction
------------

interstitial-errors is designed to detect dropped samples in audio digitization processes.  These are caused by fleeting interruptions in the hardware/software pipeline on a digital audio workstation, causing a small number of samples to be dropped from the transfer.

More information on interstitial errors can be found in [this FADGI report](http://www.digitizationguidelines.gov/audio-visual/documents/Interstitial_Error_Report_2013-04-08.pdf)

Usage
-----

This tool requires two sets of audio files: one generated as normal on a DAW, and one generated on a reference device.  Typically, a device such as a standalone recorder is used as the reference device.  This device should receive the same digital output that the DAW receives and record it to disk.

Once the two sets are generated, interstitial-errors can be pointed at the reference and DAW directories and run.  It will automatically match WAV files between the directories, find errors in the DAW-generated files, and report results.

Requires
--------

audiolab
numpy
PyQt4 (GUI only)
