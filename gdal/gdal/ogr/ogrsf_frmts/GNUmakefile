
include ../../GDALmake.opt

SUBDIRS-yes = generic geojson kml mem mitab vrt $(OGR_FORMATS)

SUBDIRS-$(HAVE_DODS)	+= dods
SUBDIRS-$(HAVE_TEIGHA)  += dwg
SUBDIRS-$(HAVE_FME)	+= fme
SUBDIRS-$(HAVE_GRASS)	+= grass
SUBDIRS-$(HAVE_IDB)	+= idb
SUBDIRS-$(HAVE_MYSQL)	+= mysql
SUBDIRS-$(HAVE_OGDI)	+= ogdi
SUBDIRS-$(HAVE_OCI)	+= oci
SUBDIRS-$(HAVE_OGR_PG)	+= pg
SUBDIRS-$(HAVE_SQLITE)	+= sqlite
SUBDIRS-$(HAVE_SDE)     += sde
SUBDIRS-$(HAVE_FGDB)    += filegdb
SUBDIRS-$(HAVE_ARCOBJECTS)  += arcobjects
SUBDIRS-$(HAVE_INGRES)  += ingres
SUBDIRS-$(HAVE_LIBKML)  += libkml
SUBDIRS-$(MDB_ENABLED)  += mdb
SUBDIRS-$(HAVE_FREEXL)  += xls
SUBDIRS-$(HAVE_SOSI)	+= sosi
SUBDIRS-$(HAVE_MONGODB) += mongodb
SUBDIRS-$(HAVE_MONGOCXXV3) += mongodbv3

default:	$(foreach d,$(SUBDIRS-yes),$(d)-target)

clean:	$(foreach d,$(SUBDIRS-yes),$(d)-clean)
	rm -f o/*.o
	$(RM) o/*.lo
