##----------------------------------------------------------------
##      _____
##     /     \
##    /____   \____
##   / \===\   \==/
##  /___\===\___\/  AVNET
##       \======/
##        \====/    
##---------------------------------------------------------------
##
## This design is the property of Avnet.  Publication of this
## design is not authorized without written consent from Avnet.
## 
## Please direct any questions to:  technical.support@avnet.com
##
## Disclaimer:
##    Avnet, Inc. makes no warranty for the use of this code or design.
##    This code is provided  "As Is". Avnet, Inc assumes no responsibility for
##    any errors, which may appear in this code, nor does it make a commitment
##    to update the information contained herein. Avnet, Inc specifically
##    disclaims any implied warranties of fitness for a particular purpose.
##                     Copyright(c) 2011 Avnet, Inc.
##                             All rights reserved.
##
##----------------------------------------------------------------
##
## Create Date:         Sep 01, 2011
## Design Name:         FMC-IMAGEON
## Module Name:         fmc_imageon_sw_v2_1_0.mld
## Project Name:        FMC-IMAGEON
## Target Devices:      Spartan-6, Virtex-6
##                      Artix-7, Kintex-7, Virtex-7, Zynq
## Avnet Boards:        FMC-IMAGEON
##
## Tool versions:       Vivado 2013.3
##
## Description:         FMC-IMAGEON Software Services
##                      Makefile
##
## Dependencies:        
##
## Revision:            Sep 01, 2011: 1.01 Initial version
##                      Nov 09, 2011: 1.02 Add HDMI I2C config sequences
##                      Dec 10, 2011: 1.03 Add HDMI functions
##                                         - fmc_imageon_hdmii_get_lock
##                                         - fmc_imageon_hdmii_get_timing
##                                         - fmc_imageon_hdmio_set_timing
##                      Feb 16, 2012: 1.04 Modify HDMI functions
##                                         - HDMI input
##                                            - I2C config for SPDIF
##                                         - HDMI output
##                                            - I2C config for SPDIF
##                                            - implement WaitForHPD
##                      Feb 21, 2012: 1.05 Modify HDMI output function
##                                         - set HDMI/DVI mode according
##                                           to pTiming argument
##                      Apr 13, 2012: 1.06 Fix typo in verbose
##                      Nov 28, 2012: 1.07 Modify ADV7611 LLC delay
##                                         for FMC-IMAGEON Rev.B hardware
##                                         (specifically for 74.25MHz)
##                      Aug 15, 2012: 1.07 Set ADV7511 clock delay to 101 (+0.8ns)
##                      Nov 28, 2012: 2.01 Configure ADV7611 LLC for inverse polarity
##                                         for FMC-IMAGEON Rev.B hardware
##
##----------------------------------------------------------------

COMPILER=
ARCHIVER=
CP=cp
COMPILER_FLAGS=
EXTRA_COMPILER_FLAGS=
LIB=libxil.a

RELEASEDIR=../../../lib
INCLUDEDIR=../../../include
INCLUDES=-I./. -I${INCLUDEDIR}

INCLUDEFILES=*.h
LIBSOURCES=*.c
OUTS = *.o

libs:
	echo "Compiling fmc_imageon_sw"
	$(COMPILER) $(COMPILER_FLAGS) $(EXTRA_COMPILER_FLAGS) $(INCLUDES) $(LIBSOURCES)
	$(ARCHIVER) -r ${RELEASEDIR}/${LIB} ${OUTS}
	make clean

include:
	${CP} $(INCLUDEFILES) $(INCLUDEDIR)

clean:
	rm -rf ${OUTS}

