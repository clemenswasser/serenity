serenity_component(
    WebDriver
    TARGETS WebDriver
)

set(SOURCES
    BrowserConnection.cpp
    Client.cpp
    Session.cpp
    TimeoutsConfiguration.cpp
    WebDriverError.cpp
    main.cpp
    )

set(GENERATED_SOURCES
    ../../Applications/Browser/WebDriverSessionClientEndpoint.h
    ../../Applications/Browser/WebDriverSessionServerEndpoint.h
    )

serenity_bin(WebDriver)
target_link_libraries(WebDriver PRIVATE LibCore LibHTTP LibMain LibIPC LibWeb LibGfx)
