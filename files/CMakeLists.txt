# these lines create the empty directory structure pvpgn needs installed
# in ./var and then installs it portably using install(DIRECTORY...)
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/users")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/userscdb")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/bnmail")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/clans")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/teams")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/reports")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/chanlogs")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/userlogs")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/charinfo")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/charsave")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/bak/charinfo")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/bak/charsave")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/ladders")
file(MAKE_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}/var/status")

install(DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/var/ DESTINATION ${LOCALSTATEDIR})

install(FILES ad000001.png ad000001.smk ad000002.mng newbie.save
	bnserver.ini bnserver-D2DV.ini bnserver-D2XP.ini bnserver-WAR3.ini
	ver-IX86-1.mpq IX86ver1.mpq PMACver1.mpq XMACver1.mpq IX86ExtraWork.mpq
	icons.bni icons-WAR3.bni icons_STAR.bni
    DESTINATION ${LOCALSTATEDIR}/files) 
