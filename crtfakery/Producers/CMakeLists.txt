include_directories( ${CMAKE_CURRENT_SOURCE_DIR} )
include_directories( $ENV{NUTOOLS_INC} )

simple_plugin( ZMQFaker module
        larcore_Geometry
        BernZMQCore
        ${ART_FRAMEWORK_CORE}
        ${ART_FRAMEWORK_IO_SOURCES}
        ${ART_FRAMEWORK_PRINCIPAL}
        art_Persistency_Common 
        canvas_Persistency_Common
        art_Persistency_Provenance 
        canvas_Persistency_Provenance
        art_Utilities 
        canvas_Utilities
        lardata_DetectorInfoServices_DetectorClocksServiceStandard_service
        nutools_RandomUtils_NuRandomService_service
        ${ART_FRAMEWORK_SERVICES_REGISTRY}
        ${ART_FRAMEWORK_SERVICES_OPTIONAL_RANDOMNUMBERGENERATOR_SERVICE}
        ${MF_MESSAGELOGGER}
        ${MF_UTILITIES}
        ${ROOT_BASIC_LIB_LIST}
        ${CLHEP}
        ${CETLIB}
    BASENAME_ONLY
)

install_headers()
install_fhicl()
install_source()
