# guiCreateBrowser-MTA

local sx, sy = guiGetScreenSize()
local browser = guiCreateBrowser(0, 0, sx, sy, true, true, false)
guiSetVisible(browser, false)
local theBrowser = guiGetBrowser(browser)

addEventHandler("onClientBrowserCreated", theBrowser, 
    function()
    loadBrowserURL(source, "http://mta/local/index.html")
    end
)
