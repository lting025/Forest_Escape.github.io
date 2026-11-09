# 音效來源與授權

本網站使用 Moodist 上游專案所提供的自然錄音，下載日期：2026-11-09。

上游：https://github.com/remvze/moodist

上游主分支快照：`11c0be2200116a3635880d600fd6953899cc51a3`。錄音下載自 main；下列 SHA-256 記錄本包實際內容。

注意：上游 README 將第三方音效列為 **CC0 與 Pixabay Content License 混合素材**，並沒有逐檔列出授權。因此本專案不宣稱所有音效都是 CC0，也不把程式碼的 MIT 授權套用到錄音。錄音隨這個有互動 3D 場景的網站整合使用，請勿另行作為獨立素材包販售或分發。

- CC0：https://creativecommons.org/publicdomain/zero/1.0/
- Pixabay Content License：https://pixabay.com/service/license-summary/
- 上游授權說明：https://github.com/remvze/moodist#license

| 本地檔名 | 上游路徑 | SHA-256 |
| --- | --- | --- |
| wind-in-trees.mp3 | public/sounds/nature/wind-in-trees.mp3 | `b29f775dda9789004aaceee392e124eaa35c0386d27f99b93a639185d98f6b4b` |
| campfire.mp3 | public/sounds/nature/campfire.mp3 | `9625b15c7f6a4a2d16db937f0e1042762421f9a3ab74f60235bd63654bba13db` |
| birds.mp3 | public/sounds/animals/birds.mp3 | `f9b022ed2df9f727a8e84e614b25965112dfe2bbb30cdf8c3db0442ae1eed489` |
| waves.mp3 | public/sounds/nature/waves.mp3 | `40c670e678b5ee19ff67a8c322490b1f7d2d53124cf9e8b07efd329138aaa8f8` |
| seagulls.mp3 | public/sounds/animals/seagulls.mp3 | `ceae3d3a3c57e6c383c86e4a427b538379299133ba595e3b4f40e051886c13a8` |
| light-rain.mp3 | public/sounds/rain/light-rain.mp3 | `967eab5ddc2b84808a05fea757460d51461e9dc56e72a3d1490bbb58e7bc6578` |
| droplets.mp3 | public/sounds/nature/droplets.mp3 | `d21f0af60663a03b477739a425ddc59be394ff60ddd1a877bff280b352a57d77` |

檔案保留原始音訊；播放時以 Web Audio 低通濾波、音量控制、壓縮器及循環重疊淡入淡出處理。感謝 Moodist 維護者與原錄音貢獻者。
