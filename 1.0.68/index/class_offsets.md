# Kenshi Class Offset Reference

Extracted from KenshiLib headers. Field offsets are
STABLE across versions (1.0.65 / 1.0.68) since the C++ class
layout doesn't change between Kenshi minor releases.

Total: 113 classes, 3001 fields.

---

## AABB2D
*ZoneManager.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `float` | `x` |
| 0x0 | `ZoneMap*` | `zone` |
| 0x0 | `ZoneSpacialGrid::ZoneCell**` | `zones` |
| 0x0 | `ZoneMapContent*` | `mapContent` |
| 0x0 | `bool` | `_zoneBeingLoaded` |
| 0x0 | `ParticleSystemHandler*` | `particle` |
| 0x0 | `unsigned int` | `limit` |
| 0x1 | `bool` | `_zoneIsLoaded` |
| 0x4 | `float` | `y` |
| 0x4 | `unsigned int` | `lastIndex` |
| 0x8 | `float` | `x2` |
| 0x8 | `SpacialCell**` | `cells` |
| 0x8 | `function*` | `createCellsFunc` |
| 0x8 | `boost::recursive_mutex` | `swapMutex` |
| 0x8 | `boost::shared_mutex` | `swapMutex` |
| 0x8 | `MapFeatureList*` | `mapFeatures` |
| 0x8 | `GameData*` | `effectData` |
| 0x8 | `ParticlePool::ParticleData*` | `particles` |
| 0x8 | `bool` | `justLoadedAGame` |
| 0xC | `float` | `y2` |
| 0x10 | `int` | `cellCount` |
| 0x10 | `ZoneSmell*` | `zoneSmell` |
| 0x10 | `Ogre::SceneNode*` | `node` |
| 0x10 | `float` | `maxTTL` |
| 0x10 | `ZoneSpacialGrid` | `characterGrid` |
| 0x14 | `float` | `cellSize` |
| 0x18 | `boost::shared_mutex` | `mutex` |
| 0x18 | `iVector2` | `coordinates` |
| 0x20 | `std::set<T, std::less<T>, std::allocator<T> >` | `mainThreadData` |
| 0x20 | `int` | `island` |
| 0x24 | `bool` | `hasFile` |
| 0x28 | `T` | `mainThreadData` |
| 0x28 | `BackThreadMessagesToMainT<ZONE_MESSAGE>` | `zoneIncomingMessagesT` |
| 0x2A | `T` | `backThreadData` |
| 0x40 | `std::set<T, std::less<T>, std::allocator<T> >` | `backThreadData` |
| 0x48 | `ZoneSpacialGrid` | `buildingGrid` |
| 0x80 | `ZoneSpacialGrid` | `itemGrid` |
| 0x88 | `MainthreadStateReaderT<ZoneMap::StateT>` | `stateT` |
| 0xB8 | `TerrainSector*` | `terrainCollision` |
| 0xB8 | `bool` | `_needCalculateIslands` |
| 0xBC | `float` | `spawnUpdateTimerMT` |
| 0xC0 | `float` | `spawnUpdateTimerTT` |
| 0xCC | `bool` | `_generateNavMeshesFlag` |
| 0xD0 | `Ogre::Aabb` | `bounds` |
| 0xE8 | `Ogre::Vector4` | `AABB` |
| 0xF8 | `Ogre::Vector3` | `center` |
| 0x108 | `lektor<GameData*>` | `biomes` |
| 0x120 | `int` | `loadCount` |
| 0x1680C8 | `ogre_unordered_set<ZoneMap*>::type` | `processingNewActiveZones` |
| 0x168108 | `ogre_unordered_set<ZoneMap*>::type` | `activeZones` |
| 0x168148 | `ogre_unordered_set<Town*>::type` | `updatedTownOverrides` |
| 0x168188 | `lektor<MapFeatureList*>` | `loadedFeatureLists` |
| 0x1681A0 | `std::set<Town*, std::less<Town*>, Ogre::STLAllocator<Town*, ` | `distantTownList` |
| 0x1681C8 | `iVector2` | `distantTownCentre` |
| 0x1681D0 | `ZoneMap*` | `centralZone` |
| 0x1681D8 | `int` | `loadingPhase` |
| 0x1681E0 | `ogre_unordered_map<iVector2, ZoneMapOverlay*>::type` | `overlays` |
| 0x168220 | `BiomeMap*` | `biomeMap` |
| 0x168228 | `ogre_unordered_map<int, unsigned char*>::type` | `groundTypes` |
| 0x168268 | `ogre_unordered_map<int, ZoneManager::BiomeGroundEffects>::ty` | `groundEffects` |
| 0x1682A8 | `ParticlePool` | `groundEffectsPool` |

## AnimalInventoryLayout : public InventoryLayout
*CharacterAnimal.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x6D8 | `bool` | `weaponIsTechnicallyEquipped` |
| 0x6DC | `float` | `HPMultiplier` |
| 0x6E0 | `TimeOfDay` | `itemInMouthTimeStamp` |
| 0x6E8 | `float` | `smellThresholdBlood` |
| 0x6EC | `float` | `smellThresholdEggs` |
| 0x6F0 | `float` | `ageSizeMin` |
| 0x6F4 | `float` | `ageSizeMax` |
| 0x6F8 | `float` | `lifespanInDays` |
| 0x6FC | `float` | `lastUpdatedAge` |
| 0x700 | `float` | `age` |
| 0x708 | `Weapon*` | `weaponInHands` |
| 0x710 | `float` | `audioTimeStamp` |

## AppearanceManager : public Ogre::GeneralAllocatedObject
*AppearanceManager.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `Ogre::FastArray<DataRange>` | `ranges` |
| 0x0 | `Gender::Enum` | `value` |
| 0x0 | `GameData*` | `race` |
| 0x0 | `Ogre::FastArray<GameData*>` | `races` |
| 0x8 | `std::string` | `name` |
| 0x8 | `Gender` | `gender` |
| 0x10 | `Ogre::FastArray<GameData*>` | `headsData` |
| 0x18 | `Ogre::FastArray<DataRangePose>` | `posesRanges` |
| 0x18 | `boost::unordered::unordered_map<GameData*, ogre_unordered_ma` | `racesAppearanceData` |
| 0x28 | `boost::unordered::unordered_map<int, Ogre::FastArray<GameDat` | `attachments` |
| 0x30 | `short` | `max` |
| 0x30 | `Ogre::FastArray<DataRangeVector>` | `vectorRanges` |
| 0x32 | `short` | `min` |
| 0x34 | `short` | `mid` |
| 0x36 | `short` | `random_group` |
| 0x38 | `short` | `random_variation` |
| 0x40 | `std::string` | `pose_name` |
| 0x40 | `Ogre::FastArray<Ogre::Vector3>` | `values` |
| 0x48 | `DataCategory::Enum` | `value` |
| 0x58 | `Ogre::FastArray<AnimationData*>` | `characterIdleAnimations` |
| 0x68 | `std::string` | `pose_opposite_name` |
| 0x68 | `ogre_unordered_map<DataCategory::Enum, DataCategory>::type` | `categories` |
| 0x70 | `GameDataCopyStandalone*` | `baseAppearanceData` |
| 0xA8 | `boost::unordered::unordered_map<std::string, DataRange const` | `rangesByName` |
| 0xE8 | `Ogre::FastArray<float>` | `headsDataProb` |
| 0x100 | `boost::unordered::unordered_map<int, Ogre::FastArray<float>,` | `attachmentsProb` |
| 0x140 | `boost::unordered::unordered_map<unsigned __int64, Ogre::Fast` | `factionAttachments` |
| 0x180 | `boost::unordered::unordered_map<std::string, std::string, bo` | `texturesSkin` |
| 0x1C0 | `std::string` | `meshFile` |

## Array2d
*Array2d.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `unsigned int` | `nRows` |
| 0x4 | `unsigned int` | `nCols` |
| 0x8 | `std::vector<T*, Ogre::STLAllocator<T*, Ogre::GeneralAllocPol` | `data` |

## Bounty
*Bounty.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `int` | `amount` |
| 0x4 | `unsigned int` | `crimes` |
| 0x8 | `bool` | `bountyHasBeenClaimedOnce` |
| 0x10 | `TimeOfDay` | `bountyAssignmentStartedTime` |

## BountyManager
*BountyManager.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `public:
    ogre_unordered_map<Faction*, Bounty>::type` | `bounties` |
| 0x40 | `Character*` | `me` |
| 0x48 | `Faction*` | `_hasAccessPass` |
| 0x50 | `TimeOfDay` | `accessPassExpirationTime` |
| 0x58 | `CrimeEnum` | `committingCrime` |
| 0x60 | `Faction*` | `crimeAgainstFaction` |
| 0x68 | `Faction*` | `usingTrainingEquipmentOf` |
| 0x70 | `hand` | `crimeAgainst` |
| 0x90 | `float` | `crimeExpiry` |
| 0x98 | `TimeOfDay` | `prisonSentenceBeganTime` |
| 0xA0 | `float` | `prisonSentenceToServe` |
| 0xA4 | `bool` | `_hadABountyAssignedForCurrentCrime` |

## BuildInventoryLayout : public InventoryLayout
*ProductionBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x3B8 | `MyGUI::TextBox*` | `input1NameText` |
| 0x3C0 | `MyGUI::TextBox*` | `input2NameText` |
| 0x3C8 | `MyGUI::TextBox*` | `input1StatusText` |
| 0x3D0 | `MyGUI::TextBox*` | `input2StatusText` |
| 0x3D8 | `MyGUI::ImageBox*` | `input1ItemIcon` |
| 0x3E0 | `MyGUI::ImageBox*` | `input2ItemIcon` |
| 0x3E8 | `MyGUI::TextBox*` | `outputNameText` |
| 0x3F0 | `MyGUI::ImageBox*` | `outputItemIcon` |
| 0x3F8 | `MyGUI::Widget*` | `input1Panel` |
| 0x400 | `MyGUI::Widget*` | `input2Panel` |
| 0x408 | `MyGUI::ProgressBar*` | `input1Progress` |
| 0x410 | `MyGUI::ProgressBar*` | `input2Progress` |
| 0x418 | `MyGUI::ProgressBar*` | `outputProgress` |
| 0x420 | `int` | `inputs` |
| 0x424 | `int` | `outputs` |
| 0x428 | `Item*` | `input1Item` |
| 0x430 | `Item*` | `input2Item` |
| 0x438 | `Item*` | `outputItem` |
| 0x468 | `ProductionBuilding::ProductionState` | `productionState` |
| 0x46C | `float` | `_resourceMiningLevel` |
| 0x470 | `InventorySection*` | `outSection` |
| 0x478 | `lektor<StorageBuilding::ConsumptionItem>` | `consumptionItems` |

## BuildModeWindow : public wraps::BaseLayout
*BuildModeWindow.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `public:
        std::string` | `name` |
| 0x0 | `public:
        std::string` | `name` |
| 0x28 | `Ogre::vector<GameData*>::type` | `buildings` |
| 0x28 | `Ogre::vector<BuildModeWindow::BuildingGroup>::type` | `buildingGroups` |
| 0xA0 | `PlayerBuildMode*` | `playerBuildMode` |
| 0xA8 | `bool` | `levelEditorMode` |
| 0xB0 | `Ogre::vector<BuildModeWindow::BuildingCategory*>::type` | `playerCategories` |
| 0xD0 | `Research*` | `playerResearch` |
| 0xD8 | `BuildModeWindow::BuildingCategory*` | `currentBuildingCategory` |
| 0xE0 | `BuildModeWindow::BuildingGroup` | `currentBuildingGroup` |
| 0x128 | `GameData*` | `currentBuildingInfo` |
| 0x130 | `short` | `currentBuildingIndex` |
| 0x132 | `short` | `switchBuildingIndex` |
| 0x138 | `DatapanelGUI*` | `statsDataPanel` |
| 0x140 | `MyGUI::Button*` | `confirmButton` |
| 0x148 | `MyGUI::Button*` | `undoButton` |
| 0x150 | `MyGUI::Button*` | `closeButton` |
| 0x158 | `MyGUI::ListBox*` | `categoriesList` |
| 0x160 | `MyGUI::ListBox*` | `buildingsList` |
| 0x168 | `MyGUI::TextBox*` | `buildingTxt` |
| 0x170 | `MyGUI::Button*` | `buildingTypePrevButton` |
| 0x178 | `MyGUI::Button*` | `buildingTypeNextButton` |
| 0x180 | `MyGUI::ImageBox*` | `buildingImageBox` |
| 0x188 | `MyGUI::Widget*` | `statsPanel` |
| 0x190 | `MyGUI::TextBox*` | `descriptionTxt` |
| 0x198 | `MyGUI::EditBox*` | `messageTextBox` |
| 0x1A0 | `MyGUI::Button*` | `floorDownButton` |
| 0x1A8 | `MyGUI::Button*` | `floorUpButton` |
| 0x1B0 | `MyGUI::TextBox*` | `floorText` |

## BuildingContainerInventoryLayout : public GenericInventoryLayout
*StorageBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `float` | `amount` |
| 0x4 | `float` | `rate` |
| 0x8 | `int` | `maxCapacity` |
| 0x10 | `GameData*` | `item` |
| 0x18 | `InventorySection*` | `inventorySection` |
| 0x3C0 | `MyGUI::EditBox*` | `capacityText` |
| 0x440 | `itemType` | `specialItemTypesOnly` |
| 0x444 | `bool` | `endOfTheLine` |
| 0x448 | `StorageBuilding::ConsumptionItem*` | `productionItem` |
| 0x450 | `lektor<StorageBuilding::ConsumptionItem*>` | `manyLimitItems` |

## CameraClass
*CameraClass.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `bool` | `isRotating` |
| 0x4 | `tagPOINT` | `lastMousePos` |
| 0x10 | `Ogre::Entity*` | `rotationMarker` |
| 0x18 | `float` | `yaw` |
| 0x1C | `float` | `pitch` |
| 0x20 | `bool` | `initialised` |
| 0x21 | `bool` | `terrainLoaded` |
| 0x28 | `hand` | `objectCurrentlyFollowing` |
| 0x48 | `Ogre::Vector3` | `objectCurrentlyFollowingOffset` |
| 0x58 | `Ogre::SceneNode*` | `center` |
| 0x60 | `float` | `altitude` |
| 0x68 | `Ogre::Camera*` | `camera` |
| 0x70 | `Ogre::SceneNode*` | `node` |
| 0x78 | `int` | `currentMusic` |
| 0x80 | `hand` | `inBuilding` |
| 0xA0 | `float` | `timeInGame` |
| 0xA4 | `float` | `targetPositionY` |
| 0xA8 | `float` | `speedY` |
| 0xB0 | `Building*` | `centerBuilding` |
| 0xB8 | `float` | `centerBuildingY` |
| 0xBC | `unsigned short` | `currentCollisionGroup` |
| 0xBE | `unsigned char` | `currentFloor` |
| 0xBF | `bool` | `freeCameraMode` |

## CampaignTriggerData
*Dialogue.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `public:
    GameData*` | `what` |
| 0x0 | `GameData*` | `data` |
| 0x0 | `public:
        DialogActionEnum` | `key` |
| 0x0 | `public:
        DialogConditionEnum` | `key` |
| 0x0 | `DialogConditionEnum` | `key` |
| 0x0 | `public:
    lektor<DialogLineData*>` | `conversationChoices` |
| 0x0 | `int` | `count` |
| 0x0 | `std::map<EventTriggerEnum, Dialogue::RepetitionCounter::Dial` | `states` |
| 0x0 | `Dialogue::RepetitionCounter` | `repCounter` |
| 0x4 | `int` | `value` |
| 0x4 | `ComparisonEnum` | `compareBy` |
| 0x4 | `bool` | `want` |
| 0x4 | `float` | `lastTimeStamp` |
| 0x8 | `int` | `minTime` |
| 0x8 | `int` | `val0` |
| 0x8 | `TalkerEnum` | `who` |
| 0x8 | `unsigned int` | `flags` |
| 0x8 | `unsigned int` | `targetFlagsNeeded` |
| 0x8 | `float` | `resetTime` |
| 0xC | `int` | `maxTime` |
| 0xC | `int` | `value` |
| 0xC | `unsigned int` | `targetFlagsNotWanted` |
| 0x10 | `float` | `chance` |
| 0x10 | `unsigned int` | `personalityNeeded` |
| 0x14 | `unsigned int` | `personalityNotWanted` |
| 0x18 | `FitnessSelector<CampaignTriggerData*>` | `campaignTriggers` |
| 0x28 | `bool` | `_needsDynamicAssessments` |
| 0x30 | `std::map<DialogLineData*, bool, std::less<DialogLineData*>, ` | `locked` |
| 0x58 | `std::string` | `sayMsg` |
| 0x78 | `lektor<GameData*>` | `isTargetRace` |
| 0x80 | `Ogre::vector<Dialogue::DT_MSG>::type` | `threadMessages` |
| 0x90 | `lektor<GameData*>` | `isTargetSubRace_specificallyTheTarget` |
| 0xA0 | `std::set<GameData*, std::less<GameData*>, Ogre::STLAllocator` | `pacakgesIHave` |
| 0xA1 | `bool` | `stayOnScreen` |
| 0xA2 | `bool` | `shout` |
| 0xA4 | `int` | `marginW` |
| 0xA8 | `int` | `marginH` |
| 0xA8 | `lektor<GameDataValuePair>` | `givesItem` |
| 0xB0 | `MyGUI::EditBox*` | `textBox` |
| 0xB8 | `MyGUI::types::TSize<int>` | `baseSize` |
| 0xC0 | `std::set<Faction*, std::less<Faction*>, Ogre::STLAllocator<F` | `inTownOf` |
| 0xC8 | `DialogLineData*` | `playerInterruptionDialog` |
| 0xD0 | `std::map<EventTriggerEnum, float, std::less<EventTriggerEnum` | `eventRepeatTimers` |
| 0xE8 | `std::set<Faction*, std::less<Faction*>, Ogre::STLAllocator<F` | `isTargetFaction` |
| 0xF8 | `std::map<EventTriggerEnum, hand, std::less<EventTriggerEnum>` | `eventDeliveredStates` |
| 0x110 | `std::set<Faction*, std::less<Faction*>, Ogre::STLAllocator<F` | `isMyFaction` |
| 0x120 | `std::map<DialogLineData*, bool, std::less<DialogLineData*>, ` | `_hasChanceLines` |
| 0x138 | `lektor<GameData*>` | `isCharacter` |
| 0x148 | `bool` | `_hasEnded` |
| 0x149 | `bool` | `shouting` |
| 0x14A | `bool` | `staysOnScreen` |
| 0x150 | `lektor<GameData*>` | `isTargetCarryingCharacter` |
| 0x150 | `Character*` | `me` |
| 0x158 | `hand` | `conversationTarget` |
| 0x168 | `lektor<GameData*>` | `_hasPackage` |
| 0x178 | `CharStats*` | `stats` |
| 0x180 | `lektor<GameData*>` | `isMyRace` |
| 0x180 | `CharMovement*` | `movement` |
| 0x188 | `EventTriggerEnum` | `currentConversationType` |
| 0x190 | `DialogLineData*` | `currentConversation` |
| 0x198 | `lektor<GameData*>` | `isMySubRace` |
| 0x198 | `DialogLineData*` | `currentLine` |
| 0x1A0 | `std::map<EventTriggerEnum, DialogChoiceList*, std::less<Even` | `conversationsMain` |
| 0x1B0 | `ItemFunction` | `hasItemType` |
| 0x1B8 | `lektor<GameData*>` | `hasItem` |
| 0x1C8 | `hand` | `interjector1` |
| 0x1D0 | `WorldEventStateQueryList*` | `worldState` |
| 0x1D8 | `GameData*` | `data` |
| 0x1E0 | `bool` | `onceOnly` |
| 0x1E1 | `bool` | `isMonologue` |
| 0x1E4 | `CharacterTypeEnum` | `forCertainType` |
| 0x1E8 | `DialogChoiceList*` | `children` |
| 0x1E8 | `hand` | `interjector2` |
| 0x1F0 | `lektor<DialogLineData::DialogCondition*>` | `conditions` |
| 0x208 | `lektor<DialogLineData::DialogAction*>` | `actions` |
| 0x208 | `hand` | `interjector3` |
| 0x220 | `int` | `lineCount` |
| 0x228 | `std::string*` | `texts` |
| 0x228 | `DialogueSpeechBubble*` | `speechBubblePanel` |
| 0x230 | `DialogLineData*` | `parent` |
| 0x230 | `float` | `speechTextTimer` |
| 0x234 | `float` | `speechTextTimer_forced` |
| 0x238 | `float` | `chancePermanent` |
| 0x238 | `Ogre::vector<std::string>::type` | `replyIds` |
| 0x23C | `float` | `chanceTemporary` |
| 0x240 | `bool` | `unique` |
| 0x248 | `hand` | `uniqueOwner` |
| 0x258 | `Ogre::vector<std::string>::type` | `responses` |
| 0x268 | `float` | `dialogRepeatMinTimeInHours` |
| 0x270 | `TimeOfDay` | `lastTimeSaid` |
| 0x278 | `int` | `score` |
| 0x278 | `std::string` | `npcReplyText` |
| 0x27C | `bool` | `oneAtATime` |
| 0x27D | `bool` | `isLocked` |
| 0x280 | `lektor<DialogLineData*>` | `locks` |
| 0x298 | `lektor<DialogLineData*>` | `unlocks_lockMe` |
| 0x2A0 | `hand` | `conversationMaster` |
| 0x2B0 | `lektor<DialogLineData*>` | `unlocks_dontLockMe` |
| 0x2C0 | `hand` | `waitingForReplyFrom` |
| 0x2C8 | `DialogLineData*` | `crowdTrigger` |
| 0x2D0 | `ogre_unordered_map<GameData*, int>::type` | `factionRelationEffects` |
| 0x310 | `DialogLineData*` | `playerInterruptionDialog` |
| 0x318 | `bool` | `isInterjection` |
| 0x31C | `TalkerEnum` | `speaker` |

## CharBody : public Ogre::GeneralAllocatedObject
*CharBody.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `CombatClass*` | `combatClass` |
| 0x10 | `AnimationClass*` | `animation` |
| 0x18 | `Character*` | `character` |
| 0x20 | `CharStats*` | `stats` |
| 0x28 | `hand` | `target` |
| 0x48 | `bool` | `gotItem` |
| 0x49 | `bool` | `crouched` |
| 0x4A | `bool` | `jogMode` |
| 0x4C | `float` | `arbitraryCatchupDist` |
| 0x50 | `AI*` | `ai` |
| 0x58 | `CharMovement*` | `movement` |
| 0x60 | `float` | `frameTIME` |
| 0x68 | `Tasker*` | `currentAction` |
| 0x70 | `bool` | `amIdle` |

## CharStats : public Ogre::GeneralAllocatedObject
*CharStats.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `MedicalSystem*` | `medical` |
| 0x10 | `Character*` | `me` |
| 0x18 | `float` | `athleticsMultiplier` |
| 0x1C | `float` | `combatSpeedMultiplier` |
| 0x20 | `int` | `_skillBonusAttack` |
| 0x24 | `int` | `_skillBonusDefence` |
| 0x28 | `int` | `skillBonusIndoors` |
| 0x2C | `int` | `skillBonusUnarmed` |
| 0x30 | `int` | `skillBonusPerception` |
| 0x34 | `float` | `ageMult` |
| 0x38 | `float` | `skillMultDodge` |
| 0x3C | `float` | `skillMultStealth` |
| 0x40 | `float` | `skillMultAssassin` |
| 0x44 | `float` | `skillMultDexterity` |
| 0x48 | `float` | `skillMultDamage` |
| 0x4C | `float` | `fistInjuryEquipmentMult` |
| 0x50 | `float` | `skillMultRanged` |
| 0x58 | `std::map<WeatherAffecting, float, std::less<WeatherAffecting` | `_weatherProtections` |
| 0x80 | `float` | `_strength` |
| 0x84 | `float` | `fitness` |
| 0x88 | `float` | `_dexterity` |
| 0x8C | `float` | `perception` |
| 0x90 | `float` | `_toughness` |
| 0x94 | `float` | `_athletics` |
| 0x98 | `float` | `medic` |
| 0x9C | `float` | `massCombat` |
| 0xA0 | `float` | `arrowDefence` |
| 0xA4 | `float` | `stealth` |
| 0xA8 | `float` | `swimming` |
| 0xAC | `float` | `thieving` |
| 0xB0 | `float` | `lockpicking` |
| 0xB4 | `float` | `bluff` |
| 0xB8 | `float` | `assassin` |
| 0xBC | `float` | `survival` |
| 0xC0 | `float` | `tracking` |
| 0xC4 | `float` | `climbing` |
| 0xC8 | `float` | `doctor` |
| 0xCC | `float` | `engineer` |
| 0xD0 | `float` | `weaponSmith` |
| 0xD4 | `float` | `armourSmith` |
| 0xD8 | `float` | `bowSmith` |
| 0xDC | `float` | `robotics` |
| 0xE0 | `float` | `science` |
| 0xE4 | `float` | `labouring` |
| 0xE8 | `float` | `farming` |
| 0xEC | `float` | `cooking` |
| 0xF0 | `float` | `dodging` |
| 0xF4 | `float` | `friendlyFire` |
| 0xF8 | `float` | `katanas` |
| 0xFC | `float` | `sabres` |
| 0x100 | `float` | `hackers` |
| 0x104 | `float` | `blunt` |
| 0x108 | `float` | `heavyWeapons` |
| 0x10C | `float` | `unarmed` |
| 0x110 | `float` | `bows` |
| 0x114 | `float` | `turrets` |
| 0x118 | `float` | `polearms` |
| 0x11C | `float` | `currentItemMaximumJuryRig` |
| 0x120 | `float` | `__meleeAttack` |
| 0x124 | `float` | `_meleeDefence` |
| 0x128 | `bool` | `_defensiveMode` |
| 0x129 | `bool` | `rangedMode` |
| 0x12A | `bool` | `tauntMode` |
| 0x12B | `bool` | `_holdPositionMode` |
| 0x12C | `bool` | `passiveCombatMode` |
| 0x130 | `Ogre::Vector3` | `holdLocation` |
| 0x13C | `float` | `warriorSpirit` |
| 0x140 | `float` | `derivedSpirit` |
| 0x144 | `float` | `aggression` |
| 0x148 | `float` | `goodness` |
| 0x14C | `float` | `evilness` |
| 0x150 | `float` | `longestReachingAttack` |
| 0x154 | `float` | `STUBBOURNESS` |
| 0x158 | `float` | `PROFESSIONALNESS` |
| 0x15C | `float` | `HOLDING_POSITION` |
| 0x160 | `float` | `IMMEDIACY` |
| 0x164 | `float` | `IMMEDIACY_MAX_RANGE` |
| 0x168 | `float` | `MANLINESS` |
| 0x16C | `float` | `MURDEROUS` |
| 0x170 | `float` | `_stealthXPMultForGUI` |
| 0x174 | `float` | `stealthXPTooManyCooksPenalty` |
| 0x178 | `float` | `currentOperatingMachineHungerRate` |
| 0x17C | `float` | `moveSpeed` |
| 0x180 | `float` | `weaponWeightSpeedMult` |
| 0x184 | `float` | `weaponWeightXPMult` |
| 0x188 | `float` | `attackSpeed` |
| 0x18C | `float` | `blockSpeed` |
| 0x190 | `float` | `encumbranceMult` |
| 0x194 | `float` | `xp` |
| 0x198 | `int` | `freeAttributePoints` |
| 0x19C | `float` | `cutDamageMult` |
| 0x1A0 | `float` | `bluntDamageMult` |
| 0x1A4 | `float` | `bleedDamageMult` |
| 0x1A8 | `float` | `pierceDamageMult` |
| 0x1AC | `float` | `cutDamageMin` |
| 0x1B0 | `float` | `bluntDamageMin` |
| 0x1B4 | `float` | `bonusRobots` |
| 0x1B8 | `float` | `bonusHumans` |
| 0x1BC | `float` | `bonusAnimals` |
| 0x1C0 | `float` | `bonusArmourPenetration` |
| 0x1C8 | `std::map<GameData*, float, std::less<GameData*>, Ogre::STLAl` | `bonusRaces` |
| 0x1F0 | `WeaponCategory` | `currentWeaponType` |
| 0x1F8 | `float*` | `pCurrentWeaponSkill` |
| 0x200 | `float` | `currentWeaponLength` |
| 0x208 | `hand` | `weapon` |
| 0x228 | `float` | `weaponWeight` |

## CharacterHuman : public Character
*CharacterHuman.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x6D8 | `Weapon*` | `weaponInHands` |
| 0x6E0 | `std::string` | `weaponInHandsSheathLocation` |

## CombatTechniqueData
*CombatTechniqueData.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `CutDirection` | `direction` |
| 0x0 | `std::string` | `animation` |
| 0x4 | `float` | `power` |
| 0x8 | `float` | `impactAnimationFrame` |
| 0xC | `float` | `motionStopsAnimationFrame` |
| 0x10 | `RobotLimbs::Limb` | `limb` |
| 0x28 | `float` | `animSpeedMultiplier` |
| 0x2C | `bool` | `isBlock` |
| 0x2D | `bool` | `isDodge` |
| 0x2E | `bool` | `stumbleDodge` |
| 0x2F | `bool` | `gainsGround` |
| 0x30 | `bool` | `isProne` |
| 0x31 | `bool` | `lowStrike` |
| 0x34 | `float` | `hesitationPoint` |
| 0x38 | `float` | `initialDistance` |
| 0x3C | `float` | `minDistanceVsStatic` |
| 0x40 | `float` | `acceptableEndTime01` |
| 0x44 | `float` | `minSkill` |
| 0x48 | `float` | `maxSkill` |
| 0x4C | `float` | `maxEncumbrance` |
| 0x50 | `float` | `chanceMult` |
| 0x54 | `int` | `maxTargetHits` |
| 0x58 | `ogre_unordered_map<GameData*, float>::type` | `events` |
| 0xB0 | `lektor<CombatTechniqueData::ImpactPoint>` | `impactPoints` |

## ConstructionState : public Ogre::GeneralAllocatedObject
*Building.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `bool` | `isComplete` |
| 0x0 | `public:
            GameData*` | `mat` |
| 0x1 | `bool` | `isPaused` |
| 0x2 | `bool` | `isDismantled` |
| 0x4 | `float` | `constructionProgress` |
| 0x8 | `float` | `msgDismantleAmount` |
| 0x8 | `float` | `buildMatsTotal` |
| 0x8 | `bool` | `wantsAboveGround` |
| 0x8 | `Ogre::SceneNode*` | `parentNode` |
| 0xC | `float` | `amountOfMaterials` |
| 0xC | `float` | `lower` |
| 0x10 | `lektor<ConstructionState::BuildMaterial*>` | `mats` |
| 0x10 | `float` | `space` |
| 0x10 | `Ogre::vector<Ogre::Entity*>::type` | `entitiesList` |
| 0x14 | `float` | `scale` |
| 0x18 | `Ogre::Entity*` | `ent` |
| 0x20 | `NxBox` | `box` |
| 0x28 | `float` | `totalMats` |
| 0x2C | `float` | `buildTimeMult` |
| 0x30 | `int` | `buildersThisFrame` |
| 0x30 | `lektor<Footprint>` | `footprints` |
| 0x34 | `float` | `pathThreshold` |
| 0x48 | `bool` | `isCurrentlySnapped` |
| 0x50 | `Building*` | `snappedTo` |
| 0x58 | `lektor<FootprintNode>` | `usageNodes` |
| 0x5C | `Ogre::Vector3` | `pos` |
| 0x68 | `Ogre::Quaternion` | `rot` |
| 0x70 | `DatapanelGUI*` | `prospectingInformation` |
| 0x78 | `BuildingPlacementGroundType::Enum` | `groundType` |
| 0x78 | `MiningResource` | `prospectResource` |
| 0x7C | `bool` | `valid` |
| 0x7C | `bool` | `roofOnly` |
| 0x80 | `PreviewBuilding*` | `parent` |
| 0x80 | `float` | `spaceAbove` |
| 0x84 | `float` | `spaceBelow` |
| 0x88 | `Ogre::vector<Ogre::Vector3>::type` | `corners` |
| 0x88 | `bool` | `collisionOK` |
| 0x89 | `bool` | `charactersOK` |
| 0x8A | `bool` | `floorOk` |
| 0x8B | `bool` | `indoorsOK` |
| 0x8C | `bool` | `slopeOK` |
| 0x8D | `bool` | `nodesOk` |
| 0x8E | `bool` | `blockedBuildings` |
| 0x8F | `bool` | `validGround` |
| 0x90 | `Town*` | `inTown` |
| 0x98 | `int` | `floorNum` |
| 0x9C | `bool` | `isOutside` |
| 0x9D | `bool` | `matchSlope` |
| 0xA0 | `lektor<PlacementResult>` | `nodeResults` |
| 0xA8 | `Ogre::Aabb` | `aabb` |
| 0xB8 | `Building*` | `justBeenBuilt` |
| 0xC0 | `bool` | `isFoliage` |
| 0xC0 | `std::string` | `nodeId` |
| 0xC0 | `float` | `yaw` |
| 0xC1 | `bool` | `hasTerrainInside` |
| 0xC2 | `bool` | `isCavernous` |
| 0xC3 | `bool` | `enforceCeiling` |
| 0xC4 | `BuildingDesignation` | `designation` |
| 0xC4 | `Ogre::Vector3` | `centreOffset` |
| 0xC8 | `bool` | `publicDaytime` |
| 0xD0 | `hand` | `residentSquad` |
| 0xD0 | `Building*` | `isFurnitureOf` |
| 0xD8 | `Building*` | `isIndoors` |
| 0xE0 | `Ogre::Aabb` | `AABB` |
| 0xE8 | `bool` | `enabled` |
| 0xF0 | `GameData*` | `residentSquadTemplate` |
| 0xF8 | `bool` | `isAnInteriorObject` |
| 0xF8 | `GameData*` | `buildDataPtr` |
| 0x100 | `InstanceID` | `instanceID` |
| 0x100 | `GameData*` | `farmData` |
| 0x108 | `bool` | `prospectingOK` |
| 0x109 | `bool` | `furniture` |
| 0x10A | `bool` | `exteriorFurniture` |
| 0x10C | `Ogre::Vector3` | `pos` |
| 0x118 | `Ogre::Quaternion` | `rot` |
| 0x128 | `int` | `positionHitGroup` |
| 0x130 | `std::string` | `layoutInstanceID` |
| 0x158 | `BuildingFunction` | `specialFunction` |
| 0x160 | `ConstructionState` | `_buildState` |
| 0x198 | `BuildingClassType` | `classType` |
| 0x19C | `bool` | `updateNavmesh` |
| 0x19D | `bool` | `visible` |
| 0x19E | `bool` | `interiorVisibility` |
| 0x19F | `bool` | `justBeenUpgradedFlag` |
| 0x1A0 | `bool` | `imADoor` |
| 0x1A1 | `bool` | `destroyed` |
| 0x1A4 | `float` | `productionMult` |
| 0x1A8 | `float` | `productionMult_baseData` |
| 0x1AC | `bool` | `hasMovingParts` |
| 0x1B0 | `int` | `saveVersion` |
| 0x1B8 | `lektor<Building*>` | `doors` |
| 0x1D0 | `hand` | `_town` |
| 0x1F0 | `BuildingInterior*` | `myInterior` |
| 0x1F8 | `TownBuildingsManager*` | `buildingsManager` |
| 0x200 | `Ogre::SceneNode*` | `rootNode` |
| 0x208 | `unsigned __int64` | `audioObject` |
| 0x210 | `SoundEmitter*` | `soundEmitter` |
| 0x218 | `bool` | `hasAudio` |
| 0x21C | `GroundType` | `interiorGround` |
| 0x220 | `GroundType` | `exteriorGround` |
| 0x228 | `PhysicsCollection*` | `physical` |
| 0x230 | `int` | `entitiesToLoad` |
| 0x234 | `bool` | `entitiesLoaded` |
| 0x238 | `Layout*` | `isFurnitureOf` |
| 0x240 | `bool` | `isOutsideFurniture` |
| 0x241 | `bool` | `isNestItem` |
| 0x248 | `GameData*` | `baseMaterial` |
| 0x250 | `lektor<std::pair<PhysicalEntity*, Effect*> >` | `effects` |
| 0x268 | `bool` | `effectsVisible` |
| 0x269 | `bool` | `effectsActive` |
| 0x26A | `bool` | `lightsVisible` |
| 0x26C | `Ogre::Vector3` | `positionMarker` |
| 0x278 | `float` | `heightAboveGround` |
| 0x27C | `Ogre::Aabb` | `AABB` |
| 0x294 | `bool` | `isRedDebugTextureMode` |
| 0x298 | `std::string` | `materialName` |
| 0x2C0 | `std::set<std::string, std::less<std::string >, Ogre::STLAllo` | `usageNodesIds` |
| 0x2E8 | `lektor<UsageNode*>` | `usageNodes` |
| 0x300 | `ogre_unordered_map<int, float>::type` | `badNodes` |
| 0x340 | `SimplePhysXEntity*` | `triggerVolume` |
| 0x348 | `lektor<std::pair<char, float> >` | `activeEffects` |

## ContextMenu : public Ogre::GeneralAllocatedObject
*ContextMenu.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `bool` | `rightMouseActivated` |
| 0x8 | `lektor<int>` | `orders` |
| 0x20 | `std::string` | `contextMenuName` |
| 0x48 | `ContextMenuGUI*` | `menuGUI` |
| 0x50 | `ContextMenuGUI*` | `menuGUI2` |
| 0x58 | `bool` | `delayedDestroyFlag` |
| 0xA8 | `hand` | `contextMenuTarget` |
| 0xC8 | `std::string` | `name` |
| 0xF0 | `MyGUI::TextBox*` | `nameText` |
| 0xF8 | `MyGUI::Widget*` | `optionsList` |
| 0x100 | `MyGUI::types::TCoord<int>` | `optionCoords` |
| 0x110 | `MyGUI::types::TCoord<int>` | `buttonCoords` |
| 0x120 | `MyGUI::types::TCoord<int>` | `valueCoords` |

## DataPanelLine : public Ogre::GeneralAllocatedObject
*DataPanelLine.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `MyGUI::TextBox*` | `w1` |
| 0x10 | `MyGUI::TextBox*` | `w2` |
| 0x18 | `int` | `category` |
| 0x20 | `MyGUI::delegates::CDelegate1<DataPanelLine*>` | `callback` |
| 0x28 | `std::string` | `keyValue` |
| 0x50 | `std::string` | `s1` |
| 0x78 | `std::string` | `s2` |
| 0xA0 | `int` | `lo` |
| 0xA4 | `int` | `hi` |
| 0xA8 | `std::string` | `skinW1` |
| 0xD0 | `std::string` | `skinW2` |
| 0xF8 | `Ogre::vector<MyGUI::Widget*>::type` | `widgets` |
| 0x118 | `DataPanelLine::LineType` | `classType` |
| 0x120 | `float` | `v1` |
| 0x120 | `float` | `v1` |
| 0x120 | `hand` | `userData` |
| 0x120 | `float` | `width` |
| 0x120 | `MyGUI::EditBox*` | `editBox` |
| 0x120 | `MyGUI::EditBox*` | `editBox` |
| 0x120 | `float` | `scale` |
| 0x120 | `MyGUI::EditBox*` | `textBox` |
| 0x120 | `bool*` | `valuePtr` |
| 0x120 | `MyGUI::ComboBox*` | `listBox` |
| 0x120 | `MyGUI::Button*` | `btn0` |
| 0x124 | `float` | `v2` |
| 0x124 | `float` | `v2` |
| 0x124 | `bool` | `showName` |
| 0x124 | `float` | `min` |
| 0x128 | `MyGUI::Widget*` | `bar` |
| 0x128 | `bool` | `hasXBut` |
| 0x128 | `float` | `min` |
| 0x128 | `MyGUI::Align` | `textAlign` |
| 0x128 | `MyGUI::EditBox*` | `nameText` |
| 0x128 | `float` | `max` |
| 0x128 | `MyGUI::ProgressBar*` | `progress` |
| 0x128 | `MyGUI::EditBox*` | `text` |
| 0x128 | `float` | `listWidth` |
| 0x128 | `MyGUI::Button*` | `btn1` |
| 0x12C | `float` | `max` |
| 0x12C | `bool` | `wordWrap` |
| 0x130 | `MyGUI::Widget*` | `bar2` |
| 0x130 | `std::string` | `barSkin` |
| 0x130 | `float*` | `valuePtr` |
| 0x130 | `MyGUI::Align` | `textAlign` |
| 0x130 | `float*` | `valuePtr` |
| 0x130 | `MyGUI::EditBox*` | `progressText` |
| 0x130 | `MyGUI::Button*` | `button` |
| 0x130 | `int*` | `valPtr` |
| 0x130 | `std::string` | `command` |
| 0x134 | `bool` | `showKey` |
| 0x135 | `bool` | `multiLine` |
| 0x138 | `MyGUI::Button*` | `but` |
| 0x138 | `float` | `scale` |
| 0x138 | `float` | `width` |
| 0x138 | `MyGUI::Slider*` | `slider` |
| 0x138 | `bool` | `showKey` |
| 0x138 | `bool` | `hasGoBox` |
| 0x140 | `MyGUI::Button*` | `button` |
| 0x140 | `MyGUI::EditBox*` | `nameText` |
| 0x140 | `MyGUI::Button*` | `goBox` |
| 0x148 | `float` | `buttonWidth` |
| 0x148 | `MyGUI::EditBox*` | `valueEditBox` |
| 0x14C | `float` | `buttonHeight` |
| 0x150 | `std::string` | `buttonSkin` |
| 0x150 | `MyGUI::ScrollBar*` | `sliderBar` |
| 0x158 | `MyGUI::Widget*` | `bar` |
| 0x160 | `MyGUI::Button*` | `but` |
| 0x168 | `MyGUI::Button*` | `Xbut` |

## DatapanelGUI : public GUIWindow
*DatapanelGUI.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x30 | `MyGUI::delegates::CMultiDelegate2<DatapanelGUI*, int>` | `tabEvent` |
| 0x48 | `bool` | `frequentUpdatesWanted` |
| 0x50 | `MyGUI::Widget*` | `scrollWin` |
| 0x58 | `bool` | `premadeParentWindow` |
| 0x59 | `bool` | `scrolling` |
| 0x5A | `bool` | `isWindow` |
| 0x60 | `std::map<int, std::map<std::string, DataPanelLine*, std::les` | `content` |
| 0x88 | `std::map<int, DataPanelLine*, std::less<int>, Ogre::STLAlloc` | `bottomLine` |
| 0xB0 | `int` | `currentCategory` |
| 0xB8 | `function*` | `mouseOverEvent` |
| 0xC0 | `void*` | `mouseOverEventDatas` |
| 0xC8 | `bool` | `automaticRefresh` |
| 0xC9 | `bool` | `automaticTarget` |
| 0xD0 | `MyGUI::Window*` | `tabWin` |
| 0xD8 | `lektor<MyGUI::Button*>` | `tabs` |
| 0xF0 | `std::string` | `panelName` |
| 0x118 | `float` | `x` |
| 0x11C | `float` | `y` |
| 0x120 | `float` | `w` |
| 0x124 | `float` | `h` |
| 0x128 | `float` | `DATALINESPACING` |
| 0x12C | `float` | `DATALINETHICKNESS` |
| 0x130 | `bool` | `basicSpacing` |
| 0x138 | `std::string` | `layer` |
| 0x160 | `MyGUI::ScrollView*` | `scrollView` |

## DoorStuff : public Building
*DoorStuff.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x360 | `bool` | `isSetupComplete` |
| 0x368 | `Building*` | `parent` |
| 0x370 | `DoorLock*` | `doorLock` |
| 0x378 | `int` | `gateCode` |
| 0x37C | `float` | `doorOpenAmount` |
| 0x380 | `DoorState` | `state` |
| 0x384 | `bool` | `wantsToLock` |
| 0x388 | `float` | `doorSpeed` |
| 0x38C | `float` | `doorDistance` |
| 0x390 | `int` | `doorMoveAxis` |
| 0x394 | `float` | `doorComesOut` |
| 0x398 | `const Ogre::Vector3` | `nodeClosedPosition` |
| 0x3A4 | `Ogre::Vector3` | `actorClosedPosition` |
| 0x3B0 | `Ogre::Vector3` | `doorClosedPosition` |
| 0x3BC | `Ogre::Vector3` | `doorClosedPositionOut` |
| 0x3C8 | `Ogre::Vector3` | `doorClosedPositionIn` |
| 0x3D4 | `Ogre::Vector3` | `axisH` |
| 0x3E0 | `Ogre::Vector3` | `axisF` |
| 0x3EC | `bool` | `_isBroken` |

## Faction : public Ogre::GeneralAllocatedObject
*Faction.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `ogre_unordered_set<GameData*>::type` | `toReplace` |
| 0x0 | `float` | `fleeRatio_squadSize` |
| 0x0 | `lektor<Faction*>` | `participants` |
| 0x4 | `float` | `fleeRatio_relativeEnemy` |
| 0x8 | `bool` | `_antiSlavery` |
| 0xC | `Faction::CharacteristicsData` | `characteristicsData` |
| 0x18 | `lektor<std::string >` | `ranks` |
| 0x18 | `boost::shared_mutex` | `addListMuto` |
| 0x30 | `bool` | `allowSlavesWeapons` |
| 0x34 | `CharacterTypeEnum` | `fundamentalNPCType` |
| 0x38 | `Faction*` | `myLawEnforcementFaction` |
| 0x38 | `lektor<Platoon*>` | `toAddList` |
| 0x40 | `FitnessSelector<GameData*>` | `replaceWith` |
| 0x40 | `bool` | `isALawEnforcementFaction` |
| 0x48 | `FactionLeader` | `factionLeader` |
| 0x70 | `FactionUniqueSquadManager*` | `diplomatMgr` |
| 0x78 | `FactionRelations*` | `relations` |
| 0x80 | `Ownerships*` | `factionOwnerships` |
| 0x88 | `FactionWarMgr*` | `warMgr` |
| 0x90 | `TradeCulture` | `tradeCulture` |
| 0x148 | `FitnessSelector<GameData*>` | `raceSelector` |
| 0x1A8 | `std::string` | `name` |
| 0x1D0 | `bool` | `notARealFaction` |
| 0x1D4 | `float` | `roadPreference` |
| 0x1D8 | `lektor<Platoon*>` | `platoonKillList` |
| 0x1F0 | `lektor<Platoon*>` | `platoonRemoveList` |
| 0x208 | `lektor<Platoon*>` | `activePlatoons` |
| 0x220 | `lektor<Platoon*>` | `unloadedPlatoons` |
| 0x238 | `int` | `periodicUpdateCounter_active` |
| 0x23C | `int` | `periodicUpdateCounter_unloaded` |
| 0x240 | `GameData*` | `data` |
| 0x248 | `AIPlayer*` | `isAI` |
| 0x250 | `PlayerInterface*` | `isPlayer` |
| 0x258 | `int` | `spawnTimeStamp` |
| 0x25C | `int` | `diplomatTimeStamp` |
| 0x260 | `int` | `platoonIDs` |
| 0x264 | `float` | `p_TIME` |
| 0x268 | `int` | `platoonPeriodicUpdateIndex` |
| 0x270 | `lektor<Faction::BuildingSwaps>` | `buildingSwaps` |

## FactionLeader
*FactionLeader.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `Faction*` | `faction` |
| 0x8 | `lektor<GameData*>` | `biomeTerritory` |
| 0x20 | `Faction*` | `worstEnemy` |

## FactionRelations
*FactionRelations.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `bool` | `alliance` |
| 0x1 | `bool` | `peaceTreaty` |
| 0x2 | `bool` | `war` |
| 0x3 | `bool` | `coexists` |
| 0x4 | `float` | `relation` |
| 0x8 | `Faction*` | `me` |
| 0x8 | `float` | `trustPositives` |
| 0xC | `float` | `trustNegatives` |
| 0x10 | `int` | `playerRank` |
| 0x10 | `float` | `percievedStrength` |
| 0x14 | `float` | `globalReputationTrust` |
| 0x18 | `std::map<std::string, int, std::less<std::string >, Ogre::ST` | `stateVariables` |
| 0x18 | `float` | `globalReputationForBadassery` |
| 0x20 | `ogre_unordered_map<Faction*, RelationData>::type` | `_factionRelations` |
| 0x60 | `float` | `defaultFactionRelation` |

## FactionWarMgr : public Ogre::GeneralAllocatedObject
*FactionWarMgr.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `Faction*` | `me` |
| 0x0 | `TimeOfDay` | `timeToStart` |
| 0x8 | `int` | `lastID` |
| 0x8 | `CampaignData*` | `data` |
| 0x10 | `lektor<TownBase*>` | `myTowns` |
| 0x10 | `hand` | `target` |
| 0x28 | `std::map<Platoon*, CampaignInstance*, std::less<Platoon*>, O` | `forces` |
| 0x30 | `hand` | `homeBase` |
| 0x50 | `lektor<hand>` | `hiredForces` |
| 0x50 | `Faction*` | `enemy` |
| 0x58 | `int` | `numAttempts` |
| 0x68 | `lektor<CampaignInstance*>` | `activeCampaigns` |
| 0x80 | `lektor<AreaBiomeGroup*>` | `biomeTerritories` |
| 0x98 | `lektor<AreaBiomeGroup*>` | `biomeNoGoZones` |
| 0xB0 | `TimeOfDay` | `nextUpdateTime` |
| 0xB8 | `lektor<FactionWarMgr::CampaignRequest*>` | `campaignRequests` |
| 0xD0 | `lektor<CampaignData*>` | `possibleCampaigns` |

## FactionsScreen
*FactionsScreen.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `MyGUI::Widget*` | `mainWidget` |
| 0x8 | `Faction*` | `selectedFaction` |
| 0x10 | `std::map<Faction*, FactionsScreen::FactionRelationsLine*, st` | `lines` |
| 0x38 | `MyGUI::ScrollView*` | `scrollList` |
| 0x40 | `int` | `scrollListItemTop` |
| 0x44 | `int` | `scrollListItemWidth` |
| 0x48 | `MyGUI::EditBox*` | `nameText` |
| 0x50 | `DatapanelGUI*` | `infoPanel` |
| 0x58 | `float` | `updateTimer` |
| 0xA0 | `Faction*` | `faction` |
| 0xA8 | `float` | `value` |
| 0xB0 | `MyGUI::TextBox*` | `valueText` |
| 0xB8 | `MyGUI::Widget*` | `leftBar` |
| 0xC0 | `MyGUI::Widget*` | `rightBar` |

## FactoryCallbackInterface
*PlayerInterface.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `bool` | `rightMouseActivated` |
| 0x0 | `Ogre::Vector2` | `startPos` |
| 0x0 | `bool` | `healAllies` |
| 0x1 | `bool` | `helpAllies` |
| 0x2 | `bool` | `rescueAllies` |
| 0x3 | `bool` | `stayInBase` |
| 0x4 | `bool` | `feedAnimals` |
| 0x5 | `bool` | `shareFood` |
| 0x6 | `bool` | `autoSleep` |
| 0x7 | `bool` | `autoDitchItems` |
| 0x8 | `lektor<int>` | `orders` |
| 0x8 | `Ogre::PlaneBoundedVolume` | `volume` |
| 0x8 | `std::string` | `factionName` |
| 0x8 | `bool` | `autoSit` |
| 0x9 | `bool` | `ejectEnemies` |
| 0xA | `bool` | `shootFirst` |
| 0x20 | `std::string` | `contextMenuName` |
| 0x30 | `MyGUI::Widget*` | `widget` |
| 0x30 | `CameraClass*` | `camera` |
| 0x38 | `bool` | `active` |
| 0x38 | `Research*` | `technology` |
| 0x40 | `bool` | `selectedObjectsChangedThisFrame` |
| 0x48 | `ContextMenuGUI*` | `menuGUI` |
| 0x48 | `ContextMenu` | `contextMenu` |
| 0x50 | `ContextMenuGUI*` | `menuGUI2` |
| 0x58 | `bool` | `delayedDestroyFlag` |
| 0xA8 | `SelectionBox` | `selectBox` |
| 0xE8 | `MoveMarker*` | `moveMarker` |
| 0xF0 | `hand` | `selectedCharacter` |
| 0x110 | `PlayerInterface::AIOptions` | `aiOptions` |
| 0x120 | `ogre_unordered_map<ZoneMap*, unsigned char>::type` | `zonesVisibilities` |
| 0x160 | `ogre_unordered_set<TownBase*>::type` | `townsActive` |
| 0x1A0 | `ogre_unordered_set<hand>::type` | `interiorsVisible` |
| 0x1E0 | `unsigned int` | `interiorsVisibleHash` |
| 0x1E4 | `int` | `currentFloor` |
| 0x1E8 | `TaskType` | `currentMouseTask` |
| 0x1EC | `itemType` | `mouseTaskTypeRestriction` |
| 0x1F0 | `bool` | `mouseRightTargetSet` |
| 0x1F8 | `RootObject*` | `mouseRightTarget` |
| 0x200 | `float` | `rmouseTimer` |
| 0x208 | `ogre_unordered_set<hand>::type` | `selectedCharacters` |
| 0x248 | `hand` | `selectedObject` |
| 0x268 | `bool` | `onlyAnimalsSelected` |
| 0x26C | `int` | `selectedLoadedLeft` |
| 0x270 | `hand` | `trackedCharacterHandle` |
| 0x290 | `int` | `trackedCharacterFloor` |
| 0x298 | `LevelEditor*` | `levelEditor` |
| 0x2A0 | `Faction*` | `participant` |
| 0x2A8 | `Platoon*` | `currentPlatoon` |
| 0x2B0 | `lektor<Character*>` | `playerCharacters` |
| 0x2C8 | `hand` | `deadPlayerSquad` |
| 0x2E8 | `PlacementObject*` | `placementObject` |
| 0x2F0 | `bool` | `characterEditorMode` |
| 0x2F1 | `bool` | `mLeftUp` |
| 0x2F2 | `bool` | `mLeftDown` |
| 0x2F3 | `bool` | `mRightUp` |
| 0x2F4 | `bool` | `mRightDown` |

## FarmBuilding : public ProductionBuilding
*FarmBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `GameData*` | `data` |
| 0x0 | `lektor<FarmBuilding::PlantSource*>` | `plantSource` |
| 0x0 | `float` | `scale` |
| 0x0 | `float` | `age` |
| 0x4 | `float` | `offset` |
| 0x4 | `Ogre::Vector3` | `position` |
| 0x8 | `Ogre::SharedPtr<Ogre::Mesh>` | `mesh` |
| 0x8 | `float` | `rv` |
| 0x10 | `FarmBuilding::PlantSource*` | `data` |
| 0x10 | `lektor<FarmBuilding::SubPlant>` | `parts` |
| 0x18 | `float` | `scaleStart` |
| 0x18 | `lektor<int>` | `plantGroups` |
| 0x18 | `int` | `index` |
| 0x1C | `float` | `scaleEnd` |
| 0x20 | `float` | `scaleVariance` |
| 0x24 | `float` | `offsetStart` |
| 0x28 | `float` | `offsetEnd` |
| 0x2C | `float` | `delay` |
| 0x30 | `float` | `delayScale` |
| 0x30 | `Ogre::SharedPtr<Ogre::Mesh>` | `geometry` |
| 0x34 | `bool` | `isStatic` |
| 0x38 | `int` | `count` |
| 0x3C | `int` | `group` |
| 0x40 | `float` | `height` |
| 0x44 | `int` | `size` |
| 0x48 | `int` | `meshesLoaded` |
| 0x50 | `lektor<FarmBuilding*>` | `farms` |
| 0x490 | `ogre_unordered_map<CropType, float>::type` | `cropMultipliers` |
| 0x4D0 | `Ogre::SharedPtr<Ogre::Material>` | `material` |
| 0x4E0 | `Ogre::Entity*` | `plantEntity` |
| 0x4E8 | `lektor<FarmBuilding::Plant>` | `plants` |
| 0x500 | `StaticBoxEntity*` | `clickHull` |
| 0x508 | `FarmBuilding::FarmBatch*` | `batch` |
| 0x510 | `float` | `lastUpdated` |
| 0x514 | `float` | `eatingTime` |
| 0x518 | `float` | `grown` |
| 0x51C | `float` | `died` |
| 0x520 | `float` | `cleared` |
| 0x524 | `float` | `growStart` |
| 0x528 | `int` | `harvested` |
| 0x52C | `float` | `itemsPerPlant` |
| 0x530 | `float` | `clearRate` |
| 0x534 | `float` | `consumptionRate` |
| 0x538 | `float` | `harvestRate` |
| 0x53C | `float` | `growthTime` |
| 0x540 | `float` | `harvestTime` |
| 0x544 | `float` | `deathTime` |
| 0x548 | `float` | `droughtTime` |
| 0x54C | `float` | `deathThreshold` |
| 0x550 | `float` | `droughtMultiplier` |
| 0x554 | `float` | `fertilityMultiplier` |
| 0x558 | `bool` | `isHydroponic` |

## FitnessSelector
*FitnessSelector.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `std::map<float, T, std::less<float>, Ogre::STLAllocator<std:` | `list` |
| 0x28 | `std::map<T, float, std::less<T>, Ogre::STLAllocator<std::pai` | `itemsScores` |
| 0x50 | `float` | `totalScore` |
| 0x54 | `float` | `highestScore` |
| 0x58 | `T` | `highestItem` |

## FogEditor : public wraps::BaseLayout
*FogEditor.h*

| Offset | Type | Field |
|--------|------|-------|
| 0xA0 | `MyGUI::Window*` | `window` |
| 0xA8 | `MyGUI::ListBox*` | `fogList` |
| 0xB0 | `MyGUI::ComboBox*` | `typeList` |
| 0xB8 | `DatapanelGUI*` | `panel` |
| 0xC0 | `FogVolume*` | `selectedFog` |
| 0xC8 | `int` | `selectedSide` |
| 0xCC | `Ogre::Vector3` | `colour` |
| 0xD8 | `float` | `distance` |
| 0xDC | `float` | `radius` |
| 0xE0 | `float` | `edge` |
| 0xE8 | `Ogre::ManualObject*` | `editCage` |
| 0xF0 | `Ogre::SceneNode*` | `editNode` |
| 0xF8 | `Ogre::Vector3` | `editPos` |
| 0x104 | `Ogre::Quaternion` | `editRot` |

## FoliageSystem : public Ogre::GeneralAllocatedObject
*FoliageSystem.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `GameData*` | `data` |
| 0x0 | `Ogre::Vector3` | `position` |
| 0x0 | `bool` | `reloaded` |
| 0x1 | `bool` | `generateOverlay` |
| 0x2 | `bool` | `firstTimeLoad` |
| 0x4 | `unsigned int` | `collisionHash` |
| 0x8 | `float` | `maxSlope` |
| 0x8 | `lektor<Forests::PagedGeometry*>` | `pageLayers` |
| 0xC | `float` | `minSlope` |
| 0xC | `Ogre::Degree` | `rotation` |
| 0x10 | `float` | `chance` |
| 0x10 | `float` | `scale` |
| 0x14 | `float` | `minAltitude` |
| 0x18 | `float` | `maxAltitude` |
| 0x18 | `Forests::TreeLoader3D*` | `target` |
| 0x1C | `bool` | `slopeAlign` |
| 0x1D | `bool` | `floating` |
| 0x1E | `bool` | `uniformScale` |
| 0x1F | `bool` | `accurateTrace` |
| 0x20 | `bool` | `upright` |
| 0x20 | `Building*` | `building` |
| 0x20 | `lektor<Forests::TreeLoader3D*>` | `treeListsWithCarvers` |
| 0x24 | `Ogre::Vector4` | `scales` |
| 0x28 | `Ogre::Matrix4` | `transform` |
| 0x34 | `float` | `minV` |
| 0x38 | `float` | `maxV` |
| 0x38 | `ogre_unordered_set<FoliageSystem::EntData*>::type` | `loadedEnts` |
| 0x3C | `bool` | `clustered` |
| 0x3D | `bool` | `limitToGrassAreas` |
| 0x3E | `bool` | `nonBatched` |
| 0x40 | `float` | `carveRadius` |
| 0x44 | `float` | `grassSpot` |
| 0x48 | `float` | `roadRadius` |
| 0x4C | `float` | `clusterMin` |
| 0x50 | `float` | `clusterMax` |
| 0x54 | `float` | `clusterRadiusMin` |
| 0x58 | `float` | `clusterRadiusMax` |
| 0x5C | `float` | `viewDistance` |
| 0x60 | `int` | `seedOffset` |
| 0x64 | `bool` | `biomeSeparation` |
| 0x68 | `float` | `childClusterRadius` |
| 0x70 | `std::string` | `xmlFilename` |
| 0x78 | `bool` | `loadComplete` |
| 0x80 | `ZoneMap*` | `zoneMap` |
| 0x88 | `RealWorldEditableImage*` | `coverageMap` |
| 0x90 | `ogre_unordered_map<GameData*, int>::type` | `usedEntsCount` |
| 0x98 | `Ogre::Entity*` | `entity1` |
| 0xA0 | `Ogre::Entity*` | `entity2` |
| 0xA8 | `ogre_unordered_map<GameData*, Ogre::Entity*>::type` | `extraEntities` |
| 0xD0 | `lektor<SimplePhysXEntity*>` | `collisionList` |
| 0xE8 | `bool` | `entity1Loaded` |
| 0xE8 | `lektor<SoundEmitter*>` | `soundEmitters` |
| 0xE9 | `bool` | `entity2Loaded` |
| 0xF0 | `lektor<FoliageSystem::EntData*>` | `subEnts` |
| 0x100 | `lektor<SoundEmitter*>` | `soundUpdate` |
| 0x108 | `Ogre::Vector3` | `position` |
| 0x114 | `itemType` | `type` |
| 0x118 | `unsigned int` | `referenceCount` |

## ForgottenGUI : public Ogre::GeneralAllocatedObject
*ForgottenGUI.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `bool` | `hasMouse` |
| 0x10 | `MainBarGUI*` | `mainbar` |
| 0x18 | `ToolTip*` | `tooltip` |
| 0x20 | `DialogueWindow*` | `dialogue` |
| 0x28 | `TutorialGUI*` | `tutorial` |
| 0x30 | `TutorialpediaGUI*` | `tutorialpedia` |
| 0x38 | `CursorType` | `currentCursor` |
| 0x3C | `Ogre::Vector2` | `Scale` |
| 0x48 | `MyGUI::Gui*` | `manager` |
| 0x50 | `MyGUI::OgrePlatform*` | `guiPlatform` |
| 0x58 | `TradeWindowType` | `_showTradeWindowMsg` |
| 0x5C | `bool` | `_closeTradeWindowMsg` |
| 0x60 | `hand` | `tradeA` |
| 0x80 | `hand` | `tradeB` |
| 0xA0 | `ogre_unordered_map<hand, InventoryGUI*>::type` | `inventoryWindowsOpen` |
| 0xE0 | `hand` | `inventoryWindowBuilding` |
| 0x100 | `hand` | `inventoryWindowCharacter` |
| 0x120 | `hand` | `inventoryWindowTrader` |
| 0x140 | `hand` | `inventoryWindowNPC` |
| 0x160 | `ogre_unordered_set<hand>::type` | `inventoryWindowsPermanent` |
| 0x1A0 | `Ogre::vector<InventoryGUI*>::type` | `inventoryWindowsKillList` |
| 0x1C0 | `CharacterEditWindow*` | `characterEditor` |
| 0x1C8 | `Ogre::vector<CharacterStatsWindow*>::type` | `characterStatsWindows` |
| 0x1E8 | `Ogre::vector<CharacterStatsWindow*>::type` | `characterStatsWindowsKillList` |
| 0x208 | `lektor<GUIWindow*>` | `guiWindows` |
| 0x220 | `lektor<DatapanelGUI*>` | `guiDatapanels` |
| 0x238 | `boost::shared_mutex` | `guiScreenLabelsMutex` |
| 0x258 | `lektor<ScreenLabelInterface*>` | `guiScreenLabels` |
| 0x270 | `lektor<ScreenLabelInterface*>` | `guiScreenLabelsToAdd` |
| 0x288 | `lektor<ScreenLabelInterface*>` | `guiScreenLabelsToRemove` |
| 0x2A0 | `hand` | `selectedObject` |
| 0x2C0 | `hand` | `selectedPlayerCharacter` |
| 0x2E0 | `DatapanelGUI*` | `cursorPanel` |
| 0x2E8 | `bool` | `cursorAction` |
| 0x2F0 | `hand` | `cursorActionPlayer` |
| 0x310 | `hand` | `cursorActionTarget` |
| 0x330 | `bool` | `visible` |
| 0x331 | `bool` | `created` |

## FurnaceInventoryLayout : public BuildInventoryLayout
*FurnaceBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x490 | `bool` | `active` |

## GUIWindow : public Ogre::GeneralAllocatedObject
*GUIWindow.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `MyGUI::Widget*` | `win` |
| 0x10 | `hand` | `selectedObject` |

## GameDataContainer : public Ogre::GeneralAllocatedObject
*GameDataManager.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `int` | `currentID` |
| 0x10 | `boost::unordered::unordered_map<int, boost::unordered::unord` | `gamedataCatName` |
| 0x50 | `ogre_unordered_map<int, GameData*>::type` | `gamedataID` |
| 0x90 | `boost::unordered::unordered_map<int, boost::unordered::unord` | `gamedataCatSID` |
| 0xD0 | `boost::unordered::unordered_map<std::string, GameData*, boos` | `gamedataSID` |
| 0x110 | `ogre_unordered_set<GameData*>::type` | `mainList` |
| 0x150 | `std::string` | `name` |
| 0x178 | `bool` | `isBaseDatafile` |
| 0x179 | `bool` | `readOnly` |

## GameDataEditorWindow : public Ogre::GeneralAllocatedObject
*GameDataEditorWindow.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `MyGUI::EditBox*` | `edit` |
| 0x8 | `DatapanelGUI*` | `win` |
| 0x8 | `MyGUI::TextBox*` | `label` |
| 0x10 | `std::string` | `name` |
| 0x10 | `GameData*` | `data` |

## GameDataGroup
*CraftingBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `GameData*` | `g1` |
| 0x8 | `GameData*` | `g2` |
| 0x440 | `MyGUI::Button*` | `queueBtn` |
| 0x448 | `MyGUI::TextBox*` | `craftingName` |
| 0x450 | `itemType` | `outputType` |
| 0x490 | `int` | `maxCraftLevel` |
| 0x498 | `std::deque<CraftingItem, std::allocator<CraftingItem> >` | `crafting` |
| 0x4C8 | `itemType` | `specialCraftItemType` |
| 0x4CC | `bool` | `repeat` |
| 0x4D0 | `hand` | `whosCrafting` |
| 0x4F0 | `bool` | `itemCrafted` |
| 0x4F1 | `bool` | `failiureNotified` |
| 0x4F8 | `GameData*` | `biggestCraftableItem` |
| 0x500 | `Item*` | `outItem` |
| 0x508 | `lektor<Item*>` | `inItems` |
| 0x520 | `ogre_unordered_map<GameData*, float>::type` | `partialItems` |

## GameDataHeader
*GameData.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `std::string` | `name` |
| 0x0 | `bool` | `visible` |
| 0x0 | `Ogre::Vector3` | `pos` |
| 0x0 | `TripleInt` | `values` |
| 0x8 | `int` | `validity` |
| 0x8 | `std::string` | `category` |
| 0xC | `Ogre::Quaternion` | `rot` |
| 0x10 | `GameDataContainer*` | `sourceContainer` |
| 0x10 | `std::string` | `sid` |
| 0x18 | `bool` | `isStandalone` |
| 0x1C | `int` | `id` |
| 0x20 | `bool` | `readOnly` |
| 0x20 | `std::string` | `refID` |
| 0x28 | `std::string` | `author` |
| 0x28 | `std::string` | `name` |
| 0x30 | `std::string` | `description` |
| 0x38 | `GameData*` | `ptr` |
| 0x48 | `short` | `created` |
| 0x4A | `short` | `modified` |
| 0x50 | `int` | `version` |
| 0x50 | `itemType` | `type` |
| 0x50 | `lektor<std::string >` | `stateIDs` |
| 0x58 | `std::string` | `description` |
| 0x58 | `std::string` | `fileTypes` |
| 0x58 | `std::string` | `stringID` |
| 0x80 | `lektor<std::string >` | `dependencies` |
| 0x80 | `itemType` | `objectType` |
| 0x80 | `bool` | `isFromActiveFile` |
| 0x84 | `int` | `maxSize` |
| 0x88 | `int` | `maxValue` |
| 0x88 | `std::map<std::string, GameData::ObjectInstance, std::less<st` | `instances` |
| 0x8C | `int` | `minValue` |
| 0x90 | `bool` | `isSlider` |
| 0x98 | `lektor<std::string >` | `references` |
| 0xB0 | `int` | `currentID` |
| 0xB8 | `boost::unordered::unordered_map<std::string, bool, boost::ha` | `activeValues` |
| 0xF8 | `boost::unordered::unordered_map<std::string, bool, boost::ha` | `bdata` |
| 0x138 | `boost::unordered::unordered_map<std::string, std::string, bo` | `sdata` |
| 0x178 | `boost::unordered::unordered_map<std::string, int, boost::has` | `idata` |
| 0x1B8 | `boost::unordered::unordered_map<std::string, float, boost::h` | `fdata` |
| 0x1F8 | `boost::unordered::unordered_map<std::string, std::string, bo` | `filesdata` |
| 0x238 | `boost::unordered::unordered_map<std::string, Ogre::Vector3, ` | `vecdata` |
| 0x278 | `boost::unordered::unordered_map<std::string, Ogre::Quaternio` | `quatdata` |
| 0x2B8 | `boost::unordered::unordered_map<std::string, Ogre::vector<Ga` | `objectReferences` |
| 0x2F8 | `unsigned short` | `createdIndex` |

## GameSaveState
*GameSaveState.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `GameData*` | `baseData` |
| 0x8 | `GameDataContainer*` | `dataSource` |
| 0x10 | `bool` | `firstTime` |
| 0x18 | `GameData::ObjectInstance*` | `instance` |
| 0x20 | `Ogre::Vector3` | `pos` |
| 0x2C | `Ogre::Quaternion` | `rot` |
| 0x40 | `std::string` | `instanceID` |
| 0x68 | `ogre_unordered_map<itemType, GameData*>::type` | `states` |

## GameplayOptions
*GameplayOptions.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `float` | `deathFrequency` |
| 0x0 | `float` | `deathFrequency` |
| 0x0 | `std::string` | `version` |
| 0x4 | `bool` | `easyProspecting` |
| 0x4 | `bool` | `easyProspecting` |
| 0x8 | `float` | `globalDamageMultiplier` |
| 0x8 | `float` | `globalDamageMultiplier` |
| 0xC | `float` | `buildingSpeed` |
| 0xC | `float` | `buildingSpeed` |
| 0x10 | `float` | `numNestsMult` |
| 0x10 | `float` | `numNestsMult` |
| 0x14 | `float` | `researchSpeed` |
| 0x14 | `float` | `researchSpeed` |
| 0x18 | `float` | `productionSpeed` |
| 0x18 | `float` | `productionSpeed` |
| 0x1C | `float` | `hungerTime` |
| 0x1C | `float` | `hungerTime` |
| 0x20 | `bool` | `banditsLootPlayer` |
| 0x20 | `bool` | `banditsLootPlayer` |
| 0x21 | `bool` | `animalsEat` |
| 0x21 | `bool` | `animalsEat` |
| 0x22 | `bool` | `difficultHealing` |
| 0x22 | `bool` | `difficultHealing` |
| 0x28 | `std::string` | `name` |
| 0x50 | `std::string` | `area` |
| 0x78 | `__int64` | `time` |
| 0x80 | `std::string` | `faction` |
| 0xA8 | `int` | `money` |
| 0xAC | `int` | `size` |
| 0xB0 | `int` | `days` |
| 0xB8 | `std::string` | `location` |
| 0xE0 | `GameplayOptions` | `advanced` |

## Gear : public Item
*Gear.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x1E8 | `Faction*` | `isUniform` |
| 0x1F0 | `int` | `value` |
| 0x1F8 | `std::string` | `crafter` |
| 0x220 | `float` | `level` |
| 0x224 | `int` | `level_0_100` |
| 0x228 | `float` | `bleedDamage` |
| 0x228 | `float` | `cutResistance` |
| 0x22C | `int` | `modAttack` |
| 0x22C | `float` | `bluntResistance` |
| 0x230 | `float` | `combatWeight` |
| 0x230 | `float` | `pierceResistance` |
| 0x234 | `WeaponCategory` | `category` |
| 0x234 | `float` | `minCutResistance` |
| 0x238 | `WeaponCategory` | `category_animationOverride` |
| 0x238 | `float` | `cutToStun` |
| 0x23C | `ArmourType` | `materialType` |
| 0x240 | `float` | `cutDamage` |
| 0x240 | `GunClass*` | `gunClass` |
| 0x240 | `ArmourClass` | `armourClassEnum` |
| 0x244 | `float` | `bluntDamage` |
| 0x244 | `CharacterTypeEnum` | `stigma` |
| 0x248 | `float` | `minCutDamage` |
| 0x248 | `float` | `athleticsMult` |
| 0x24C | `int` | `modDefence` |
| 0x24C | `int` | `combatSkillBonusAttk` |
| 0x250 | `int` | `modIndoors` |
| 0x250 | `int` | `combatSkillBonusDef` |
| 0x254 | `int` | `perceptionBonus` |
| 0x258 | `float` | `combatSpeedMult` |
| 0x25C | `float` | `stealthMult` |
| 0x260 | `float` | `assassinMult` |
| 0x264 | `float` | `dexterityMult` |
| 0x268 | `float` | `damageMult` |
| 0x26C | `float` | `dodgeMult` |
| 0x270 | `int` | `unarmedBonus` |
| 0x274 | `float` | `fistInjuryMult` |
| 0x278 | `float` | `weatherProtectionAmount` |
| 0x27C | `float` | `rangedSkillMult` |
| 0x280 | `std::set<WeatherAffecting, std::less<WeatherAffecting>, Ogre` | `weatherProtections` |
| 0x2A8 | `ogre_unordered_map<GameData*, float>::type` | `bodypartCoverage` |
| 0x2E8 | `float` | `craftTime` |
| 0x2F0 | `DoorLock*` | `lock` |

## GenericInventoryLayout : public InventoryLayout
*UseableStuff.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x360 | `hand` | `shopOwner` |
| 0x380 | `hand` | `callbackOwner` |
| 0x3A0 | `bool` | `hasProgressBarWhenUsed` |
| 0x3A4 | `float` | `progressBarLevel` |
| 0x3A8 | `bool` | `occupantSelection` |
| 0x3A9 | `bool` | `needsOperating` |
| 0x3AC | `int` | `numOperatorsMax` |
| 0x3B0 | `float` | `hungerRate` |
| 0x3B4 | `bool` | `_recievesBatteryPower` |
| 0x3B5 | `bool` | `powerOn` |
| 0x3B6 | `bool` | `_isBroken` |
| 0x3B8 | `MyGUI::Widget*` | `arrangeButton` |
| 0x3B8 | `float` | `batteryOutputStat` |
| 0x3BC | `float` | `_powerOutputMax` |
| 0x3C0 | `float` | `currentPower` |
| 0x3C4 | `float` | `powerTimeStored` |
| 0x3C8 | `float` | `_powerTimeStoreMax` |
| 0x3D0 | `std::set<hand, std::less<hand>, Ogre::STLAllocator<hand, Ogr` | `currentOperators` |
| 0x3F8 | `StatsEnumerated` | `usesStat` |
| 0x400 | `GameData*` | `functionalityData` |
| 0x408 | `GameData*` | `animation` |
| 0x410 | `GameData*` | `animationKO` |
| 0x418 | `GameData*` | `animationDazed` |
| 0x420 | `float` | `maxUseRange` |
| 0x430 | `Inventory*` | `inventory` |
| 0x438 | `DoorLock*` | `doorLock` |

## GlobalConstants
*GlobalConstants.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `float` | `EXTRA_BLEED_FROM_BODYPARTS_MULTIPLIER` |
| 0x4 | `float` | `BLEED_RATE_MULTIPLIER` |
| 0x8 | `float` | `INITIAL_BLEED_LOSS_MULTIPLIER` |
| 0xC | `float` | `BLEED_CLOT_RATE` |
| 0x10 | `float` | `BLUNT_DAMAGE_1` |
| 0x14 | `float` | `BLUNT_DAMAGE_99` |
| 0x18 | `float` | `CUT_DAMAGE_1` |
| 0x1C | `float` | `CUT_DAMAGE_99` |
| 0x20 | `float` | `BOW_DAMAGE_0` |
| 0x24 | `float` | `BOW_DAMAGE_99` |
| 0x28 | `float` | `PIERCE_MULTIPLIER` |
| 0x2C | `float` | `MIN_STUMBLE_DAMAGE_MAX` |
| 0x30 | `float` | `DAMAGE_RESISTANCE_MIN` |
| 0x34 | `float` | `DAMAGE_RESISTANCE_MAX` |
| 0x38 | `float` | `STUN_RECOVERY_RATE` |
| 0x3C | `float` | `BLOOD_RECOVERY_RATE` |
| 0x40 | `float` | `ATTACK_CHANCE_SKILL_DIFFERENCE_FACTOR` |
| 0x44 | `float` | `BASE_BLOCK_CHANCE` |
| 0x48 | `float` | `BLOCK_CHANCE_REDUCTION` |
| 0x4C | `float` | `BLOCK_CHANCE_INCREASE` |
| 0x50 | `float` | `DEGENERATION_MULT_1` |
| 0x54 | `float` | `DEGENERATION_MULT_99` |
| 0x58 | `float` | `MEDIC_SPEED_MULT` |
| 0x5C | `float` | `KNOCKOUT_MULT_1` |
| 0x60 | `float` | `KNOCKOUT_MULT_99` |
| 0x64 | `float` | `KNOCKOUT_BASE_TIME` |
| 0x68 | `float` | `BODYPART_DEGENERATE_RATE_MULT` |
| 0x6C | `float` | `BODYPART_HEAL_RATE_MULT` |
| 0x70 | `float` | `BODYPART_HEAL_RATE_MULT_RESTING` |
| 0x74 | `float` | `XP_MEDIC_1` |
| 0x78 | `float` | `XP_MEDIC_99` |
| 0x7C | `float` | `MEDKIT_DRAIN_1` |
| 0x80 | `float` | `MEDKIT_DRAIN_99` |
| 0x84 | `float` | `ROBOT_WEAR_RATE` |
| 0x88 | `float` | `ROBOT_FIRST_AID_SPEED` |
| 0x8C | `float` | `STARVATION_TIME_HRS` |
| 0x90 | `float` | `FED_RECOVERY_RATE_MULT` |
| 0x94 | `float` | `BED_HUNGER_RATE` |
| 0x98 | `float` | `ENCUMBRANCE_HUNGER_RATE` |
| 0x9C | `float` | `FOOD_QUALITY_MULT` |
| 0xA0 | `float` | `FOOD_PRICE_MULT` |
| 0xA4 | `float` | `SKILL_DIFFERENCE_XP_RATIO_MULT_BONUS` |
| 0xA8 | `float` | `SKILL_DIFFERENCE_XP_RATIO_MULT_PENALTY` |
| 0xAC | `float` | `XP_HIT_THEM` |
| 0xB0 | `float` | `XP_HIT_ME` |
| 0xB4 | `float` | `XP_BLOCKED_THEM` |
| 0xB8 | `float` | `XP_BLOCKED_ME` |
| 0xBC | `float` | `XP_FIRSTAID` |
| 0xC0 | `float` | `XP_FITNESS` |
| 0xC4 | `float` | `XP_TOUGHNESS` |
| 0xC8 | `float` | `PRICE_ROBOTICS` |
| 0xCC | `float` | `PRICE_CROSSBOWS` |
| 0xD0 | `float` | `PRICE_ARMOUR` |
| 0xD4 | `float` | `PRICE_SWORDS` |
| 0xD8 | `float` | `PRICE_TRADE` |
| 0xDC | `float` | `PRICE_GLOBAL_MULT` |
| 0xE0 | `float` | `PRICE_CLOTHING` |
| 0xE4 | `float` | `TRADE_PROFIT_MARGINS` |
| 0xE8 | `float` | `PRICE_LOOT_GEAR` |
| 0xEC | `float` | `PRICE_LOOT_ITEMS` |
| 0xF0 | `float` | `PRICE_LOOT_PLAYER_CRAFTED_ARMOUR` |
| 0xF4 | `float` | `PRICE_LOOT_PLAYER_CRAFTED_WEAPONS` |
| 0xF8 | `float` | `BLUEPRINT_COST_MULT` |
| 0xFC | `float` | `UNIFORM_PRICE_MULT` |
| 0x100 | `float` | `BLUNT_PERMANENT_DAMAGE_RATIO` |
| 0x104 | `float` | `UNARMED_DAMAGE_MULT` |
| 0x108 | `int` | `MAX_NUM_ATTACK_SLOTS` |
| 0x10C | `float` | `MINIMUM_STRENGTH_XP_MULT` |
| 0x110 | `float` | `WEIGHT_STR_DIFF_1X` |
| 0x114 | `float` | `WEIGHT_STR_DIFF_MAX` |
| 0x118 | `float` | `WEAPON_INVENTORY_WEIGHT_MULT` |
| 0x11C | `float` | `STRENGTH_XP_RATE_FROM_WALKING` |
| 0x120 | `float` | `STRENGTH_XP_RATE` |
| 0x124 | `float` | `ATHLETICS_XP_RATE` |
| 0x128 | `float` | `ENCUMBRANCE_BASE` |
| 0x12C | `float` | `CARRY_WEIGHT_MULT` |
| 0x130 | `float` | `CARRY_PERSON_WEIGHT` |
| 0x134 | `float` | `MIN_MATS_FROM_DISMANTLE_01` |
| 0x138 | `double` | `EXPERIENCE_GAIN` |
| 0x140 | `double` | `EXPERIENCE_GAIN_1` |
| 0x148 | `double` | `EXPERIENCE_GAIN_99` |
| 0x150 | `float` | `RESEARCH_LEVEL_INCREASE` |
| 0x154 | `float` | `RESEARCH_RATE` |
| 0x158 | `float` | `LOCKPICK_CHANCE_MINIMUM` |
| 0x15C | `float` | `EXPERIENCE_CURVE` |
| 0x160 | `float` | `ANIMATION_BLEND_RATE` |
| 0x164 | `float` | `PRODUCTION_MULTIPLIER` |
| 0x168 | `float` | `BUILD_SPEED_MULTIPLIER` |
| 0x16C | `float` | `PRISON_TIME_MULT` |
| 0x170 | `float` | `TOUGHNESS_KO_POINT_MIN` |
| 0x174 | `float` | `TOUGHNESS_KO_POINT_MAX` |
| 0x178 | `int` | `MAX_SQUAD_SIZE` |
| 0x17C | `int` | `MAX_SQUADS` |
| 0x180 | `int` | `MAX_FACTION_SIZE` |
| 0x184 | `bool` | `attackDiplomats` |
| 0x188 | `GameData*` | `settings` |
| 0x190 | `float` | `APPEARANCE_RANDOM_DEVIATION` |
| 0x194 | `float` | `fogDistMax` |
| 0x198 | `float` | `fogDistMin` |

## HavokCharacter
*HavokCharacter.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `hkVector4f` | `mLeft` |
| 0x0 | `hkVector4f` | `a` |
| 0x0 | `hkVector4f` | `centre` |
| 0x0 | `hkArray<EdgePathNode, hkContainerHeapAllocator>` | `currentPath` |
| 0x10 | `hkVector4f` | `mRight` |
| 0x10 | `hkVector4f` | `b` |
| 0x10 | `float` | `radius` |
| 0x10 | `unsigned int` | `startingFace` |
| 0x14 | `bool` | `hasDoor` |
| 0x14 | `unsigned int` | `currentFace` |
| 0x18 | `hkArray<EdgeCache::Edge, hkContainerHeapAllocator>` | `edges` |
| 0x18 | `int` | `nextEdge` |
| 0x20 | `unsigned int` | `face` |
| 0x20 | `hkVector4f` | `position` |
| 0x24 | `unsigned int` | `edge` |
| 0x28 | `float` | `leftClearance` |
| 0x2C | `float` | `rightClearance` |
| 0x30 | `float` | `maxPoint` |
| 0x30 | `hkVector4f` | `velocity` |
| 0x40 | `hkVector4f` | `goal` |
| 0x50 | `hkVector4f` | `waypointDirection` |
| 0x60 | `hkVector4f` | `directionMoved` |
| 0x70 | `float` | `radius` |
| 0x74 | `float` | `waterModifier` |
| 0x78 | `float` | `acceleration` |
| 0x7C | `float` | `desiredSpeed` |
| 0x80 | `bool` | `positionChanged` |
| 0x84 | `float` | `timeOffPath` |
| 0x88 | `HavokCharacter::CharacterState` | `characterState` |
| 0x8C | `HavokCharacter::CharacterState` | `lastState` |
| 0x90 | `HavokCharacter::PathState` | `pathState` |
| 0x98 | `hand` | `handle` |
| 0xB8 | `hand` | `collided` |
| 0xE0 | `hkVector4f` | `boundaryPos` |
| 0xF0 | `hkArray<EdgePathNode, hkContainerHeapAllocator>` | `boundary` |
| 0x100 | `SensoryData*` | `sensoryData` |
| 0x110 | `EdgePathNode` | `cachedEdge` |
| 0x150 | `EdgeCache` | `edgeCache` |
| 0x180 | `char` | `resolveFlag` |

## InputHandler : public Ogre::GeneralAllocatedObject
*InputHandler.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `GameMode` | `gameMode` |
| 0x0 | `std::map<std::string, Command, std::less<std::string >, Ogre` | `commands` |
| 0x4 | `bool` | `isKey` |
| 0x8 | `int` | `code` |
| 0x10 | `bool*` | `boolean` |
| 0x18 | `std::string` | `name` |
| 0x28 | `std::map<int, Command*, std::less<int>, Ogre::STLAllocator<s` | `map` |
| 0x40 | `int` | `bound` |
| 0x44 | `Masks` | `masks` |
| 0x50 | `std::map<int, Command*, std::less<int>, Ogre::STLAllocator<s` | `editMap` |
| 0x78 | `std::set<Command*, std::less<Command*>, Ogre::STLAllocator<C` | `events` |
| 0xA0 | `OIS::Keyboard*` | `keyboard` |
| 0xA8 | `std::map<std::string, int, std::less<std::string >, Ogre::ST` | `keyNameMap` |
| 0xD0 | `bool` | `controlEnabled` |
| 0xD4 | `GameMode` | `gameMode` |
| 0xD8 | `bool` | `ctrl` |
| 0xD9 | `bool` | `shift` |
| 0xDA | `bool` | `alt` |
| 0xDB | `bool` | `up` |
| 0xDC | `bool` | `down` |
| 0xDD | `bool` | `left` |
| 0xDE | `bool` | `right` |
| 0xDF | `bool` | `space` |
| 0xE0 | `bool` | `pgup` |
| 0xE1 | `bool` | `pgdn` |
| 0xE2 | `bool` | `comma` |
| 0xE3 | `bool` | `period` |
| 0xE4 | `bool` | `f1` |
| 0xE5 | `bool` | `f2` |
| 0xE6 | `bool` | `escape` |
| 0xE7 | `bool` | `del` |
| 0xE8 | `bool` | `escape_msg` |
| 0xE9 | `bool` | `zoomin` |
| 0xEA | `bool` | `zoomout` |
| 0xEB | `bool` | `buildTiltInc` |
| 0xEC | `bool` | `buildTiltDec` |
| 0xED | `bool` | `rotate` |
| 0xEE | `bool` | `rotRight` |
| 0xEF | `bool` | `rotLeft` |
| 0xF0 | `bool` | `tiltDown` |
| 0xF1 | `bool` | `tiltUp` |
| 0xF2 | `bool` | `highlight` |
| 0xF3 | `bool` | `mLeft` |
| 0xF4 | `bool` | `mRight` |
| 0xF5 | `bool` | `lastMLeft` |
| 0xF6 | `bool` | `lastMRight` |
| 0xF7 | `bool` | `mLDown` |
| 0xF8 | `bool` | `mRDown` |
| 0xF9 | `bool` | `mLUp` |
| 0xFA | `bool` | `mRUp` |
| 0xFB | `bool` | `swapMouseButtons` |
| 0xFC | `Ogre::Vector2` | `mPos` |
| 0x104 | `Ogre::Vector2` | `mPosAbs` |
| 0x10C | `Ogre::Vector3` | `mSpeed` |
| 0x118 | `int` | `mWheel` |

## InstanceID
*InstanceID.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `public:
    std::string` | `uid` |
| 0x28 | `short` | `baseIndex` |
| 0x2A | `short` | `modIndex` |
| 0x2C | `bool` | `modified` |

## InventorySection
*Inventory.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `public:
        Item*` | `item` |
| 0x0 | `public:
        std::map<GameData*, bool, std::less<GameData` | `itemStates` |
| 0x8 | `unsigned short` | `x` |
| 0x8 | `std::string` | `name` |
| 0x8 | `Inventory::HasRoomCache*` | `hasRoomCache` |
| 0xA | `unsigned short` | `y` |
| 0xC | `unsigned short` | `w` |
| 0xE | `unsigned short` | `h` |
| 0x10 | `lektor<Item*>` | `_allItems` |
| 0x28 | `boost::unordered::unordered_map<std::string, InventorySectio` | `sections` |
| 0x30 | `int` | `width` |
| 0x34 | `int` | `height` |
| 0x38 | `bool` | `armourOnly` |
| 0x40 | `Ogre::vector<InventorySection::SectionItem>::type` | `items` |
| 0x60 | `Array2d<Item>` | `content` |
| 0x68 | `lektor<InventorySection*>` | `sectionsInSearchOrder` |
| 0x80 | `RootObject*` | `callbackObject` |
| 0x88 | `int` | `stackingBonusMin` |
| 0x88 | `RootObject*` | `owner` |
| 0x8C | `float` | `stackingBonusMult` |
| 0x90 | `lektor<GameData*>` | `veryLimitedSlot` |
| 0x90 | `float` | `totalWeight` |
| 0xA8 | `int` | `itemsLimit` |
| 0xAC | `float` | `weightMultiplier` |
| 0xB0 | `float` | `totalWeight` |
| 0xB4 | `bool` | `isAnEquippedItemSection` |
| 0xB8 | `AttachSlot` | `limitedSlot` |
| 0xBC | `bool` | `containerSlot` |
| 0xC0 | `RootObject*` | `callbackObject` |
| 0xC8 | `Inventory*` | `parentInventory` |
| 0xD0 | `bool` | `enabled` |

## InventorySectionGUI
*InventoryGUI.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `MyGUI::Widget*` | `widget` |
| 0x0 | `Enum` | `value` |
| 0x0 | `InventoryGUI*` | `inventory` |
| 0x0 | `int` | `mode` |
| 0x8 | `Ogre::vector<InventoryIcon*>::type` | `itemsIcons` |
| 0x8 | `bool` | `paymentRequired` |
| 0x8 | `std::string` | `sectionName` |
| 0x9 | `bool` | `canDropItems` |
| 0xA | `bool` | `isPlayer` |
| 0x10 | `hand` | `owner` |
| 0x30 | `MyGUI::types::TPoint<int>` | `point` |
| 0x30 | `InventoryLayout*` | `layoutMgr` |
| 0x38 | `InventoryGUI*` | `ownerInventory` |
| 0x40 | `InventoryGUI*` | `childInventory` |
| 0x48 | `bool` | `mouseFocus` |
| 0x50 | `RootObject*` | `callbackObject` |
| 0x58 | `bool` | `needItemsUpdate` |
| 0x59 | `bool` | `visible` |
| 0x60 | `std::map<std::string, InventorySectionGUI*, std::less<std::s` | `inventorySections` |
| 0xA0 | `Item*` | `item` |
| 0xA8 | `MyGUI::ImageBox*` | `image` |
| 0xA8 | `DatapanelGUI*` | `datapanel` |
| 0xB0 | `MyGUI::TextBox*` | `quantityText` |
| 0xB0 | `GameDataCopyStandalone` | `dataPanelInfos` |
| 0xB8 | `MyGUI::Widget*` | `chargesProgress` |
| 0x3B0 | `MyGUI::Window*` | `window` |

## Item : public InventoryItemBase
*Item.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `std::set<RaceData*, std::less<RaceData*>, Ogre::STLAllocator` | `racesExclude` |
| 0x8 | `ogre_unordered_map<GameData*, RaceLimiter::Limiter>::type` | `limits` |
| 0x30 | `std::set<RaceData*, std::less<RaceData*>, Ogre::STLAllocator` | `racesInclude` |
| 0xC0 | `GameData*` | `manufacturerData` |
| 0xC8 | `GameData*` | `materialData` |
| 0xD0 | `GameData*` | `coloriseData` |
| 0xD8 | `bool` | `isInInventory` |
| 0xDC | `iVector2` | `inventoryPos` |
| 0xE8 | `std::string` | `inventorySection` |
| 0x110 | `AttachSlot` | `slotType` |
| 0x114 | `float` | `originalFullChargeAmount` |
| 0x118 | `float` | `chargesLeft` |
| 0x11C | `float` | `quality` |
| 0x120 | `float` | `weight` |
| 0x124 | `ItemFunction` | `itemFunction` |
| 0x128 | `bool` | `isTradeItem` |
| 0x129 | `bool` | `isEquipped` |
| 0x12A | `bool` | `isUnique` |
| 0x12C | `int` | `quantity` |
| 0x130 | `int` | `itemWidth` |
| 0x134 | `int` | `itemHeight` |
| 0x138 | `bool` | `deathItem` |
| 0x13C | `itemType` | `objectType` |
| 0x140 | `hand` | `properOwner` |
| 0x160 | `hand` | `_whosInventoryWeAreIn` |
| 0x180 | `bool` | `_isResearchArtifact` |
| 0x188 | `BuildingItemGroup*` | `itemGroup` |
| 0x190 | `bool` | `physicalShouldExist` |
| 0x191 | `bool` | `existAsBareWeapon` |
| 0x198 | `hand` | `persistant` |
| 0x1B8 | `bool` | `visible` |
| 0x1C0 | `SimplePhysXEntity*` | `physical` |
| 0x1C8 | `bool` | `_isPhysical` |
| 0x1D0 | `Ogre::Entity*` | `physicalEntity` |
| 0x1D8 | `bool` | `creatingPhysical` |
| 0x1D9 | `bool` | `fixedPhysicalPosition` |
| 0x1DA | `bool` | `useDynamicPhysics` |
| 0x1E0 | `Ogre::Entity*` | `loadingEntity` |
| 0x230 | `RootObject*` | `callbackOwner` |
| 0x238 | `float` | `athleticsMult` |
| 0x23C | `float` | `weightMult` |
| 0x240 | `float` | `combatSpeedMult` |
| 0x244 | `int` | `combatSkillBonus` |
| 0x248 | `float` | `stealthMult` |
| 0x250 | `ogre_unordered_set<GameData*>::type` | `racesExclude` |
| 0x290 | `Inventory*` | `inventory` |

## LevelEditor : public Ogre::GeneralAllocatedObject
*LevelEditor.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `bool` | `levelEditModeOn` |
| 0x8 | `LevelEditorPanel*` | `panel` |
| 0x8 | `MyGUI::Window*` | `win` |
| 0x10 | `InteriorModeButtonWindow*` | `interiorModeWindow` |
| 0x10 | `MyGUI::ListBox*` | `list` |
| 0x18 | `int` | `selectedLocked` |
| 0x18 | `lektor<GameData*>` | `items` |
| 0x20 | `hand` | `selectedObject` |
| 0x30 | `LevelEditor*` | `levelEditor` |
| 0x38 | `unsigned __int64` | `lastItem` |
| 0x40 | `MapFeature*` | `selectedFeature` |
| 0x48 | `int` | `seedMode` |
| 0x4C | `int` | `roadMode` |
| 0x50 | `lektor<Road*>` | `selectedRoads` |
| 0x68 | `int` | `roadIndex` |
| 0x70 | `Ogre::SceneNode*` | `roadMarker` |
| 0x78 | `Ogre::ManualObject*` | `roadMakerMO` |
| 0x80 | `FoliageEraser*` | `foliageEraser` |
| 0x88 | `FogEditor*` | `fogEditor` |
| 0x90 | `LevelEditor::TownListWindow*` | `townListWindow` |
| 0x98 | `LevelEditor::FactionListWindow*` | `factionListWindow` |
| 0xA0 | `LevelEditor::SquadListWindow*` | `squadListWindow` |
| 0xA8 | `LevelEditor::NpcListWindow*` | `npcListWindow` |
| 0xB0 | `LevelEditor::NpcListWindow*` | `featureListWindow` |
| 0xB8 | `LevelEditor::ItemListWindow*` | `itemListWindow` |
| 0xC0 | `DatapanelGUI*` | `navmeshWindow` |
| 0xC8 | `MyGUI::Window*` | `editMapTitleWindow` |
| 0xD0 | `MyGUI::TextBox*` | `factionTxt` |
| 0xD8 | `MyGUI::TextBox*` | `altitudeTxt` |
| 0xE0 | `MyGUI::ComboBox*` | `activeModTxt` |

## LightBuilding : public UseableStuff
*LightBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x440 | `hand` | `mountedBuilding` |

## LimbsInventoryLayout : public InventoryLayout
*MedicalSystem.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `Character*` | `character` |
| 0x0 | `public:
        GameData*` | `data` |
| 0x8 | `RootObject*` | `inventory` |
| 0x8 | `MedicalSystem::HealthPartStatus::PartType` | `whatAmI` |
| 0x8 | `ogre_unordered_map<GameData*, MedicalSystem::HealthPartStatu` | `status` |
| 0x10 | `MedicalSystem*` | `medical` |
| 0x18 | `Character*` | `me` |
| 0x20 | `LeftRight` | `side` |
| 0x28 | `RobotLimbItem*` | `robotLimb` |
| 0x30 | `bool` | `selfHealing` |
| 0x31 | `bool` | `collapses` |
| 0x32 | `bool` | `fatal` |
| 0x34 | `float` | `KOMult` |
| 0x38 | `float` | `hitChance` |
| 0x3C | `float` | `hitChanceMult` |
| 0x40 | `float` | `flesh` |
| 0x44 | `float` | `fleshStun` |
| 0x48 | `float` | `bandaging` |
| 0x48 | `lektor<Armour*>` | `armourList` |
| 0x4C | `float` | `juryRigging` |
| 0x50 | `float` | `wearDamage` |
| 0x54 | `float` | `_maxHealth` |
| 0x58 | `float` | `age` |
| 0x5C | `float` | `HPMult` |
| 0x60 | `float` | `derivedFleshHealthPercent` |
| 0x60 | `float` | `hunger` |
| 0x64 | `float` | `fed` |
| 0x68 | `TimeOfDay` | `lastPeriodicUpdate` |
| 0x70 | `float` | `blood` |
| 0x74 | `float` | `extraBloodLossFromBodyparts` |
| 0x78 | `float` | `currentBleedRate` |
| 0x80 | `MedicalSystem::HealthPartStatus*` | `leftLeg` |
| 0x88 | `MedicalSystem::HealthPartStatus*` | `rightLeg` |
| 0x90 | `MedicalSystem::HealthPartStatus*` | `leftArm` |
| 0x98 | `MedicalSystem::HealthPartStatus*` | `rightArm` |
| 0xA0 | `float` | `knockoutTimer` |
| 0xA4 | `float` | `worstDamage` |
| 0xA8 | `float` | `needsFirstAidScoreTotal_robot` |
| 0xAC | `float` | `needsFirstAidScoreTotal_fleshy` |
| 0xB0 | `float` | `restedState` |
| 0xB4 | `float` | `stealthHinderance` |
| 0xB8 | `float` | `partBestArm` |
| 0xBC | `float` | `partHead` |
| 0xC0 | `float` | `partWorstTorso` |
| 0xC4 | `float` | `dazedOrAlert` |
| 0xC8 | `RobotLimbs*` | `robotLimbs` |
| 0xD0 | `bool` | `bloodynessChanged` |
| 0xD1 | `bool` | `bloodynessCleanedUp` |
| 0xD8 | `AnimationClass*` | `animation` |
| 0xE0 | `Character*` | `me` |
| 0xE8 | `StringPair` | `weatherGUIfeedback` |
| 0x148 | `WeatherAffecting` | `currentWeatherAffect` |
| 0x14C | `float` | `currentWeatherAffectStrength` |
| 0x150 | `TimeOfDay` | `lastHungerKO` |
| 0x158 | `float` | `nextKOTime` |
| 0x15C | `int` | `_eatenDeathDelay` |
| 0x160 | `bool` | `crippled` |
| 0x161 | `bool` | `unconcious` |
| 0x162 | `bool` | `sub50KO` |
| 0x163 | `bool` | `bloodlossTrauma` |
| 0x164 | `bool` | `dead` |
| 0x165 | `bool` | `rightArmOk` |
| 0x166 | `bool` | `leftArmOk` |
| 0x168 | `Ogre::Vector3` | `lastBloodPosition` |
| 0x178 | `Ogre::FastArray<Wound*>` | `wounds` |
| 0x190 | `lektor<MedicalSystem::HealthPartStatus*>` | `anatomy` |
| 0x1A8 | `CharStats*` | `stats` |
| 0x3B8 | `Character*` | `character` |

## ListScrollBar : public ScrollBar
*MyGUI_ListScrollBar.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x510 | `MyGUI::delegates::CMultiDelegate3<MyGUI::ListScrollBar*, std` | `eventValueChange` |
| 0x528 | `bool` | `disableEvents` |
| 0x530 | `MyGUI::TextBox*` | `mListName` |
| 0x538 | `MyGUI::TextBox*` | `mListValue` |
| 0x540 | `MyGUI::TextBox*` | `mListIndex` |
| 0x548 | `std::vector<std::string, std::allocator<std::string > >` | `mValues` |

## LoadSaveWindow : public wraps::BaseLayout
*LoadSaveWindow.h*

| Offset | Type | Field |
|--------|------|-------|
| 0xA0 | `MyGUI::MultiListBox*` | `list` |
| 0xA8 | `lektor<SaveInfo>` | `games` |
| 0xC0 | `DatapanelGUI*` | `infoPanel` |
| 0xC8 | `lektor<MyGUI::Button*>` | `options` |
| 0xE0 | `std::map<MyGUI::UString, int, std::less<MyGUI::UString>, Ogr` | `savesTimesStr` |
| 0x108 | `NewGameOptionsWindow*` | `newGameOptions` |

## LoadingWindow : public wraps::BaseLayout
*LoadingWindow.h*

| Offset | Type | Field |
|--------|------|-------|
| 0xA0 | `unsigned char` | `currentIndex` |
| 0xA4 | `float` | `currentTime` |
| 0xA8 | `MyGUI::UString` | `loadingStr` |
| 0xE8 | `MyGUI::TextBox*` | `loadingText` |
| 0xF0 | `MyGUI::EditBox*` | `messageText` |
| 0xF8 | `MyGUI::ImageBox*` | `backgroundImage` |
| 0x100 | `lektor<MyGUI::UString>` | `tips` |

## MainTabPortraitPlatoon : public Ogre::GeneralAllocatedObject
*MainBarGUI.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `PortraitMainItemBox*` | `portraitBox` |
| 0x8 | `ActivePlatoon*` | `platoon` |
| 0x10 | `MyGUI::TabItem*` | `tab` |
| 0x18 | `int` | `tabIndex` |
| 0x20 | `MyGUI::ImageBox*` | `flashImage` |
| 0x28 | `char` | `flashing` |
| 0x2C | `float` | `animationTime` |
| 0x30 | `float` | `currentAlpha` |
| 0x38 | `MainBarGUI*` | `mainbar` |
| 0xD0 | `int` | `closeManagerWindowMsg` |
| 0xD4 | `bool` | `isLevelEditMode` |
| 0xD5 | `bool` | `isInteriorLevelEditMode` |
| 0xD8 | `boost::unordered::unordered_map<std::string, DatapanelGUI*, ` | `datapanels` |
| 0x118 | `MyGUI::Widget*` | `bountyPanel` |
| 0x120 | `DatapanelGUI*` | `bountyDatapanel` |
| 0x128 | `TownPanel*` | `townPanel` |
| 0x130 | `MyGUI::TabControl*` | `portraitsTabPanel` |
| 0x138 | `MyGUI::Button*` | `floorDownButton` |
| 0x140 | `MyGUI::Button*` | `floorUpButton` |
| 0x148 | `MyGUI::TextBox*` | `floorText` |
| 0x150 | `Ogre::FastArray<MyGUI::Button*>` | `speedButtons` |
| 0x168 | `MyGUI::TextBox*` | `dayText` |
| 0x170 | `MyGUI::TextBox*` | `moneyLabel` |
| 0x178 | `MyGUI::TextBox*` | `moneyText` |
| 0x180 | `MyGUI::TextBox*` | `timeText` |
| 0x188 | `MedicalDatapanel*` | `medicalPanel` |
| 0x190 | `OrdersPanel*` | `ordersDataPanel` |
| 0x198 | `MyGUI::Button*` | `extendInfoPanelButton` |
| 0x1A0 | `MyGUI::Widget*` | `extendedInfoPanel` |
| 0x1A8 | `MyGUI::types::TPoint<int>` | `extendedInfoPanelShow` |
| 0x1B0 | `MyGUI::types::TPoint<int>` | `extendedInfoPanelHide` |
| 0x1B8 | `float` | `extendedInfoPanelDuration` |
| 0x1BC | `bool` | `infoPanelEnabled` |
| 0x1BD | `bool` | `infoPanelExtended` |
| 0x1C0 | `MyGUI::Widget*` | `biomePanel` |
| 0x1C8 | `MyGUI::TextBox*` | `biomePanelText` |
| 0x1D0 | `float` | `biomePanelVisibleTimer` |
| 0x1D4 | `float` | `biomeTimer` |
| 0x1D8 | `GameData*` | `lastFrameBiomeGroup` |
| 0x1E0 | `GameData*` | `rememberlastBiomeGroup` |
| 0x1E8 | `hand` | `portraitContextMenuTarget` |
| 0x208 | `float` | `portraitContextMenuTimer` |
| 0x210 | `Ogre::FastArray<MainTabPortraitPlatoon>` | `tabPortraits` |
| 0x228 | `char` | `portraitSelectedContextIndex` |
| 0x230 | `ogre_unordered_map<hand, PortraitData*>::type` | `portraits` |
| 0x270 | `boost::unordered::unordered_map<PortraitData*, std::pair<Por` | `portraitsIndices` |
| 0x2B0 | `bool` | `portraitsUpdating` |
| 0x2B8 | `ToolTipFixed*` | `toolTip` |
| 0x2C0 | `MyGUI::types::TPoint<int>` | `toolTipBasePosition` |
| 0x2C8 | `MyGUI::Widget*` | `pausePanel` |
| 0x2D0 | `MyGUI::Widget*` | `loadingPanel` |
| 0x2D8 | `MyGUI::types::TPoint<int>` | `buildingInventoryPosition` |
| 0x2E0 | `MyGUI::types::TPoint<int>` | `messagePosition` |

## ManagementScreen : public wraps::BaseLayout
*ManagementScreen.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `ResearchItem*` | `item` |
| 0xA0 | `SquadManagementScreen*` | `squadScreen` |
| 0xA8 | `MapScreen*` | `mapScreen` |
| 0xB0 | `FactionsScreen*` | `factionScreen` |
| 0xB8 | `MyGUI::ListBox*` | `researchCategoriesListBox` |
| 0xC0 | `DatapanelGUI*` | `availableList` |
| 0xC8 | `DatapanelGUI*` | `info` |
| 0xD0 | `DatapanelGUI*` | `info2` |
| 0xD8 | `std::string` | `techCategory` |
| 0x100 | `MyGUI::delegates::CDelegate2<int, int>` | `eventReordered` |
| 0x100 | `GameData*` | `currentResearch` |
| 0x108 | `MyGUI::delegates::CDelegate2<int, T2 const&>` | `eventRemove` |
| 0x108 | `MyGUI::EditBox*` | `researchBenchMessage` |
| 0x110 | `MyGUI::delegates::CDelegate3<int, int, bool&>` | `eventValidate` |
| 0x110 | `bool` | `researchDescriptionUpdateRequest` |
| 0x118 | `T1*` | `data` |
| 0x118 | `lektor<GameData*>` | `currentCategoryList` |
| 0x130 | `float` | `lastResearchRate` |
| 0x138 | `ReorderableList<std::deque<ResearchItem, Ogre::STLAllocator<` | `todoList` |
| 0x140 | `CraftingQueue*` | `craftingQueue` |
| 0x148 | `MyGUI::EditBox*` | `messagesTextBox` |
| 0x150 | `std::basic_ostringstream<char, std::char_traits<char>, std::` | `messagesStream` |
| 0x238 | `bool` | `messagesUpdated` |
| 0x240 | `boost::shared_mutex` | `messagesMutex` |
| 0x260 | `std::string` | `messagesPlayerColor` |
| 0x288 | `std::string` | `messagesNPCColor` |
| 0x2B0 | `DatapanelGUI*` | `aiScreen` |
| 0x2B8 | `ToolTip*` | `aiToolTip` |
| 0x2C0 | `ToolTip*` | `toolTip` |
| 0x2C8 | `MyGUI::Window*` | `window` |
| 0x2D0 | `MyGUI::TabControl*` | `tabs` |

## MapScreen
*MapScreen.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `hand` | `handle` |
| 0x0 | `hand` | `handle` |
| 0x0 | `float` | `updateTimer` |
| 0x0 | `MyGUI::Widget*` | `widget` |
| 0x8 | `ToolTip*` | `toolTip` |
| 0x8 | `std::vector<MyGUI::types::TPoint<float>, std::allocator<MyGU` | `line` |
| 0x10 | `MyGUI::Widget*` | `mainWidget` |
| 0x18 | `MyGUI::ScrollView*` | `mapScrollView` |
| 0x20 | `MapZoomLevel` | `zoomLayer` |
| 0x20 | `MyGUI::ImageBox*` | `image` |
| 0x20 | `MyGUI::ImageBox*` | `mapImage` |
| 0x28 | `MyGUI::Widget*` | `root` |
| 0x28 | `MyGUI::ImageBox*` | `cameraMarker` |
| 0x30 | `MyGUI::ImageBox*` | `image` |
| 0x30 | `MyGUI::RotatingSkin*` | `cameraMarkerSkin` |
| 0x38 | `MyGUI::TextBox*` | `label` |
| 0x38 | `bool` | `zoomUpdated` |
| 0x3C | `float` | `zoomValueBase` |
| 0x40 | `MyGUI::types::TSize<int>` | `fullSize` |
| 0x40 | `float` | `zoomValueMax` |
| 0x44 | `float` | `zoomValueCurrent` |
| 0x48 | `Ogre::Vector4` | `zoomCenterOffset` |
| 0x58 | `MapZoomLevel` | `zoomLevelCurrent` |
| 0x90 | `ogre_unordered_map<hand, MapScreen::MapMarkerTown*>::type` | `mapMarkersTowns` |
| 0xD0 | `Ogre::FastArray<hand>` | `mapMarkersTownsNew` |
| 0xE8 | `ogre_unordered_map<hand, MapScreen::MapMarkerCharacter*>::ty` | `mapMarkersCharacters` |
| 0x128 | `MyGUI::ImageBox*` | `mapMarkerMovement` |
| 0x130 | `Ogre::Vector3` | `mapMarkerMovementPosition` |
| 0x13C | `float` | `mapMarkerMovementFadeOutDelay` |
| 0x140 | `ogre_unordered_set<hand>::type` | `squadsList` |
| 0x180 | `bool` | `mapDragging` |
| 0x184 | `Ogre::Vector2` | `mapMouseLastPosition` |
| 0x18C | `Ogre::Vector2` | `mapOffsetView` |
| 0x194 | `Ogre::Vector4` | `worldBounds` |
| 0x1A4 | `Ogre::Vector2` | `worldSize` |
| 0x1B0 | `lektor<MapScreen::MapRoad*>` | `roads` |

## MeshDataLookup : public Ogre::GeneralAllocatedObject
*Appearance.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `boost::unordered::unordered_map<Ogre::IdString, lektor<lekto` | `boneAssignments` |
| 0x8 | `const boost::unordered::unordered_map<std::string, Attachmen` | `slots` |
| 0x10 | `boost::unordered::unordered_map<std::string, AttachedEntity*` | `attachedObjects` |
| 0x40 | `unsigned __int64` | `vertCount` |
| 0x48 | `Ogre::Vector3*` | `verts` |
| 0x50 | `Ogre::Vector2*` | `uvs` |
| 0x50 | `Ogre::FastArray<Harpoon*>` | `attachedHarpoons` |
| 0x68 | `bool` | `msgClearHarpoons` |
| 0x70 | `Ogre::FastArray<AttachedEffect*>` | `attachedEffects` |
| 0x88 | `Ogre::FastArray<AttachedEffect*>` | `attachedEffectsToRemove` |
| 0xA0 | `Ogre::FastArray<Wound*>` | `woundsList` |
| 0xB8 | `boost::shared_mutex` | `woundsListMutex` |
| 0xD8 | `Ogre::Entity*` | `body` |
| 0xE0 | `Ogre::Entity*` | `bodyLoader` |
| 0xE8 | `bool` | `isCreatingBody` |
| 0xEC | `float` | `bodyRadius` |
| 0xF0 | `Character*` | `me` |
| 0xF8 | `bool` | `visible` |
| 0x100 | `std::string` | `bodyFilename` |
| 0x128 | `Ogre::SharedPtr<Ogre::Material>` | `bodyMaterial` |
| 0x138 | `AnimationClass*` | `animation` |
| 0x140 | `bool` | `female` |
| 0x141 | `bool` | `updatedAttachments` |
| 0x142 | `bool` | `updatedAppearanceData` |
| 0x143 | `bool` | `updateBody` |
| 0x144 | `int` | `suid` |
| 0x148 | `GameDataCopyStandalone*` | `appearanceData` |
| 0x150 | `GameData*` | `raceData` |
| 0x158 | `GameData*` | `factionColor` |
| 0x160 | `GameData*` | `hairStyle` |
| 0x168 | `bool` | `shaved` |
| 0x16C | `Ogre::Vector4` | `waterline` |
| 0x17C | `float` | `waterLineFadeTimer` |
| 0x180 | `bool` | `barefoot` |
| 0x181 | `bool` | `hideAttachments` |
| 0x184 | `float` | `characterHeight` |
| 0x188 | `float` | `characterHeightSpeedMultiplier` |
| 0x18C | `float` | `characterHeight_0to1` |
| 0x190 | `float` | `robotLegScale` |
| 0x194 | `Ogre::Vector3` | `lastPhysiqueStats` |
| 0x1A0 | `float` | `bulkMult` |
| 0x1A4 | `float` | `muscleMult` |
| 0x1A8 | `float` | `skinnyMult` |
| 0x1AC | `bool` | `flayed` |
| 0x1B0 | `GameData*` | `beard` |
| 0x1B8 | `bool` | `hiddenPartsEnabled` |

## MessageBoxManager : public Ogre::GeneralAllocatedObject
*MessageBoxManager.h*

| Offset | Type | Field |
|--------|------|-------|
| 0xA0 | `Ogre::vector<MyGUI::Button*>::type` | `buttons` |
| 0xC0 | `bool` | `modal` |
| 0xC8 | `MyGUI::delegates::IDelegate1<int>*` | `callback` |

## MessageForB
*Enums.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `MessageForB::MessageType` | `messageType` |
| 0x4 | `int` | `messageInt` |

## MessageQueue
*NavMesh.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `T` | `value` |
| 0x0 | `int` | `s` |
| 0x0 | `hand` | `handle` |
| 0x0 | `NavMesh::MessageType` | `message` |
| 0x8 | `MessageQueue<T>::Node*` | `next` |
| 0x8 | `MessageQueue<T>::Node*` | `root` |
| 0x8 | `ZoneMap*` | `zone` |
| 0x10 | `MessageQueue<T>::Node*` | `split` |
| 0x10 | `hand` | `handle` |
| 0x18 | `MessageQueue<T>::Node*` | `back` |
| 0x20 | `boost::shared_mutex` | `mutex` |
| 0x20 | `unsigned int` | `hash` |
| 0x24 | `Ogre::Aabb` | `bounds` |
| 0x30 | `unsigned int` | `hash` |
| 0x34 | `Ogre::Aabb` | `bounds` |
| 0x40 | `std::string` | `name` |
| 0x50 | `lektor<NavMesh::BuildingInfo>` | `interiors` |
| 0x68 | `NavMesh::NavMeshMessage*` | `next` |
| 0x88 | `hkaiWorld*` | `world` |
| 0x90 | `boost::shared_mutex` | `shiftMutex` |
| 0xB0 | `bool` | `worldShiftEnabled` |
| 0xB8 | `MessageQueue<HavokCharacterMessage*>` | `characterMessages` |
| 0xF8 | `MessageQueue<HavokCharacterMessage*>` | `completedMessages` |
| 0x138 | `MessageQueue<NavMesh::NavMeshMessage*>` | `navMessages` |
| 0x178 | `MessageQueue<ZoneMap*>` | `doorRequests` |
| 0x1B8 | `hkArray<HavokCharacterMessage*, hkContainerHeapAllocator>` | `pathRequests` |
| 0x1C8 | `bool` | `running` |
| 0x1CC | `float` | `worldX` |
| 0x1D0 | `float` | `worldY` |
| 0x1D4 | `float` | `cellSize` |
| 0x1D8 | `hkVector4f*` | `worldShift` |
| 0x1E0 | `boost::shared_mutex` | `mutex` |
| 0x200 | `boost::shared_mutex` | `changeMutex` |
| 0x220 | `std::map<iVector2, NavMeshSector*, std::less<iVector2>, Ogre` | `sectors` |
| 0x248 | `std::map<hand, NavInstance*, std::less<hand>, Ogre::STLAlloc` | `interiors` |
| 0x270 | `lektor<NavInstance*>` | `addList` |
| 0x288 | `hkaiAstarEdgeFilter*` | `edgeFilter` |
| 0x290 | `NavMeshGenerator*` | `generator` |
| 0x298 | `lektor<ZoneMap*>` | `deferredList` |
| 0x2B0 | `hkArray<int, hkContainerHeapAllocator>` | `removed` |

## ModInfo : public Ogre::GeneralAllocatedObject
*ModInfo.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `std::string` | `name` |
| 0x28 | `std::string` | `file` |
| 0x50 | `std::string` | `path` |
| 0x78 | `bool` | `isWorkshop` |
| 0x79 | `bool` | `isBaseMod` |
| 0x80 | `std::string` | `leveldataFolder` |
| 0xA8 | `GameDataHeader` | `header` |

## MultiSlider : public Widget
*MyGUI_MultiSlider.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x478 | `delegates::CMultiDelegate4<MultiSlider*, Slider*, int, int>` | `eventValueChange` |
| 0x490 | `MyGUI::TextBox*` | `mName` |
| 0x498 | `bool` | `mDisableEvents` |
| 0x4A0 | `std::vector<Slider*>` | `mSliders` |

## NavMeshSeeds
*NavMeshGenerator.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `std::map<ZoneMap*, lektor<Ogre::Vector3>, std::less<ZoneMap*` | `seedPoints` |
| 0x0 | `ZoneMap*` | `zone` |
| 0x0 | `NavMeshGenerator::Task*` | `front` |
| 0x8 | `lektor<hand>` | `buildings` |
| 0x8 | `NavMeshGenerator::Task**` | `back` |
| 0x10 | `boost::shared_mutex` | `mutex` |
| 0x20 | `unsigned int` | `hash` |
| 0x24 | `Ogre::Vector3` | `offset` |
| 0x30 | `Ogre::Aabb` | `bounds` |
| 0x48 | `hkaiNavMesh*` | `mesh` |
| 0x50 | `NavInstance*` | `output` |
| 0x58 | `int` | `flags` |
| 0x60 | `NavMeshGenerator::Task*` | `next` |
| 0x88 | `NavMeshGenerator::TaskQueue` | `queue` |
| 0xB8 | `NavMeshGenerator::TaskQueue` | `done` |
| 0xE8 | `NavMeshGenerator::Task*` | `current` |
| 0xF0 | `NavMesh*` | `navmesh` |
| 0xF8 | `bool` | `needSave` |
| 0x100 | `hkaiNavMeshGenerationSettings*` | `settings` |
| 0x108 | `bool` | `threadRunning` |
| 0x109 | `bool` | `doingStuff` |
| 0x110 | `boost::shared_mutex` | `taskMutex` |
| 0x130 | `NavMeshGenerator::Task*` | `lockedTask` |
| 0x138 | `NavMeshSeeds` | `seedPoints` |

## NewGameOptionsWindow : public wraps::BaseLayout
*NewGameOptionsWindow.h*

| Offset | Type | Field |
|--------|------|-------|
| 0xA0 | `DatapanelGUI*` | `optionsPanel` |
| 0xA8 | `ToolTip*` | `tooltip` |

## NxUserTriggerReport
*PhysicsActual.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `float` | `x` |
| 0x0 | `float` | `_11` |
| 0x0 | `S` | `s` |
| 0x0 | `Nx9Real` | `data` |
| 0x0 | `NxVec3` | `center` |
| 0x4 | `float` | `y` |
| 0x4 | `float` | `_12` |
| 0x8 | `lektor<T>` | `mainThreadData` |
| 0x8 | `ogre_unordered_map<hand, hand>::type` | `triggerUpdateMap` |
| 0x8 | `float` | `z` |
| 0x8 | `float` | `_13` |
| 0xC | `float` | `_21` |
| 0xC | `NxVec3` | `extents` |
| 0x10 | `float` | `_22` |
| 0x14 | `float` | `_23` |
| 0x18 | `float` | `_31` |
| 0x18 | `NxMat33` | `rot` |
| 0x1C | `float` | `_32` |
| 0x20 | `lektor<T>` | `backThreadData` |
| 0x20 | `float` | `_33` |
| 0x88 | `CPerfTimer` | `timer` |
| 0x98 | `boost::shared_mutex` | `mute` |
| 0xB8 | `bool` | `paused` |
| 0xC0 | `double` | `speedMult` |
| 0xC8 | `boost::shared_mutex` | `haltEverythingMutex` |
| 0xE8 | `NxScene*` | `nWorld` |
| 0xF0 | `MessageChain<ConstantTracerT*>` | `newConstantTracers` |
| 0x128 | `MessageChain<ConstantTracerT*>` | `removeConstantTracers` |
| 0x160 | `ogre_unordered_set<ConstantTracerT*>::type` | `constantTracers` |
| 0x1A0 | `MessageChain<PhysicsThreadedBaseInterface*>` | `hullsToMake` |
| 0x1D8 | `lektor<PhysicsThreadedBaseInterface*>` | `hulls` |
| 0x1F0 | `MessageChain<PhysicsThreadedBaseInterface*>` | `hullsToDestroy` |
| 0x228 | `MessageChain<std::pair<SimplePhysXEntity*, int> >` | `hullsToChangeGroup` |
| 0x260 | `MessageChain<boost::tuples::tuple<SimplePhysXEntity*, Ogre::` | `impulse` |
| 0x298 | `MessageChain<NxActor*>` | `actorsToDestroy` |
| 0x2D0 | `lektor<DoorStuff*>` | `doorsToSetup` |
| 0x2E8 | `MessageChain<TerrainSector*>` | `terrainToLoad` |
| 0x320 | `bool` | `_queuesClear` |
| 0x328 | `boost::shared_mutex` | `queuesClearMuto` |
| 0x348 | `NxMaterial*` | `materialConcrete` |
| 0x350 | `NxMaterial*` | `materialMetal` |
| 0x358 | `NxMaterial*` | `materialSand` |
| 0x360 | `NxMaterial*` | `materialHuman` |
| 0x368 | `PhysicsActual::TriggerCallback` | `myTriggerCallback` |
| 0x3B0 | `bool` | `HW` |
| 0x3B1 | `bool` | `debugRenderOn` |
| 0x3B2 | `Scythe::PhysicsClass` | `scytheClass` |
| 0x3B8 | `NxControllerManager*` | `controllerMgr` |
| 0x3C0 | `NxPhysicsSDK*` | `physicsSDK` |

## OpenSaveFileDialog : public wraps::BaseLayout
*OpenSaveFileDialog.h*

| Offset | Type | Field |
|--------|------|-------|
| 0xC8 | `MyGUI::ListBox*` | `filesList` |
| 0xD0 | `MyGUI::EditBox*` | `fileNameTxt` |
| 0xD8 | `MyGUI::ComboBox*` | `currentFolderList` |
| 0xE0 | `MyGUI::Button*` | `openSaveButton` |
| 0xE8 | `std::string` | `currentFolder` |
| 0x110 | `std::string` | `fileName` |
| 0x138 | `std::string` | `fileMask` |
| 0x160 | `std::string` | `currentSelected` |
| 0x188 | `bool` | `folderMode` |

## OptionsHolder
*OptionsHolder.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `float` | `CAMERA_MOVE_SPEED` |
| 0x4 | `float` | `CAMERA_PAN_SPEED` |
| 0x8 | `float` | `CAMERA_TILT_SPEED` |
| 0xC | `float` | `CAMERA_ZOOM_SPEED` |
| 0x10 | `float` | `invertX` |
| 0x14 | `float` | `invertY` |
| 0x18 | `float` | `VIEW_DISTANCE` |
| 0x1C | `float` | `terrainDetail` |
| 0x20 | `float` | `terrainDistant` |
| 0x24 | `float` | `terrainThreshold` |
| 0x28 | `int` | `terrainPatchSize` |
| 0x2C | `float` | `grassRange` |
| 0x30 | `float` | `grassDensity` |
| 0x34 | `float` | `foliageRange` |
| 0x38 | `float` | `NPCRange` |
| 0x3C | `float` | `smallBuildingRange` |
| 0x40 | `bool` | `stencilsDisabled` |
| 0x41 | `bool` | `fancyShaders` |
| 0x42 | `bool` | `HWmouse` |
| 0x43 | `bool` | `tutorials` |
| 0x44 | `bool` | `_enabledCivilians` |
| 0x48 | `float` | `populationMult` |
| 0x4C | `float` | `squadSizeMult` |
| 0x50 | `float` | `raidSizeMult` |
| 0x54 | `float` | `raidFrequencyMult` |
| 0x58 | `int` | `passingAttacksOnBase` |
| 0x5C | `int` | `shadowMode` |
| 0x60 | `int` | `shadowQuality` |
| 0x64 | `float` | `harpoonLimit` |
| 0x68 | `float` | `decalRange` |
| 0x6C | `int` | `decalResolution` |
| 0x70 | `bool` | `characterMultithreading` |
| 0x74 | `int` | `limbLossFrequency` |
| 0x78 | `bool` | `showNames` |
| 0x79 | `bool` | `edgeScrolling` |
| 0x7C | `int` | `damageFloaters` |
| 0x80 | `bool` | `showRotationMarker` |
| 0x81 | `bool` | `showMoveMarker` |
| 0x84 | `float` | `fontSize` |
| 0x88 | `bool` | `manyActiveZones` |
| 0x8C | `float` | `distantTownRange` |
| 0x90 | `float` | `featureRange` |
| 0x94 | `bool` | `generateDistantTowns` |
| 0x98 | `float` | `shadowRange` |
| 0x9C | `int` | `ddsTextureMipMapGimping` |
| 0xA0 | `int` | `reflectionMode` |
| 0xA4 | `float` | `reflectionDistance` |
| 0xA8 | `lektor<std::pair<std::string, bool> >` | `compositors` |
| 0xC0 | `float` | `musicVolume` |
| 0xC4 | `float` | `ambientVolume` |
| 0xC8 | `float` | `footstepVolume` |
| 0xCC | `float` | `sfxVolume` |
| 0xD0 | `float` | `uiVolume` |
| 0xD4 | `float` | `voVolume` |
| 0xD8 | `float` | `musicFrequency` |
| 0xDC | `float` | `autosavetime` |
| 0xE0 | `bool` | `fullscreen` |
| 0xE1 | `bool` | `borderless` |
| 0xE2 | `bool` | `autosave` |
| 0xE3 | `bool` | `userSaves` |
| 0xE4 | `bool` | `blood` |
| 0xE5 | `bool` | `censorship` |

## OrderData : public Ogre::GeneralAllocatedObject
*OrdersPanel.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `const Tasker*` | `task` |
| 0x0 | `hand` | `ordersCharacter` |
| 0x8 | `int` | `index` |
| 0x10 | `std::string` | `text` |
| 0x20 | `OrdersItemBox*` | `ordersItemBox` |
| 0x28 | `int` | `ordersItemWidth` |
| 0x2C | `int` | `ordersItemBoxScrollBarSize` |
| 0x30 | `int` | `ordersItemBoxMaxVisible` |
| 0x38 | `bool` | `enabled` |
| 0x38 | `MyGUI::Widget*` | `ordersEmptyPanel` |
| 0x40 | `lektor<OrderData>` | `orders` |
| 0x58 | `MyGUI::Button*` | `blocksCheckbox` |
| 0x60 | `MyGUI::Button*` | `holdCheckBox` |
| 0x68 | `MyGUI::Button*` | `passiveCheckBox` |
| 0x70 | `MyGUI::Button*` | `chaseCheckBox` |
| 0x78 | `MyGUI::Button*` | `tauntCheckBox` |
| 0x80 | `MyGUI::Button*` | `rangedCheckBox` |
| 0x88 | `MyGUI::Button*` | `stealthCheckBox` |
| 0x90 | `MyGUI::Button*` | `speedPrevButton` |
| 0x98 | `MyGUI::Button*` | `speedNextButton` |
| 0xA0 | `MyGUI::ImageBox*` | `speedImagePanel` |
| 0xA8 | `MyGUI::TextBox*` | `orderText` |
| 0xA8 | `Ogre::vector<std::string>::type` | `speedImageNames` |
| 0xB0 | `MyGUI::Button*` | `removeButton` |
| 0xB8 | `OrderData*` | `data` |
| 0xC8 | `char` | `speedImageNamesIdx` |

## Ownerships
*Platoon.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `std::set<hand, std::less<hand>, Ogre::STLAllocator<hand, Ogr` | `slaves` |
| 0x30 | `TownBase*` | `_homeTown` |
| 0x38 | `hand` | `_homeBuilding` |
| 0x58 | `lektor<hand>` | `stuff` |
| 0x68 | `GroupSense*` | `_groupSense` |
| 0x70 | `Faction*` | `faction` |
| 0x70 | `bool` | `isAnimalsOnly` |
| 0x78 | `Platoon*` | `me` |
| 0x78 | `std::string` | `stringID` |
| 0x78 | `Platoon*` | `me` |
| 0x80 | `TownBase*` | `occupiedTown` |
| 0x80 | `HandleList*` | `characterHandles` |
| 0x88 | `int` | `money` |
| 0x88 | `float` | `p_TIME` |
| 0x90 | `ZoneMap*` | `lastActiveZone` |
| 0x98 | `CharacterMemory*` | `_myMemory` |
| 0xA0 | `int` | `_characterCountCurrent` |
| 0xA0 | `Character*` | `squadleader` |
| 0xA4 | `int` | `_characterCountOriginal` |
| 0xA8 | `SquadType` | `squadType` |
| 0xA8 | `Character*` | `backupLeader` |
| 0xAC | `YesNoMaybe` | `hasUniques` |
| 0xB0 | `MoveSpeed` | `speedOverride` |
| 0xB0 | `float` | `deactivationTimer` |
| 0xB4 | `Ogre::Vector3` | `workingPos` |
| 0xB8 | `hand` | `isSeparatedSquad` |
| 0xC0 | `Tasker*` | `currentGoal` |
| 0xC8 | `Ogre::Vector3` | `positionMoved` |
| 0xD4 | `Ogre::Vector3` | `teleportTo` |
| 0xD8 | `bool` | `canRefresh` |
| 0xD9 | `bool` | `regenerates` |
| 0xE0 | `GameData*` | `myBaseHomeTownData` |
| 0xE0 | `bool` | `teleportMessage` |
| 0xE8 | `float` | `priceMultWhenITrade` |
| 0xE8 | `PlayerInterface*` | `isPlayer` |
| 0xEC | `bool` | `_iBuyStolenGoods` |
| 0xED | `bool` | `_iBuyIllegalGoods` |
| 0xF0 | `Ogre::Entity*` | `locatorModel` |
| 0xF0 | `bool` | `isPhysical` |
| 0xF8 | `Blackboard*` | `blackboard` |
| 0x100 | `bool` | `_isIntact` |
| 0x108 | `GameData*` | `squadTemplate` |
| 0x110 | `float` | `malnourishedLevel` |
| 0x114 | `bool` | `hasNeverBeenActivated` |
| 0x115 | `bool` | `_persistentSquad` |
| 0x116 | `bool` | `isResidentSquad` |
| 0x118 | `PlatoonCreationMessage` | `messageOnActivation` |
| 0x120 | `AreaSector*` | `currentSpawnArea` |
| 0x128 | `hand` | `squadleader` |
| 0x148 | `Ownerships` | `ownerships` |
| 0x1D8 | `ActivePlatoon*` | `activePlatoon` |
| 0x1E0 | `UnloadedPlatoon*` | `unloadedPlatoon` |
| 0x1E8 | `PatrolInfo*` | `patrolSettings` |
| 0x1F0 | `bool` | `isDead` |
| 0x1F1 | `bool` | `imprisoned` |
| 0x1F2 | `short` | `index` |
| 0x1F8 | `TimeOfDay` | `traderInventoryRefreshTime` |

## ParticlePool : public Ogre::GeneralAllocatedObject
*CombatClass.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `ParticleSystemHandler*` | `particle` |
| 0x0 | `unsigned int` | `limit` |
| 0x0 | `hand` | `who` |
| 0x0 | `Character*` | `me` |
| 0x0 | `GameData*` | `data` |
| 0x4 | `unsigned int` | `lastIndex` |
| 0x8 | `GameData*` | `effectData` |
| 0x8 | `ParticlePool::ParticleData*` | `particles` |
| 0x8 | `CombatClass*` | `combatClass` |
| 0x8 | `CombatClass::AttackSlotManager` | `attackSlots` |
| 0x8 | `hand` | `character` |
| 0x10 | `Ogre::SceneNode*` | `node` |
| 0x10 | `float` | `maxTTL` |
| 0x20 | `float` | `time` |
| 0x28 | `std::string` | `boneName` |
| 0x50 | `Ogre::Vector3` | `pos` |
| 0x5C | `Ogre::Quaternion` | `rot` |
| 0xE0 | `ogre_unordered_map<swordStateEnum, CombatState*>::type` | `stateMap` |
| 0x120 | `bool` | `wantsToBlock` |
| 0x121 | `bool` | `isStumbleBlocking` |
| 0x124 | `float` | `stumbleTimer` |
| 0x128 | `float` | `whenCanStopStumble` |
| 0x12C | `float` | `stumbleForce` |
| 0x130 | `bool` | `combatModeActive` |
| 0x138 | `double` | `lastCombatModeTimeStamp` |
| 0x140 | `float` | `_isAttacking` |
| 0x144 | `bool` | `inDeadTime` |
| 0x148 | `float` | `deadTimer` |
| 0x14C | `float` | `stateTimer` |
| 0x150 | `CombatTechniqueData*` | `currentTechnique` |
| 0x158 | `bool` | `currentTechniqueHasFinished` |
| 0x15C | `Ogre::Vector3` | `attackStartPos` |
| 0x168 | `float` | `frameTIME` |
| 0x170 | `CharMovement*` | `movement` |
| 0x178 | `AI*` | `ai` |
| 0x180 | `AnimationClass*` | `animation` |
| 0x188 | `Character*` | `me` |
| 0x190 | `CharStats*` | `stats` |
| 0x198 | `MedicalSystem*` | `medical` |
| 0x1A0 | `float` | `myRadiusX` |
| 0x1A8 | `Character*` | `blockingTarget` |
| 0x1B0 | `hand` | `blockingTargetH` |
| 0x1D0 | `int` | `lastIncomingAttackComboSection` |
| 0x1D4 | `bool` | `calculatedTargetsInAttackZoneThisFrame` |
| 0x1D8 | `lektor<hand>` | `targetsInAttackZone` |
| 0x1F0 | `swordStateEnum` | `combatState` |
| 0x1F4 | `swordStateEnum` | `nextMove` |
| 0x1F8 | `lektor<hand>` | `attackersH` |
| 0x210 | `int` | `numEnemiesWaitingForMe1` |
| 0x214 | `int` | `numEnemiesWaitingForMe2` |
| 0x218 | `bool` | `waitCountAlternator` |
| 0x220 | `lektor<Character*>` | `threats` |
| 0x238 | `lektor<hand>` | `threatsH` |
| 0x250 | `lektor<hand>` | `notifiedThreats` |
| 0x268 | `int` | `currentComboSection` |
| 0x26C | `int` | `lastComboSection` |
| 0x270 | `int` | `lastSoundIndex` |
| 0x274 | `float` | `techniqueIntegrityCheckTimer` |
| 0x278 | `float` | `MEI_MIN` |
| 0x27C | `float` | `MEI_MAX` |
| 0x280 | `float` | `MINIMUM_DISTANCE_TO_OTHERS` |
| 0x284 | `float` | `BLOCKING_MEI_DISTANCE_MIN` |
| 0x288 | `float` | `BLOCKING_MEI_DISTANCE_MAX` |
| 0x290 | `Character*` | `currentTarget` |
| 0x298 | `hand` | `currentTargetHandle` |

## PhysicalEntity : public Ogre::GeneralAllocatedObject
*PhysicsCollection.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `AreaBiomeGroup*` | `biomeGroup` |
| 0x0 | `Ogre::Light*` | `light` |
| 0x0 | `lektor<PhysicsCollection::StaticEnt*>` | `staticEnts` |
| 0x8 | `Ogre::MovableObject*` | `ent` |
| 0x8 | `Ogre::vector<Season*>::type` | `seasons` |
| 0x8 | `float` | `brightness` |
| 0xC | `float` | `range` |
| 0x10 | `PhysicalEntity*` | `parent` |
| 0x18 | `char` | `floorNumber` |
| 0x18 | `lektor<SimplePhysXEntity*>` | `parts` |
| 0x20 | `GameData*` | `mat` |
| 0x28 | `GameData*` | `partData` |
| 0x28 | `float` | `weatherStrengthMultiplierMin` |
| 0x2C | `float` | `weatherStrengthMultiplierMax` |
| 0x30 | `bool` | `instanced` |
| 0x30 | `WeatherInstance*` | `weatherInstance` |
| 0x30 | `lektor<PhysicsCollection::LightEnt*>` | `lights` |
| 0x31 | `bool` | `isShell` |
| 0x32 | `bool` | `isEmissive` |
| 0x38 | `Season*` | `currentSeason` |
| 0x40 | `int` | `currentSeasonIndex` |
| 0x40 | `Ogre::Vector3` | `rotAxis` |
| 0x44 | `int` | `currentSeasonEndDay` |
| 0x48 | `Ogre::vector<WeatherRegion::Listener*>::type` | `listeners` |
| 0x4C | `Ogre::Radian` | `rotAngle` |
| 0x50 | `float` | `rotationSpeed` |
| 0x54 | `float` | `rotationPower` |
| 0x58 | `float` | `speedMin` |
| 0x5C | `float` | `speedMax` |
| 0x60 | `BuildingRotation` | `rotationFunction` |
| 0x64 | `Ogre::Quaternion` | `rotationBase` |
| 0x68 | `bool` | `biomeGroupLoaded` |
| 0x69 | `bool` | `requestUpdateEffects` |
| 0x70 | `Ogre::vector<EffectGroup*>::type` | `effects` |
| 0x74 | `bool` | `isRotating` |
| 0x78 | `Ogre::Quaternion` | `rotationSrc` |
| 0x88 | `Ogre::Quaternion` | `rotationDst` |
| 0x90 | `std::vector<std::pair<EffectType::Enum, float>, Ogre::STLAll` | `activeGlobalEffects` |
| 0x98 | `float` | `rotatingTime` |
| 0x9C | `float` | `rotationDuration` |
| 0xA0 | `float` | `windSpeedRotationMin` |
| 0xA4 | `float` | `windSpeedRotationMax` |
| 0xA8 | `float` | `windSpeedRotationDanger` |
| 0xB0 | `bool` | `activeCameraBiome` |
| 0xB1 | `bool` | `weatherUpdated` |
| 0xB2 | `bool` | `instanceUpdated` |

## PortraitData : public Ogre::GeneralAllocatedObject
*SquadManagementScreen.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `std::string` | `name` |
| 0x0 | `ActivePlatoon*` | `platoon` |
| 0x0 | `MyGUI::Widget*` | `mainWidget` |
| 0x8 | `MyGUI::Button*` | `btnAddSquad` |
| 0x10 | `MyGUI::TextBox*` | `txtFactionSize` |
| 0x18 | `int` | `factionSize` |
| 0x20 | `SquadManagementScreen::SquadItemBox*` | `panelSquads` |
| 0x28 | `char` | `flashing` |
| 0x28 | `SquadManagementScreen::PortraitSquadItemBox*` | `panelDismiss` |
| 0x2C | `PortraitData::State` | `state` |
| 0x30 | `bool` | `reloadPortrait` |
| 0x30 | `Character*` | `dismissChar` |
| 0x38 | `hand` | `characterHandle` |
| 0x38 | `Faction*` | `faction` |
| 0x40 | `std::map<ActivePlatoon*, SquadManagementScreen::SquadData*, ` | `squads` |
| 0x58 | `bool` | `updateRequested` |
| 0xA0 | `hand` | `characterHandle` |
| 0xA0 | `SquadManagementScreen::PortraitSquadItemBox*` | `portraitsBox` |
| 0xA8 | `MyGUI::EditBox*` | `txtName` |
| 0xB0 | `MyGUI::TextBox*` | `txtSquadSize` |
| 0xB8 | `SquadManagementScreen::SquadData*` | `squad` |
| 0xC0 | `std::string` | `name` |
| 0xE8 | `MyGUI::Button*` | `border` |
| 0xF0 | `MyGUI::ImageBox*` | `imgBoxPortrait` |
| 0xF8 | `MyGUI::TextBox*` | `txtName` |
| 0xF8 | `SquadManagementScreen::SquadData*` | `squad` |
| 0x100 | `SquadManagementScreen::SquadCellView*` | `squadView` |

## PortraitImage : public Ogre::GeneralAllocatedObject
*PortraitManager.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `unsigned short` | `index` |
| 0x0 | `iVector2` | `textureSize` |
| 0x2 | `bool` | `created` |
| 0x8 | `std::string` | `textureName` |
| 0x8 | `std::string` | `textureName` |
| 0x30 | `Ogre::TRect<float>` | `textureRect` |
| 0x30 | `iVector2` | `texturePortraitSize` |
| 0x38 | `unsigned short` | `maxIndex` |
| 0x40 | `MyGUI::types::TCoord<int>` | `coords` |
| 0x40 | `Ogre::SharedPtr<Ogre::Texture>` | `texture` |
| 0x50 | `std::vector<std::pair<bool, PortraitImage*>, Ogre::STLAlloca` | `images` |
| 0x70 | `std::map<hand, std::pair<PortraitData*, PortraitImage*>, std` | `characterPortraits` |
| 0x98 | `bool*` | `imagesIndices` |
| 0xA0 | `bool` | `disableUpdate` |
| 0xA8 | `hand` | `characterHandle` |
| 0xC8 | `std::string` | `name` |
| 0xF0 | `MyGUI::Button*` | `border` |
| 0xF8 | `MyGUI::ImageBox*` | `imageBackground` |
| 0x100 | `MyGUI::ImageBox*` | `imagePortrait` |
| 0x108 | `MyGUI::ImageBox*` | `imageOverlayBack` |
| 0x110 | `MyGUI::ImageBox*` | `imageOverlayFront` |
| 0x118 | `MyGUI::TextBox*` | `textName` |

## ProspectingWindow : public wraps::BaseLayout
*ProspectingWindow.h*

| Offset | Type | Field |
|--------|------|-------|
| 0xA0 | `MyGUI::Button*` | `button` |
| 0xA0 | `MyGUI::Window*` | `window` |
| 0xA8 | `MyGUI::ImageBox*` | `imgMap` |
| 0xB0 | `MyGUI::Widget*` | `listResourcesPanel` |
| 0xB8 | `MyGUI::Button*` | `listResourcesSelected` |
| 0xC0 | `MyGUI::ImageBox*` | `cameraMarker` |
| 0xC8 | `MyGUI::RotatingSkin*` | `cameraMarkerSkin` |
| 0xD0 | `DatapanelGUI*` | `datapanelOverview1` |
| 0xD8 | `DatapanelGUI*` | `datapanelOverview2` |
| 0xE0 | `Ogre::vector<ProspectingWindow::ResourceLinePanel*>::type` | `lines` |
| 0x100 | `RealWorldEditableImage*` | `resourceImage` |
| 0x108 | `Ogre::Vector3` | `lastPos` |
| 0x114 | `float` | `lastSkill` |
| 0x118 | `std::string` | `lastName` |

## ProsperityManager
*FactionUniqueSquadManager.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `public:
    double` | `actualProsperity` |
| 0x0 | `GameData*` | `squadTemplate` |
| 0x8 | `float` | `maxProsperity` |
| 0x8 | `ProsperityManager` | `prosperityMgr` |
| 0x8 | `int` | `desiredNumberToHave` |
| 0xC | `float` | `respawnTimer` |
| 0x10 | `lektor<hand>` | `existingSquadsList` |
| 0x18 | `Faction*` | `me` |
| 0x20 | `GameData*` | `squadListData` |
| 0x28 | `Town*` | `homeTown` |
| 0x30 | `lektor<FactionUniqueSquadManager::UniqueSpawnData*>` | `squads` |

## RaceData
*RaceData.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `public:
    ogre_unordered_set<GameData*>::type` | `specialFoods` |
| 0x40 | `GameData*` | `data` |
| 0x48 | `float` | `runSpeedMaxSkill` |
| 0x4C | `float` | `runSpeedMinSkill` |
| 0x50 | `float` | `originalBloodMin` |
| 0x54 | `float` | `originalBloodMax` |
| 0x58 | `float` | `healRate` |
| 0x5C | `float` | `bleedRate` |
| 0x60 | `float` | `swimSpeed` |
| 0x64 | `float` | `walkSpeed` |
| 0x68 | `float` | `swimOffset` |
| 0x6C | `float` | `waterAvoidance` |
| 0x70 | `float` | `hungerRate` |
| 0x74 | `float` | `visionMultiplier` |
| 0x78 | `bool` | `gigantic` |
| 0x79 | `bool` | `swims` |
| 0x7A | `bool` | `carriable` |
| 0x7B | `bool` | `singleGender` |
| 0x7C | `bool` | `robot` |
| 0x7D | `bool` | `vampiric` |
| 0x7E | `bool` | `noHats` |
| 0x7F | `bool` | `noShirts` |
| 0x80 | `bool` | `noShoes` |
| 0x84 | `int` | `extraAttackSlots` |
| 0x88 | `StatsEnumerated` | `firstAidSkill` |
| 0x8C | `Ogre::ColourValue` | `bloodColour` |
| 0x9C | `bool` | `canGoIndoors` |
| 0xA0 | `ogre_unordered_map<StatsEnumerated, float>::type` | `statMods` |
| 0xE0 | `ogre_unordered_set<WeatherAffecting>::type` | `weatherImmunities` |
| 0x120 | `RaceGroupData*` | `raceGroup` |

## ResearchBuildingInventoryLayout : public GenericInventoryLayout
*ResearchBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x3C0 | `MyGUI::Button*` | `researchButton` |

## RootObject : public RootObjectBase
*RootObject.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `bool` | `isStored` |
| 0x8 | `itemType` | `baseTypes` |
| 0xC | `itemType` | `stateEnum` |
| 0x10 | `GameDataContainer*` | `objectDatas` |
| 0x10 | `std::string` | `specificProperty` |
| 0x18 | `std::string` | `datasFile` |
| 0x38 | `bool` | `desiredSpecificProperty` |
| 0x40 | `DataObjectContainer::GroupType` | `selfType` |
| 0x50 | `lektor<RootObject*>` | `things` |
| 0x78 | `RootObjectContainer*` | `container` |
| 0x80 | `hand` | `isInsideBuilding` |
| 0xA0 | `int` | `isInsideTownWalls` |
| 0xA4 | `int` | `floorNum` |
| 0xA8 | `unsigned int` | `spacialKey` |
| 0xAC | `int` | `outdoorDelayNotification_timer` |
| 0xB0 | `Ogre::Quaternion` | `rot` |

## RootObjectBase
*RootObjectBase.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `int` | `validKey` |
| 0x10 | `Faction*` | `owner` |
| 0x18 | `std::string` | `displayName` |
| 0x40 | `GameData*` | `data` |
| 0x48 | `Ogre::Vector3` | `pos` |
| 0x58 | `hand` | `handle` |

## RootObjectFactory : public Ogre::GeneralAllocatedObject
*RootObjectFactory.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `RootObjectContainer*` | `container` |
| 0x0 | `boost::shared_mutex` | `todoMutex` |
| 0x8 | `Building*` | `homeBuilding` |
| 0x10 | `Faction*` | `faction` |
| 0x18 | `GameData*` | `data` |
| 0x20 | `Ogre::Vector3` | `position` |
| 0x20 | `std::deque<RootObjectFactory::CreatelistItem*, std::allocato` | `todoList` |
| 0x2C | `bool` | `isFromActiveLevelMod` |
| 0x30 | `Ogre::Quaternion` | `rotation` |
| 0x40 | `FactoryCallbackInterface*` | `callbackObject` |
| 0x48 | `GameSaveState*` | `saveState` |
| 0x50 | `float` | `age` |

## SaveFileSystem : public ThreadClass
*SaveFileSystem.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `SaveFileSystem::MessageType` | `mode` |
| 0x8 | `std::string` | `source` |
| 0x30 | `std::string` | `dest` |
| 0x88 | `std::map<std::string, int, std::less<std::string >, Ogre::ST` | `fileSystem` |
| 0xB0 | `boost::unordered::unordered_set<std::string, boost::hash<std` | `deletedFiles` |
| 0xF0 | `lektor<std::string >` | `paths` |
| 0x108 | `lektor<std::string >` | `oldCurrentFolders` |
| 0x120 | `std::string` | `currentSave` |
| 0x148 | `std::string` | `currentFolder` |
| 0x170 | `std::string` | `tempFolder` |
| 0x198 | `int` | `currentPathIndex` |
| 0x1A0 | `boost::shared_mutex` | `currentMutex` |
| 0x1C0 | `MyGUI::ImageBox*` | `savingIcon` |
| 0x1C8 | `lektor<SaveFileSystem::FileMessage>` | `messages` |
| 0x1E0 | `SaveFileSystem::State` | `state` |
| 0x1E8 | `std::string` | `failedToCopyError` |
| 0x210 | `std::basic_ofstream<char, std::char_traits<char> >` | `saveLog` |

## SaveManager : public Ogre::GeneralAllocatedObject
*SaveManager.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `std::string` | `currentGame` |
| 0x28 | `std::string` | `saveVersion` |
| 0x50 | `std::string` | `localSavePath` |
| 0x78 | `std::string` | `userSavePath` |
| 0xA0 | `int` | `signal` |
| 0xA4 | `int` | `flags` |
| 0xA8 | `int` | `delay` |
| 0xB0 | `std::string` | `name` |
| 0xD8 | `std::string` | `location` |
| 0x100 | `LoadGameMenu*` | `loadMenu` |
| 0x108 | `SaveGameMenu*` | `saveMenu` |
| 0x110 | `ImportGameMenu*` | `importMenu` |
| 0x118 | `float` | `autoSaveTimer` |
| 0x11C | `bool` | `pauseAutoSaveTimer` |

## ScreenLabelInterface : public Ogre::GeneralAllocatedObject
*ScreenLabel.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `bool` | `visible` |
| 0xC | `Ogre::Vector3` | `position` |
| 0x18 | `bool` | `needUpdate` |
| 0x20 | `std::string` | `caption` |
| 0x20 | `std::string` | `caption` |
| 0x48 | `MyGUI::TextBox*` | `textWidget` |
| 0x48 | `int` | `progress` |
| 0x50 | `MyGUI::Colour` | `color` |
| 0x50 | `FloatingProgressBar::ProgressBarWidget*` | `bar` |
| 0x60 | `float` | `risingSpeed` |
| 0x64 | `float` | `risingHeight` |
| 0x68 | `ScreenLabel::LabelSize` | `labelSize` |
| 0x70 | `hand` | `trackingHandle` |
| 0x90 | `Ogre::Vector3` | `trackingOffset` |
| 0x9C | `bool` | `destroyed` |
| 0xA0 | `float` | `timeLeft` |
| 0xA0 | `MyGUI::ProgressBar*` | `bar` |
| 0xA8 | `MyGUI::TextBox*` | `label` |

## SeenSomeone
*SensoryData.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `Ogre::Vector3` | `lastPosition` |
| 0x0 | `boost::unordered::iterator_detail::c_iterator<boost::unorder` | `it` |
| 0x0 | `hand` | `handle` |
| 0x0 | `public:
    float` | `nearestEnemy` |
| 0x0 | `float` | `timeSoFar` |
| 0x0 | `std::map<hand, SensoryData::SpottingPeopleMgr::Spot, std::le` | `spottedPeople` |
| 0x4 | `float` | `timeLimitMax` |
| 0x8 | `boost::unordered::iterator_detail::c_iterator<boost::unorder` | `_end` |
| 0x8 | `ogre_unordered_map<hand, SeenSomeone*>::type` | `seen` |
| 0x8 | `bool` | `stillSeen` |
| 0x10 | `TimeOfDay` | `lastSeenTime` |
| 0x10 | `unsigned int` | `flagsAny` |
| 0x14 | `unsigned int` | `flagsNot` |
| 0x18 | `Faction*` | `percievedFaction` |
| 0x20 | `SlaveStateEnum` | `percievedSlave` |
| 0x20 | `float` | `range` |
| 0x24 | `float` | `FOVScore` |
| 0x24 | `bool` | `isEnemy` |
| 0x28 | `TagsClass<SenseType>` | `type` |
| 0x38 | `bool` | `canSee` |
| 0x39 | `bool` | `canHear` |
| 0x3C | `float` | `alarmState` |
| 0x48 | `int` | `numUnconsciousAllies` |
| 0x4C | `int` | `numConsciousAllies` |
| 0x50 | `lektor<hand>` | `threats` |
| 0x68 | `Ogre::vector<VisibleObjectInfo>::type` | `flockingList` |
| 0x88 | `float` | `totalThreatLevelPersonal` |
| 0x8C | `float` | `totalThreatLevelAllies` |
| 0x90 | `float` | `totalIntendedThreatLevelGeneral` |
| 0x94 | `int` | `numEnemies` |
| 0x98 | `int` | `numNeutrals` |
| 0x9C | `float` | `lastThreat` |
| 0xA0 | `std::map<hand, float, std::less<hand>, std::allocator<std::p` | `hearTestTimers` |
| 0xC0 | `ogre_unordered_set<hand>::type` | `killList` |
| 0x100 | `int` | `currentAssessIndex` |
| 0x104 | `int` | `currentAssessList` |
| 0x108 | `ogre_unordered_set<hand>::type` | `assessList` |
| 0x148 | `Character*` | `me` |
| 0x150 | `SensoryData::SpottingPeopleMgr` | `spottedSneakingPeople` |
| 0x178 | `SensoryData::SpottingPeopleMgr` | `spottedSuspiciousPeople` |
| 0x1A0 | `FloatingProgressBar*` | `progressBar` |
| 0x1A8 | `int` | `progressBarStillNeeded` |
| 0x1B0 | `hand` | `spottedGuyIndexForProgressBar` |
| 0x1D0 | `bool` | `amSharingThisFrame` |

## ShopTraderInventorySection : public InventorySection
*ShopTraderInventory.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x98 | `ogre_unordered_map<hand, InventorySection*>::type` | `inventories` |
| 0xD8 | `ShopTraderInventorySection*` | `section` |

## SimpleTimeStamper
*GameWorld.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `public:
    CPerfTimer` | `timer` |
| 0x0 | `public:
        GameWorld::SysMessageEnum` | `msg` |
| 0x8 | `float` | `tempSpawnsDisableTimer` |
| 0x8 | `hand` | `target` |
| 0xC | `bool` | `initialized` |
| 0x10 | `RendererT*` | `render` |
| 0x18 | `PhysicsInterface*` | `physics` |
| 0x20 | `GameDataManager` | `gamedata` |
| 0x28 | `hand` | `from` |
| 0x48 | `bool` | `on` |
| 0x4C | `float` | `number` |
| 0x50 | `void*` | `data` |
| 0x1A0 | `GameDataManager` | `leveldata` |
| 0x320 | `GameDataManager` | `savedata` |
| 0x4A0 | `RootObjectFactory*` | `theFactory` |
| 0x4A8 | `FactionManager*` | `factionMgr` |
| 0x4B0 | `NavMesh*` | `navmesh` |
| 0x4B8 | `NodeList*` | `nodeList` |
| 0x4C0 | `hand` | `guiDisplayObject` |
| 0x4E0 | `MessageRoller*` | `messageRoller` |
| 0x4E8 | `Ogre::Log*` | `ogreLogger` |
| 0x4F0 | `bool` | `steamEnabled` |
| 0x4F8 | `lektor<ModInfo>` | `baseMods` |
| 0x510 | `lektor<std::string >` | `baseModsNames` |
| 0x528 | `lektor<ModInfo*>` | `activeMods` |
| 0x540 | `std::map<std::string, ModInfo, std::less<std::string >, Ogre` | `availableModsByName` |
| 0x568 | `lektor<ModInfo*>` | `availabelModsOrderedList` |
| 0x580 | `PlayerInterface*` | `player` |
| 0x588 | `ogre_unordered_set<Character*>::type` | `charactersWithLights` |
| 0x5C8 | `std::list<GameWorld::SysMessage, Ogre::STLAllocator<GameWorl` | `sysMessageList` |
| 0x5E8 | `ogre_unordered_map<hand, float>::type` | `updatePortraitsMap` |
| 0x628 | `lektor<hand>` | `dynamicDestroyBuildingsList` |
| 0x640 | `ogre_unordered_set<AttachedEntity*>::type` | `destroyListAE` |
| 0x680 | `ogre_unordered_set<Ogre::MovableObject*>::type` | `destroyListOE` |
| 0x6C0 | `ogre_unordered_set<TownBuildingsManager*>::type` | `destroyListTBM` |
| 0x700 | `float` | `frameSpeedMult` |
| 0x708 | `ogre_unordered_map<hand, Character*>::type` | `deathParade` |
| 0x748 | `bool` | `deathParadeWasMeddledWith` |
| 0x749 | `bool` | `charUpdateListMain_inUse` |
| 0x750 | `ogre_unordered_set<Character*>::type` | `charUpdateListMain` |
| 0x790 | `RenderTimeBackthread*` | `_AINonRenderThread` |
| 0x798 | `std::deque<NestBatcher*, Ogre::STLAllocator<NestBatcher*, Og` | `nestBatcherKillList` |
| 0x7D0 | `ogre_unordered_set<RootObject*>::type` | `killListPhase0` |
| 0x810 | `ogre_unordered_map<RootObject*, float>::type` | `killListPhase1` |
| 0x850 | `std::deque<RootObject*, Ogre::STLAllocator<RootObject*, Ogre` | `killListPhase2` |
| 0x888 | `lektor<Character*>` | `mainUpdateListRemovalQueue` |
| 0x8A0 | `SimpleTimeStamper` | `timeStamper` |
| 0x8B0 | `ZoneManager*` | `zoneMgr` |
| 0x8B8 | `bool` | `debugFlag` |
| 0x8B9 | `bool` | `paused` |
| 0x8BA | `bool` | `gameResetting` |
| 0x8C0 | `AudioSystemGlobal*` | `audioThread` |

## Slider : public Widget
*MyGUI_Slider.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x478 | `delegates::CMultiDelegate2<Slider*, int>` | `eventValueChange` |
| 0x490 | `bool` | `mDisableEvents` |
| 0x498 | `ScrollBar*` | `mScrollbar` |
| 0x4A0 | `TextBox*` | `mSliderName` |
| 0x4A8 | `TextBox*` | `mSliderValue` |
| 0x4B0 | `int` | `mLoValue` |
| 0x4B4 | `int` | `mHiValue` |

## SplashScreen
*SplashScreen.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `char` | `currentState` |
| 0x8 | `double` | `startTime` |
| 0x10 | `bool` | `skipLogo` |
| 0x14 | `int` | `delay` |
| 0x18 | `MyGUI::Widget*` | `mainPanel` |
| 0x20 | `lektor<MyGUI::ImageBox*>` | `logos` |

## Stat
*CharacterStatsWindow.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `StatsEnumerated` | `type` |
| 0x0 | `CharacterStatsWindow::StatGroup::Group` | `group` |
| 0x8 | `std::string` | `id` |
| 0x8 | `std::string` | `name` |
| 0x30 | `std::string` | `name` |
| 0x58 | `std::string` | `description` |
| 0x80 | `bool` | `active` |
| 0xD0 | `Character*` | `character` |
| 0xD8 | `int` | `statsSum` |
| 0xDC | `StatsEnumerated` | `statProgress` |
| 0xE0 | `std::string` | `currentStatIdDescription` |
| 0x108 | `DatapanelGUI*` | `attributesDatapanel` |
| 0x110 | `DatapanelGUI*` | `skills1Datapanel` |
| 0x118 | `DatapanelGUI*` | `skills2Datapanel` |
| 0x120 | `DatapanelGUI*` | `skills3Datapanel` |
| 0x128 | `DatapanelGUI*` | `skills4Datapanel` |
| 0x130 | `DatapanelGUI*` | `statsDatapanel` |
| 0x138 | `DatapanelGUI*` | `description1Datapanel` |
| 0x140 | `DatapanelGUI*` | `description2Datapanel` |
| 0x148 | `bool` | `autoUpdateMode` |

## StringPair
*StringPair.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `std::string` | `s1` |
| 0x30 | `std::string` | `s2` |
| 0x58 | `float` | `val1` |

## TagsClass
*TagsClass.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `unsigned int` | `flags` |

## TaskStateData
*Tasker.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `StateType` | `key` |
| 0x0 | `bool` | `infrequentGoalChecks` |
| 0x4 | `bool` | `val` |
| 0x4 | `PermajobType` | `permaJob` |
| 0x5 | `bool` | `progressionOnly` |
| 0x8 | `bool` | `permaJob_FixedTarget` |
| 0x8 | `taskPriority` | `priority` |
| 0xC | `TaskType` | `permaJob_Associated` |
| 0xC | `bool` | `resetsWhenDone` |
| 0x10 | `TaskType` | `permaJob_Associated_Secondary` |
| 0x10 | `hand` | `subject` |
| 0x14 | `bool` | `requirementsAlwaysFalse` |
| 0x15 | `bool` | `_resultsAlwaysFalse` |
| 0x16 | `bool` | `_requirementsCantEndActionPrematurely` |
| 0x18 | `float` | `durationMin` |
| 0x1C | `float` | `durationFuzz` |
| 0x20 | `bool` | `isDurationBased` |
| 0x21 | `bool` | `endsAfterTime` |
| 0x22 | `bool` | `isUnstoppableTask` |
| 0x23 | `bool` | `canDoTaskInStages` |
| 0x24 | `float` | `aggressionLevel` |
| 0x28 | `float` | `noisyness` |
| 0x2C | `float` | `aidLevel` |
| 0x30 | `float` | `followMeWeight` |
| 0x30 | `float` | `weight` |
| 0x34 | `float` | `copyMeInfluence` |
| 0x38 | `bool` | `normallyLeadsToSomething` |
| 0x38 | `hand` | `currentSubTarget` |
| 0x3C | `float` | `alertnessMult` |
| 0x40 | `bool` | `forDirectPlayerOrdersOnly` |
| 0x41 | `bool` | `forFulfillPlayerOrdersOrNPCOnly` |
| 0x44 | `TaskType` | `key` |
| 0x48 | `bool` | `needsTarget` |
| 0x4C | `int` | `numResults` |
| 0x58 | `Ogre::Vector3` | `location` |
| 0x64 | `int` | `startTime` |
| 0x68 | `int` | `endTime` |
| 0x70 | `TaskData*` | `taskData` |
| 0xA8 | `int` | `numRequirements` |
| 0x108 | `function*` | `scoreFunction` |
| 0x120 | `bool` | `justDoOneTarget` |
| 0x128 | `TaskStateData*` | `subTask` |
| 0x130 | `EventTriggerEnum` | `dialogueDelivery` |
| 0x134 | `bool` | `hasAction` |
| 0x138 | `std::string` | `description` |
| 0x160 | `function*` | `_findTarget` |

## TextureLoadData
*ResourceLoader.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `std::string` | `skeletonName` |
| 0x0 | `public:
        unsigned __int64` | `requestId` |
| 0x0 | `public:
        Ogre::SharedPtr<Ogre::Material>` | `material` |
| 0x8 | `std::string` | `name` |
| 0x10 | `Ogre::TextureUnitState*` | `textureUnitState` |
| 0x28 | `std::string` | `materialName` |
| 0x30 | `std::string` | `group` |
| 0x30 | `MeshLoadData` | `data` |
| 0x50 | `Ogre::SharedPtr<Ogre::Material>` | `material` |
| 0x58 | `Ogre::Image` | `image` |
| 0x60 | `unsigned char` | `renderQueue` |
| 0x90 | `bool` | `running` |
| 0x98 | `bool` | `loaded` |
| 0x98 | `Ogre::Entity*` | `entity` |
| 0x98 | `Ogre::SceneManager*` | `sceneManager` |
| 0x99 | `bool` | `queued` |
| 0x9A | `bool` | `success` |
| 0xA0 | `Ogre::vector<std::string>::type` | `filesNames` |
| 0xA0 | `ogre_unordered_map<unsigned __int64, ResourceLoadRequestMesh` | `activeMeshLoaders` |
| 0xC0 | `Ogre::vector<Ogre::Image>::type` | `images` |
| 0xE0 | `ogre_unordered_map<unsigned __int64, ResourceLoadRequestMesh` | `abortedMeshLoaders` |
| 0x120 | `std::list<ResourceLoadRequestMesh*, Ogre::STLAllocator<Resou` | `loadedMeshesList` |
| 0x140 | `std::list<ResourceLoadRequestMesh*, Ogre::STLAllocator<Resou` | `loadingMeshQueue` |
| 0x160 | `boost::shared_mutex` | `loadingMeshQueueMutex` |
| 0x180 | `boost::unordered::unordered_map<TextureLoadData*, Ogre::Fast` | `activeTextureLoaders` |
| 0x1C0 | `ogre_unordered_set<TextureLoadData*>::type` | `texturesToLoad` |
| 0x200 | `boost::shared_mutex` | `texturesLoadingMutex` |
| 0x220 | `boost::shared_mutex` | `texturesLoadedMutex` |
| 0x240 | `Ogre::FastArray<TextureLoadData*>` | `texturesLoading` |
| 0x258 | `Ogre::FastArray<TextureLoadData*>` | `texturesLoaded` |
| 0x270 | `boost::unordered::unordered_map<Ogre::SharedPtr<Ogre::Textur` | `manualTexturesLoaded` |
| 0x2B0 | `ogre_unordered_set<Ogre::TextureUnitState*>::type` | `textureUnitsLoading` |

## ThreadClass
*ThreadClass.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `void*` | `threadHandle` |
| 0x10 | `unsigned int` | `threadID` |
| 0x14 | `bool` | `_running` |
| 0x18 | `std::string` | `name` |
| 0x40 | `float` | `frameTime` |
| 0x44 | `bool` | `infiniteMode` |
| 0x45 | `bool` | `pretendThread` |
| 0x48 | `boost::shared_mutex` | `runMute` |
| 0x68 | `boost::shared_mutex` | `lockedWhileRunningMute` |

## TimeOfDay
*TimeOfDay.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `double` | `time` |

## ToolTip : public Ogre::GeneralAllocatedObject
*ToolTip.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `MyGUI::Widget*` | `content` |
| 0x8 | `MyGUI::EditBox*` | `leftBox` |
| 0x8 | `MyGUI::Widget*` | `panel` |
| 0x10 | `MyGUI::EditBox*` | `rightBox` |
| 0x10 | `Ogre::vector<ToolTip::ToolTipLine*>::type` | `lines` |
| 0x18 | `int` | `width` |
| 0x30 | `int` | `panelWidth` |
| 0x34 | `float` | `lineMarginH` |
| 0x38 | `int` | `panelMarginV` |
| 0x3C | `int` | `lineSpacing` |
| 0x40 | `MyGUI::Widget*` | `caller` |
| 0x48 | `MyGUI::Widget*` | `parentPanel` |
| 0x48 | `ToolTipInventory*` | `compareTooltip` |
| 0x50 | `int` | `minHeight` |

## TortureBuilding : public ProductionBuilding
*TortureBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x490 | `float` | `timer` |

## TownPositionCacher
*Town.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `TimeOfDay` | `lastUpdateStamp` |
| 0x0 | `GameData*` | `data` |
| 0x0 | `hand` | `parentTown` |
| 0x0 | `Ogre::Vector3` | `pos` |
| 0x8 | `ogre_unordered_map<Building*, TownBuildingsManager::Building` | `buildingEntities` |
| 0x8 | `float` | `updateRateInHours` |
| 0x8 | `ogre_unordered_set<GameData*>::type` | `buildingsBad` |
| 0xC | `Ogre::Vector3` | `pos` |
| 0x10 | `GameData*` | `data` |
| 0x18 | `hand` | `building` |
| 0x20 | `Item*` | `item` |
| 0x28 | `GameData*` | `nestData` |
| 0x30 | `Ogre::Vector3` | `pos` |
| 0x40 | `hand` | `insideBuilding` |
| 0x48 | `boost::unordered::unordered_map<std::string, Ogre::InstanceM` | `instancesManagers` |
| 0x48 | `ogre_unordered_set<GameData*>::type` | `buildingsGood` |
| 0x60 | `unsigned char` | `visibleFloor` |
| 0x88 | `Ogre::FastArray<std::pair<Building*, Ogre::Entity*> >` | `signs` |
| 0x88 | `int` | `count` |
| 0x8C | `int` | `chance` |
| 0x90 | `int` | `priority` |
| 0xA0 | `bool` | `signsVisible` |
| 0xA8 | `TownBase*` | `town` |
| 0xC0 | `TownPositionCacher` | `positionCacher` |
| 0xD8 | `TownType` | `townType` |
| 0xE0 | `BasePopulationManager*` | `population` |
| 0xE8 | `std::set<Faction*, std::less<Faction*>, Ogre::STLAllocator<F` | `factionsResidentHere` |
| 0x110 | `bool` | `alreadyInitialisedPopulationParams` |
| 0x111 | `bool` | `isSecret` |
| 0x118 | `std::set<hand, std::less<hand>, Ogre::STLAllocator<hand, Ogr` | `occupiers` |
| 0x140 | `TimeOfDay` | `timeOfDeath` |
| 0x148 | `float` | `p_TIME` |
| 0x150 | `NestBatcher*` | `nestBatcher` |
| 0x158 | `std::string` | `unexploredName` |
| 0x180 | `bool` | `discovered` |
| 0x181 | `bool` | `explored` |
| 0x182 | `bool` | `recentlyDiscovered` |
| 0x188 | `Ogre::Entity*` | `entityMarker` |
| 0x190 | `ScreenLabel*` | `entityLabel` |
| 0x198 | `PhysicsHullT*` | `clickHull` |
| 0x1A0 | `AreaBiomeGroup*` | `biome` |
| 0x1A8 | `TownAlarmState` | `alarmState` |
| 0x1AC | `bool` | `isActivated` |
| 0x1B0 | `ogre_unordered_set<ZoneMap*>::type` | `myZoneCoverage` |
| 0x1F0 | `ogre_unordered_map<ZoneMap*, bool>::type` | `populatedZones` |
| 0x230 | `Ogre::FastArray<ArtifactItemData>` | `artifacts` |
| 0x248 | `unsigned char` | `currentFloorVisibility` |
| 0x250 | `TownBuildingsManager` | `buildingsManager` |
| 0x300 | `lektor<ResidentData>` | `residentsSpawned` |
| 0x318 | `lektor<ResidentData>` | `residentsSpawned_BarsOrSomething` |
| 0x330 | `GameData*` | `defaultResident` |
| 0x338 | `GameData*` | `replacementTown` |
| 0x340 | `bool` | `isAccessible` |
| 0x348 | `AlarmManager*` | `alarms` |
| 0x350 | `InstanceID` | `instanceID` |
| 0x380 | `bool` | `openToPublic` |
| 0x384 | `float` | `minFoliageRange` |
| 0x388 | `int` | `playerTownLevel` |
| 0x390 | `ogre_unordered_set<hand>::type` | `gates` |
| 0x3D0 | `bool` | `playerHasBuildingsInThisTown` |
| 0x3D8 | `Ogre::FastArray<hand>` | `powerInList` |
| 0x3F0 | `ogre_unordered_set<hand>::type` | `powerOutList` |
| 0x430 | `ogre_unordered_set<hand>::type` | `batteryList` |
| 0x470 | `bool` | `batteryMode` |
| 0x474 | `float` | `power_Stat` |
| 0x478 | `float` | `maxPower_Stat` |
| 0x47C | `float` | `neededPowerTotal_Stat` |
| 0x480 | `float` | `batteryPowerTotal_Stat` |
| 0x484 | `float` | `batteryDrain_Stat` |
| 0x488 | `float` | `batteryChargingupTotal` |
| 0x48C | `float` | `batteryCharge_Stat` |
| 0x490 | `float` | `batteryChargeMax_Stat` |
| 0x498 | `TagsClass<BuildingDesignation>` | `_facilitesWeHaveHere` |
| 0x4A8 | `TradeCulture*` | `tradeCulture` |
| 0x4B0 | `ogre_unordered_map<GameData*, float>::type` | `tradeGoodsMults` |
| 0x4F0 | `GameData*` | `buildingMaterial` |
| 0x4F8 | `DistantTown*` | `distantTown` |
| 0x500 | `lektor<Town::NestSpot>` | `nestSpots` |
| 0x518 | `bool` | `nestsLoaded` |
| 0x51C | `float` | `overrideRange` |
| 0x520 | `float` | `townRangeMultiplier` |

## TradeCulture
*TradeCulture.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `lektor<GameData*>` | `forbiddenItems` |
| 0x18 | `std::set<GameData*, std::less<GameData*>, Ogre::STLAllocator` | `illegalBuildings` |
| 0x40 | `std::set<GameData*, std::less<GameData*>, Ogre::STLAllocator` | `happyBuildings` |
| 0x68 | `std::set<GameData*, std::less<GameData*>, Ogre::STLAllocator` | `illegalItems` |
| 0x90 | `std::map<GameData*, float, std::less<GameData*>, Ogre::STLAl` | `tradeGoodsMults` |

## TraderInventoryLayout : public InventoryLayout
*InventoryTraderGUI.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x88 | `int` | `sectionWidth` |
| 0x8C | `int` | `sectionHeight` |
| 0x3B8 | `MyGUI::ScrollView*` | `scrollBackpack` |

## TransformWindow : public Ogre::GeneralAllocatedObject
*TransformWindow.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `DatapanelGUI*` | `window` |
| 0x8 | `DataPanelLine_TextEditable*` | `windowXValue` |
| 0x10 | `DataPanelLine_TextEditable*` | `windowYValue` |
| 0x18 | `DataPanelLine_TextEditable*` | `windowZValue` |
| 0x20 | `DataPanelLine_Button*` | `modeButton` |
| 0x28 | `DataPanelLine_Button*` | `axisButton` |
| 0x30 | `DataPanelLine_Button*` | `revertButton` |
| 0x38 | `Ogre::SceneNode*` | `node` |
| 0x40 | `Ogre::SceneNode*` | `parentNode` |
| 0x48 | `Gizmo*` | `gizmo` |
| 0x50 | `int` | `mode` |
| 0x54 | `int` | `coordinateSystem` |
| 0x58 | `bool` | `hasScale` |
| 0x60 | `ZoneMap*` | `lastZone` |
| 0x68 | `ZoneMap*` | `currentZone` |
| 0x70 | `const InstanceID*` | `currentInstance` |
| 0x78 | `bool` | `changed` |
| 0x79 | `bool` | `editChanged` |
| 0x7C | `Ogre::Vector2` | `lastMouse` |

## TurretBuilding : public UseableStuff
*TurretBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x440 | `GunClassTurret*` | `gunClass` |
| 0x448 | `float` | `aimDistInDegrees` |
| 0x44C | `Ogre::Vector3` | `currentAimDir` |
| 0x458 | `Ogre::Vector3` | `rootAimDir` |
| 0x464 | `float` | `currentAimSpeed` |
| 0x468 | `Ogre::Vector3` | `currentAimTarget` |
| 0x478 | `hand` | `mountedBuilding` |
| 0x498 | `PhysicsCollection::RotatingEnt*` | `hingePart` |
| 0x4A0 | `PhysicsCollection::RotatingEnt*` | `gunPart` |
| 0x4A8 | `Ogre::Vector3` | `aimTargetPos` |
| 0x4B4 | `int` | `rotating` |

## TutorialSubItem : public Ogre::GeneralAllocatedObject
*TutorialGUI.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `std::string` | `description` |
| 0x8 | `unsigned int` | `id` |
| 0xC | `bool` | `started` |
| 0xD | `bool` | `locked` |
| 0x10 | `std::string` | `title` |
| 0x30 | `bool` | `skippeable` |
| 0x38 | `TutorialItem::State` | `state` |
| 0x3C | `unsigned char` | `subItemIndex` |
| 0x40 | `Ogre::FastArray<TutorialSubItem*>` | `subItems` |
| 0x58 | `Ogre::FastArray<std::string >` | `requiredTutorialsStr` |
| 0x70 | `Ogre::FastArray<TutorialItem*>` | `requiredTutorials` |
| 0xA0 | `MyGUI::Button*` | `nameButton` |
| 0xA8 | `MyGUI::Button*` | `closeButton` |
| 0xB0 | `MyGUI::Widget*` | `flashWidget` |
| 0xD0 | `TutorialGUI::HighlightItem` | `highlightItem` |
| 0xD0 | `TutorialItem*` | `currentItem` |
| 0xD8 | `MyGUI::Widget*` | `highlightItemWidget` |
| 0xD8 | `int` | `currentItemIndex` |
| 0xE0 | `MyGUI::Widget*` | `highlightPanel` |
| 0xE0 | `MyGUI::ListBox*` | `tutorialsList` |
| 0xE8 | `char` | `highlightDirection` |
| 0xE8 | `MyGUI::EditBox*` | `descriptionText` |
| 0xEC | `float` | `highlightAlpha` |
| 0xF0 | `MyGUI::Window*` | `window` |
| 0xF0 | `MyGUI::Button*` | `activateButton` |
| 0xF8 | `MyGUI::Button*` | `windowPrevButton` |
| 0xF8 | `MyGUI::Button*` | `prevButton` |
| 0x100 | `MyGUI::Button*` | `windowNextButton` |
| 0x100 | `MyGUI::Button*` | `nextButton` |
| 0x108 | `MyGUI::EditBox*` | `windowText` |
| 0x108 | `MyGUI::TextBox*` | `pagingText` |
| 0x110 | `MyGUI::Button*` | `dismissButton` |
| 0x118 | `MyGUI::TextBox*` | `pagingText` |
| 0x120 | `MyGUI::Widget*` | `tooltipsPanel` |
| 0x128 | `TutorialItem*` | `currentTutorialItem` |
| 0x130 | `Ogre::vector<TutorialGUI::TutorialGUILine*>::type` | `activeTutorialsList` |
| 0x150 | `ogre_unordered_map<TutorialItem*, TutorialGUI::TutorialGUILi` | `activeTutorials` |
| 0x190 | `bool` | `flashNewItem` |
| 0x191 | `bool` | `enabled` |

## WallBuilding : public Building
*WallBuilding.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x360 | `WallSectionLinkType` | `wallSectionLinkType` |
| 0x368 | `hand` | `shareBuildStateOfAnother` |
| 0x388 | `lektor<hand>` | `othersSharingMyBuildState` |

## WaterState
*Character.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `float` | `X` |
| 0x0 | `AkVector` | `Position` |
| 0x0 | `double` | `lastUpdated` |
| 0x0 | `lektor<Ogre::Entity*>` | `ents` |
| 0x0 | `bool` | `on` |
| 0x0 | `bool` | `on` |
| 0x1 | `bool` | `rag` |
| 0x2 | `bool` | `hull` |
| 0x4 | `float` | `Y` |
| 0x4 | `RagdollPart::Enum` | `part` |
| 0x8 | `float` | `Z` |
| 0x8 | `YesNoMaybe` | `seeState` |
| 0xC | `AkVector` | `Orientation` |
| 0xC | `float` | `progressOfMaybe` |
| 0x18 | `int` | `index` |
| 0xC0 | `float` | `offscreenFrameTime` |
| 0xC4 | `float` | `frameTIME` |
| 0xC8 | `float` | `frameTIMEfour` |
| 0xCC | `float` | `frameTIME_P` |
| 0xD0 | `float` | `bodyDecayTimer` |
| 0xD4 | `bool` | `stealthMode` |
| 0xD5 | `bool` | `_isOnARoof` |
| 0xD8 | `float` | `_lightLevel` |
| 0xDC | `bool` | `needsLightLevel` |
| 0xE0 | `ProneState` | `_currentProneState` |
| 0xE4 | `bool` | `isVisibleUpdateMode` |
| 0xE5 | `bool` | `setVisibleMsg` |
| 0xE8 | `YesNoMaybe` | `stealthUnseen` |
| 0xEC | `bool` | `playerWantsMeToGetUp` |
| 0xF0 | `BountyManager` | `crimes` |
| 0x198 | `StatsEnumerated` | `currentSkillUsing` |
| 0x1A0 | `StateBroadcastData*` | `stateBroadcast` |
| 0x1A8 | `bool` | `isVisibleAndNear` |
| 0x1A9 | `bool` | `isOnScreen` |
| 0x1B0 | `ogre_unordered_map<Character::DisguiseGUIFeedback, float>::t` | `disguiseGUIFeedbacks` |
| 0x1F0 | `ogre_unordered_map<hand, Character::WhoSeesMe>::type` | `whoSeesMeSneaking` |
| 0x230 | `Character::AttachedArrowManager` | `stealthMarkerArrows` |
| 0x250 | `bool` | `_isEngagedWithAPlayer` |
| 0x258 | `hand` | `isUsingTurret` |
| 0x278 | `bool` | `isCurrentlyGettingUp` |
| 0x279 | `unsigned char` | `isGettingEaten` |
| 0x280 | `Dialogue*` | `dialogue` |
| 0x288 | `std::string` | `currentStumblePainAnimation` |
| 0x2B0 | `bool` | `_isLiterallyUnderMeleeAttackRightNowForSure` |
| 0x2B8 | `CharacterMemory*` | `_myMemory` |
| 0x2C0 | `hand` | `lastGuyWhoDefeatedMe` |
| 0x2E0 | `RaceData*` | `myRace` |
| 0x2E8 | `Inventory*` | `inventory` |
| 0x2F0 | `RangedCombatClass*` | `rangedCombat` |
| 0x2F8 | `UseStuffState` | `inSomething` |
| 0x300 | `hand` | `inWhat` |
| 0x320 | `bool` | `isChained` |
| 0x328 | `hand` | `slaveOwner` |
| 0x348 | `bool` | `isCarryingSomething` |
| 0x350 | `std::string` | `carringObjectLeftOrRight` |
| 0x378 | `bool` | `isCarryingLeftSide` |
| 0x380 | `hand` | `carryingObject` |
| 0x3A0 | `Character::CharMessage` | `messages` |
| 0x3A8 | `hand` | `messageSubject` |
| 0x3C8 | `Ogre::Vector3` | `ragdollNavmeshPosition` |
| 0x3D4 | `bool` | `_isBeingCarried` |
| 0x3D8 | `WeaponCategory` | `lastUsedWeaponCategory` |
| 0x3E0 | `std::deque<Character::RagdollMsg, std::allocator<Character::` | `ragdollMessages` |
| 0x410 | `Character::CarryMsg*` | `msgCarryMode` |
| 0x418 | `int` | `squadMemberID` |
| 0x41C | `float` | `diplomacyMultiplier` |
| 0x420 | `hand` | `_destinationInsideBuilding` |
| 0x440 | `int` | `_destinationInsideWalls` |
| 0x448 | `AnimationClass*` | `animation` |
| 0x450 | `CharStats*` | `stats` |
| 0x458 | `MedicalSystem` | `medical` |
| 0x608 | `bool` | `isPhysicalMode` |
| 0x610 | `std::string` | `sex` |
| 0x638 | `CharacterNameTag*` | `nameTag` |
| 0x640 | `CharMovement*` | `movement` |
| 0x648 | `CharBody*` | `body` |
| 0x650 | `AI*` | `ai` |
| 0x658 | `ActivePlatoon*` | `platoon` |
| 0x660 | `short` | `portraitIndex` |
| 0x664 | `unsigned int` | `portraitSerial` |
| 0x668 | `unsigned __int64` | `audioObject` |
| 0x670 | `AkSoundPosition` | `audioData` |
| 0x688 | `GroundType` | `groundType` |
| 0x68C | `ArmourType` | `armourType` |
| 0x690 | `SoundEmitter*` | `audioEmitter` |
| 0x698 | `float` | `terrainHeightPosition` |
| 0x69C | `char` | `inDoorsSetCooldown` |
| 0x6A0 | `lektor<std::pair<WeatherAffecting, float> >` | `activeEffects` |
| 0x6B8 | `lektor<Effect*>` | `particleEffects` |
| 0x6D0 | `Sword*` | `naturalWeapon` |

## WorldEventStateQuery
*WorldEventStateQuery.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `ogre_unordered_map<GameData*, WorldStateEnum>::type` | `uniqueNPCsAre` |
| 0x0 | `ogre_unordered_map<WorldEventStateQuery*, bool>::type` | `statesList` |
| 0x40 | `ogre_unordered_map<GameData*, WorldStateEnum>::type` | `uniqueNPCsAreNot` |
| 0x80 | `ogre_unordered_map<GameData*, WorldStateEnum>::type` | `towns` |
| 0xC0 | `ogre_unordered_map<Faction*, bool>::type` | `isAllyOf` |
| 0x100 | `ogre_unordered_map<Faction*, bool>::type` | `isEnemyOf` |
| 0x140 | `bool` | `playerInvolvement` |

## YesNoMaybe
*YesNoMaybe.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `YesNoMaybe::ynm` | `key` |

## hand
*hand.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x8 | `itemType` | `type` |
| 0xC | `unsigned int` | `container` |
| 0x10 | `unsigned int` | `containerSerial` |
| 0x14 | `unsigned int` | `index` |
| 0x18 | `unsigned int` | `serial` |

## hkVector4fComparison
*Havok.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `union __m128` | `m_mask` |
| 0x0 | `char` | `m_bool` |
| 0x0 | `union __m128` | `m_quad` |
| 0x0 | `hkResultEnum` | `m_enum` |
| 0x0 | `__int64` | `m_allocated` |
| 0x0 | `T1*` | `m_data` |
| 0x8 | `__int64` | `m_inUse` |
| 0x8 | `int` | `m_size` |
| 0xC | `int` | `m_capacityAndFlags` |
| 0x10 | `__int64` | `m_peakInUse` |
| 0x18 | `__int64` | `m_available` |
| 0x20 | `__int64` | `m_totalAvailable` |
| 0x28 | `__int64` | `m_largestBlock` |

## iVector2
*iVector2.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `int` | `x` |
| 0x4 | `int` | `y` |

## physHit
*CharMovement.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `public:
    float` | `_defaultAltitudeFallback` |
| 0x0 | `ogre_unordered_set<hand>::type` | `members` |
| 0x0 | `bool` | `isPositionsFilter` |
| 0x0 | `hand` | `getOutOfTheWayOfCharacter` |
| 0x0 | `float` | `mWeightModifier` |
| 0x0 | `ogre_unordered_map<hand, float>::type` | `characterCollisions` |
| 0x0 | `public:
    Character*` | `me` |
| 0x4 | `bool` | `_traceWasAborted` |
| 0x4 | `int` | `edgeSkips` |
| 0x5 | `bool` | `_doNotAbort` |
| 0x6 | `bool` | `_needsGroup` |
| 0x7 | `bool` | `hit` |
| 0x8 | `Ogre::Vector3` | `position` |
| 0x8 | `int` | `maxLength` |
| 0x8 | `bool` | `officiallyStopped` |
| 0x8 | `std::deque<float, std::allocator<float> >` | `mHistoryBufferX` |
| 0x8 | `Ogre::Vector3` | `destination` |
| 0x10 | `std::deque<float, std::allocator<float> >` | `mHistoryBufferX` |
| 0x10 | `Ogre::SharedPtr<SpeedGroup>` | `speedGroup` |
| 0x14 | `Ogre::Vector3` | `normal` |
| 0x14 | `Ogre::Vector3` | `direction` |
| 0x20 | `float` | `distance` |
| 0x20 | `MoveSpeed` | `speedOrders` |
| 0x20 | `Ogre::Vector3` | `currentPosition` |
| 0x20 | `hand` | `movementTarget` |
| 0x24 | `bool` | `currentlyMoving` |
| 0x28 | `NxShape*` | `shape` |
| 0x28 | `MedianFilter2DVector` | `positionSmoother` |
| 0x30 | `hand` | `hitObject` |
| 0x30 | `Character*` | `me` |
| 0x38 | `CombatMovementController*` | `combatMover` |
| 0x40 | `Ogre::Vector3` | `position` |
| 0x40 | `CharMovement*` | `movement` |
| 0x40 | `int` | `currentFormationID` |
| 0x48 | `bool` | `chaseMode` |
| 0x4C | `Ogre::Vector3` | `direction` |
| 0x4C | `float` | `chaseStateTimer` |
| 0x50 | `unsigned short` | `_group` |
| 0x50 | `bool` | `hasForcedWP` |
| 0x54 | `Ogre::Vector3` | `forcedWP` |
| 0x58 | `RootObject*` | `_hitObjectUnsafePtr` |
| 0x58 | `float` | `speed` |
| 0x5C | `unsigned long` | `last` |
| 0x60 | `MotionFilter` | `flockFilterX` |
| 0x98 | `MotionFilter` | `flockFilterZ` |
| 0xA8 | `Ogre::Vector3` | `currentMotion` |
| 0xB4 | `float` | `maxSpeed` |
| 0xB8 | `float` | `currentSpeed` |
| 0xBC | `float` | `desiredSpeed` |
| 0xC0 | `float` | `walkSpeed` |
| 0xC4 | `Ogre::Vector3` | `pos` |
| 0xD0 | `Ogre::Vector3` | `direction` |
| 0xD0 | `FlockingTools*` | `flockingControl` |
| 0xD8 | `CharStats*` | `stats` |
| 0xDC | `Ogre::Vector3` | `destination` |
| 0xE0 | `float` | `radius` |
| 0xE4 | `bool` | `jogMode` |
| 0xE8 | `Ogre::Vector3` | `pathDestination` |
| 0xE8 | `float` | `TOTALREPULSION_DAMPING` |
| 0xEC | `float` | `STRAFE_STATE_DAMPING` |
| 0xF0 | `float` | `STRAFE_THRESHOLD` |
| 0xF4 | `float` | `FORWARD_THRESHOLD` |
| 0xF8 | `RoadFollower*` | `roadFollower` |
| 0xF8 | `float` | `MIN_RANGE_FW` |
| 0xFC | `float` | `ENEMY_DIST` |
| 0x100 | `float` | `roadWeight` |
| 0x100 | `float` | `ALLY_DIST` |
| 0x104 | `float` | `STOP_THRESHOLD` |
| 0x108 | `float` | `START_THRESHOLD` |
| 0x108 | `Ogre::Vector3` | `flockingVector` |
| 0x10C | `float` | `ACCEL_RATE_COMBATMODE` |
| 0x110 | `float` | `meiMin` |
| 0x114 | `float` | `circlingSpeed` |
| 0x118 | `float` | `combatMinDistance` |
| 0x118 | `CombatMovementController` | `combatMover` |
| 0x11C | `float` | `combatMaxDistance` |
| 0x120 | `float` | `strafeStateTimer` |
| 0x124 | `bool` | `strafing` |
| 0x125 | `bool` | `powerThrough` |
| 0x126 | `bool` | `canStrafe` |
| 0x128 | `float` | `speedLimit` |
| 0x12C | `float` | `currentAccelSpeed` |
| 0x130 | `hand` | `lookAtCharacter` |
| 0x150 | `hand` | `combatTarget` |
| 0x288 | `FormationMover` | `combatMover2` |
| 0x2D0 | `FlockingTools` | `flockingTools` |
| 0x310 | `Formation*` | `formation` |
| 0x318 | `Formation*` | `enemyFormation` |
| 0x320 | `HavokCharacter*` | `havokCharacter` |
| 0x328 | `ConstantTracerT*` | `tracer` |
| 0x330 | `bool` | `dontEverRecreateMe` |
| 0x334 | `int` | `floorGroup` |
| 0x338 | `hand` | `building` |
| 0x358 | `bool` | `initCheck` |
| 0x35C | `float` | `_combatMoveSpeedMult` |
| 0x360 | `bool` | `destinationLoaded` |
| 0x364 | `float` | `footprintRadius` |
| 0x368 | `int` | `edgeTarget` |
| 0x36C | `float` | `_lastOffMeshCheck` |
| 0x370 | `bool` | `movingToEdge` |
| 0x374 | `float` | `lastStepTime` |
| 0x378 | `MovementMode` | `movementMode` |
| 0x37C | `bool` | `animationOverride` |
| 0x380 | `Ogre::Vector3` | `trackingAnimRelocationVector` |
| 0x38C | `Ogre::Vector3` | `desiredMotion` |
| 0x398 | `float` | `moveLimit` |
| 0x3A0 | `AnimationClass*` | `animation` |
| 0x3A8 | `Character*` | `character` |
| 0x3B0 | `PhysicsHullT*` | `clickHull` |

## rendHit
*UtilityT.h*

| Offset | Type | Field |
|--------|------|-------|
| 0x0 | `int` | `data` |
| 0x0 | `__int64` | `freq` |
| 0x0 | `Ogre::Matrix4` | `cachedViewMatrix` |
| 0x4 | `Ogre::Vector3` | `hit` |
| 0x8 | `__int64` | `ctr1` |
| 0x10 | `__int64` | `ctr2` |
| 0x40 | `TimerClass` | `timer` |
| 0x58 | `Ogre::Entity*` | `marker` |

