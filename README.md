# vscode-lua-server-plugin-ultraschall

This project aims to add support for Meo's custom US_DocBloc doc blocks used in https://ultraschall.fm/api/ to the [VS Code Lua language server](https://github.com/sumneko/lua-language-server/wiki/Plugin
)





```lua
function ultraschall.SplitMediaItems_Position(position, trackstring, crossfade)
--[[
<US_DocBloc version="1.0" spok_lang="en" prog_lang="*">
  <slug>SplitMediaItems_Position</slug>
  <requires>
    Ultraschall=4.00
    Reaper=5.40
    Lua=5.3
  </requires>
  <functioncall>boolean retval, array MediaItemArray = ultraschall.SplitMediaItems_Position(number position, string trackstring, boolean crossfade)</functioncall>
  <description>
    Splits items at position, in the tracks given by trackstring.
    If auto-crossfade is set in the Reaper-preferences, crossfade turns it on(true) or off(false).
    
    Returns false, in case of error.
  </description>
  <parameters>
    number position - the position in seconds
    string trackstring - the numbers for the tracks, where split shall be applied to; numbers separated by a comma
    boolean crossfade - true or nil, automatic crossfade(if enabled) will be applied; false, automatic crossfade is off
  </parameters>
  <retvals>
    boolean retval - true - success, false - error
    array MediaItemArray - an array with the items on the right side of the split
  </retvals>
  <chapter_context>
    MediaItem Management
    Edit
  </chapter_context>
  <target_document>US_Api_Functions</target_document>
  <source_document>Modules/ultraschall_functions_MediaItem_Module.lua</source_document>
  <tags>mediaitemmanagement, tracks, media, item, split, edit, crossfade</tags>
</US_DocBloc>
]]
…
```
