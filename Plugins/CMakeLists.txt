function (set_default_plugin targetName)
    target_compile_definitions(${targetName}
            PUBLIC
            JUCE_WEB_BROWSER=0
            JUCE_USE_CURL=0
            JUCE_VST3_CAN_REPLACE_VST2=0)

    target_link_libraries(${targetName} PRIVATE
            shared_plugin_helpers
            juce_audio_utils
            juce_recommended_config_flags
            juce_recommended_lto_flags
            juce_recommended_warning_flags)
endfunction()

add_subdirectory(TestPlugin)
