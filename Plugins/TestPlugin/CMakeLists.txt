project(TestPlugin VERSION 0.0.1)

set (BaseTargetName TestPlugin)

juce_add_plugin("${BaseTargetName}"
        COMPANY_NAME "MyCompany"
        IS_SYNTH FALSE
        NEEDS_MIDI_INPUT TRUE
        NEEDS_MIDI_OUTPUT FALSE
        IS_MIDI_EFFECT FALSE
        EDITOR_WANTS_KEYBOARD_FOCUS FALSE
        COPY_PLUGIN_AFTER_BUILD TRUE
        PLUGIN_MANUFACTURER_CODE Juce
        PLUGIN_CODE Tspl
        FORMATS AU VST3 Standalone
        PRODUCT_NAME "Test Plugin")

target_sources(${BaseTargetName} PRIVATE
        Source/PluginProcessor.cpp)

set_default_plugin(${BaseTargetName})