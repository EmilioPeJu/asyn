TOP = ../
include $(TOP)/configure/CONFIG

DIRS += edm
include $(TOP)/configure/RULES_DIRS

ADL_DIR = medm
UI_DIR  = caqtdm/autoconvert
EDL_DIR = edm/autoconvert
OPI_DIR = boy/autoconvert
BOB_DIR = bob/autoconvert

include $(CONFIG)/RULES_DIRS

-include $(SUPPORT)/configure/RULES_OPI
