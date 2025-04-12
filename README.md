! (1/11) YouTube 4 Videos Per Row Fix (Home and Channel Pages) / YouTube Fix & Customization
youtube.com##ytd-rich-grid-row, #contents.ytd-rich-grid-row:style(display:contents !important;)
youtube.com##ytd-rich-grid-renderer, html:style(--ytd-rich-grid-items-per-row: 4 !important;)
youtube.com##ytd-rich-grid-renderer, html:style(--ytd-rich-grid-posts-per-row: 4 !important;)
! (2/11) YouTube Home Short Section 7 Videos Per Row Fix / YouTube Fix & Customization
youtube.com##ytd-rich-grid-renderer, html:style(--ytd-rich-grid-slim-items-per-row: 7 !important;)
youtube.com##ytd-rich-shelf-renderer, html:style(--ytd-rich-grid-items-per-row: 7 !important;)
youtube.com##ytd-rich-grid-renderer, html:style(--ytd-rich-grid-game-cards-per-row: 7 !important;)
youtube.com##ytd-rich-shelf-renderer, html:style(--ytd-rich-shelf-items-count: 7 !important;)
youtube.com##+js(set-attr, ytd-rich-shelf-renderer, is-show-more-hidden)
youtube.com##+js(ra, hidden, ytd-rich-item-renderer, stay)
! (3/11) YouTube Home and Channel Page Margin Fix / YouTube Fix & Customization
youtube.com##ytd-rich-item-renderer[rendered-from-rich-grid][is-in-first-column]:style(margin-left: calc(var(--ytd-rich-grid-item-margin)/2) !important;)
youtube.com##ytd-rich-item-renderer[is-slim-grid]:first-of-type, ytd-rich-item-renderer[is-shorts-grid]:first-of-type:style(margin-left: auto !important;)
youtube.com##ytd-rich-item-renderer[is-slim-grid]:last-of-type, ytd-rich-item-renderer[is-shorts-grid]:last-of-type:style(margin-right: auto !important;)
! (4/11) YouTube Font Size Fix / YouTube Fix & Customization
youtube.com###video-title.ytd-rich-grid-media, #video-title.ytd-rich-grid-slim-media:style(font-size: 1.4rem !important; line-height: 2rem !important;)
youtube.com###metadata-line.ytd-video-meta-block:style(font-size: 1.2rem !important; line-height: 1.8rem !important;)
! (5/11) YouTube Search Results Video Thumb Size Fix / YouTube Fix & Customization
youtube.com##ytd-video-renderer[use-bigger-thumbs][bigger-thumbs-style="BIG"] ytd-thumbnail.ytd-video-renderer, ytd-video-renderer[use-bigger-thumbs] ytd-thumbnail.ytd-video-renderer, ytd-radio-renderer[use-bigger-thumbs] ytd-thumbnail.ytd-radio-renderer, #avatar-section.ytd-channel-renderer, ytd-radio-renderer[use-bigger-thumbs][bigger-thumbs-style="BIG"] ytd-playlist-thumbnail.ytd-radio-renderer, ytd-playlist-renderer[use-bigger-thumbs][bigger-thumbs-style="BIG"] ytd-playlist-thumbnail.ytd-playlist-renderer:style(max-width: 360px !important;)

! (6/11) YouTube Horizontal Scrollbar Fix / YouTube Fix & Customization
youtube.com##body, ytd-app[scrolling]:style(overflow-x: hidden !important;)
! (7/11) YouTube Customizations (Closes menu to have more space for videos) Notice: This rule prevents the menu from opening even when you click on it for now. If you often use the menu, exclude this rule. / YouTube Fix & Customization
youtube.com##tp-yt-app-drawer:remove-attr(/opened|persistent/)
! Only use these 2 rules below if you set items-per-row and posts-per-row to 5 or 6 from the first filter set, "(1/11) 4 Videos Per Row Fix"
! (8/11) YouTube Channel Page Videos, Shorts, Live, Podcasts and Playlists Tabs Full Width Video Content (Makes video thumbs to fill the page) / YouTube Fix & Customization
youtube.com##:matches-path(//videos|/shorts|/streams|/podcasts|/playlists/) ytd-two-column-browse-results-renderer.grid-5-columns, ytd-two-column-browse-results-renderer.grid-6-columns:style(width: 100% !important;)
youtube.com##ytd-two-column-browse-results-renderer.grid, ytd-rich-grid-renderer[is-shorts-grid] #contents.ytd-rich-grid-renderer:style(max-width: initial !important;)

! (9/11) YouTube Channel Block (You can block/hide any videos from a specific channel or multiple channels with these filters on the home page. Replace "/@channelURL" with the channel URL and ChannelName with the channel name that you want to block/hide) / YouTube Fix & Customization
youtube.com##[page-subtype="home"] a[href="/@channelURL"]:upward(ytd-rich-item-renderer)
youtube.com##ytd-search a[href="/@channelURL"]:upward(ytd-video-renderer)
youtube.com##.ytp-suggestion-set[aria-label*="ChannelName"]
youtube.com##yt-formatted-string:has-text(channelName):upward(ytd-compact-video-renderer)
youtube.com##[title="channelName"]:upward(ytd-compact-video-renderer)
! Blocks multiple channels with a single filter
youtube.com##[page-subtype="home"] :is(a[href="/@channelURL"], a[href="/@channelURL"]):upward(ytd-rich-item-renderer)
youtube.com##ytd-search :is(a[href="/@channelURL"], a[href="/@channelURL"]):upward(ytd-video-renderer)

! (10/11) YouTube Live Theater Mode Chat Fix (Removes the sidebar chat from the video player, restores Full Width Theater Mode, and disables chat or reverts its location. Choose one option.) / YouTube Fix & Customization by Arch
youtube.com##+js(ra, live-chat-present-and-expanded|panel-expanded|fixed-panels|watch-while-panels-active, ytd-watch-flexy, stay)
youtube.com##+js(set-attr, ytd-watch-flexy, is-two-columns_)
! Disables Chat
youtube.com###chat-container
||youtube.com/live_chat
! Keeps Chat and reverts its location
youtube.com###columns.ytd-watch-flexy:style(display: grid !important; grid-template-columns: 1fr auto !important;)
youtube.com###primary.ytd-watch-flexy, #chat-container.ytd-watch-flexy:style(grid-row: 1 !important;)
youtube.com###secondary.ytd-watch-flexy:style(grid-column: 2 !important;)
youtube.com###chat-container.ytd-watch-flexy:style(margin-top: var(--ytd-margin-6x) !important; width: var(--ytd-watch-flexy-sidebar-width) !important;)

! (11/11) YouTube Title, Description, Comments and Related Videos Swap Fix (Restore the title, description, and comments section to the left, and related videos to the right of the page.) / YouTube Fix & Customization by Arch 
youtube.com##+js(set, yt.config_.EXPERIMENT_FLAGS.kevlar_watch_grid, false)
youtube.com##:matches-path(/watch) ytd-rich-item-renderer[is-link-card-full-width]:style(width: auto !important;)
youtube.com##:matches-path(/watch) #thumbnail.ytd-rich-grid-media:style(width: 168px !important; margin-right: 8px !important;)
youtube.com##:matches-path(/watch) #dismissible.ytd-rich-grid-media:style(display: grid !important; grid-template-columns: 1fr auto !important;)
youtube.com##:matches-path(/watch) #details > #avatar-link.ytd-rich-grid-media:style(display: none !important;)
youtube.com##:matches-path(/watch) #meta > h3.ytd-rich-grid-media:style(margin: initial !important;)
youtube.com##:matches-path(/watch) ytd-video-owner-renderer.ytd-watch-metadata, #bottom-actions.ytd-watch-metadata:style(width: initial !important;)
youtube.com##:matches-path(/watch) #owner.ytd-watch-metadata:style(justify-content: initial !important;)
youtube.com##:matches-path(/watch) ytd-rich-item-renderer:style(margin-bottom: 8px !important;)
youtube.com##:matches-path(/watch) #secondary.ytd-watch-flexy:style(padding: 0 !important;)

! YouTube Premium Logo
youtube.com##svg[id^="yt-logo"] > g:nth-child(2)
youtube.com##svg[id^="yt-ringo"] > g:nth-child(2)
youtube.com##yt-icon.ytd-logo:style(width: 100% !important; margin-left: -10px !important;)
youtube.com###logo-icon::after:style(content: "Premium"; font-size: 20px; margin-left: -70px; letter-spacing: -1px;)
youtube.com###country-code.ytd-topbar-logo-renderer:style(margin-left: 12px !important;)
!youtube.com###country-codeyoutube.com##svg[id^="yt-ringo"]youtube.com##svg[id^="yt-logo"]youtube.com##svg[id^="yt-ringo"]
