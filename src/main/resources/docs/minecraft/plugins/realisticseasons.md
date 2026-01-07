# RealisticSeasons-11.10.1 API Reference

## Package: me.casperge.enums

### Class: me.casperge.enums.ArmorStandPart
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- HEAD
- BODY
- LEFT_ARM
- RIGHT_ARM
- LEFT_LEG
- RIGHT_LEG

Methods:
- **static** ArmorStandPart valueOf(String)
- **static** ArmorStandPart[] values()

### Class: me.casperge.enums.GameRuleType
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- SNOW_ACCUMULATION_HEIGHT
- PLAYER_SLEEPING_PERCENTAGE
- DO_MOB_SPAWNING
- DO_DAYLIGHT_CYCLE

Methods:
- **static** GameRuleType valueOf(String)
- **static** GameRuleType[] values()

### Class: me.casperge.enums.GrassType
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- NORMAL
- SWAMP
- DARK_FOREST

Methods:
- **static** GrassType valueOf(String)
- **static** GrassType[] values()

## Package: me.casperge.interfaces

### Class: me.casperge.interfaces.CustomBiome
Type: Interface

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.interfaces.FakeArmorStand
Type: Interface

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.interfaces.GameRuleGetter
Type: Interface

Methods:
- void SetIntegerGameRule(GameRuleType, World, Integer)
- Integer GetIntegerGameRule(GameRuleType, World)
- void SetBooleanGameRule(GameRuleType, World, Boolean)
- Boolean GetBooleanGameRule(GameRuleType, World)

### Class: me.casperge.interfaces.NmsCode
Type: Interface

Methods:
- void sendGameStateChangePacket(int, float, Player)
- float getBiomeTemperature(String)
- List<String> getBiomes(String)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(String)
- int getBiomeID(Biome)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String) throws ClassNotFoundException
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- String getBiomeName(Biome)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- int[] getBiomeColors(String)
- void refreshChunk(Player, Chunk)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.interfaces.ProtocolLibUtils
Type: Interface

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)

## Package: me.casperge.realisticseasons

### Class: me.casperge.realisticseasons.RealisticSeasons
Type: Class
Extends: org.bukkit.plugin.java.JavaPlugin

Methods:
- boolean hasSeasons(int, int, World)
- void addRunnable(BukkitRunnable)
- void createDump(UUID, String)
- boolean supportsCustomBiomes(Player)
- void createConsoleDump(String)
- LanguageManager getLangManager()
- NmsCode getNMSUtils()
- void enable()
- **static** CustomBiome createCustomBiome(String, String, String)
- List<LandPlugin> getLandPluginAPIs()
- String setPlaceHolders(String, Player)
- SeasonCycle getSeasonCycle()
- void setLoadedTime(ZonedDateTime)
- BiomeRegister getBiomeRegister()
- boolean hasBlockChanges(int, int, World)
- AnimalUtils getAnimalUtils()
- ParticleManager getParticleManager()
- boolean isPaper()
- List<String> getActiveAsyncTasks()
- ZonedDateTime getLoadedTime()
- ChunkDataHandler getAsyncChunkHandler()
- Settings getSettings()
- boolean loadConfig()
- GameRuleGetter getGameRuleGetter()
- void updatemapplugins(Season, SubSeason, World)
- void onEnable()
- DataHandler getDataReader()
- void onDisable()
- TemperatureManager getTemperatureManager()
- ActionbarListener getActionbarListener()
- FileConfiguration getRSConfig()
- void reload()
- void loadLandPlugins()
- int createSeasonsBiome(String, String, String, String, String, String, String, String, boolean)
- boolean hasMobSpawns(int, int, World)
- BlockStorage getBlockStorage()
- boolean hasLandPlugin()
- CropSettings getCropSettings()
- void addSeasonBiomeForAPI(String, SeasonBiome)
- HashMap<String, SeasonBiome> getSeasonBiomesForAPI()
- LitterGeneration getLitterGeneration()
- void loadPAPI()
- SeasonManager getSeasonManager()
- JavaPlugin getPlugin()
- EventManager getEventManager()
- TimeManager getTimeManager()
- BlockUtils getBlockUtils()
- void onLoad()
- **static** RealisticSeasons getInstance()
- ChunkUtils getChunkUtils()

### Class: me.casperge.realisticseasons.Version
Type: Class

Methods:
- **static** int getSnowID()
- **static** int getIceID()
- **static** boolean is_1_21_9_or_up()
- **static** boolean is_1_19_or_up()
- **static** void setupChunkPacketEvent(RealisticSeasons)
- **static** boolean is_1_21_5_or_up()
- **static** boolean is_1_21_2_or_up()
- **static** boolean is_1_20_or_up()
- **static** String craftBukkitVersionFromMinecraftRelease(String)
- **static** boolean is_1_19_3_or_up()
- **static** boolean is_1_19_4_or_up()
- **static** int getWaterID()
- **static** NmsCode setupBiomeRegister()
- **static** GameRuleGetter setupGameRuleGetter()
- **static** FakeArmorStand createFakeArmorStand(World, double, double, double, double, boolean, boolean, boolean, boolean)
- **static** boolean is_1_17_or_up()
- **static** CustomBiome createCustomBiome(String, String, String)
- **static** boolean is_1_21_4_or_up()
- **static** boolean is_1_21_11_or_up()

## Package: me.casperge.realisticseasons.api

### Class: me.casperge.realisticseasons.api.TemperatureEffect
Type: Interface

Methods:
- void cancel()
- int getModifier()

### Class: me.casperge.realisticseasons.api.CustomBiomeFileLoader
Type: Class

Methods:
- **static** List<CustomWorldGenerator> getActiveGenerators()
- **static** void writeFiles(CustomWorldGenerator)
- **static** List<CustomWorldGenerator> getAlreadyInstalledGenerators()

### Class: me.casperge.realisticseasons.api.CustomWorldGenerator
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- TERRALITH_2

Methods:
- **static** boolean isKnownBiome(String)
- **static** boolean isWorldGenerator(String)
- String getResourceFolderName()
- **static** CustomWorldGenerator valueOf(String)
- **static** List<String> getAllGenerators()
- **static** CustomWorldGenerator fromBiome(String)
- String getDetectionBiome()
- **static** CustomWorldGenerator[] values()
- String toString()
- **static** CustomWorldGenerator fromFile(String)

### Class: me.casperge.realisticseasons.api.MMobs
Type: Class
Implements: org.bukkit.event.Listener

Constructors:
- MMobs(RealisticSeasons main)

Methods:
- void onMythicConditionLoad(MythicConditionLoadEvent)

### Class: me.casperge.realisticseasons.api.PAPI
Type: Class
Extends: me.clip.placeholderapi.expansion.PlaceholderExpansion

Constructors:
- PAPI(RealisticSeasons main)

Methods:
- String getVersion()
- boolean canRegister()
- String onRequest(OfflinePlayer, String)
- String getAuthor()
- String getIdentifier()
- boolean persist()
- String setPlaceHolders(Player, String)

### Class: me.casperge.realisticseasons.api.SeasonBiome
Type: Class

Constructors:
- SeasonBiome(Season season, String originalBiome, String fogColor, String waterColor, String waterFogColor, String skyColor, String grassColor, String[] foliageColor)

Methods:
- String[] getFoliageColorsHex()
- String getFogColorHex()
- String getWaterColoHex()
- Season getSeason()
- String getOriginalBiome()
- String getWaterFogColorHex()
- String getGrassColorHex()
- String getSkyColorHex()

### Class: me.casperge.realisticseasons.api.SeasonChangeEvent
Type: Class
Extends: org.bukkit.event.Event
Implements: org.bukkit.event.Cancellable

Constructors:
- SeasonChangeEvent(World world, Season newSeason, Season oldSeason)

Methods:
- Season getOldSeason()
- World getWorld()
- boolean isCancelled()
- HandlerList getHandlers()
- void setCancelled(boolean)
- **static** HandlerList getHandlerList()
- Season getNewSeason()

### Class: me.casperge.realisticseasons.api.SeasonCondition
Type: Class
Implements: io.lumine.mythic.api.skills.conditions.IEntityCondition

Constructors:
- SeasonCondition(MythicLineConfig seasons, RealisticSeasons main)

Methods:
- boolean check(AbstractEntity)

### Class: me.casperge.realisticseasons.api.SeasonEventEnd
Type: Class
Extends: org.bukkit.event.Event

Constructors:
- SeasonEventEnd(World world, SeasonCustomEvent e)

Methods:
- World getWorld()
- SeasonCustomEvent getCustomEvent()
- HandlerList getHandlers()
- **static** HandlerList getHandlerList()

### Class: me.casperge.realisticseasons.api.SeasonEventStart
Type: Class
Extends: org.bukkit.event.Event
Implements: org.bukkit.event.Cancellable

Constructors:
- SeasonEventStart(World world, SeasonCustomEvent e)

Methods:
- World getWorld()
- boolean isCancelled()
- SeasonCustomEvent getCustomEvent()
- HandlerList getHandlers()
- void setCancelled(boolean)
- **static** HandlerList getHandlerList()

### Class: me.casperge.realisticseasons.api.SeasonParticle
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- FIREFLY
- SHOOTING_STAR
- FALLING_LEAF
- SMALL_FALLING_LEAF
- COLD_BREATH

Methods:
- **static** SeasonParticle valueOf(String)
- **static** SeasonParticle[] values()

### Class: me.casperge.realisticseasons.api.SeasonParticleStartEvent
Type: Class
Extends: org.bukkit.event.Event
Implements: org.bukkit.event.Cancellable

Constructors:
- SeasonParticleStartEvent(Location loc, Player p, SeasonParticle particle)

Methods:
- Location getLocation()
- Player getPlayer()
- boolean isCancelled()
- SeasonParticle getParticleType()
- HandlerList getHandlers()
- void setCancelled(boolean)
- **static** HandlerList getHandlerList()

### Class: me.casperge.realisticseasons.api.SeasonsAPI
Type: Class

Constructors:
- SeasonsAPI(RealisticSeasons main)

Methods:
- void setSeason(World, Season)
- Season getSeason(World)
- List<String> getActiveEvents(World)
- int getMinutes(World)
- SeasonBiome getReplacementSeasonBiome(Biome, Season)
- SeasonBiome getReplacementSeasonBiome(String, Season)
- SeasonBiome getReplacementSeasonBiome(Location, Season)
- int getAirTemperature(Location)
- int getHours(World)
- int getSeconds(World)
- String getDayOfWeek(World)
- void applyTimedTemperatureEffect(Player, int, int)
- String getCurrentMonthName(World)
- TemperatureEffect applyPermanentTemperatureEffect(Player, int)
- void setDate(World, Date)
- Date getDate(World)
- **static** SeasonsAPI getInstance()
- int getTemperature(Player)

## Package: me.casperge.realisticseasons.api.landplugins

### Class: me.casperge.realisticseasons.api.landplugins.LandPlugin
Type: Interface

Methods:
- Integer getTemperatureModifier(int, int, World)
- boolean hasSeasonEffects(int, int, World)
- boolean hasBlockChanges(int, int, World)
- Integer getPermanentTemperature(int, int, World)
- Priority getPriority()
- boolean hasMobSpawns(int, int, World)
- Season getPermanentSeason(int, int, World)

### Class: me.casperge.realisticseasons.api.landplugins.Factions
Type: Class
Implements: me.casperge.realisticseasons.api.landplugins.LandPlugin

Constructors:
- Factions(RealisticSeasons main)

Methods:
- Integer getTemperatureModifier(int, int, World)
- boolean hasSeasonEffects(int, int, World)
- boolean hasBlockChanges(int, int, World)
- Integer getPermanentTemperature(int, int, World)
- Priority getPriority()
- boolean hasMobSpawns(int, int, World)
- Season getPermanentSeason(int, int, World)

### Class: me.casperge.realisticseasons.api.landplugins.GriefPrevention
Type: Class
Implements: me.casperge.realisticseasons.api.landplugins.LandPlugin

Constructors:
- GriefPrevention(RealisticSeasons main)

Methods:
- Integer getTemperatureModifier(int, int, World)
- boolean hasSeasonEffects(int, int, World)
- boolean hasBlockChanges(int, int, World)
- Integer getPermanentTemperature(int, int, World)
- Priority getPriority()
- boolean hasMobSpawns(int, int, World)
- Season getPermanentSeason(int, int, World)

### Class: me.casperge.realisticseasons.api.landplugins.Lands
Type: Class
Implements: me.casperge.realisticseasons.api.landplugins.LandPlugin

Constructors:
- Lands(RealisticSeasons main)

Methods:
- Integer getTemperatureModifier(int, int, World)
- boolean hasSeasonEffects(int, int, World)
- boolean hasBlockChanges(int, int, World)
- Integer getPermanentTemperature(int, int, World)
- Priority getPriority()
- boolean hasMobSpawns(int, int, World)
- Season getPermanentSeason(int, int, World)

### Class: me.casperge.realisticseasons.api.landplugins.Priority
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- LOWEST
- LOW
- MEDIUM
- HIGH
- HIGHEST

Methods:
- boolean isHigherThan(Priority)
- int intValue()
- **static** Priority valueOf(String)
- **static** Priority[] values()

### Class: me.casperge.realisticseasons.api.landplugins.WGSeason
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- SUMMER
- WINTER
- FALL
- SPRING

Methods:
- **static** WGSeason valueOf(String)
- **static** WGSeason[] values()
- **static** Season getRSSeason(WGSeason)

### Class: me.casperge.realisticseasons.api.landplugins.WGuard
Type: Class
Implements: me.casperge.realisticseasons.api.landplugins.LandPlugin

Constructors:
- WGuard(RealisticSeasons main)

Methods:
- Integer getTemperatureModifier(int, int, World)
- boolean hasSeasonEffects(int, int, World)
- boolean hasBlockChanges(int, int, World)
- Integer getPermanentTemperature(int, int, World)
- Priority getPriority()
- boolean hasMobSpawns(int, int, World)
- Season getPermanentSeason(int, int, World)

## Package: me.casperge.realisticseasons.api.maps

### Class: me.casperge.realisticseasons.api.maps.MapPlugin
Type: Interface

Methods:
- boolean isFullRenderPause(World)
- void setFullRenderPause(boolean, World)

### Class: me.casperge.realisticseasons.api.maps.BMap
Type: Class
Implements: me.casperge.realisticseasons.api.maps.MapPlugin

Constructors:
- BMap(RealisticSeasons main)

Methods:
- boolean isFullRenderPause(World)
- void setFullRenderPause(boolean, World)

### Class: me.casperge.realisticseasons.api.maps.DMap
Type: Class
Implements: me.casperge.realisticseasons.api.maps.MapPlugin

Constructors:
- DMap(RealisticSeasons dynmapAPI)

Methods:
- boolean isFullRenderPause(World)
- void setFullRenderPause(boolean, World)

## Package: me.casperge.realisticseasons.biome

### Class: me.casperge.realisticseasons.biome.BiomeRegister
Type: Class

Methods:
- **static** void setBiomeOverride(int)
- **static** int getSummerReplacement(int)
- **static** void update1_18BlockParticleColor()
- **static** int getMixWinterReplacement(int, int)
- **static** List<Integer> getFallReplacements(int)
- **static** boolean isBiomeOverride()
- **static** int getMixSpringReplacement(int, int)
- **static** void disableBiomeOverride()
- **static** int getMixSummerReplacement(int, int)
- **static** int getWinterReplacement(int)
- **static** int getMixFallReplacement(int, int)
- **static** int getSpringReplacement(int)

### Class: me.casperge.realisticseasons.biome.BiomeUtils
Type: Class

Methods:
- **static** int getSeasonsTemperature(float)
- **static** int[] updateBiomes(int[], int, int, int, int)
- **static** int getDefaultBiomeTemperature(String)

### Class: me.casperge.realisticseasons.biome.BlockReplacement
Type: Class

Constructors:
- BlockReplacement(List<Integer> seasons, List<Integer> phases, Material original, Material replacent)

Methods:
- List<Integer> getPhases()
- List<Integer> getSeasons()
- Material getOriginal()
- Material getReplacent()

### Class: me.casperge.realisticseasons.biome.BlockReplacements
Type: Class

Methods:
- **static** void addBlockReplacement(BlockReplacement)

### Class: me.casperge.realisticseasons.biome.HeightAccessor
Type: Class

Methods:
- void add(Integer, Integer)
- Integer getSectionYFromSectionIndex(Integer)

## Package: me.casperge.realisticseasons.blockscanner

### Class: me.casperge.realisticseasons.blockscanner.BlockEffect
Type: Class

Constructors:
- BlockEffect(int range, int modifier)

Methods:
- int getRange()
- int getModifier()

### Class: me.casperge.realisticseasons.blockscanner.BlockProcessor
Type: Class

Constructors:
- BlockProcessor(RealisticSeasons main)

Methods:
- V process(HashMap<UUID, ChunkSystem>, HashMap<UUID, SimpleLocation>)
- boolean hasLineOfSight(SimpleLocation, BlockProcessor$SimpleBlock, ChunkSystem, double)
- V handleParticleResults(HashMap<UUID, List<SimpleLocation>>)
- V handleTemperatureResult(HashMap<UUID, Integer>)
- boolean isProcessing()
- boolean hasAnyLineOfSight(SimpleLocation, BlockProcessor$SimpleBlock, ChunkSystem, double)
- **static** double distanceTo(int, int, int, int, int, int)

### Class: me.casperge.realisticseasons.blockscanner.ChunkSupplier
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- ChunkSupplier(RealisticSeasons main)

Methods:
- void run()

### Class: me.casperge.realisticseasons.blockscanner.ChunkSystem
Type: Class

Constructors:
- ChunkSystem(Chunk worldName, int range, int minY, int maxY)

Methods:
- String getWorld()
- boolean isNether()
- Material getBlockType(int, int, int)

### Class: me.casperge.realisticseasons.blockscanner.SimpleLocation
Type: Class

Constructors:
- SimpleLocation(Location x, int maxY, int minY)
- SimpleLocation(int x, int y, int z, String worldName)

Methods:
- String getWorldName()
- int getX()
- int getY()
- int getZ()
- int hashCode()
- boolean equals(Object)
- int getMaxY()
- int getMinY()

## Package: me.casperge.realisticseasons.blockscanner.blocksaver

### Class: me.casperge.realisticseasons.blockscanner.blocksaver.BlockStorage
Type: Class

Constructors:
- BlockStorage(RealisticSeasons main)

Methods:
- void load(ConfigurationSection, StoredBlockType)
- void logBreak(Location, StoredBlockType)
- void logPlacement(Location, StoredBlockType)
- void save(YamlConfiguration)
- List<SimpleLocation> getEggs(Chunk)
- boolean isStored(Location, StoredBlockType)
- List<SimpleLocation> getPresents(Chunk)

### Class: me.casperge.realisticseasons.blockscanner.blocksaver.StoredBlockType
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- FLOWER
- PRESENT
- EGG

Methods:
- **static** StoredBlockType valueOf(String)
- **static** StoredBlockType[] values()

## Package: me.casperge.realisticseasons.calendar

### Class: me.casperge.realisticseasons.calendar.Calendar
Type: Class

Constructors:
- Calendar(Week week, Year year, Date winterstart, Date springstart, Date summerstart, Date fallstart)

Methods:
- int getTotalDaysPassedThisYear(Date)
- int getTotalMonths()
- int getTotalDays(Date)
- Season getSeason(Date)
- int getDaysUntil(Date, Date)
- Date getSeasonStart(Season)
- Month getMonth(int)
- int weekDayFromString(String)
- int getWeekDayAsInt(Date)
- Date getNextDate(Date)
- String getWeekDay(int)
- String getWeekDay(Date)

### Class: me.casperge.realisticseasons.calendar.Date
Type: Class

Constructors:
- Date(int day, int month, int year)
- Date(int day, int month)

Methods:
- int getYear()
- boolean isLaterInYear(Date)
- String toString(boolean)
- String toString()
- **static** Date fromString(String, boolean)
- int getMonth()
- int getDay()

### Class: me.casperge.realisticseasons.calendar.DayChangeEvent
Type: Class
Extends: org.bukkit.event.Event

Constructors:
- DayChangeEvent(World w, Date from, Date to)

Methods:
- World getWorld()
- HandlerList getHandlers()
- **static** HandlerList getHandlerList()
- Date getTo()
- Date getFrom()

### Class: me.casperge.realisticseasons.calendar.DayChangeHandler
Type: Class
Implements: org.bukkit.event.Listener

Constructors:
- DayChangeHandler(RealisticSeasons main)

Methods:
- void dayChange(DayChangeEvent)

### Class: me.casperge.realisticseasons.calendar.DayTime
Type: Class

Constructors:
- DayTime(int dayLength, int nightLength)

Methods:
- List<Integer> getDayArray()
- int getDayLength()
- **static** List<Integer> getCorrectListBelow10(int)
- **static** List<Integer> generateIntList(int)
- List<Integer> getNightArray()
- int getNightLength()

### Class: me.casperge.realisticseasons.calendar.Month
Type: Class

Constructors:
- Month(String name, int length, int, int daytime)

Methods:
- int getDayLength()
- List<Integer> getDayArray()
- String getName()
- int getLength()
- List<Integer> getNightArray()
- double getNightLengthMultiplier()
- int getNightLength()
- double getDayLengthMultiplier()

### Class: me.casperge.realisticseasons.calendar.Time
Type: Class

Methods:
- **static** Long getTimeModified(World, double, double)
- **static** int getHours(World, double, double)
- **static** int getFullSeconds(World, double, double)
- **static** int getSeconds(World, double, double)
- **static** int getMinutes(World, double, double)

### Class: me.casperge.realisticseasons.calendar.TimeManager
Type: Class

Constructors:
- TimeManager(RealisticSeasons main)

Methods:
- Date currentDateFromCalendar()
- WeakHashMap<World, Date> getDates()
- SubSeason getCorrectSubSeason(World)
- ZonedDateTime getCurrentZonedDateTime()
- List<World> getPausedWorlds()
- boolean hasTime(World)
- Calendar getCalendar()
- int getWeekDayAsInt(Date, boolean)
- int getMinutes(World)
- String getTimeAsString(World)
- void resumeTime(World)
- Date getHalfwaySeason(Season)
- int getHours(World)
- int getSeconds(World)
- void pauseTime(World)
- void load()
- int getDaysUntilNextSeason(World)
- double getSeasonProgressPercentage(Date, Long)
- int getTotalDays(Season)
- void setDate(World, Date)
- Date getDate(World)
- V addToDatesRegister(HashMap<World, Date>)
- void nextDay(World)
- String getWeekDay(Date)

### Class: me.casperge.realisticseasons.calendar.Week
Type: Class

Constructors:
- Week(List<String> weekdays)

Methods:
- String getNextWeekDay(String)
- List<String> getWeekDays()
- int weekDayFromString(String)
- String getWeekDay(int)

### Class: me.casperge.realisticseasons.calendar.Year
Type: Class

Constructors:
- Year(List<Month> months)

Methods:
- Month getMonth(int)
- Month getMonth(String)
- Month getNextMonth(Month)
- List<Month> getMonths()

## Package: me.casperge.realisticseasons.commands

### Class: me.casperge.realisticseasons.commands.BiomeCommand
Type: Class
Implements: org.bukkit.command.CommandExecutor

Constructors:
- BiomeCommand(RealisticSeasons main)

Methods:
- boolean onCommand(CommandSender, Command, String, String[])

### Class: me.casperge.realisticseasons.commands.DumpCommand
Type: Class
Implements: org.bukkit.command.CommandExecutor

Constructors:
- DumpCommand(RealisticSeasons main)

Methods:
- boolean onCommand(CommandSender, Command, String, String[])

### Class: me.casperge.realisticseasons.commands.RealisticSeasonsCommand
Type: Class
Implements: org.bukkit.command.CommandExecutor

Constructors:
- RealisticSeasonsCommand(RealisticSeasons main)

Methods:
- boolean hasSeasons(Player)
- void setByPlayer(Player, World, String[])
- void reload()
- boolean setSeason(Season, World)
- boolean disable(World)
- boolean onCommand(CommandSender, Command, String, String[])
- void displayHelp(Player)
- void getinfo(Player)
- boolean nextSeason(World)
- void displayConsoleHelp()

### Class: me.casperge.realisticseasons.commands.RealisticSeasonsTabCompl
Type: Class
Implements: org.bukkit.command.TabCompleter

Constructors:
- RealisticSeasonsTabCompl(RealisticSeasons main)

Methods:
- List<String> onTabComplete(CommandSender, Command, String, String)

### Class: me.casperge.realisticseasons.commands.SeasonCommand
Type: Class
Implements: org.bukkit.command.CommandExecutor

Constructors:
- SeasonCommand(RealisticSeasons main)

Methods:
- boolean onCommand(CommandSender, Command, String, String[])

### Class: me.casperge.realisticseasons.commands.ToggleFahrenheitCommand
Type: Class
Implements: org.bukkit.command.CommandExecutor

Constructors:
- ToggleFahrenheitCommand(RealisticSeasons main)

Methods:
- boolean onCommand(CommandSender, Command, String, String[])

### Class: me.casperge.realisticseasons.commands.ToggleParticleCommand
Type: Class
Implements: org.bukkit.command.CommandExecutor

Constructors:
- ToggleParticleCommand(RealisticSeasons main)

Methods:
- boolean onCommand(CommandSender, Command, String, String[])

### Class: me.casperge.realisticseasons.commands.ToggleSeasonsCommand
Type: Class
Implements: org.bukkit.command.CommandExecutor

Constructors:
- ToggleSeasonsCommand(RealisticSeasons main)

Methods:
- boolean onCommand(CommandSender, Command, String, String[])

### Class: me.casperge.realisticseasons.commands.ToggleTemperatureCommand
Type: Class
Implements: org.bukkit.command.CommandExecutor

Constructors:
- ToggleTemperatureCommand(RealisticSeasons main)

Methods:
- boolean onCommand(CommandSender, Command, String, String[])

## Package: me.casperge.realisticseasons.crop

### Class: me.casperge.realisticseasons.crop.CropFileLoader
Type: Class

Constructors:
- CropFileLoader(RealisticSeasons conf)

Methods:
- CropSettings getCropSettings()

### Class: me.casperge.realisticseasons.crop.CropGrowEvent
Type: Class
Implements: org.bukkit.event.Listener

Constructors:
- CropGrowEvent(RealisticSeasons main)

Methods:
- void onSpread(BlockSpreadEvent)
- void onGrow(BlockGrowEvent)

### Class: me.casperge.realisticseasons.crop.CropSettings
Type: Class

Constructors:
- CropSettings(YamlConfiguration enabled)

Methods:
- int getMinLightLevel(Material, Season)
- double getOutdoorSpeed(Material, Season)
- boolean isEnabled()
- double getIndoorSpeed(Material, Season)
- boolean requiresBlockLight(Material, Season)

## Package: me.casperge.realisticseasons.data

### Class: me.casperge.realisticseasons.data.BiomeFileLoader
Type: Class

Constructors:
- BiomeFileLoader(RealisticSeasons main)

Methods:
- void load()
- void checkDataFolder()
- void registerMixedColorBiomes()
- void loadFile(CustomBiomeData, boolean, boolean)
- boolean isCustomBiomeFile(File)
- CustomBiomeData fromFile(String, boolean, boolean)

### Class: me.casperge.realisticseasons.data.CalendarFileLoader
Type: Class

Constructors:
- CalendarFileLoader(RealisticSeasons main)

Methods:
- Calendar load()
- int getMonthFromString(String)
- Date dateFromString(String)
- I getMonthIndex(List<Month>, Month)

### Class: me.casperge.realisticseasons.data.CustomBiomeData
Type: Class

Methods:
- int getTemperatureModifier()
- void addSeasonColorData(Season, CustomBiomeData$SeasonColorData)
- boolean getFreezeInWinter()
- void setBiomeRegName(String)
- void setDoSnow(Season, boolean)
- void setS(String)
- boolean isSnow(Season)
- void setRelatedConf(String)
- void setOriginalBiomeName(String)
- void setFreezeInWinter(boolean)
- String getBiomeRegName()
- HashMap<Season, Integer> getBiomeWaterTemps()
- String getOriginalBiomeName()
- String getS()
- CustomBiomeData$SeasonColorData getSeasonColorData(Season)
- void setTemperatureModifier(int)
- void setModifyPlants(boolean)
- boolean getModifyPlants()
- void setBiomeWaterTemperatures(Season, int)
- String getRelatedConf()

### Class: me.casperge.realisticseasons.data.CustomBiomeData$SeasonColorData
Type: Class

Constructors:
- CustomBiomeData$SeasonColorData(CustomBiomeData this$0)

Methods:
- void setFogColor(String)
- String getSkyColor()
- void setGrassColor(String)
- void setWaterFogColor(String)
- String getGrassColor()
- String getFogColor()
- void setSkyColor(String)
- String getTreeColor()
- String getWaterFogColor()
- String getWaterColor()
- void setTreeColor(String)
- void setWaterColor(String)

### Class: me.casperge.realisticseasons.data.DataHandler
Type: Class

Constructors:
- DataHandler(RealisticSeasons dataFile)

Methods:
- void load()
- void save()

### Class: me.casperge.realisticseasons.data.LanguageManager
Type: Class

Constructors:
- LanguageManager(RealisticSeasons main)

Methods:
- void copyDefaults()
- void reload()

### Class: me.casperge.realisticseasons.data.MessageType
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- SEASON_TO_WINTER
- SEASON_TO_FALL
- SEASON_TO_SPRING
- SEASON_TO_SUMMER
- NO_PERMISSION
- WINTER_DISPLAY
- SUMMER_DISPLAY
- FALL_DISPLAY
- SPRING_DISPLAY
- SEASONSCOMMAND_DISABLED
- SEASONSCOMMAND_RESTORE
- SEASONSCOMMAND_CURRENTSEASON
- SEASONSCOMMAND_CURRENTDATE
- SEASONSCOMMAND_DAYSUNTILNEXT
- SEASONSCOMMAND_DAYSUNTILNEXTEVENT
- SEASONSCOMMAND_TIME
- TOGGLESEASONCOMMAND_MESSAGE
- SEASONSCOMMAND_EVENTS
- ENABLED
- DISABLED
- TOGGLETEMPERATURECOMMAND
- TOGGLEPARTICLESCOMMAND
- SEASONSCOMMAND_AIRTEMPERATURE
- FAHRENHEITCOMMAND_TOFAHRENHEIT
- FAHRENHEITCOMMAND_TOCELCIUS
- CURRENTBIOME_MESSAGE

Methods:
- **static** MessageType getMessageType(String)
- **static** MessageType valueOf(String)
- **static** MessageType[] values()

### Class: me.casperge.realisticseasons.data.Settings
Type: Class

Constructors:
- Settings(RealisticSeasons main, boolean)

Methods:
- void reload()
- void load(boolean)
- void addSyncedWorld(String)

### Class: me.casperge.realisticseasons.data.Settings$WeatherSettings
Type: Class

Constructors:
- Settings$WeatherSettings(Settings this$0, double downfall, boolean rain)

Methods:
- boolean hasRain()
- double getDownfallChance()

## Package: me.casperge.realisticseasons.data.chunksaver

### Class: me.casperge.realisticseasons.data.chunksaver.AsyncDataSaver
Type: Class

Constructors:
- AsyncDataSaver(RealisticSeasons dataFile)

Methods:
- void deleteChunk(SeasonChunk)
- SeasonChunk getRandomChunk(String)
- void saveChunk(SeasonChunk)
- void tick()
- Set<String> getWorlds()

### Class: me.casperge.realisticseasons.data.chunksaver.ChunkDataHandler
Type: Class

Constructors:
- ChunkDataHandler(RealisticSeasons main)

Methods:
- void remove(SeasonChunk)
- void logChunk(SeasonChunk)

## Package: me.casperge.realisticseasons.dump

### Class: me.casperge.realisticseasons.dump.DumpCreator
Type: Class

Constructors:
- DumpCreator(RealisticSeasons main)

Methods:
- **static** String generateString(Random, String, int)
- void createDump(UUID, String)
- void createConsoleDump(String)

### Class: me.casperge.realisticseasons.dump.DumpInformation
Type: Class

Methods:
- void setRateLimit(boolean)
- void setPassword(String)
- String getKey()
- String getPassword()
- boolean isRateLimit()
- void addEntry(String, String)
- void setKey(String)

### Class: me.casperge.realisticseasons.dump.DumpProcessor
Type: Class

Methods:
- **static** DumpResponse processDump(DumpInformation)

### Class: me.casperge.realisticseasons.dump.DumpResponse
Type: Class

Constructors:
- DumpResponse(boolean isSucces, String message)

Methods:
- boolean isSucces()
- String getMessage()
- void setSucces(boolean)
- void setMessage(String)

### Class: me.casperge.realisticseasons.dump.LogGrabber
Type: Class

Methods:
- **static** String grabLatestLog()

## Package: me.casperge.realisticseasons.event

### Class: me.casperge.realisticseasons.event.ActionbarListener
Type: Class

Constructors:
- ActionbarListener(RealisticSeasons tsettings)

Methods:
- void setWaitingForTempBar(Player, boolean)
- boolean canReceiveTempBar(Player)
- boolean isWaitingForTemp(Player)

### Class: me.casperge.realisticseasons.event.BlockEvents
Type: Class
Implements: org.bukkit.event.Listener

Constructors:
- BlockEvents(RealisticSeasons main)

Methods:
- void grassDestroy(BlockFadeEvent)
- void blockBreak(BlockBreakEvent)
- void onGrow(CauldronLevelChangeEvent)
- void naturalFreezeEvent(BlockFormEvent)
- void blockPlace(BlockPlaceEvent)
- void moistureChange(MoistureChangeEvent)

### Class: me.casperge.realisticseasons.event.ChunkLoadManager
Type: Class
Implements: org.bukkit.event.Listener

Constructors:
- ChunkLoadManager(RealisticSeasons main)

Methods:
- void onUnload(ChunkUnloadEvent)
- void onLoad(ChunkLoadEvent)

### Class: me.casperge.realisticseasons.event.ChunkPacketEntry
Type: Class

Constructors:
- ChunkPacketEntry(PacketEvent event, int season, boolean isBedrock, int phase, int ySectionCount, HeightAccessor accessor, boolean christmasMode, int weatherStatus, boolean seasonchanges)

Methods:
- PacketEvent getEvent()
- boolean isChristmasMode()
- HeightAccessor getAccessor()
- boolean isBedrock()
- int getSeason()
- boolean isSeasonchanges()
- int getWeatherStatus()
- int getPhase()
- int getySectionCount()

### Class: me.casperge.realisticseasons.event.ChunkPacketEventProtocolLib
Type: Class

No public methods found

### Class: me.casperge.realisticseasons.event.ChunkPacketEventProtocolLib1_18
Type: Class

No public methods found

### Class: me.casperge.realisticseasons.event.ChunkPacketEventProtocolLib1_18_R2
Type: Class

No public methods found

### Class: me.casperge.realisticseasons.event.ChunkPacketEventProtocolLib1_19_R1
Type: Class

No public methods found

### Class: me.casperge.realisticseasons.event.ChunkPacketEventProtocolLib1_19_R2
Type: Class

No public methods found

### Class: me.casperge.realisticseasons.event.ChunkPacketEventProtocolLibAsync
Type: Class

Constructors:
- ChunkPacketEventProtocolLibAsync(RealisticSeasons main, ChunkPacketProcessor processor)

Methods:
- void processSyncPreConditions(Player, World, int, int, PacketContainer, PacketEvent)
- void cancelPacketProcessing(PacketEvent)
- void processBiomeData(PacketEvent, PacketContainer, World, int, boolean, int, boolean, int, boolean)

### Class: me.casperge.realisticseasons.event.ChunkPacketProcessor
Type: Class
Implements: java.lang.Runnable

Constructors:
- ChunkPacketProcessor(ProtocolLibUtils protutils)

Methods:
- void addEntry(PacketEvent, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- void run()

### Class: me.casperge.realisticseasons.event.EntityEvents
Type: Class
Implements: org.bukkit.event.Listener

Constructors:
- EntityEvents(RealisticSeasons main)

Methods:
- void onLogin(PlayerLoginEvent)
- void entityFeedEvent(PlayerInteractAtEntityEvent)
- void onDeath(PlayerDeathEvent)
- void onTarget(EntityTargetEvent)
- void onDrink(PlayerItemConsumeEvent)
- void onCreeperExplode(EntityExplodeEvent)
- void onRespawn(PlayerRespawnEvent)
- boolean containsMaterial(Material, Material[])
- void onDamage(EntityDamageByBlockEvent)
- void onSnowball(ProjectileLaunchEvent)
- void onJoin(PlayerJoinEvent)
- void onMobSpawn(CreatureSpawnEvent)
- void snow(EntityBlockFormEvent)
- void damageEvent(EntityDamageByEntityEvent)
- void onHeal(EntityRegainHealthEvent)
- void EntityDamage(EntityDamageEvent)

### Class: me.casperge.realisticseasons.event.SeasonRefreshChunkEvent
Type: Class
Extends: org.bukkit.event.Event
Implements: org.bukkit.event.Cancellable

Constructors:
- SeasonRefreshChunkEvent(Chunk chunk, Player p)

Methods:
- Player getPlayer()
- boolean isCancelled()
- Chunk getChunk()
- HandlerList getHandlers()
- void setCancelled(boolean)
- **static** HandlerList getHandlerList()

### Class: me.casperge.realisticseasons.event.WorldEvents
Type: Class
Implements: org.bukkit.event.Listener

Constructors:
- WorldEvents(RealisticSeasons main)

Methods:
- void weatherChange(WeatherChangeEvent)
- void onWorldCreate(WorldInitEvent)

## Package: me.casperge.realisticseasons.metrics

### Class: me.casperge.realisticseasons.metrics.MetricsBase
Type: Class

Constructors:
- MetricsBase(String platform, String serverUuid, int serviceId, boolean enabled, Consumer<JsonObjectBuilder> appendPlatformDataConsumer, Consumer<JsonObjectBuilder> appendServiceDataConsumer, Consumer<Runnable> submitTaskConsumer, Supplier<Boolean> checkServiceEnabledSupplier, BiConsumer<String, Throwable> errorLogger, Consumer<String> infoLogger, boolean logErrors, boolean logSentData, boolean logResponseStatusText)

Methods:
- void addCustomChart(CustomChart)

## Package: me.casperge.realisticseasons.metrics.bukkit

### Class: me.casperge.realisticseasons.metrics.bukkit.Metrics
Type: Class

Constructors:
- Metrics(JavaPlugin plugin, int)

Methods:
- void addCustomChart(CustomChart)

## Package: me.casperge.realisticseasons.metrics.charts

### Class: me.casperge.realisticseasons.metrics.charts.AdvancedBarChart
Type: Class
Extends: me.casperge.realisticseasons.metrics.charts.CustomChart

Constructors:
- AdvancedBarChart(String, Callable<Map<String, [I>> callable)

No public methods found

### Class: me.casperge.realisticseasons.metrics.charts.AdvancedPie
Type: Class
Extends: me.casperge.realisticseasons.metrics.charts.CustomChart

Constructors:
- AdvancedPie(String, Callable<Map<String, Integer>> callable)

No public methods found

### Class: me.casperge.realisticseasons.metrics.charts.CustomChart
Type: Abstract Class

Methods:
- JsonObjectBuilder$JsonObject getRequestJsonObject(BiConsumer<String, Throwable>, boolean)

### Class: me.casperge.realisticseasons.metrics.charts.DrilldownPie
Type: Class
Extends: me.casperge.realisticseasons.metrics.charts.CustomChart

Constructors:
- DrilldownPie(String, Callable<Map<String, Map<String, Integer>>> callable)

Methods:
- JsonObjectBuilder$JsonObject getChartData()

### Class: me.casperge.realisticseasons.metrics.charts.MultiLineChart
Type: Class
Extends: me.casperge.realisticseasons.metrics.charts.CustomChart

Constructors:
- MultiLineChart(String, Callable<Map<String, Integer>> callable)

No public methods found

### Class: me.casperge.realisticseasons.metrics.charts.SimpleBarChart
Type: Class
Extends: me.casperge.realisticseasons.metrics.charts.CustomChart

Constructors:
- SimpleBarChart(String, Callable<Map<String, Integer>> callable)

No public methods found

### Class: me.casperge.realisticseasons.metrics.charts.SimplePie
Type: Class
Extends: me.casperge.realisticseasons.metrics.charts.CustomChart

Constructors:
- SimplePie(String, Callable<String> callable)

No public methods found

### Class: me.casperge.realisticseasons.metrics.charts.SingleLineChart
Type: Class
Extends: me.casperge.realisticseasons.metrics.charts.CustomChart

Constructors:
- SingleLineChart(String, Callable<Integer> callable)

No public methods found

## Package: me.casperge.realisticseasons.metrics.config

### Class: me.casperge.realisticseasons.metrics.config.MetricsConfig
Type: Class

Constructors:
- MetricsConfig(File file, boolean defaultEnabled)

Methods:
- boolean isLogResponseStatusTextEnabled()
- boolean isLogSentDataEnabled()
- boolean didExistBefore()
- boolean isEnabled()
- boolean isLogErrorsEnabled()
- String getServerUUID()

## Package: me.casperge.realisticseasons.metrics.json

### Class: me.casperge.realisticseasons.metrics.json.JsonObjectBuilder
Type: Class

Methods:
- JsonObjectBuilder$JsonObject build()
- JsonObjectBuilder appendNull(String)
- JsonObjectBuilder appendField(String, String)
- JsonObjectBuilder appendField(String, int)
- JsonObjectBuilder appendField(String, JsonObjectBuilder$JsonObject)
- JsonObjectBuilder appendField(String, String[])
- JsonObjectBuilder appendField(String, int[])
- JsonObjectBuilder appendField(String, JsonObjectBuilder$JsonObject[])

### Class: me.casperge.realisticseasons.metrics.json.JsonObjectBuilder$JsonObject
Type: Class

Methods:
- String toString()

## Package: me.casperge.realisticseasons.paperlib

### Class: me.casperge.realisticseasons.paperlib.PaperLib
Type: Class

Methods:
- **static** boolean isPaper()
- **static** CompletableFuture<Location> getBedSpawnLocationAsync(Player, boolean)
- **static** CompletableFuture<Chunk> getChunkAtAsync(Location)
- **static** CompletableFuture<Chunk> getChunkAtAsync(Location, boolean)
- **static** CompletableFuture<Chunk> getChunkAtAsync(World, int, int)
- **static** CompletableFuture<Chunk> getChunkAtAsync(World, int, int, boolean)
- **static** CompletableFuture<Chunk> getChunkAtAsync(World, int, int, boolean, boolean)
- **static** int getMinecraftVersion()
- **static** boolean isVersion(int)
- **static** boolean isVersion(int, int)
- **static** Environment getEnvironment()
- **static** int getMinecraftPatchVersion()
- **static** CompletableFuture<Boolean> teleportAsync(Entity, Location)
- **static** CompletableFuture<Boolean> teleportAsync(Entity, Location, PlayerTeleportEvent$TeleportCause)
- **static** boolean isSpigot()
- **static** CompletableFuture<Chunk> getChunkAtAsyncUrgently(World, int, int, boolean)
- **static** boolean isChunkGenerated(Location)
- **static** boolean isChunkGenerated(World, int, int)
- **static** void setCustomEnvironment(Environment)
- **static** void suggestPaper(Plugin)
- **static** void suggestPaper(Plugin, Level)
- **static** BlockStateSnapshotResult getBlockState(Block, boolean)
- **static** int getMinecraftPreReleaseVersion()

## Package: me.casperge.realisticseasons.paperlib.environments

### Class: me.casperge.realisticseasons.paperlib.environments.CraftBukkitEnvironment
Type: Class
Extends: me.casperge.realisticseasons.paperlib.environments.Environment

Methods:
- String getName()

### Class: me.casperge.realisticseasons.paperlib.environments.Environment
Type: Abstract Class

Methods:
- CompletableFuture<Chunk> getChunkAtAsyncUrgently(World, int, int, boolean)
- boolean isPaper()
- boolean isChunkGenerated(World, int, int)
- String getName()
- CompletableFuture<Location> getBedSpawnLocationAsync(Player, boolean)
- CompletableFuture<Boolean> teleport(Entity, Location, PlayerTeleportEvent$TeleportCause)
- CompletableFuture<Chunk> getChunkAtAsync(World, int, int, boolean)
- CompletableFuture<Chunk> getChunkAtAsync(World, int, int, boolean, boolean)
- int getMinecraftVersion()
- boolean isVersion(int)
- boolean isVersion(int, int)
- BlockStateSnapshotResult getBlockState(Block, boolean)
- int getMinecraftPreReleaseVersion()
- int getMinecraftPatchVersion()
- boolean isSpigot()

### Class: me.casperge.realisticseasons.paperlib.environments.PaperEnvironment
Type: Class
Extends: me.casperge.realisticseasons.paperlib.environments.SpigotEnvironment

Methods:
- boolean isPaper()
- String getName()

### Class: me.casperge.realisticseasons.paperlib.environments.SpigotEnvironment
Type: Class
Extends: me.casperge.realisticseasons.paperlib.environments.CraftBukkitEnvironment

Methods:
- String getName()
- boolean isSpigot()

## Package: me.casperge.realisticseasons.paperlib.features.asyncchunks

### Class: me.casperge.realisticseasons.paperlib.features.asyncchunks.AsyncChunks
Type: Interface

Methods:
- CompletableFuture<Chunk> getChunkAtAsync(World world, int x, int z, boolean gen)
- CompletableFuture<Chunk> getChunkAtAsync(World, int, int, boolean, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.asyncchunks.AsyncChunksPaper_13
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.asyncchunks.AsyncChunks

Methods:
- CompletableFuture<Chunk> getChunkAtAsync(World, int, int, boolean, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.asyncchunks.AsyncChunksPaper_15
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.asyncchunks.AsyncChunks

Methods:
- CompletableFuture<Chunk> getChunkAtAsync(World, int, int, boolean, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.asyncchunks.AsyncChunksPaper_9_12
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.asyncchunks.AsyncChunks

Methods:
- CompletableFuture<Chunk> getChunkAtAsync(World, int, int, boolean, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.asyncchunks.AsyncChunksSync
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.asyncchunks.AsyncChunks

Methods:
- CompletableFuture<Chunk> getChunkAtAsync(World, int, int, boolean, boolean)

## Package: me.casperge.realisticseasons.paperlib.features.asyncteleport

### Class: me.casperge.realisticseasons.paperlib.features.asyncteleport.AsyncTeleport
Type: Interface

Methods:
- CompletableFuture<Boolean> teleportAsync(Entity, Location, PlayerTeleportEvent$TeleportCause)

### Class: me.casperge.realisticseasons.paperlib.features.asyncteleport.AsyncTeleportPaper
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.asyncteleport.AsyncTeleport

Methods:
- CompletableFuture<Boolean> teleportAsync(Entity, Location, PlayerTeleportEvent$TeleportCause)

### Class: me.casperge.realisticseasons.paperlib.features.asyncteleport.AsyncTeleportPaper_13
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.asyncteleport.AsyncTeleport

Methods:
- CompletableFuture<Boolean> teleportAsync(Entity, Location, PlayerTeleportEvent$TeleportCause)

### Class: me.casperge.realisticseasons.paperlib.features.asyncteleport.AsyncTeleportSync
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.asyncteleport.AsyncTeleport

Methods:
- CompletableFuture<Boolean> teleportAsync(Entity, Location, PlayerTeleportEvent$TeleportCause)

## Package: me.casperge.realisticseasons.paperlib.features.bedspawnlocation

### Class: me.casperge.realisticseasons.paperlib.features.bedspawnlocation.BedSpawnLocation
Type: Interface

Methods:
- CompletableFuture<Location> getBedSpawnLocationAsync(Player, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.bedspawnlocation.BedSpawnLocationPaper
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.bedspawnlocation.BedSpawnLocation

Methods:
- CompletableFuture<Location> getBedSpawnLocationAsync(Player, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.bedspawnlocation.BedSpawnLocationSync
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.bedspawnlocation.BedSpawnLocation

Methods:
- CompletableFuture<Location> getBedSpawnLocationAsync(Player, boolean)

## Package: me.casperge.realisticseasons.paperlib.features.blockstatesnapshot

### Class: me.casperge.realisticseasons.paperlib.features.blockstatesnapshot.BlockStateSnapshot
Type: Interface

Methods:
- BlockStateSnapshotResult getBlockState(Block, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.blockstatesnapshot.BlockStateSnapshotBeforeSnapshots
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.blockstatesnapshot.BlockStateSnapshot

Methods:
- BlockStateSnapshotResult getBlockState(Block, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.blockstatesnapshot.BlockStateSnapshotNoOption
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.blockstatesnapshot.BlockStateSnapshot

Methods:
- BlockStateSnapshotResult getBlockState(Block, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.blockstatesnapshot.BlockStateSnapshotOptionalSnapshots
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.blockstatesnapshot.BlockStateSnapshot

Methods:
- BlockStateSnapshotResult getBlockState(Block, boolean)

### Class: me.casperge.realisticseasons.paperlib.features.blockstatesnapshot.BlockStateSnapshotResult
Type: Class

Constructors:
- BlockStateSnapshotResult(boolean isSnapshot, BlockState state)

Methods:
- BlockState getState()
- boolean isSnapshot()

## Package: me.casperge.realisticseasons.paperlib.features.chunkisgenerated

### Class: me.casperge.realisticseasons.paperlib.features.chunkisgenerated.ChunkIsGenerated
Type: Interface

Methods:
- boolean isChunkGenerated(World, int, int)

### Class: me.casperge.realisticseasons.paperlib.features.chunkisgenerated.ChunkIsGeneratedApiExists
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.chunkisgenerated.ChunkIsGenerated

Methods:
- boolean isChunkGenerated(World, int, int)

### Class: me.casperge.realisticseasons.paperlib.features.chunkisgenerated.ChunkIsGeneratedUnknown
Type: Class
Implements: me.casperge.realisticseasons.paperlib.features.chunkisgenerated.ChunkIsGenerated

Methods:
- boolean isChunkGenerated(World, int, int)

## Package: me.casperge.realisticseasons.particle

### Class: me.casperge.realisticseasons.particle.ParticleManager
Type: Class

Constructors:
- ParticleManager(RealisticSeasons main)

Methods:
- void spawnFireFlies(Location)
- void playWhiteSparkles(Player)
- V spawnFireworkBox(List<Player>, Location)
- void spawnFireworkBox(Location)
- V spawnSmallFallingLeaves(List<Player>, Location)
- void playRandomSweatParticle(Player)
- V spawnMeteorite(List<Player>, Location)
- V spawnLeaf(List<Player>, Location)
- SeasonEntity spawnEntity(ParticleManager$SeasonEntityType, List<Player>, Location)
- void playColdBreathEffect(Player)
- void playRandomFireParticle(Entity)
- void runTest(Location, Player)

### Class: me.casperge.realisticseasons.particle.ParticleManager$SeasonEntityType
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- METEORITE
- FALLING_LEAF
- SMALL_FALLING_LEAVES
- FIREFLIES
- FIREWORKBOX

Methods:
- **static** ParticleManager$SeasonEntityType valueOf(String)
- **static** ParticleManager$SeasonEntityType[] values()

### Class: me.casperge.realisticseasons.particle.ParticleSpawner
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- ParticleSpawner(RealisticSeasons main, ParticleManager pman)

Methods:
- void run()

## Package: me.casperge.realisticseasons.particle.entity

### Class: me.casperge.realisticseasons.particle.entity.SeasonEntity
Type: Interface

Methods:
- Location getLocation()
- boolean isDestroyed()
- V tick(List<Player>)

### Class: me.casperge.realisticseasons.particle.entity.FallingLeaf
Type: Class
Implements: me.casperge.realisticseasons.particle.entity.SeasonEntity

Constructors:
- FallingLeaf(Location currentLocation, List<Player> startVector, Vector wind, Material, Integer)

Methods:
- Location getLocation()
- boolean isDestroyed()
- V tick(List<Player>)
- V setOnGround(List<Player>)

### Class: me.casperge.realisticseasons.particle.entity.FireFlies
Type: Class
Implements: me.casperge.realisticseasons.particle.entity.SeasonEntity

Constructors:
- FireFlies(Location loc)

Methods:
- Location getLocation()
- boolean isDestroyed()
- V tick(List<Player>)

### Class: me.casperge.realisticseasons.particle.entity.FireworkBox
Type: Class
Implements: me.casperge.realisticseasons.particle.entity.SeasonEntity

Constructors:
- FireworkBox(Location currentLocation, List<Player> boxType)

Methods:
- Location getLocation()
- boolean isDestroyed()
- V tick(List<Player>)
- V shootFirework(int, boolean, boolean, FireworkEffect$Type, List<Color>)

### Class: me.casperge.realisticseasons.particle.entity.Meteorite
Type: Class
Implements: me.casperge.realisticseasons.particle.entity.SeasonEntity

Constructors:
- Meteorite(Location currentLocation, List<Player>)

Methods:
- Location getLocation()
- boolean isDestroyed()
- V tick(List<Player>)

### Class: me.casperge.realisticseasons.particle.entity.NMSEntityCreator
Type: Class

Methods:
- **static** FakeArmorStand createFakeArmorStand(World, double, double, double, double, boolean, boolean, boolean, boolean)

### Class: me.casperge.realisticseasons.particle.entity.SmallFallingLeaf
Type: Class
Implements: me.casperge.realisticseasons.particle.entity.SeasonEntity

Constructors:
- SmallFallingLeaf(Location currentLocation, List<Player>)

Methods:
- Location getLocation()
- boolean isDestroyed()
- V tick(List<Player>)

## Package: me.casperge.realisticseasons.runnables

### Class: me.casperge.realisticseasons.runnables.AnimalRemover
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- AnimalRemover(RealisticSeasons main)

Methods:
- void run()

### Class: me.casperge.realisticseasons.runnables.ChunkRefresher
Type: Class

Constructors:
- ChunkRefresher(RealisticSeasons main, World w)

Methods:
- void runRefresher()

### Class: me.casperge.realisticseasons.runnables.FallBlockTicker
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- FallBlockTicker(RealisticSeasons main, World wr)

Methods:
- boolean isTraveling(Player)
- World getWorld()
- void run()
- **static** void checkChunk(SeasonChunk)

### Class: me.casperge.realisticseasons.runnables.RestoreWorldTicker
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- RestoreWorldTicker(RealisticSeasons main, World wr)

Methods:
- World getWorld()
- void run()
- **static** void checkChunk(SeasonChunk)

### Class: me.casperge.realisticseasons.runnables.SpringBlockTicker
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- SpringBlockTicker(RealisticSeasons main, World wr)

Methods:
- World getWorld()
- void run()
- **static** void checkChunk(SeasonChunk)

### Class: me.casperge.realisticseasons.runnables.SummerBlockTicker
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- SummerBlockTicker(RealisticSeasons main, World wr)

Methods:
- World getWorld()
- void run()
- **static** void checkChunk(SeasonChunk)

### Class: me.casperge.realisticseasons.runnables.TemperatureUpdater
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- TemperatureUpdater(RealisticSeasons main, TemperatureManager tman)

Methods:
- String removeSpaces(String, int)
- void run()
- String placeInString(String, String)

### Class: me.casperge.realisticseasons.runnables.TimeHandler
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- TimeHandler(RealisticSeasons main)

Methods:
- void run()

### Class: me.casperge.realisticseasons.runnables.WinterBlockTicker
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- WinterBlockTicker(RealisticSeasons runDelay, World wr)

Methods:
- boolean isTraveling(Player)
- World getWorld()
- void run()

## Package: me.casperge.realisticseasons.season

### Class: me.casperge.realisticseasons.season.Season
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- WINTER
- SPRING
- SUMMER
- FALL
- DISABLED
- RESTORE

Methods:
- Season getNextSeason()
- int intValue()
- **static** Season valueOf(String)
- **static** Season[] values()
- **static** Season getSeason(String)
- Season getPreviousSeason()
- String getConfigName()

### Class: me.casperge.realisticseasons.season.SeasonChunk
Type: Class

Constructors:
- SeasonChunk(String worldname, int x, int z, Long loaded)
- SeasonChunk(String worldname, int x, int z)
- SeasonChunk(Chunk x)

Methods:
- String getWorldName()
- World getWorld()
- Long getLoadTime()
- int getX()
- int getZ()
- int hashCode()
- Chunk getChunk()
- boolean equals(Object)
- String toString()

### Class: me.casperge.realisticseasons.season.SeasonCycle
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- SeasonCycle(RealisticSeasons main)

Methods:
- void handleTimeChanges()
- void run()

### Class: me.casperge.realisticseasons.season.SeasonManager
Type: Class

Constructors:
- SeasonManager(RealisticSeasons main)

Methods:
- void sendCycleMessage(World, Season)
- Season getNextSeason(World)
- boolean setSeason(World, Season, boolean)
- boolean setSeason(World, Season)
- HashSet<SeasonChunk> getCheckedList(World, Season)
- void setSpring(World)
- void setRestoring(World)
- Season getSeason(World)
- void sendSeasonInfoToConsole(World)
- void setSubSeason(World, SubSeason, boolean)
- void checkChunk(SeasonChunk)
- void clearChunkCheckedList(World, Season)
- void runSubSeasonCheck()
- void clearChunkQueue(World, Season)
- void checkWorlds()
- void setFall(World)
- LinkedHashSet<SeasonChunk> getQueue(World, Season)
- void setup()
- Season nextSeason(World)
- SubSeason getSubSeason(World)
- void setSummer(World)
- void setWinter(World)
- void sendSeasonInfo(Player)

### Class: me.casperge.realisticseasons.season.SubSeason
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- START
- EARLY
- MIDDLE
- LATE
- END

Methods:
- **static** SubSeason valueOf(String)
- **static** SubSeason[] values()
- int getPhase()

## Package: me.casperge.realisticseasons.seasonevent

### Class: me.casperge.realisticseasons.seasonevent.SeasonCustomEvent
Type: Interface

Methods:
- String getName()
- boolean doDisplay()
- List<String> getCommands(boolean)

### Class: me.casperge.realisticseasons.seasonevent.CustomDailyEvent
Type: Class
Implements: me.casperge.realisticseasons.seasonevent.SeasonCustomEvent

Constructors:
- CustomDailyEvent(ConfigurationSection commands)

Methods:
- String getName()
- boolean doDisplay()
- List<String> getCommands(boolean)

### Class: me.casperge.realisticseasons.seasonevent.CustomDatedEvent
Type: Class
Implements: me.casperge.realisticseasons.seasonevent.SeasonCustomEvent

Constructors:
- CustomDatedEvent(ConfigurationSection startCommands)

Methods:
- Date getStartDate()
- String getName()
- boolean hasEvent(World)
- Date getEndDate()
- boolean isActive(Date)
- boolean doDisplay()
- List<String> getCommands(boolean)

### Class: me.casperge.realisticseasons.seasonevent.CustomWeeklyEvent
Type: Class
Implements: me.casperge.realisticseasons.seasonevent.SeasonCustomEvent

Constructors:
- CustomWeeklyEvent(ConfigurationSection startCommands)

Methods:
- String getName()
- boolean isToday(int)
- boolean doDisplay()
- List<String> getCommands(boolean)

### Class: me.casperge.realisticseasons.seasonevent.EventFileLoader
Type: Class

Constructors:
- EventFileLoader(RealisticSeasons conf, EventManager)

No public methods found

### Class: me.casperge.realisticseasons.seasonevent.EventManager
Type: Class

Constructors:
- EventManager(RealisticSeasons main)

Methods:
- List<CustomWeeklyEvent> getWeeklyEvents()
- V setDailyEvents(List<CustomDailyEvent>)
- V setWeeklyEvents(List<CustomWeeklyEvent>)
- void start(World, SeasonCustomEvent, Date)
- List<String> getActiveEvents(World)
- String getActiveEventsAsString(World)
- List<CustomDatedEvent> getDatedEvents()
- DefaultEvent getDefaultEvent(DefaultEventType)
- List<CustomDailyEvent> getDailyEvents()
- void stop(World, SeasonCustomEvent, Date)
- void load()
- int getDaysUntilNextEvent(World)
- V setDatedEvents(List<CustomDatedEvent>)
- String getNextEventsAsString(World)
- List<CustomDatedEvent> getNextEvent(World)

### Class: me.casperge.realisticseasons.seasonevent.EventUtils
Type: Class

Constructors:
- EventUtils(RealisticSeasons main)

Methods:
- List<String> replacePlaceholders(World, List<String>, Date)
- V execute(World, List<String>, Date)

## Package: me.casperge.realisticseasons.seasonevent.buildin

### Class: me.casperge.realisticseasons.seasonevent.buildin.DefaultEvent
Type: Interface

Methods:
- DefaultEventType getType()
- void disable(World)
- void enable(World)
- boolean isEnabled(World)
- **static** ItemStack randomItemFromList(RandomItemStack[] stacks)

### Class: me.casperge.realisticseasons.seasonevent.buildin.ChristmasEvent
Type: Class
Extends: me.casperge.realisticseasons.seasonevent.CustomDatedEvent
Implements: me.casperge.realisticseasons.seasonevent.buildin.DefaultEvent

Constructors:
- ChristmasEvent(ConfigurationSection r)

Methods:
- void placePresent(Location)
- DefaultEventType getType()
- void tickPresentSpawning()
- void disable(World)
- void enable(World)
- void presentOpened(Player, Location)
- boolean isEnabled(World)

### Class: me.casperge.realisticseasons.seasonevent.buildin.DefaultEventType
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- CHRISTMAS
- NEWYEAR
- EASTER
- HALLOWEEN

Methods:
- **static** DefaultEventType valueOf(String)
- **static** DefaultEventType[] values()

### Class: me.casperge.realisticseasons.seasonevent.buildin.EasterEvent
Type: Class
Extends: me.casperge.realisticseasons.seasonevent.CustomDatedEvent
Implements: me.casperge.realisticseasons.seasonevent.buildin.DefaultEvent, org.bukkit.event.Listener

Constructors:
- EasterEvent(ConfigurationSection r)

Methods:
- void placeEgg(Location)
- void onMobSpawn(CreatureSpawnEvent)
- void tickEggSpawning()
- DefaultEventType getType()
- void disable(World)
- void enable(World)
- boolean isEnabled(World)
- void eggOpened(Player, Location)

### Class: me.casperge.realisticseasons.seasonevent.buildin.HalloweenEvent
Type: Class
Extends: me.casperge.realisticseasons.seasonevent.CustomDatedEvent
Implements: me.casperge.realisticseasons.seasonevent.buildin.DefaultEvent, org.bukkit.event.Listener

Constructors:
- HalloweenEvent(ConfigurationSection r)

Methods:
- void duplicateMob(LivingEntity)
- void onMobSpawn(CreatureSpawnEvent)
- DefaultEventType getType()
- void disable(World)
- void enable(World)
- boolean isEnabled(World)
- void hitEvent(EntityDamageByEntityEvent)
- void onProjectile(ProjectileLaunchEvent)

### Class: me.casperge.realisticseasons.seasonevent.buildin.NewYearEvent
Type: Class
Extends: me.casperge.realisticseasons.seasonevent.CustomDatedEvent
Implements: me.casperge.realisticseasons.seasonevent.buildin.DefaultEvent

Constructors:
- NewYearEvent(ConfigurationSection r)

Methods:
- DefaultEventType getType()
- void disable(World)
- void enable(World)
- boolean isEnabled(World)

### Class: me.casperge.realisticseasons.seasonevent.buildin.RandomItemStack
Type: Class

Constructors:
- RandomItemStack(Material material, int min, int max)

Methods:
- ItemStack generateStack()

### Class: me.casperge.realisticseasons.seasonevent.buildin.StandardEventFileLoader
Type: Class

Constructors:
- StandardEventFileLoader(RealisticSeasons conf, EventManager)

No public methods found

## Package: me.casperge.realisticseasons.temperature

### Class: me.casperge.realisticseasons.temperature.AnimalTemperature
Type: Class
Extends: org.bukkit.scheduler.BukkitRunnable

Constructors:
- AnimalTemperature(RealisticSeasons main)

Methods:
- void run()

### Class: me.casperge.realisticseasons.temperature.CustomTemperatureItem
Type: Class

Constructors:
- CustomTemperatureItem(Material material, int custommodeldata, int modifier, boolean onWearing, boolean onHold, boolean useCustomModelData, boolean worksUnderwater)

Methods:
- int getModifier()
- boolean isItem(ItemStack)
- boolean isActive(Player)
- boolean onWear()

### Class: me.casperge.realisticseasons.temperature.PermanentTemperatureEffect
Type: Class
Implements: me.casperge.realisticseasons.api.TemperatureEffect

Constructors:
- PermanentTemperatureEffect(TempData tempdata, UUID uuid, int modifier)

Methods:
- void cancel()
- int getModifier()
- int getID()

### Class: me.casperge.realisticseasons.temperature.TempData
Type: Class

Constructors:
- TempData(RealisticSeasons main)

Methods:
- void disableWorld(World)
- void clearCustomTemperatureEffects(Player)
- void drinked(Player)
- int getWaterTemperatureModifier(Location, Season)
- int getPermanentEffectsModified(Player, int)
- int getBiomeTemperatureModifier(Location)
- void removeFromWaterList(Player)
- int getWaterModifier(Player)
- void setSprintingModifier(Player, Integer)
- boolean load()
- void addBiomeTemperature(String, Integer)
- int getSprintingModifier(Player)
- void applyCustomEffect(Player, int, int)
- void applyCustomEffect(UUID, int, int, long)
- int getCustomEffectsModified(Player, int)
- List<World> getEnabledWorlds()
- void resetBlockEffects(UUID)
- Long getLastDrink(Player)
- int getBaseTemperature(World)
- void setWaterModifier(Player, Integer)
- void removeIfDrinked(Player)
- void setBaseTemperature(World, Integer)
- V addWaterBiomeTemperature(String, HashMap<Season, Integer>)
- boolean isEnabledWorld(World)
- void enableWorld(World)
- HashMap<UUID, Integer> getBlockEffects()
- void toggleTemperature(World)
- TemperatureSettings getTempSettings()
- V updateBlockEffects(HashMap<UUID, Integer>)
- boolean isEnabled()
- HashMap<UUID, List<TempData$CustomTemperatureEffect>> getActiveCustomEffects()
- **static** String readParticlePacket(byte[])
- TemperatureEffect applyPermanentEffect(Player, int)

### Class: me.casperge.realisticseasons.temperature.TempData$CustomTemperatureEffect
Type: Class

Constructors:
- TempData$CustomTemperatureEffect(TempData this$0, int temperatureModifier, int duration)
- TempData$CustomTemperatureEffect(TempData this$0, int temperatureModifier, int duration, long startTime)

Methods:
- int getTemperatureModifier()
- int getDuration()
- long getStartTime()
- boolean isActive()

### Class: me.casperge.realisticseasons.temperature.TempEffect
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- COLD_SLOWNESS
- COLD_HUNGER
- COLD_FREEZING
- HEAT_NO_HEALING
- HEAT_SLOWNESS
- HEAT_FIRE
- BOOSTS
- HYDRATED

Methods:
- **static** TempEffect valueOf(String)
- **static** TempEffect[] values()

### Class: me.casperge.realisticseasons.temperature.TempUtils
Type: Class

Constructors:
- TempUtils(RealisticSeasons main, TempData tempdata)

Methods:
- int getHeightModified(Location, int)
- boolean isInWater(Entity)
- int getSprintingModified(Player, int)
- boolean containsMaterial(Material, Material[])
- void applyEffect(Player, TempEffect)
- boolean hasDrinked(Player)
- int generateNewBaseTemperature(World)
- int getVelocityModified(Player, int)
- int getBiomeModified(Location, int)
- int getArmorModified(Player, int)
- int getCurrentWorldTemperature(World)
- boolean flashingWaterBottle(Player)
- int getFoodModified(Player, int)
- int getBlockLightModified(Entity, int)
- int generateNextDayBaseTemp(World, int)
- int getWaterModified(LivingEntity, int, Season)
- int getWaterModified(Player, int, Season)

### Class: me.casperge.realisticseasons.temperature.TemperatureManager
Type: Class

Constructors:
- TemperatureManager(RealisticSeasons main)

Methods:
- void disableTemperature(Player)
- void disableTemperature(UUID)
- ChatColor getColorCode(int)
- void generateTempForLoadedWorlds()
- List<UUID> getKnownPlayers()
- void resetTemperature(UUID)
- List<UUID> getFahrenheitEnabled()
- int getPlayerAirTemperature(Player)
- List<UUID> getTemperatureDisabled()
- int getAirTemperature(Location)
- void setHealing(Player, boolean)
- boolean hasFahrenheitEnabled(Player)
- void load()
- void setRSBurn(UUID, boolean)
- void updateTemperature(Player)
- TempData getTempData()
- TempUtils getTempUtils()
- boolean hasTemperature(Player)
- boolean isFrozen(Player)
- void enableTemperature(Player)
- void enableTemperature(UUID)
- int calculateTemperature(Player)
- boolean hasRSBurn(UUID)
- void setFreezing(Player, boolean, boolean)
- boolean canHeal(Player)
- void loadWorld(World)
- boolean hasPlayedBefore(UUID)
- void loggedIn(UUID)
- int getTemperature(Player)
- void toggleFahrenheit(Player)
- void toggleFahrenheit(UUID)

### Class: me.casperge.realisticseasons.temperature.TemperatureSettings
Type: Class

Constructors:
- TemperatureSettings(YamlConfiguration tempfile)

Methods:
- int getWarmFireTemp()
- boolean hasBlockEffect(Material)
- int getWarmNoHealingTemp()
- int getWarmSlownessTemp()
- boolean isEntityTemperatureEnabled()
- PotionEffectType getColdHungerType()
- int getTemperatureUpdateInterval()
- int getColdSlownessLevel()
- boolean isHeightModifying()
- List<EntityType> getEntitiesImmuneToHeat()
- List<EntityType> getEntitiesResilient()
- int getEntityColdFreezing()
- PotionEffectType getEntityWarmSlownessEffect()
- int getMinTemperature(Season)
- boolean isActionbarWarningEnabled()
- String getActionbarFreezingWarning()
- double getVelocityModifier()
- int getWaterBottleEffectDuration()
- int getSwimmingModifier(Season)
- PotionEffectType getColdSlownessType()
- String getActionbarOverheatingWarning()
- int getEntityWarmSlownessLevel()
- List<EntityType> getEntitiesWithoutTemperature()
- boolean blockEffectsEnabled()
- int getColdHungerTemp()
- BlockEffect getBlockEffect(Material)
- PotionEffectType getWarmSlownessType()
- String getFahrenheitMessage()
- boolean isMessageWarningsEnabled()
- boolean isIpBasedTemperature()
- int getWarmMovementStart()
- String getMessageFreezingWarning()
- double getHeightBlockIncrease()
- List<CustomTemperatureItem> getCustomItems()
- PotionEffectType getEntityColdSlownessEffect()
- boolean isOverwriteActionbar()
- boolean isReducedMovementSpeedEnabled()
- int getBoostsMinHunger()
- List<PotionEffectType> getBoostPotionEffects()
- int getLavaTemp()
- boolean isDisplayTempOnActionBar()
- int getWeatherModifier(TemperatureSettings$Weather)
- int getEntityColdSlownessStart()
- int getWarmMovementEnd()
- boolean isConvertToFahrenheit()
- int getLeatherCap()
- int getWarmSlownessLevel()
- int getBoostMinTemp()
- String getMessageOverheatingWarning()
- float getTemperatureChangeRate()
- int getColdMovementEnd()
- int getColdFreezingTemp()
- PotionEffectType getHydrationEffect()
- int getHydrationLevel()
- int getEntityWarmBurn()
- void load()
- int getWaterBottleModifier()
- int getMaxSprintingModifier()
- int getEntityWarmSlownessStart()
- int getEntityColdSlownessLevel()
- int getColdHungerLevel()
- int getColdSlownessTemp()
- List<EntityType> getEntitiesImmuneToCold()
- String getCelciusMessage()
- int getNetherTemperature()
- int getMaxTemperature(Season)
- int getEndTemperature()
- int getBoostMaxTemp()
- int getColdMovementStart()
- String getActionbarDisplay()
- int getArmorModifier(TemperatureSettings$Armor)
- int getFullHungerModifier()
- HashMap<String, Double> getHeightBlockIncreaseOverwrites()

### Class: me.casperge.realisticseasons.temperature.TemperatureSettings$Armor
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- LEATHER
- IRON
- GOLD
- DIAMOND
- NETHERITE

Methods:
- **static** TemperatureSettings$Armor valueOf(String)
- **static** TemperatureSettings$Armor[] values()

### Class: me.casperge.realisticseasons.temperature.TemperatureSettings$Weather
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- RAIN
- STORM

Methods:
- **static** TemperatureSettings$Weather valueOf(String)
- **static** TemperatureSettings$Weather[] values()

## Package: me.casperge.realisticseasons.utils

### Class: me.casperge.realisticseasons.utils.AnimalUtils
Type: Class

Constructors:
- AnimalUtils(RealisticSeasons main)

Methods:
- void updateAnimalSpawns(Season, Chunk)
- **static** boolean generateInGroups(EntityType)
- boolean checkEntity(Entity, Season, boolean)
- void removeAllAnimals(Season, World)
- void generateAnimal(Chunk, EntityType, Season)
- boolean isSpawnable(Material)
- void checkRandomEntity(Season, World)

### Class: me.casperge.realisticseasons.utils.BiomeMappings
Type: Class

Constructors:
- BiomeMappings(RealisticSeasons main)

Methods:
- **static** String getFoliageColor(String)
- **static** String getGrassHex(String)
- String[] getBiomeNames(String)
- int[] getBiomeIDs(String)

### Class: me.casperge.realisticseasons.utils.BlockUtils
Type: Class

Constructors:
- BlockUtils(RealisticSeasons main)

Methods:
- **static** boolean canLeafDrop(Block)
- boolean isSnowing(Location)
- boolean isSnowable(Block)
- **static** Skull getSkullStateFromURL(String, Skull)
- boolean affectBlockInWinter(World, int, int, int)
- boolean affectBlockInWinter(Block)
- void placePuddleBlock(Block)
- boolean affectFlora(Block)
- **static** ItemStack getSkullFromURL(String)

### Class: me.casperge.realisticseasons.utils.ChunkUtils
Type: Class

Constructors:
- ChunkUtils(RealisticSeasons main)

Methods:
- **static** boolean checkBiome(ChunkUtils$BiomeType, String)
- boolean unfreezeChunk(Chunk)
- boolean unfreezeChunk(Chunk, double)
- void getId(Material, Player)
- **static** List<String> getBiomeList(ChunkUtils$BiomeType)
- List<Block> getGrowableBlocks(Chunk)
- boolean affectFlora(Chunk)
- **static** Collection<Chunk> around(Chunk, int)
- **static** Collection<Chunk> around(Chunk, int, int)
- **static** Collection<String> aroundString(int, int, String, int)
- **static** int[] addToList(int[], int, int)
- **static** Class<*> getCbClass(String)
- List<Block> getGrassBlocks(Chunk)
- **static** boolean isChunkLoaded(Location)
- boolean dontAffectInWinter(int, int, World)
- boolean checkPopulation(Chunk, float, float, int, int, Season, boolean)
- **static** double get2dDistance(Block, Block)
- **static** double get2dDistance(int, int, int, int)
- List<Block> getPlantBlocks(Chunk)
- **static** boolean isChunkLoadedString(String)
- void increasePopulation(Chunk, int, int, ChunkUtils$PlantType)
- HashMap<Material, Integer> getChunkPopulation(Chunk)
- **static** Chunk chunkFromString(String)
- **static** List<[I> generateChunkPackets()
- **static** double get2dDistanceFromCenter(Block, Chunk)
- void reducePopulation(Chunk, int, int, ChunkUtils$PlantType)
- int[] getTotalPlantPopulation(Chunk)

### Class: me.casperge.realisticseasons.utils.ChunkUtils$BiomeType
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- AFFECTFLORA
- AFFECTINWINTER

Methods:
- **static** ChunkUtils$BiomeType valueOf(String)
- **static** ChunkUtils$BiomeType[] values()

### Class: me.casperge.realisticseasons.utils.ChunkUtils$FallChunkType
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- GROUNDONLY
- ALL
- NONE

Methods:
- **static** ChunkUtils$FallChunkType valueOf(String)
- **static** ChunkUtils$FallChunkType[] values()

### Class: me.casperge.realisticseasons.utils.ChunkUtils$PlantType
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- GRASS
- FLOWER
- BERRY
- MUSHROOM

Methods:
- **static** ChunkUtils$PlantType valueOf(String)
- **static** ChunkUtils$PlantType[] values()

### Class: me.casperge.realisticseasons.utils.JavaUtils
Type: Class

Methods:
- **static** double[] toCartesianAsVector(double)
- **static** String getMonthOfStringDate(String)
- **static** void saveDefaultConfigValues(String, String)
- **static** int convertToFahrenheit(int)
- **static** String getGeoLocationCountryCode(String)
- **static** double randomDouble(double, double)
- **static** int gcd(int, int)
- **static** Random getRandom()
- **static** int hexToDecimal(String)
- **static** boolean isNumeric(String)
- **static** V moveToBack(LinkedHashSet<TT>, T)
- **static** String hex(String)
- **static** String getDayOfStringDate(String)
- **static** String decimalToHex(int)
- **static** String mixColor(String, String, double)
- **static** Color mixColor(Color, Color, double)

### Class: me.casperge.realisticseasons.utils.LitterGeneration
Type: Class

Constructors:
- LitterGeneration(RealisticSeasons main)

Methods:
- void spawnLeafLitter(Location)
- List<Block> getLeafLitterBlocks(Chunk)
- void removeLeafLitter(Chunk)

### Class: me.casperge.realisticseasons.utils.SnowPatterns
Type: Class

Methods:
- **static** Integer[] getArray(int, int)
- **static** void generate()

## Package: me.casperge.realisticseasons1_16_R2

### Class: me.casperge.realisticseasons1_16_R2.CustomBiome1_16_R2
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_16_R2(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_16_R2.FakeArmorStand_1_16_R2
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_16_R2(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_16_R2.NmsCode_16_R2
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- float getBiomeTemperature(String)
- List<String> getBiomes(String)
- **static** V sendPacket(Player, Packet<*>)
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- double getTPS()
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void setBlockInNativeChunkSection(World, int, int, int, int, byte)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- void sendManualChange(Block, Player)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

## Package: me.casperge.realisticseasons1_16_R3

### Class: me.casperge.realisticseasons1_16_R3.CustomBiome1_16_R3
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_16_R3(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_16_R3.FakeArmorStand_1_16_R3
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_16_R3(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_16_R3.NmsCode_16_R3
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- double getTPS()
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void setBlockInNativeChunkSection(World, int, int, int, int, byte)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- void sendManualChange(Block, Player)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

## Package: me.casperge.realisticseasons1_17_R1

### Class: me.casperge.realisticseasons1_17_R1.CustomBiome1_17_R1
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_17_R1(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- int hexToDecimal(String)
- float getScale()
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_17_R1.FakeArmorStand_1_17_R1
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_17_R1(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_17_R1.NmsCode_17_R1
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- List<String> getAllBiomes()
- double getTPS()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void setBlockInNativeChunkSection(World, int, int, int, int, byte)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

## Package: me.casperge.realisticseasons1_18_R1

### Class: me.casperge.realisticseasons1_18_R1.CustomBiome1_18_R1
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_18_R1(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_18_R1.FakeArmorStand_1_18_R1
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_18_R1(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_18_R1.NmsCode_18_R1
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- List<String> getAllBiomes()
- double getTPS()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_18_R1.ProtocolLibUtils1_18_R1
Type: Class

Methods:
- void readPacket(PacketContainer, World, int, boolean, int)
- ChunkSection[] extractData(ClientboundLevelChunkPacketData, World)
- byte[] toByteArray(ChunkSection[])

## Package: me.casperge.realisticseasons1_18_R2

### Class: me.casperge.realisticseasons1_18_R2.CustomBiome1_18_R2
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_18_R2(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_18_R2.FakeArmorStand_1_18_R2
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_18_R2(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_18_R2.NmsCode_18_R2
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_18_R2.ProtocolLibUtils1_18_R2
Type: Class

Methods:
- void readPacket(PacketContainer, World, int, boolean, int)
- ChunkSection[] extractData(ClientboundLevelChunkPacketData, World)
- byte[] toByteArray(ChunkSection[])

## Package: me.casperge.realisticseasons1_19_R1

### Class: me.casperge.realisticseasons1_19_R1.CustomBiome1_19_R1
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_19_R1(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_19_R1.FakeArmorStand_1_19_R1
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_19_R1(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_19_R1.NmsCode_19_R1
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_19_R1.ProtocolLibUtils1_19_R1
Type: Class

Methods:
- long readVarLong(PacketDataSerializer)
- void readPacket(PacketContainer, World, int, boolean, int)
- ProtocolLibUtils1_19_R1$CustomChunkSection[] extractData(ClientboundLevelChunkPacketData, World)
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, World)
- byte[] toByteArray(ProtocolLibUtils1_19_R1$CustomChunkSection[])
- byte[] toByteArray(ChunkSection[])
- void readPacketOld(PacketContainer, World, int, boolean, int)
- int readVarInt(PacketDataSerializer)

## Package: me.casperge.realisticseasons1_19_R2

### Class: me.casperge.realisticseasons1_19_R2.CustomBiome1_19_R2
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_19_R2(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_19_R2.FakeArmorStand_1_19_R2
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_19_R2(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_19_R2.NmsCode_19_R2
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_19_R2.ProtocolLibUtils1_19_R2
Type: Class

Methods:
- long readVarLong(PacketDataSerializer)
- void readPacket(PacketContainer, World, int, boolean, int)
- ProtocolLibUtils1_19_R2$CustomChunkSection[] extractData(ClientboundLevelChunkPacketData, World)
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, World)
- byte[] toByteArray(ProtocolLibUtils1_19_R2$CustomChunkSection[])
- byte[] toByteArray(ChunkSection[])
- void readPacketOld(PacketContainer, World, int, boolean, int)
- int readVarInt(PacketDataSerializer)

## Package: me.casperge.realisticseasons1_19_R3

### Class: me.casperge.realisticseasons1_19_R3.CustomBiome1_19_R3
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_19_R3(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_19_R3.FakeArmorStand_1_19_R3
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_19_R3(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_19_R3.NmsCode_19_R3
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)
- HashMap<Integer, Integer> generateHeightAccessor(World)

### Class: me.casperge.realisticseasons1_19_R3.ProtocolLibUtils1_19_R3
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int, HeightAccessor)
- void readPacketOld(PacketContainer, int, boolean, int, int, HeightAccessor, int, boolean)

## Package: me.casperge.realisticseasons1_20_R1

### Class: me.casperge.realisticseasons1_20_R1.CustomBiome1_20_R1
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_20_R1(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_20_R1.FakeArmorStand_1_20_R1
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_20_R1(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_20_R1.NmsCode_20_R1
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_20_R1.ProtocolLibUtils1_20_R1
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int)

## Package: me.casperge.realisticseasons1_20_R2

### Class: me.casperge.realisticseasons1_20_R2.CustomBiome1_20_R2
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_20_R2(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_20_R2.FakeArmorStand_1_20_R2
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_20_R2(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_20_R2.NmsCode_20_R2
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_20_R2.ProtocolLibUtils1_20_R2
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int)

## Package: me.casperge.realisticseasons1_20_R3

### Class: me.casperge.realisticseasons1_20_R3.CustomBiome1_20_R3
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_20_R3(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_20_R3.FakeArmorStand_1_20_R3
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_20_R3(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_20_R3.NmsCode_20_R3
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_20_R3.ProtocolLibUtils1_20_R3
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int, boolean)

## Package: me.casperge.realisticseasons1_20_R4

### Class: me.casperge.realisticseasons1_20_R4.CustomBiome1_20_R4
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_20_R4(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_20_R4.FakeArmorStand_1_20_R4
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_20_R4(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_20_R4.NmsCode_20_R4
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_20_R4.ProtocolLibUtils1_20_R4
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int, boolean)

## Package: me.casperge.realisticseasons1_21_R1

### Class: me.casperge.realisticseasons1_21_R1.CustomBiome1_21_R1
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_21_R1(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_21_R1.FakeArmorStand_1_21_R1
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_21_R1(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_21_R1.NmsCode_21_R1
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_21_R1.ProtocolLibUtils1_21_R1
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int, boolean)

## Package: me.casperge.realisticseasons1_21_R2

### Class: me.casperge.realisticseasons1_21_R2.CustomBiome1_21_R2
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_21_R2(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_21_R2.FakeArmorStand_1_21_R2
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_21_R2(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_21_R2.NmsCode_21_R2
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- **static** void setWolfVariant(Wolf, int)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_21_R2.ProtocolLibUtils1_21_R2
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int, boolean)

## Package: me.casperge.realisticseasons1_21_R3

### Class: me.casperge.realisticseasons1_21_R3.CustomBiome1_21_R3
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_21_R3(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_21_R3.FakeArmorStand_1_21_R3
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_21_R3(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_21_R3.NmsCode_21_R3
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- float getBiomeTemperature(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- int getSectionCount(World)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- Class<*> getCbClass(String)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)
- int getMaxHeight(World)
- **static** void setWolfVariant(Wolf, int)
- String getBiome(int)

### Class: me.casperge.realisticseasons1_21_R3.ProtocolLibUtils1_21_R3
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int, boolean)

## Package: me.casperge.realisticseasons1_21_R4

### Class: me.casperge.realisticseasons1_21_R4.CustomBiome1_21_R4
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_21_R4(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_21_R4.FakeArmorStand_1_21_R4
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_21_R4(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_21_R4.NmsCode_21_R4
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getSectionCount(World)
- **static** void setLeafLitterCount(Block, int)
- Class<*> getCbClass(String)
- **static** boolean isLeafLitter(Material)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- int getMaxHeight(World)
- **static** void setWolfVariant(Wolf, int)
- String getBiome(int)
- float getBiomeTemperature(String)
- **static** Material getLeafLitter()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)

### Class: me.casperge.realisticseasons1_21_R4.ProtocolLibUtils1_21_R4
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int, boolean)

## Package: me.casperge.realisticseasons1_21_R5

### Class: me.casperge.realisticseasons1_21_R5.CustomBiome1_21_R5
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_21_R5(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_21_R5.FakeArmorStand_1_21_R5
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_21_R5(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_21_R5.NmsCode_21_R5
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getSectionCount(World)
- **static** void setLeafLitterCount(Block, int)
- Class<*> getCbClass(String)
- **static** boolean isLeafLitter(Material)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- int getMaxHeight(World)
- **static** void setWolfVariant(Wolf, int)
- String getBiome(int)
- float getBiomeTemperature(String)
- **static** Material getLeafLitter()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)

### Class: me.casperge.realisticseasons1_21_R5.ProtocolLibUtils1_21_R5
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int, boolean)

## Package: me.casperge.realisticseasons1_21_R6

### Class: me.casperge.realisticseasons1_21_R6.CustomBiome1_21_R6
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_21_R6(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_21_R6.FakeArmorStand_1_21_R6
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_21_R6(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_21_R6.GameRuleGetter1_21_R6
Type: Class
Implements: me.casperge.interfaces.GameRuleGetter

Methods:
- void SetIntegerGameRule(GameRuleType, World, Integer)
- Integer GetIntegerGameRule(GameRuleType, World)
- void SetBooleanGameRule(GameRuleType, World, Boolean)
- Boolean GetBooleanGameRule(GameRuleType, World)

### Class: me.casperge.realisticseasons1_21_R6.NmsCode_21_R6
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getSectionCount(World)
- **static** void setLeafLitterCount(Block, int)
- Class<*> getCbClass(String)
- **static** boolean isLeafLitter(Material)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- int getMaxHeight(World)
- **static** void setWolfVariant(Wolf, int)
- String getBiome(int)
- float getBiomeTemperature(String)
- **static** Material getLeafLitter()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)

### Class: me.casperge.realisticseasons1_21_R6.ProtocolLibUtils1_21_R6
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int, boolean)

## Package: me.casperge.realisticseasons1_21_R7

### Class: me.casperge.realisticseasons1_21_R7.CustomBiome1_21_R7
Type: Class
Implements: me.casperge.interfaces.CustomBiome

Constructors:
- CustomBiome1_21_R7(String name, String prename, String originalname)

Methods:
- String getFoliageColor()
- void setFogColor(String)
- float getDepth()
- String getName()
- void setGrassColor(String)
- void setFoliageColor(String)
- void setWaterColor(String)
- void setSkyColor(String)
- void setTemperature(Float)
- String getPreName()
- boolean isFrozen()
- String getFullName()
- void setDepth(Float)
- String getWaterColor()
- float getDownfall()
- String getSkyColor()
- String getGrassColor()
- void setScale(Float)
- GrassType getGrassType()
- int getBiomeID()
- float getScale()
- int hexToDecimal(String)
- void setDownfall(Float)
- void setWaterFogColor(String)
- String getFogColor()
- void setFrozen(Boolean)
- boolean isRegistered()
- float getTemperature()
- String getWaterFogColor()
- void register()

### Class: me.casperge.realisticseasons1_21_R7.FakeArmorStand_1_21_R7
Type: Class
Implements: me.casperge.interfaces.FakeArmorStand

Constructors:
- FakeArmorStand_1_21_R7(World, double, double, double armorstand, double, boolean, boolean, boolean, boolean)

Methods:
- V updatePose(ArmorStandPart, float, float, float, List<Player>)
- float getYaw(ArmorStandPart)
- V sendSpawnPacket(List<Player>)
- void setItemSlot(int, ItemStack)
- V move(Location, List<Player>)
- Location getLocation()
- float getPitch(ArmorStandPart)
- void updateMetaData(Player)
- float getRoll(ArmorStandPart)
- V destroy(List<Player>)

### Class: me.casperge.realisticseasons1_21_R7.GameRuleGetter1_21_R7
Type: Class
Implements: me.casperge.interfaces.GameRuleGetter

Methods:
- void SetIntegerGameRule(GameRuleType, World, Integer)
- Integer GetIntegerGameRule(GameRuleType, World)
- void SetBooleanGameRule(GameRuleType, World, Boolean)
- Boolean GetBooleanGameRule(GameRuleType, World)

### Class: me.casperge.realisticseasons1_21_R7.NmsCode_21_R7
Type: Class
Implements: me.casperge.interfaces.NmsCode

Methods:
- void sendGameStateChangePacket(int, float, Player)
- List<String> getBiomes(String)
- **static** V sendPacket(Player, Packet<*>)
- V resendChunks(List<Chunk>)
- double getTPS()
- List<String> getAllBiomes()
- int getSectionCount(World)
- **static** void setLeafLitterCount(Block, int)
- Class<*> getCbClass(String)
- **static** boolean isLeafLitter(Material)
- boolean isInPowderedSnow(Entity)
- int getMinHeight(World)
- Class<*> getNmsPacketClass(String)
- String getBiomeName(Biome)
- String getBiomeName(Location)
- String getBiomeName(int, int, int, World)
- int getMaxHeight(World)
- **static** void setWolfVariant(Wolf, int)
- String getBiome(int)
- float getBiomeTemperature(String)
- **static** Material getLeafLitter()
- int getBiomeID(Biome)
- int getBiomeID(String)
- List<String> getCustomBiomes(String)
- void changeRegistryLock(boolean)
- void setBlockInNMSChunk(World, int, int, int, int, byte, boolean)
- void setFrozen(Player, boolean)
- Biome[] getAssociatedBiomes(String)
- void refreshChunk(Player, Chunk)
- int[] getBiomeColors(String)

### Class: me.casperge.realisticseasons1_21_R7.ProtocolLibUtils1_21_R7
Type: Class
Implements: me.casperge.interfaces.ProtocolLibUtils

Methods:
- void readPacket(PacketContainer, int, boolean, int, int, HeightAccessor, boolean, int, boolean)
- byte[] toByteArray(ChunkSection[])
- ChunkSection[] extractDataSafe(ClientboundLevelChunkPacketData, int)
- void readPacketOld(PacketContainer, int, boolean, int, int, boolean)

## Package: org.apache.commons.io

### Class: org.apache.commons.io.ByteOrderMark
Type: Class
Implements: java.io.Serializable

Constructors:
- ByteOrderMark(String charsetName, int[] bytes)

Methods:
- int hashCode()
- boolean equals(Object)
- int get(int)
- int length()
- String toString()
- byte[] getBytes()
- String getCharsetName()

### Class: org.apache.commons.io.ByteOrderParser
Type: Class

Methods:
- **static** ByteOrder parseByteOrder(String)

### Class: org.apache.commons.io.Charsets
Type: Class

Methods:
- **static** SortedMap<String, Charset> requiredCharsets()
- **static** Charset toCharset(Charset)
- **static** Charset toCharset(String)

### Class: org.apache.commons.io.CopyUtils
Type: Class

Methods:
- **static** void copy(byte[], OutputStream)
- **static** void copy(byte[], Writer)
- **static** void copy(byte[], Writer, String)
- **static** int copy(InputStream, OutputStream)
- **static** int copy(Reader, Writer)
- **static** void copy(InputStream, Writer)
- **static** void copy(InputStream, Writer, String)
- **static** void copy(Reader, OutputStream)
- **static** void copy(Reader, OutputStream, String)
- **static** void copy(String, OutputStream)
- **static** void copy(String, OutputStream, String)
- **static** void copy(String, Writer)

### Class: org.apache.commons.io.DirectoryWalker
Type: Abstract Class

No public methods found

### Class: org.apache.commons.io.DirectoryWalker$CancelException
Type: Class
Extends: java.io.IOException

Constructors:
- DirectoryWalker$CancelException(String, File file, int depth)

Methods:
- int getDepth()
- File getFile()

### Class: org.apache.commons.io.EndianUtils
Type: Class

Methods:
- **static** float readSwappedFloat(byte[], int)
- **static** float readSwappedFloat(InputStream)
- **static** long readSwappedUnsignedInteger(byte[], int)
- **static** long readSwappedUnsignedInteger(InputStream)
- **static** void writeSwappedDouble(byte[], int, double)
- **static** void writeSwappedDouble(OutputStream, double)
- **static** void writeSwappedFloat(byte[], int, float)
- **static** void writeSwappedFloat(OutputStream, float)
- **static** int readSwappedUnsignedShort(byte[], int)
- **static** int readSwappedUnsignedShort(InputStream)
- **static** long swapLong(long)
- **static** short swapShort(short)
- **static** long readSwappedLong(byte[], int)
- **static** long readSwappedLong(InputStream)
- **static** int readSwappedInteger(byte[], int)
- **static** int readSwappedInteger(InputStream)
- **static** double swapDouble(double)
- **static** void writeSwappedInteger(byte[], int, int)
- **static** void writeSwappedInteger(OutputStream, int)
- **static** int swapInteger(int)
- **static** double readSwappedDouble(byte[], int)
- **static** double readSwappedDouble(InputStream)
- **static** void writeSwappedShort(byte[], int, short)
- **static** void writeSwappedShort(OutputStream, short)
- **static** float swapFloat(float)
- **static** void writeSwappedLong(byte[], int, long)
- **static** void writeSwappedLong(OutputStream, long)
- **static** short readSwappedShort(byte[], int)
- **static** short readSwappedShort(InputStream)

### Class: org.apache.commons.io.FileCleaner
Type: Class

Methods:
- **static** void exitWhenFinished()
- **static** FileCleaningTracker getInstance()
- **static** void track(File, Object)
- **static** void track(File, Object, FileDeleteStrategy)
- **static** void track(String, Object)
- **static** void track(String, Object, FileDeleteStrategy)
- **static** int getTrackCount()

### Class: org.apache.commons.io.FileCleaningTracker
Type: Class

Methods:
- void exitWhenFinished()
- List<String> getDeleteFailures()
- void track(File, Object)
- void track(File, Object, FileDeleteStrategy)
- void track(String, Object)
- void track(String, Object, FileDeleteStrategy)
- int getTrackCount()

### Class: org.apache.commons.io.FileDeleteStrategy
Type: Class

Methods:
- String toString()
- void delete(File)
- boolean deleteQuietly(File)

### Class: org.apache.commons.io.FileExistsException
Type: Class
Extends: java.io.IOException

No public methods found

### Class: org.apache.commons.io.FileSystem
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- GENERIC
- LINUX
- MAC_OSX
- WINDOWS

Methods:
- boolean isCaseSensitive()
- char[] getIllegalFileNameChars()
- boolean isReservedFileName(CharSequence)
- boolean isLegalFileName(CharSequence)
- boolean isCasePreserving()
- int getMaxFileNameLength()
- **static** FileSystem valueOf(String)
- **static** FileSystem[] values()
- int getMaxPathLength()
- boolean supportsDriveLetter()
- **static** FileSystem getCurrent()
- String toLegalFileName(String, char)
- String[] getReservedFileNames()

### Class: org.apache.commons.io.FileSystemUtils
Type: Class

Methods:
- **static** long freeSpaceKb(String)
- **static** long freeSpaceKb(String, long)
- **static** long freeSpaceKb()
- **static** long freeSpaceKb(long)
- **static** long freeSpace(String)

### Class: org.apache.commons.io.FileUtils
Type: Class

Methods:
- **static** void forceMkdir(File)
- **static** long sizeOf(File)
- **static** BigInteger sizeOfAsBigInteger(File)
- **static** File convertFileCollectionToFileArray(Collection<File>)
- **static** boolean isFileOlder(File, ChronoLocalDate)
- **static** boolean isFileOlder(File, ChronoLocalDate, LocalTime)
- **static** Z isFileOlder(File, ChronoLocalDateTime<*>)
- **static** Z isFileOlder(File, ChronoLocalDateTime<*>, ZoneId)
- **static** Z isFileOlder(File, ChronoZonedDateTime<*>)
- **static** boolean isFileOlder(File, Date)
- **static** boolean isFileOlder(File, File)
- **static** boolean isFileOlder(File, Instant)
- **static** boolean isFileOlder(File, long)
- **static** File getFile(File, String[])
- **static** File getFile(String[])
- **static** void writeByteArrayToFile(File, byte[])
- **static** void writeByteArrayToFile(File, byte[], boolean)
- **static** void writeByteArrayToFile(File, byte[], int, int)
- **static** void writeByteArrayToFile(File, byte[], int, int, boolean)
- **static** void copyToFile(InputStream, File)
- **static** void copyDirectoryToDirectory(File, File)
- **static** boolean contentEqualsIgnoreEOL(File, File, String)
- **static** Collection<File> listFilesAndDirs(File, IOFileFilter, IOFileFilter)
- **static** void writeStringToFile(File, String)
- **static** void writeStringToFile(File, String, boolean)
- **static** void writeStringToFile(File, String, Charset)
- **static** void writeStringToFile(File, String, Charset, boolean)
- **static** void writeStringToFile(File, String, String)
- **static** void writeStringToFile(File, String, String, boolean)
- **static** BigInteger sizeOfDirectoryAsBigInteger(File)
- **static** List<String> readLines(File)
- **static** List<String> readLines(File, Charset)
- **static** List<String> readLines(File, String)
- **static** long lastModifiedUnchecked(File)
- **static** void write(File, CharSequence)
- **static** void write(File, CharSequence, boolean)
- **static** void write(File, CharSequence, Charset)
- **static** void write(File, CharSequence, Charset, boolean)
- **static** void write(File, CharSequence, String)
- **static** void write(File, CharSequence, String, boolean)
- **static** boolean waitFor(File, int)
- **static** FileInputStream openInputStream(File)
- **static** boolean deleteQuietly(File)
- **static** LineIterator lineIterator(File)
- **static** LineIterator lineIterator(File, String)
- **static** File createParentDirectories(File)
- **static** void moveToDirectory(File, File, boolean)
- **static** void touch(File)
- **static** String getUserDirectoryPath()
- **static** void copyInputStreamToFile(InputStream, File)
- **static** File getTempDirectory()
- **static** void moveFile(File, File)
- **static** void moveFile(File, File, CopyOption[])
- **static** String byteCountToDisplaySize(BigInteger)
- **static** String byteCountToDisplaySize(long)
- **static** void moveDirectoryToDirectory(File, File, boolean)
- **static** String readFileToString(File)
- **static** String readFileToString(File, Charset)
- **static** String readFileToString(File, String)
- **static** File toFile(URL)
- **static** Iterator<File> iterateFilesAndDirs(File, IOFileFilter, IOFileFilter)
- **static** long lastModified(File)
- **static** File getUserDirectory()
- **static** boolean isSymlink(File)
- **static** void deleteDirectory(File)
- **static** boolean isDirectory(File, LinkOption[])
- **static** void forceMkdirParent(File)
- **static** void copyToDirectory(File, File)
- **static** V copyToDirectory(Iterable<File>, File)
- **static** void copyFile(File, File)
- **static** void copyFile(File, File, boolean)
- **static** void copyFile(File, File, boolean, CopyOption[])
- **static** void copyFile(File, File, CopyOption[])
- **static** long copyFile(File, OutputStream)
- **static** URL[] toURLs(File[])
- **static** Stream<File> streamFiles(File, boolean, String)
- **static** File delete(File)
- **static** void cleanDirectory(File)
- **static** void copyURLToFile(URL, File)
- **static** void copyURLToFile(URL, File, int, int)
- **static** void copyFileToDirectory(File, File)
- **static** void copyFileToDirectory(File, File, boolean)
- **static** void forceDelete(File)
- **static** Checksum checksum(File, Checksum)
- **static** FileOutputStream openOutputStream(File)
- **static** FileOutputStream openOutputStream(File, boolean)
- **static** void moveDirectory(File, File)
- **static** String getTempDirectoryPath()
- **static** Collection<File> listFiles(File, IOFileFilter, IOFileFilter)
- **static** Collection<File> listFiles(File, String, boolean)
- **static** byte[] readFileToByteArray(File)
- **static** boolean directoryContains(File, File)
- **static** V writeLines(File, Collection<*>)
- **static** V writeLines(File, Collection<*>, boolean)
- **static** V writeLines(File, Collection<*>, String)
- **static** V writeLines(File, Collection<*>, String, boolean)
- **static** V writeLines(File, String, Collection<*>)
- **static** V writeLines(File, String, Collection<*>, boolean)
- **static** V writeLines(File, String, Collection<*>, String)
- **static** V writeLines(File, String, Collection<*>, String, boolean)
- **static** Iterator<File> iterateFiles(File, IOFileFilter, IOFileFilter)
- **static** Iterator<File> iterateFiles(File, String, boolean)
- **static** boolean contentEquals(File, File)
- **static** boolean isRegularFile(File, LinkOption[])
- **static** void forceDeleteOnExit(File)
- **static** void moveFileToDirectory(File, File, boolean)
- **static** long sizeOfDirectory(File)
- **static** void copyDirectory(File, File)
- **static** void copyDirectory(File, File, boolean)
- **static** void copyDirectory(File, File, FileFilter)
- **static** void copyDirectory(File, File, FileFilter, boolean)
- **static** void copyDirectory(File, File, FileFilter, boolean, CopyOption[])
- **static** File[] toFiles(URL[])
- **static** boolean isFileNewer(File, ChronoLocalDate)
- **static** boolean isFileNewer(File, ChronoLocalDate, LocalTime)
- **static** Z isFileNewer(File, ChronoLocalDateTime<*>)
- **static** Z isFileNewer(File, ChronoLocalDateTime<*>, ZoneId)
- **static** Z isFileNewer(File, ChronoZonedDateTime<*>)
- **static** boolean isFileNewer(File, Date)
- **static** boolean isFileNewer(File, File)
- **static** boolean isFileNewer(File, Instant)
- **static** boolean isFileNewer(File, long)
- **static** long checksumCRC32(File)
- **static** boolean isEmptyDirectory(File)

### Class: org.apache.commons.io.FilenameUtils
Type: Class

Methods:
- **static** String removeExtension(String)
- **static** String getName(String)
- **static** boolean wildcardMatch(String, String)
- **static** boolean wildcardMatch(String, String, IOCase)
- **static** boolean wildcardMatchOnSystem(String, String)
- **static** String getBaseName(String)
- **static** boolean equalsNormalized(String, String)
- **static** int indexOfExtension(String)
- **static** boolean isExtension(String, String)
- **static** boolean isExtension(String, String[])
- **static** Z isExtension(String, Collection<String>)
- **static** boolean equalsNormalizedOnSystem(String, String)
- **static** String normalize(String)
- **static** String normalize(String, boolean)
- **static** String getPath(String)
- **static** String getPathNoEndSeparator(String)
- **static** String separatorsToWindows(String)
- **static** boolean equalsOnSystem(String, String)
- **static** String getFullPathNoEndSeparator(String)
- **static** boolean directoryContains(String, String)
- **static** String getExtension(String)
- **static** String getPrefix(String)
- **static** String getFullPath(String)
- **static** String separatorsToSystem(String)
- **static** int indexOfLastSeparator(String)
- **static** String concat(String, String)
- **static** int getPrefixLength(String)
- **static** boolean equals(String, String)
- **static** boolean equals(String, String, boolean, IOCase)
- **static** String normalizeNoEndSeparator(String)
- **static** String normalizeNoEndSeparator(String, boolean)
- **static** String separatorsToUnix(String)

### Class: org.apache.commons.io.HexDump
Type: Class

Methods:
- **static** void dump(byte[], long, OutputStream, int)

### Class: org.apache.commons.io.IOCase
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- SENSITIVE
- INSENSITIVE
- SYSTEM

Methods:
- String getName()
- **static** boolean isCaseSensitive(IOCase)
- boolean isCaseSensitive()
- boolean checkEquals(String, String)
- **static** IOCase forName(String)
- boolean checkEndsWith(String, String)
- boolean checkStartsWith(String, String)
- **static** IOCase valueOf(String)
- int checkIndexOf(String, int, String)
- **static** IOCase[] values()
- String toString()
- boolean checkRegionMatches(String, int, String)
- int checkCompareTo(String, String)

### Class: org.apache.commons.io.IOExceptionList
Type: Class
Extends: java.io.IOException

Constructors:
- IOExceptionList(String, List<Throwable> causeList)

Methods:
- List<TT> getCauseList()
- List<TT> getCauseList(Class<TT>)
- TT getCause(int)
- TT getCause(int, Class<TT>)

### Class: org.apache.commons.io.IOExceptionWithCause
Type: Class
Extends: java.io.IOException

No public methods found

### Class: org.apache.commons.io.IOIndexedException
Type: Class
Extends: java.io.IOException

Constructors:
- IOIndexedException(int index, Throwable)

Methods:
- int getIndex()

### Class: org.apache.commons.io.IOUtils
Type: Class

Methods:
- **static** URL resourceToURL(String)
- **static** URL resourceToURL(String, ClassLoader)
- **static** char[] toCharArray(InputStream)
- **static** char[] toCharArray(InputStream, Charset)
- **static** char[] toCharArray(InputStream, String)
- **static** char[] toCharArray(Reader)
- **static** BufferedReader toBufferedReader(Reader)
- **static** BufferedReader toBufferedReader(Reader, int)
- **static** long skip(InputStream, long)
- **static** long skip(ReadableByteChannel, long)
- **static** long skip(Reader, long)
- **static** long consume(InputStream)
- **static** String resourceToString(String, Charset)
- **static** String resourceToString(String, Charset, ClassLoader)
- **static** boolean contentEqualsIgnoreEOL(Reader, Reader)
- **static** void readFully(InputStream, byte[])
- **static** void readFully(InputStream, byte[], int, int)
- **static** byte[] readFully(InputStream, int)
- **static** void readFully(ReadableByteChannel, ByteBuffer)
- **static** void readFully(Reader, char[])
- **static** void readFully(Reader, char[], int, int)
- **static** List<String> readLines(InputStream)
- **static** List<String> readLines(InputStream, Charset)
- **static** List<String> readLines(InputStream, String)
- **static** List<String> readLines(Reader)
- **static** int copy(InputStream, OutputStream)
- **static** long copy(InputStream, OutputStream, int)
- **static** void copy(InputStream, Writer)
- **static** void copy(InputStream, Writer, Charset)
- **static** void copy(InputStream, Writer, String)
- **static** long copy(Reader, Appendable)
- **static** long copy(Reader, Appendable, CharBuffer)
- **static** void copy(Reader, OutputStream)
- **static** void copy(Reader, OutputStream, Charset)
- **static** void copy(Reader, OutputStream, String)
- **static** int copy(Reader, Writer)
- **static** long copy(URL, File)
- **static** long copy(URL, OutputStream)
- **static** BufferedInputStream buffer(InputStream)
- **static** BufferedInputStream buffer(InputStream, int)
- **static** BufferedOutputStream buffer(OutputStream)
- **static** BufferedOutputStream buffer(OutputStream, int)
- **static** BufferedReader buffer(Reader)
- **static** BufferedReader buffer(Reader, int)
- **static** BufferedWriter buffer(Writer)
- **static** BufferedWriter buffer(Writer, int)
- **static** void write(byte[], OutputStream)
- **static** void write(byte[], Writer)
- **static** void write(byte[], Writer, Charset)
- **static** void write(byte[], Writer, String)
- **static** void write(char[], OutputStream)
- **static** void write(char[], OutputStream, Charset)
- **static** void write(char[], OutputStream, String)
- **static** void write(char[], Writer)
- **static** void write(CharSequence, OutputStream)
- **static** void write(CharSequence, OutputStream, Charset)
- **static** void write(CharSequence, OutputStream, String)
- **static** void write(CharSequence, Writer)
- **static** void write(String, OutputStream)
- **static** void write(String, OutputStream, Charset)
- **static** void write(String, OutputStream, String)
- **static** void write(String, Writer)
- **static** void write(StringBuffer, OutputStream)
- **static** void write(StringBuffer, OutputStream, String)
- **static** void write(StringBuffer, Writer)
- **static** void close(Closeable)
- **static** void close(Closeable[])
- **static** V close(Closeable, IOConsumer<IOException>)
- **static** void close(URLConnection)
- **static** LineIterator lineIterator(InputStream, Charset)
- **static** LineIterator lineIterator(InputStream, String)
- **static** LineIterator lineIterator(Reader)
- **static** int read(InputStream, byte[])
- **static** int read(InputStream, byte[], int, int)
- **static** int read(ReadableByteChannel, ByteBuffer)
- **static** int read(Reader, char[])
- **static** int read(Reader, char[], int, int)
- **static** V writeLines(Collection<*>, String, OutputStream)
- **static** V writeLines(Collection<*>, String, OutputStream, Charset)
- **static** V writeLines(Collection<*>, String, OutputStream, String)
- **static** V writeLines(Collection<*>, String, Writer)
- **static** boolean contentEquals(InputStream, InputStream)
- **static** boolean contentEquals(Reader, Reader)
- **static** byte[] byteArray()
- **static** byte[] byteArray(int)
- **static** int length(byte[])
- **static** int length(char[])
- **static** int length(CharSequence)
- **static** int length(Object[])
- **static** InputStream toBufferedInputStream(InputStream)
- **static** InputStream toBufferedInputStream(InputStream, int)
- **static** void writeChunked(byte[], OutputStream)
- **static** void writeChunked(char[], Writer)
- **static** long copyLarge(InputStream, OutputStream)
- **static** long copyLarge(InputStream, OutputStream, byte[])
- **static** long copyLarge(InputStream, OutputStream, long, long)
- **static** long copyLarge(InputStream, OutputStream, long, long, byte[])
- **static** long copyLarge(Reader, Writer)
- **static** long copyLarge(Reader, Writer, char[])
- **static** long copyLarge(Reader, Writer, long, long)
- **static** long copyLarge(Reader, Writer, long, long, char[])
- **static** void skipFully(InputStream, long)
- **static** void skipFully(ReadableByteChannel, long)
- **static** void skipFully(Reader, long)
- **static** byte[] toByteArray(InputStream)
- **static** byte[] toByteArray(InputStream, int)
- **static** byte[] toByteArray(InputStream, long)
- **static** byte[] toByteArray(Reader)
- **static** byte[] toByteArray(Reader, Charset)
- **static** byte[] toByteArray(Reader, String)
- **static** byte[] toByteArray(String)
- **static** byte[] toByteArray(URI)
- **static** byte[] toByteArray(URL)
- **static** byte[] toByteArray(URLConnection)
- **static** String toString(byte[])
- **static** String toString(byte[], String)
- **static** String toString(InputStream)
- **static** String toString(InputStream, Charset)
- **static** String toString(InputStream, String)
- **static** String toString(Reader)
- **static** String toString(URI)
- **static** String toString(URI, Charset)
- **static** String toString(URI, String)
- **static** String toString(URL)
- **static** String toString(URL, Charset)
- **static** String toString(URL, String)
- **static** Writer writer(Appendable)
- **static** void closeQuietly(Closeable)
- **static** void closeQuietly(Closeable[])
- **static** V closeQuietly(Closeable, Consumer<IOException>)
- **static** void closeQuietly(InputStream)
- **static** void closeQuietly(OutputStream)
- **static** void closeQuietly(Reader)
- **static** void closeQuietly(Selector)
- **static** void closeQuietly(ServerSocket)
- **static** void closeQuietly(Socket)
- **static** void closeQuietly(Writer)
- **static** byte[] resourceToByteArray(String)
- **static** byte[] resourceToByteArray(String, ClassLoader)
- **static** InputStream toInputStream(CharSequence)
- **static** InputStream toInputStream(CharSequence, Charset)
- **static** InputStream toInputStream(CharSequence, String)
- **static** InputStream toInputStream(String)
- **static** InputStream toInputStream(String, Charset)
- **static** InputStream toInputStream(String, String)

### Class: org.apache.commons.io.LineIterator
Type: Class
Implements: java.util.Iterator, java.io.Closeable

Constructors:
- LineIterator(Reader bufferedReader)

Methods:
- String next()
- Object next()
- String nextLine()
- boolean hasNext()
- **static** void closeQuietly(LineIterator)
- void close()
- void remove()

### Class: org.apache.commons.io.StandardLineSeparator
Type: Enum
Extends: java.lang.Enum

Enum Constants:
- CR
- CRLF
- LF

Methods:
- **static** StandardLineSeparator valueOf(String)
- **static** StandardLineSeparator[] values()
- String getString()
- byte[] getBytes(Charset)

### Class: org.apache.commons.io.TaggedIOException
Type: Class
Extends: org.apache.commons.io.IOExceptionWithCause

Constructors:
- TaggedIOException(IOException, Serializable tag)

Methods:
- **static** void throwCauseIfTaggedWith(Throwable, Object)
- **static** boolean isTaggedWith(Throwable, Object)
- Serializable getTag()
- IOException getCause()
- Throwable getCause()

## Package: org.apache.commons.io.comparator

### Class: org.apache.commons.io.comparator.CompositeFileComparator
Type: Class
Extends: org.apache.commons.io.comparator.AbstractFileComparator
Implements: java.io.Serializable

Constructors:
- CompositeFileComparator(Comparator<File> delegates)
- CompositeFileComparator(Iterable<Comparator<File>> delegates)

Methods:
- int compare(File, File)
- int compare(Object, Object)
- String toString()
- List sort(List)
- File[] sort(File[])

### Class: org.apache.commons.io.comparator.DefaultFileComparator
Type: Class
Extends: org.apache.commons.io.comparator.AbstractFileComparator
Implements: java.io.Serializable

Methods:
- int compare(File, File)
- int compare(Object, Object)
- String toString()
- List sort(List)
- File[] sort(File[])

### Class: org.apache.commons.io.comparator.DirectoryFileComparator
Type: Class
Extends: org.apache.commons.io.comparator.AbstractFileComparator
Implements: java.io.Serializable

Methods:
- int compare(File, File)
- int compare(Object, Object)
- String toString()
- List sort(List)
- File[] sort(File[])

### Class: org.apache.commons.io.comparator.ExtensionFileComparator
Type: Class
Extends: org.apache.commons.io.comparator.AbstractFileComparator
Implements: java.io.Serializable

Constructors:
- ExtensionFileComparator(IOCase caseSensitivity)

Methods:
- int compare(File, File)
- int compare(Object, Object)
- String toString()
- List sort(List)
- File[] sort(File[])

### Class: org.apache.commons.io.comparator.LastModifiedFileComparator
Type: Class
Extends: org.apache.commons.io.comparator.AbstractFileComparator
Implements: java.io.Serializable

Methods:
- int compare(File, File)
- int compare(Object, Object)
- String toString()
- List sort(List)
- File[] sort(File[])

### Class: org.apache.commons.io.comparator.NameFileComparator
Type: Class
Extends: org.apache.commons.io.comparator.AbstractFileComparator
Implements: java.io.Serializable

Constructors:
- NameFileComparator(IOCase caseSensitivity)

Methods:
- int compare(File, File)
- int compare(Object, Object)
- String toString()
- List sort(List)
- File[] sort(File[])

### Class: org.apache.commons.io.comparator.PathFileComparator
Type: Class
Extends: org.apache.commons.io.comparator.AbstractFileComparator
Implements: java.io.Serializable

Constructors:
- PathFileComparator(IOCase caseSensitivity)

Methods:
- int compare(File, File)
- int compare(Object, Object)
- String toString()
- List sort(List)
- File[] sort(File[])

### Class: org.apache.commons.io.comparator.SizeFileComparator
Type: Class
Extends: org.apache.commons.io.comparator.AbstractFileComparator
Implements: java.io.Serializable

Constructors:
- SizeFileComparator(boolean sumDirectoryContents)

Methods:
- int compare(File, File)
- int compare(Object, Object)
- String toString()
- List sort(List)
- File[] sort(File[])

## Package: org.apache.commons.io.file

### Class: org.apache.commons.io.file.Counters$Counter
Type: Interface

Methods:
- Long getLong()
- void add(long)
- BigInteger getBigInteger()
- long get()
- void reset()
- void increment()

### Class: org.apache.commons.io.file.Counters$PathCounters
Type: Interface

Methods:
- Counters$Counter getFileCounter()
- void reset()
- Counters$Counter getByteCounter()
- Counters$Counter getDirectoryCounter()

### Class: org.apache.commons.io.file.DeleteOption
Type: Interface

No public methods found

### Class: org.apache.commons.io.file.PathFilter
Type: Interface

Methods:
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.file.PathVisitor
Type: Interface
Implements: java.nio.file.FileVisitor

No public methods found

### Class: org.apache.commons.io.file.AccumulatorPathVisitor
Type: Class
Extends: org.apache.commons.io.file.CountingPathVisitor

Constructors:
- AccumulatorPathVisitor(Counters$PathCounters dirList)
- AccumulatorPathVisitor(Counters$PathCounters, PathFilter, PathFilter dirList)

Methods:
- int hashCode()
- List<Path> getDirList()
- boolean equals(Object)
- **static** AccumulatorPathVisitor withBigIntegerCounters()
- **static** AccumulatorPathVisitor withBigIntegerCounters(PathFilter, PathFilter)
- List<Path> relativizeDirectories(Path, boolean, Comparator<Path>)
- **static** AccumulatorPathVisitor withLongCounters()
- **static** AccumulatorPathVisitor withLongCounters(PathFilter, PathFilter)
- List<Path> relativizeFiles(Path, boolean, Comparator<Path>)
- List<Path> getFileList()

### Class: org.apache.commons.io.file.CleaningPathVisitor
Type: Class
Extends: org.apache.commons.io.file.CountingPathVisitor

Constructors:
- CleaningPathVisitor(Counters$PathCounters, DeleteOption[] overrideReadOnly, String[] skip)

Methods:
- FileVisitResult visitFile(Path, BasicFileAttributes)
- FileVisitResult visitFile(Object, BasicFileAttributes)
- int hashCode()
- boolean equals(Object)
- **static** CountingPathVisitor withBigIntegerCounters()
- **static** CountingPathVisitor withLongCounters()
- FileVisitResult preVisitDirectory(Path, BasicFileAttributes)
- FileVisitResult preVisitDirectory(Object, BasicFileAttributes)

### Class: org.apache.commons.io.file.CopyDirectoryVisitor
Type: Class
Extends: org.apache.commons.io.file.CountingPathVisitor

Constructors:
- CopyDirectoryVisitor(Counters$PathCounters, Path sourceDirectory, Path targetDirectory, CopyOption[] copyOptions)
- CopyDirectoryVisitor(Counters$PathCounters, PathFilter, PathFilter, Path sourceDirectory, Path targetDirectory, CopyOption[] copyOptions)

Methods:
- FileVisitResult visitFile(Path, BasicFileAttributes)
- FileVisitResult visitFile(Object, BasicFileAttributes)
- int hashCode()
- boolean equals(Object)
- Path getTargetDirectory()
- Path getSourceDirectory()
- CopyOption[] getCopyOptions()
- FileVisitResult preVisitDirectory(Path, BasicFileAttributes)
- FileVisitResult preVisitDirectory(Object, BasicFileAttributes)

### Class: org.apache.commons.io.file.Counters
Type: Class

Methods:
- **static** Counters$Counter longCounter()
- **static** Counters$PathCounters noopPathCounters()
- **static** Counters$Counter noopCounter()
- **static** Counters$PathCounters longPathCounters()
- **static** Counters$Counter bigIntegerCounter()
- **static** Counters$PathCounters bigIntegerPathCounters()

### Class: org.apache.commons.io.file.CountingPathVisitor
Type: Class
Extends: org.apache.commons.io.file.SimplePathVisitor

Constructors:
- CountingPathVisitor(Counters$PathCounters pathCounters, PathFilter fileFilter, PathFilter dirFilter)

Methods:
- FileVisitResult postVisitDirectory(Path, IOException)
- FileVisitResult postVisitDirectory(Object, IOException)
- FileVisitResult visitFile(Path, BasicFileAttributes)
- FileVisitResult visitFile(Object, BasicFileAttributes)
- int hashCode()
- Counters$PathCounters getPathCounters()
- boolean equals(Object)
- **static** CountingPathVisitor withBigIntegerCounters()
- String toString()
- **static** CountingPathVisitor withLongCounters()
- FileVisitResult preVisitDirectory(Path, BasicFileAttributes)
- FileVisitResult preVisitDirectory(Object, BasicFileAttributes)

### Class: org.apache.commons.io.file.DeletingPathVisitor
Type: Class
Extends: org.apache.commons.io.file.CountingPathVisitor

Constructors:
- DeletingPathVisitor(Counters$PathCounters, LinkOption[] linkOptions, DeleteOption[] overrideReadOnly, String[] skip)

Methods:
- FileVisitResult postVisitDirectory(Path, IOException)
- FileVisitResult postVisitDirectory(Object, IOException)
- FileVisitResult visitFile(Path, BasicFileAttributes)
- FileVisitResult visitFile(Object, BasicFileAttributes)
- int hashCode()
- boolean equals(Object)
- **static** DeletingPathVisitor withBigIntegerCounters()
- **static** DeletingPathVisitor withLongCounters()
- FileVisitResult preVisitDirectory(Path, BasicFileAttributes)
- FileVisitResult preVisitDirectory(Object, BasicFileAttributes)

### Class: org.apache.commons.io.file.DirectoryStreamFilter
Type: Class
Implements: java.nio.file.DirectoryStream$Filter

Constructors:
- DirectoryStreamFilter(PathFilter pathFilter)

Methods:
- PathFilter getPathFilter()
- boolean accept(Path)
- boolean accept(Object)

### Class: org.apache.commons.io.file.NoopPathVisitor
Type: Class
Extends: org.apache.commons.io.file.SimplePathVisitor

No public methods found

### Class: org.apache.commons.io.file.PathUtils
Type: Class

Methods:
- **static** Path copyFile(URL, Path, CopyOption[])
- **static** TT visitFileTree(T, T)
- **static** TT visitFileTree(T, T, ;, Path)
- **static** TT visitFileTree(T, T, ;)
- **static** TT visitFileTree(T, T)
- **static** BasicFileAttributes readBasicFileAttributesUnchecked(Path)
- **static** boolean isEmptyFile(Path)
- **static** Counters$PathCounters delete(Path)
- **static** Counters$PathCounters delete(Path, DeleteOption[])
- **static** Counters$PathCounters delete(Path, LinkOption[], DeleteOption[])
- **static** boolean fileContentEquals(Path, Path)
- **static** boolean fileContentEquals(Path, Path, LinkOption[], OpenOption[])
- **static** Counters$PathCounters cleanDirectory(Path)
- **static** Counters$PathCounters cleanDirectory(Path, DeleteOption[])
- **static** BasicFileAttributes readBasicFileAttributes(Path)
- **static** Path copyFileToDirectory(Path, Path, CopyOption[])
- **static** Path copyFileToDirectory(URL, Path, CopyOption[])
- **static** Path current()
- **static** Counters$PathCounters deleteFile(Path)
- **static** Counters$PathCounters deleteFile(Path, DeleteOption[])
- **static** Counters$PathCounters deleteFile(Path, LinkOption[], DeleteOption[])
- **static** boolean isNewer(Path, long, LinkOption[])
- **static** boolean directoryContentEquals(Path, Path)
- **static** boolean directoryContentEquals(Path, Path, int, LinkOption[], FileVisitOption[])
- **static** Path createParentDirectories(Path, FileAttribute<*>)
- **static** boolean isRegularFile(Path, LinkOption[])
- **static** boolean isEmpty(Path)
- **static** DirectoryStream<Path> newDirectoryStream(Path, PathFilter)
- **static** Path[] filter(PathFilter, Path[])
- **static** Counters$PathCounters copyDirectory(Path, Path, CopyOption[])
- **static** boolean directoryAndFileContentEquals(Path, Path)
- **static** boolean directoryAndFileContentEquals(Path, Path, LinkOption[], OpenOption[], FileVisitOption[])
- **static** List<AclEntry> getAclEntryList(Path)
- **static** boolean isEmptyDirectory(Path)
- **static** Counters$PathCounters deleteDirectory(Path)
- **static** Counters$PathCounters deleteDirectory(Path, DeleteOption[])
- **static** Counters$PathCounters deleteDirectory(Path, LinkOption[], DeleteOption[])
- **static** Counters$PathCounters countDirectory(Path)
- **static** Stream<Path> walk(Path, PathFilter, int, boolean, FileVisitOption)
- **static** Path setReadOnly(Path, boolean, LinkOption[])
- **static** boolean isDirectory(Path, LinkOption[])

### Class: org.apache.commons.io.file.SimplePathVisitor
Type: Abstract Class
Extends: java.nio.file.SimpleFileVisitor
Implements: org.apache.commons.io.file.PathVisitor

No public methods found

### Class: org.apache.commons.io.file.StandardDeleteOption
Type: Enum
Extends: java.lang.Enum
Implements: org.apache.commons.io.file.DeleteOption

Enum Constants:
- OVERRIDE_READ_ONLY

Methods:
- **static** StandardDeleteOption valueOf(String)
- **static** StandardDeleteOption[] values()
- **static** boolean overrideReadOnly(DeleteOption[])

## Package: org.apache.commons.io.file.spi

### Class: org.apache.commons.io.file.spi.FileSystemProviders
Type: Class

Methods:
- **static** FileSystemProviders installed()
- **static** FileSystemProvider getFileSystemProvider(Path)
- FileSystemProvider getFileSystemProvider(String)
- FileSystemProvider getFileSystemProvider(URI)
- FileSystemProvider getFileSystemProvider(URL)

## Package: org.apache.commons.io.filefilter

### Class: org.apache.commons.io.filefilter.ConditionalFileFilter
Type: Interface

Methods:
- boolean removeFileFilter(IOFileFilter)
- V setFileFilters(List<IOFileFilter>)
- List<IOFileFilter> getFileFilters()
- void addFileFilter(IOFileFilter)

### Class: org.apache.commons.io.filefilter.IOFileFilter
Type: Interface
Implements: java.io.FileFilter, java.io.FilenameFilter, org.apache.commons.io.file.PathFilter

Methods:
- IOFileFilter or(IOFileFilter fileFilter)
- IOFileFilter negate()
- IOFileFilter and(IOFileFilter fileFilter)
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path path, BasicFileAttributes attributes)

### Class: org.apache.commons.io.filefilter.AbstractFileFilter
Type: Abstract Class
Implements: org.apache.commons.io.filefilter.IOFileFilter, org.apache.commons.io.file.PathVisitor

Methods:
- FileVisitResult postVisitDirectory(Path, IOException)
- FileVisitResult postVisitDirectory(Object, IOException)
- FileVisitResult visitFile(Path, BasicFileAttributes)
- FileVisitResult visitFile(Object, BasicFileAttributes)
- String toString()
- FileVisitResult visitFileFailed(Path, IOException)
- FileVisitResult visitFileFailed(Object, IOException)
- FileVisitResult preVisitDirectory(Path, BasicFileAttributes)
- FileVisitResult preVisitDirectory(Object, BasicFileAttributes)
- boolean accept(File)
- boolean accept(File, String)

### Class: org.apache.commons.io.filefilter.AgeFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- AgeFileFilter(long cutoffMillis, boolean acceptOlder)

Methods:
- String toString()
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.AndFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: org.apache.commons.io.filefilter.ConditionalFileFilter, java.io.Serializable

Methods:
- boolean removeFileFilter(IOFileFilter)
- V setFileFilters(List<IOFileFilter>)
- String toString()
- List<IOFileFilter> getFileFilters()
- void addFileFilter(IOFileFilter)
- void addFileFilter(IOFileFilter[])
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.CanExecuteFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.CanReadFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.CanWriteFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.DelegateFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- DelegateFileFilter(FileFilter fileFilter)
- DelegateFileFilter(FilenameFilter filenameFilter)

Methods:
- String toString()
- boolean accept(File)
- boolean accept(File, String)

### Class: org.apache.commons.io.filefilter.DirectoryFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.EmptyFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.FalseFileFilter
Type: Class
Implements: org.apache.commons.io.filefilter.IOFileFilter, java.io.Serializable

Methods:
- IOFileFilter or(IOFileFilter)
- IOFileFilter and(IOFileFilter)
- IOFileFilter negate()
- String toString()
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.FileEqualsFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter

Constructors:
- FileEqualsFileFilter(File file)

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.FileFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.FileFilterUtils
Type: Class

Methods:
- **static** IOFileFilter fileFileFilter()
- **static** IOFileFilter or(IOFileFilter[])
- **static** IOFileFilter nameFileFilter(String)
- **static** IOFileFilter nameFileFilter(String, IOCase)
- **static** IOFileFilter magicNumberFileFilter(byte[])
- **static** IOFileFilter magicNumberFileFilter(byte[], long)
- **static** IOFileFilter magicNumberFileFilter(String)
- **static** IOFileFilter magicNumberFileFilter(String, long)
- **static** IOFileFilter makeFileOnly(IOFileFilter)
- **static** IOFileFilter trueFileFilter()
- **static** IOFileFilter sizeRangeFileFilter(long, long)
- **static** List<IOFileFilter> toList(IOFileFilter)
- **static** File[] filter(IOFileFilter, File[])
- **static** File filter(IOFileFilter, Iterable<File>)
- **static** IOFileFilter orFileFilter(IOFileFilter, IOFileFilter)
- **static** IOFileFilter ageFileFilter(Date)
- **static** IOFileFilter ageFileFilter(Date, boolean)
- **static** IOFileFilter ageFileFilter(File)
- **static** IOFileFilter ageFileFilter(File, boolean)
- **static** IOFileFilter ageFileFilter(long)
- **static** IOFileFilter ageFileFilter(long, boolean)
- **static** IOFileFilter prefixFileFilter(String)
- **static** IOFileFilter prefixFileFilter(String, IOCase)
- **static** IOFileFilter asFileFilter(FileFilter)
- **static** IOFileFilter asFileFilter(FilenameFilter)
- **static** IOFileFilter andFileFilter(IOFileFilter, IOFileFilter)
- **static** IOFileFilter and(IOFileFilter[])
- **static** IOFileFilter directoryFileFilter()
- **static** IOFileFilter notFileFilter(IOFileFilter)
- **static** IOFileFilter falseFileFilter()
- **static** List<File> filterList(IOFileFilter, File)
- **static** List<File> filterList(IOFileFilter, Iterable<File>)
- **static** IOFileFilter makeSVNAware(IOFileFilter)
- **static** IOFileFilter makeCVSAware(IOFileFilter)
- **static** Set<File> filterSet(IOFileFilter, File)
- **static** Set<File> filterSet(IOFileFilter, Iterable<File>)
- **static** IOFileFilter sizeFileFilter(long)
- **static** IOFileFilter sizeFileFilter(long, boolean)
- **static** IOFileFilter suffixFileFilter(String)
- **static** IOFileFilter suffixFileFilter(String, IOCase)
- **static** IOFileFilter makeDirectoryOnly(IOFileFilter)

### Class: org.apache.commons.io.filefilter.HiddenFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.MagicNumberFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- MagicNumberFileFilter(byte[] magicNumbers, long byteOffset)
- MagicNumberFileFilter(String magicNumbers, long byteOffset)

Methods:
- String toString()
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.NameFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- NameFileFilter(List<String> names, IOCase caseSensitivity)
- NameFileFilter(String names, IOCase caseSensitivity)
- NameFileFilter(String[] names, IOCase caseSensitivity)

Methods:
- String toString()
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.NotFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- NotFileFilter(IOFileFilter filter)

Methods:
- String toString()
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.OrFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: org.apache.commons.io.filefilter.ConditionalFileFilter, java.io.Serializable

Methods:
- boolean removeFileFilter(IOFileFilter)
- V setFileFilters(List<IOFileFilter>)
- String toString()
- List<IOFileFilter> getFileFilters()
- void addFileFilter(IOFileFilter)
- void addFileFilter(IOFileFilter[])
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.PathEqualsFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter

Constructors:
- PathEqualsFileFilter(Path path)

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.PathVisitorFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter

Constructors:
- PathVisitorFileFilter(PathVisitor pathVisitor)

Methods:
- FileVisitResult visitFile(Path, BasicFileAttributes)
- FileVisitResult visitFile(Object, BasicFileAttributes)
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.PrefixFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- PrefixFileFilter(List<String> prefixes, IOCase caseSensitivity)
- PrefixFileFilter(String prefixes, IOCase caseSensitivity)
- PrefixFileFilter(String[] prefixes, IOCase caseSensitivity)

Methods:
- String toString()
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.RegexFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- RegexFileFilter(Pattern pattern, Function<Path, String> pathToString)

Methods:
- String toString()
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.SizeFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- SizeFileFilter(long size, boolean acceptLarger)

Methods:
- FileVisitResult visitFile(Path, BasicFileAttributes)
- FileVisitResult visitFile(Object, BasicFileAttributes)
- String toString()
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.SuffixFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- SuffixFileFilter(List<String> suffixes, IOCase caseSensitivity)
- SuffixFileFilter(String suffixes, IOCase caseSensitivity)
- SuffixFileFilter(String[] suffixes, IOCase caseSensitivity)

Methods:
- String toString()
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.SymbolicLinkFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.TrueFileFilter
Type: Class
Implements: org.apache.commons.io.filefilter.IOFileFilter, java.io.Serializable

Methods:
- IOFileFilter or(IOFileFilter)
- IOFileFilter and(IOFileFilter)
- IOFileFilter negate()
- String toString()
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.WildcardFileFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- WildcardFileFilter(List<String> wildcards, IOCase caseSensitivity)
- WildcardFileFilter(String wildcards, IOCase caseSensitivity)
- WildcardFileFilter(String[] wildcards, IOCase caseSensitivity)

Methods:
- String toString()
- boolean accept(File)
- boolean accept(File, String)
- FileVisitResult accept(Path, BasicFileAttributes)

### Class: org.apache.commons.io.filefilter.WildcardFilter
Type: Class
Extends: org.apache.commons.io.filefilter.AbstractFileFilter
Implements: java.io.Serializable

Constructors:
- WildcardFilter(List<String> wildcards)
- WildcardFilter(String wildcards)
- WildcardFilter(String[] wildcards)

Methods:
- boolean accept(File)
- FileVisitResult accept(Path, BasicFileAttributes)
- boolean accept(File, String)

## Package: org.apache.commons.io.function

### Class: org.apache.commons.io.function.IOConsumer
Type: Interface

Methods:
- **static** IOConsumer<TT> noop()
- IOConsumer<TT> andThen(IOConsumer<-TT> after)
- V accept(T) throws IOException

### Class: org.apache.commons.io.function.IOFunction
Type: Interface

Methods:
- IOFunction<TV, TR> compose(IOFunction<-TV, +TT> before)
- IOFunction<TV, TR> compose(Function<-TV, +TT> before)
- IOSupplier<TR> compose(IOSupplier<+TT> before)
- IOSupplier<TR> compose(Supplier<+TT> before)
- TR apply(T) throws IOException
- **static** IOFunction<TT, TT> identity()
- IOFunction<TT, TV> andThen(IOFunction<-TR, +TV> after)
- IOFunction<TT, TV> andThen(Function<-TR, +TV> after)
- IOConsumer<TT> andThen(IOConsumer<-TR> after)
- IOConsumer<TT> andThen(Consumer<-TR> after)

### Class: org.apache.commons.io.function.IOSupplier
Type: Interface

Methods:
- TT get() throws IOException

## Package: org.apache.commons.io.input

### Class: org.apache.commons.io.input.TailerListener
Type: Interface

Methods:
- void fileRotated()
- void init(Tailer)
- void handle(String)
- void handle(Exception)
- void fileNotFound()

### Class: org.apache.commons.io.input.AbstractCharacterFilterReader
Type: Abstract Class
Extends: java.io.FilterReader

Methods:
- int read()
- int read(char[], int, int)

### Class: org.apache.commons.io.input.AutoCloseInputStream
Type: Class
Extends: org.apache.commons.io.input.ProxyInputStream

Methods:
- void close()

### Class: org.apache.commons.io.input.BOMInputStream
Type: Class
Extends: org.apache.commons.io.input.ProxyInputStream

Constructors:
- BOMInputStream(InputStream, boolean include, ByteOrderMark[] boms)

Methods:
- String getBOMCharsetName()
- ByteOrderMark getBOM()
- boolean hasBOM()
- boolean hasBOM(ByteOrderMark)
- int read()
- int read(byte[], int, int)
- int read(byte[])
- void reset()
- long skip(long)
- void mark(int)

### Class: org.apache.commons.io.input.BoundedInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- BoundedInputStream(InputStream in, long max)

Methods:
- void setPropagateClose(boolean)
- int read()
- int read(byte[])
- int read(byte[], int, int)
- boolean isPropagateClose()
- boolean markSupported()
- int available()
- void reset()
- String toString()
- long skip(long)
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.BoundedReader
Type: Class
Extends: java.io.Reader

Constructors:
- BoundedReader(Reader target, int maxCharsFromTargetReader)

Methods:
- int read()
- int read(char[], int, int)
- void reset()
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.BrokenInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- BrokenInputStream(IOException exception)

Methods:
- int read()
- int available()
- void reset()
- long skip(long)
- void close()

### Class: org.apache.commons.io.input.BrokenReader
Type: Class
Extends: java.io.Reader

Constructors:
- BrokenReader(IOException exception)

Methods:
- int read(char[], int, int)
- boolean ready()
- void reset()
- long skip(long)
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.BufferedFileChannelInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- BufferedFileChannelInputStream(Path fileChannel, int byteBuffer)

Methods:
- int read()
- int read(byte[], int, int)
- int available()
- long skip(long)
- void close()

### Class: org.apache.commons.io.input.CharSequenceInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- CharSequenceInputStream(CharSequence cbuf, Charset encoder, int bbuf)

Methods:
- int read(byte[], int, int)
- int read()
- int read(byte[])
- boolean markSupported()
- int available()
- void reset()
- long skip(long)
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.CharSequenceReader
Type: Class
Extends: java.io.Reader
Implements: java.io.Serializable

Constructors:
- CharSequenceReader(CharSequence charSequence, int start, int end)

Methods:
- int read()
- int read(char[], int, int)
- boolean markSupported()
- boolean ready()
- void reset()
- String toString()
- long skip(long)
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.CharacterFilterReader
Type: Class
Extends: org.apache.commons.io.input.AbstractCharacterFilterReader

No public methods found

### Class: org.apache.commons.io.input.CharacterSetFilterReader
Type: Class
Extends: org.apache.commons.io.input.AbstractCharacterFilterReader

No public methods found

### Class: org.apache.commons.io.input.CircularInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- CircularInputStream(byte[] repeatedContent, long targetByteCount)

Methods:
- int read()

### Class: org.apache.commons.io.input.ClassLoaderObjectInputStream
Type: Class
Extends: java.io.ObjectInputStream

Constructors:
- ClassLoaderObjectInputStream(ClassLoader classLoader, InputStream)

No public methods found

### Class: org.apache.commons.io.input.CloseShieldInputStream
Type: Class
Extends: org.apache.commons.io.input.ProxyInputStream

Methods:
- void close()
- **static** CloseShieldInputStream wrap(InputStream)

### Class: org.apache.commons.io.input.CloseShieldReader
Type: Class
Extends: org.apache.commons.io.input.ProxyReader

Methods:
- void close()
- **static** CloseShieldReader wrap(Reader)

### Class: org.apache.commons.io.input.ClosedInputStream
Type: Class
Extends: java.io.InputStream

Methods:
- int read()

### Class: org.apache.commons.io.input.ClosedReader
Type: Class
Extends: java.io.Reader

Methods:
- int read(char[], int, int)
- void close()

### Class: org.apache.commons.io.input.CountingInputStream
Type: Class
Extends: org.apache.commons.io.input.ProxyInputStream

Methods:
- int resetCount()
- long skip(long)
- int getCount()
- long resetByteCount()
- long getByteCount()

### Class: org.apache.commons.io.input.DemuxInputStream
Type: Class
Extends: java.io.InputStream

Methods:
- int read()
- InputStream bindStream(InputStream)
- void close()

### Class: org.apache.commons.io.input.InfiniteCircularInputStream
Type: Class
Extends: org.apache.commons.io.input.CircularInputStream

No public methods found

### Class: org.apache.commons.io.input.MarkShieldInputStream
Type: Class
Extends: org.apache.commons.io.input.ProxyInputStream

Methods:
- boolean markSupported()
- void reset()
- void mark(int)

### Class: org.apache.commons.io.input.MessageDigestCalculatingInputStream
Type: Class
Extends: org.apache.commons.io.input.ObservableInputStream

Constructors:
- MessageDigestCalculatingInputStream(InputStream, MessageDigest messageDigest)

Methods:
- MessageDigest getMessageDigest()

### Class: org.apache.commons.io.input.MessageDigestCalculatingInputStream$MessageDigestMaintainingObserver
Type: Class
Extends: org.apache.commons.io.input.ObservableInputStream$Observer

Constructors:
- MessageDigestCalculatingInputStream$MessageDigestMaintainingObserver(MessageDigest messageDigest)

Methods:
- void data(int)
- void data(byte[], int, int)

### Class: org.apache.commons.io.input.NullInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- NullInputStream(long size, boolean markSupported, boolean throwEofException)

Methods:
- long getSize()
- int read()
- int read(byte[])
- int read(byte[], int, int)
- long getPosition()
- boolean markSupported()
- int available()
- void reset()
- long skip(long)
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.NullReader
Type: Class
Extends: java.io.Reader

Constructors:
- NullReader(long size, boolean markSupported, boolean throwEofException)

Methods:
- long getSize()
- int read()
- int read(char[])
- int read(char[], int, int)
- long getPosition()
- boolean markSupported()
- void reset()
- long skip(long)
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.ObservableInputStream
Type: Class
Extends: org.apache.commons.io.input.ProxyInputStream

Methods:
- void add(ObservableInputStream$Observer)
- int read()
- int read(byte[])
- int read(byte[], int, int)
- List<ObservableInputStream$Observer> getObservers()
- void consume()
- void removeAllObservers()
- void close()
- void remove(ObservableInputStream$Observer)

### Class: org.apache.commons.io.input.ObservableInputStream$Observer
Type: Abstract Class

Methods:
- void data(byte[], int, int)
- void data(int)
- void closed()
- void finished()
- void error(IOException)

### Class: org.apache.commons.io.input.ProxyInputStream
Type: Abstract Class
Extends: java.io.FilterInputStream

Methods:
- int read()
- int read(byte[])
- int read(byte[], int, int)
- boolean markSupported()
- int available()
- void reset()
- long skip(long)
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.ProxyReader
Type: Abstract Class
Extends: java.io.FilterReader

Methods:
- int read()
- int read(char[])
- int read(char[], int, int)
- int read(CharBuffer)
- boolean markSupported()
- boolean ready()
- void reset()
- long skip(long)
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.QueueInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- QueueInputStream(BlockingQueue<Integer> blockingQueue)

Methods:
- QueueOutputStream newQueueOutputStream()
- int read()

### Class: org.apache.commons.io.input.RandomAccessFileInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- RandomAccessFileInputStream(RandomAccessFile randomAccessFile, boolean closeOnClose)

Methods:
- int read()
- int read(byte[])
- int read(byte[], int, int)
- long availableLong()
- boolean isCloseOnClose()
- RandomAccessFile getRandomAccessFile()
- int available()
- long skip(long)
- void close()

### Class: org.apache.commons.io.input.ReadAheadInputStream
Type: Class
Extends: java.io.InputStream

Methods:
- int read()
- int read(byte[], int, int)
- int available()
- long skip(long)
- void close()

### Class: org.apache.commons.io.input.ReaderInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- ReaderInputStream(Reader reader, CharsetEncoder encoder, int encoderIn)

Methods:
- int read(byte[], int, int)
- int read(byte[])
- int read()
- void close()

### Class: org.apache.commons.io.input.ReversedLinesFileReader
Type: Class
Implements: java.io.Closeable

Constructors:
- ReversedLinesFileReader(Path channel, int blockSize, Charset charset)

Methods:
- List<String> readLines(int)
- String toString(int)
- String readLine()
- void close()

### Class: org.apache.commons.io.input.SequenceReader
Type: Class
Extends: java.io.Reader

Constructors:
- SequenceReader(Iterable<Reader> readers)

Methods:
- int read()
- int read(char[], int, int)
- void close()

### Class: org.apache.commons.io.input.SwappedDataInputStream
Type: Class
Extends: org.apache.commons.io.input.ProxyInputStream
Implements: java.io.DataInput

Methods:
- String readLine()
- char readChar()
- int skipBytes(int)
- String readUTF()
- long readLong()
- short readShort()
- void readFully(byte[])
- void readFully(byte[], int, int)
- double readDouble()
- float readFloat()
- boolean readBoolean()
- int readInt()
- byte readByte()
- int readUnsignedByte()
- int readUnsignedShort()

### Class: org.apache.commons.io.input.TaggedInputStream
Type: Class
Extends: org.apache.commons.io.input.ProxyInputStream

Constructors:
- TaggedInputStream(InputStream tag)

Methods:
- boolean isCauseOf(Throwable)
- void throwIfCauseOf(Throwable)

### Class: org.apache.commons.io.input.TaggedReader
Type: Class
Extends: org.apache.commons.io.input.ProxyReader

Constructors:
- TaggedReader(Reader tag)

Methods:
- boolean isCauseOf(Throwable)
- void throwIfCauseOf(Throwable)

### Class: org.apache.commons.io.input.Tailer
Type: Class
Implements: java.lang.Runnable

Constructors:
- Tailer(File file, Charset charset, TailerListener listener, long delayMillis, boolean end, boolean reOpen, int inbuf)

Methods:
- long getDelay()
- void stop()
- **static** Tailer create(File, TailerListener, long, boolean, int)
- **static** Tailer create(File, TailerListener, long, boolean, boolean, int)
- **static** Tailer create(File, Charset, TailerListener, long, boolean, boolean, int)
- **static** Tailer create(File, TailerListener, long, boolean)
- **static** Tailer create(File, TailerListener, long, boolean, boolean)
- **static** Tailer create(File, TailerListener, long)
- **static** Tailer create(File, TailerListener)
- void run()
- File getFile()

### Class: org.apache.commons.io.input.TailerListenerAdapter
Type: Class
Implements: org.apache.commons.io.input.TailerListener

Methods:
- void fileRotated()
- void init(Tailer)
- void handle(String)
- void handle(Exception)
- void fileNotFound()
- void endOfFileReached()

### Class: org.apache.commons.io.input.TeeInputStream
Type: Class
Extends: org.apache.commons.io.input.ProxyInputStream

Constructors:
- TeeInputStream(InputStream, OutputStream branch, boolean closeBranch)

Methods:
- int read()
- int read(byte[], int, int)
- int read(byte[])
- void close()

### Class: org.apache.commons.io.input.TeeReader
Type: Class
Extends: org.apache.commons.io.input.ProxyReader

Constructors:
- TeeReader(Reader, Writer branch, boolean closeBranch)

Methods:
- int read()
- int read(char[])
- int read(char[], int, int)
- int read(CharBuffer)
- void close()

### Class: org.apache.commons.io.input.TimestampedObserver
Type: Class
Extends: org.apache.commons.io.input.ObservableInputStream$Observer

Methods:
- Duration getOpenToCloseDuration()
- Instant getOpenInstant()
- void closed()
- String toString()
- Duration getOpenToNowDuration()
- Instant getCloseInstant()

### Class: org.apache.commons.io.input.UnixLineEndingInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- UnixLineEndingInputStream(InputStream target, boolean ensureLineFeedAtEndOfFile)

Methods:
- int read()
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.UnsynchronizedByteArrayInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- UnsynchronizedByteArrayInputStream(byte[] data)
- UnsynchronizedByteArrayInputStream(byte[] data, int offset)
- UnsynchronizedByteArrayInputStream(byte[] data, int offset, int)

Methods:
- int read()
- int read(byte[])
- int read(byte[], int, int)
- boolean markSupported()
- int available()
- void reset()
- long skip(long)
- void mark(int)

### Class: org.apache.commons.io.input.WindowsLineEndingInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- WindowsLineEndingInputStream(InputStream target, boolean ensureLineFeedAtEndOfFile)

Methods:
- int read()
- void close()
- void mark(int)

### Class: org.apache.commons.io.input.XmlStreamReader
Type: Class
Extends: java.io.Reader

Constructors:
- XmlStreamReader(InputStream, boolean encoding, String defaultEncoding)
- XmlStreamReader(InputStream, String, boolean encoding, String defaultEncoding)
- XmlStreamReader(URLConnection encoding, String defaultEncoding)

Methods:
- String getEncoding()
- int read(char[], int, int)
- String getDefaultEncoding()
- void close()

### Class: org.apache.commons.io.input.XmlStreamReaderException
Type: Class
Extends: java.io.IOException

Constructors:
- XmlStreamReaderException(String, String contentTypeMime, String contentTypeEncoding, String bomEncoding, String xmlGuessEncoding, String xmlEncoding)

Methods:
- String getXmlEncoding()
- String getContentTypeEncoding()
- String getContentTypeMime()
- String getXmlGuessEncoding()
- String getBomEncoding()

## Package: org.apache.commons.io.input.buffer

### Class: org.apache.commons.io.input.buffer.CircularBufferInputStream
Type: Class
Extends: java.io.InputStream

Constructors:
- CircularBufferInputStream(InputStream in, int buffer)

Methods:
- int read()
- int read(byte[])
- int read(byte[], int, int)
- void close()

### Class: org.apache.commons.io.input.buffer.CircularByteBuffer
Type: Class

Constructors:
- CircularByteBuffer(int buffer)

Methods:
- void add(byte)
- void add(byte[], int, int)
- byte read()
- void read(byte[], int, int)
- boolean hasSpace()
- boolean hasSpace(int)
- int getSpace()
- void clear()
- int getCurrentNumberOfBytes()
- boolean hasBytes()
- boolean peek(byte[], int, int)

### Class: org.apache.commons.io.input.buffer.PeekableInputStream
Type: Class
Extends: org.apache.commons.io.input.buffer.CircularBufferInputStream

Methods:
- boolean peek(byte[])
- boolean peek(byte[], int, int)

## Package: org.apache.commons.io.monitor

### Class: org.apache.commons.io.monitor.FileAlterationListener
Type: Interface

Methods:
- void onDirectoryCreate(File)
- void onDirectoryDelete(File)
- void onDirectoryChange(File)
- void onStart(FileAlterationObserver)
- void onFileDelete(File)
- void onFileCreate(File)
- void onFileChange(File)
- void onStop(FileAlterationObserver)

### Class: org.apache.commons.io.monitor.FileAlterationListenerAdaptor
Type: Class
Implements: org.apache.commons.io.monitor.FileAlterationListener

Methods:
- void onDirectoryCreate(File)
- void onDirectoryDelete(File)
- void onDirectoryChange(File)
- void onStart(FileAlterationObserver)
- void onFileDelete(File)
- void onFileCreate(File)
- void onFileChange(File)
- void onStop(FileAlterationObserver)

### Class: org.apache.commons.io.monitor.FileAlterationMonitor
Type: Class
Implements: java.lang.Runnable

Constructors:
- FileAlterationMonitor(long interval)

Methods:
- long getInterval()
- void addObserver(FileAlterationObserver)
- void stop()
- void stop(long)
- void setThreadFactory(ThreadFactory)
- Iterable<FileAlterationObserver> getObservers()
- void removeObserver(FileAlterationObserver)
- void start()
- void run()

### Class: org.apache.commons.io.monitor.FileAlterationObserver
Type: Class
Implements: java.io.Serializable

Methods:
- Iterable<FileAlterationListener> getListeners()
- void destroy()
- String toString()
- File getDirectory()
- void initialize()
- void removeListener(FileAlterationListener)
- FileFilter getFileFilter()
- void checkAndNotify()
- void addListener(FileAlterationListener)

### Class: org.apache.commons.io.monitor.FileEntry
Type: Class
Implements: java.io.Serializable

Constructors:
- FileEntry(FileEntry parent, File file)

Methods:
- void setName(String)
- FileEntry getParent()
- long getLastModified()
- String getName()
- boolean refresh(File)
- void setDirectory(boolean)
- void setExists(boolean)
- File getFile()
- FileEntry[] getChildren()
- int getLevel()
- void setLength(long)
- FileEntry newChildInstance(File)
- boolean isExists()
- long getLength()
- void setChildren(FileEntry[])
- boolean isDirectory()
- void setLastModified(long)

## Package: org.apache.commons.io.output

### Class: org.apache.commons.io.output.AbstractByteArrayOutputStream$InputStreamConstructor
Type: Interface

Methods:
- TT construct([B, int, int)

### Class: org.apache.commons.io.output.AbstractByteArrayOutputStream
Type: Abstract Class
Extends: java.io.OutputStream

Methods:
- void writeTo(OutputStream)
- int size()
- byte[] toByteArray()
- void reset()
- String toString()
- String toString(String)
- String toString(Charset)
- InputStream toInputStream()
- void close()
- void write(byte[], int, int)
- void write(int)
- int write(InputStream)

### Class: org.apache.commons.io.output.AppendableOutputStream
Type: Class
Extends: java.io.OutputStream

Constructors:
- AppendableOutputStream(T appendable)

Methods:
- TT getAppendable()
- void write(int)

### Class: org.apache.commons.io.output.AppendableWriter
Type: Class
Extends: java.io.Writer

Constructors:
- AppendableWriter(T appendable)

Methods:
- void flush()
- TT getAppendable()
- void write(char[], int, int)
- void write(int)
- void write(String, int, int)
- void close()
- Writer append(char)
- Writer append(CharSequence)
- Writer append(CharSequence, int, int)
- Appendable append(char)
- Appendable append(CharSequence, int, int)
- Appendable append(CharSequence)

### Class: org.apache.commons.io.output.BrokenOutputStream
Type: Class
Extends: java.io.OutputStream

Constructors:
- BrokenOutputStream(IOException exception)

Methods:
- void flush()
- void close()
- void write(int)

### Class: org.apache.commons.io.output.BrokenWriter
Type: Class
Extends: java.io.Writer

Constructors:
- BrokenWriter(IOException exception)

Methods:
- void flush()
- void close()
- void write(char[], int, int)

### Class: org.apache.commons.io.output.ByteArrayOutputStream
Type: Class
Extends: org.apache.commons.io.output.AbstractByteArrayOutputStream

Methods:
- void writeTo(OutputStream)
- int size()
- byte[] toByteArray()
- **static** InputStream toBufferedInputStream(InputStream)
- **static** InputStream toBufferedInputStream(InputStream, int)
- void reset()
- InputStream toInputStream()
- void write(byte[], int, int)
- void write(int)
- int write(InputStream)

### Class: org.apache.commons.io.output.ChunkedOutputStream
Type: Class
Extends: java.io.FilterOutputStream

Constructors:
- ChunkedOutputStream(OutputStream, int chunkSize)

Methods:
- void write(byte[], int, int)

### Class: org.apache.commons.io.output.ChunkedWriter
Type: Class
Extends: java.io.FilterWriter

Constructors:
- ChunkedWriter(Writer, int chunkSize)

Methods:
- void write(char[], int, int)

### Class: org.apache.commons.io.output.CloseShieldOutputStream
Type: Class
Extends: org.apache.commons.io.output.ProxyOutputStream

Methods:
- void close()
- **static** CloseShieldOutputStream wrap(OutputStream)

### Class: org.apache.commons.io.output.CloseShieldWriter
Type: Class
Extends: org.apache.commons.io.output.ProxyWriter

Methods:
- void close()
- **static** CloseShieldWriter wrap(Writer)

### Class: org.apache.commons.io.output.ClosedOutputStream
Type: Class
Extends: java.io.OutputStream

Methods:
- void flush()
- void write(int)

### Class: org.apache.commons.io.output.ClosedWriter
Type: Class
Extends: java.io.Writer

Methods:
- void flush()
- void close()
- void write(char[], int, int)

### Class: org.apache.commons.io.output.CountingOutputStream
Type: Class
Extends: org.apache.commons.io.output.ProxyOutputStream

Methods:
- int resetCount()
- int getCount()
- long resetByteCount()
- long getByteCount()

### Class: org.apache.commons.io.output.DeferredFileOutputStream
Type: Class
Extends: org.apache.commons.io.output.ThresholdingOutputStream

Methods:
- void writeTo(OutputStream)
- boolean isInMemory()
- InputStream toInputStream()
- File getFile()
- void close()
- byte[] getData()

### Class: org.apache.commons.io.output.DemuxOutputStream
Type: Class
Extends: java.io.OutputStream

Methods:
- void flush()
- OutputStream bindStream(OutputStream)
- void write(int)
- void close()

### Class: org.apache.commons.io.output.FileWriterWithEncoding
Type: Class
Extends: java.io.Writer

Constructors:
- FileWriterWithEncoding(File, String, boolean out)
- FileWriterWithEncoding(File, Charset, boolean out)
- FileWriterWithEncoding(File, CharsetEncoder, boolean out)

Methods:
- void flush()
- void close()
- void write(int)
- void write(char[])
- void write(char[], int, int)
- void write(String)
- void write(String, int, int)

### Class: org.apache.commons.io.output.FilterCollectionWriter
Type: Class
Extends: java.io.Writer

Methods:
- void flush()
- void write(char[])
- void write(char[], int, int)
- void write(int)
- void write(String)
- void write(String, int, int)
- void close()
- Writer append(char)
- Writer append(CharSequence)
- Writer append(CharSequence, int, int)
- Appendable append(char)
- Appendable append(CharSequence, int, int)
- Appendable append(CharSequence)

### Class: org.apache.commons.io.output.LockableFileWriter
Type: Class
Extends: java.io.Writer

Constructors:
- LockableFileWriter(File lockFile, Charset, boolean out, String)

Methods:
- void flush()
- void write(int)
- void write(char[])
- void write(char[], int, int)
- void write(String)
- void write(String, int, int)
- void close()

### Class: org.apache.commons.io.output.NullAppendable
Type: Class
Implements: java.lang.Appendable

Methods:
- Appendable append(char)
- Appendable append(CharSequence)
- Appendable append(CharSequence, int, int)

### Class: org.apache.commons.io.output.NullOutputStream
Type: Class
Extends: java.io.OutputStream

Methods:
- void write(byte[], int, int)
- void write(int)
- void write(byte[])

### Class: org.apache.commons.io.output.NullPrintStream
Type: Class
Extends: java.io.PrintStream

No public methods found

### Class: org.apache.commons.io.output.NullWriter
Type: Class
Extends: java.io.Writer

Methods:
- void flush()
- void close()
- void write(int)
- void write(char[])
- void write(char[], int, int)
- void write(String)
- void write(String, int, int)
- Writer append(char)
- Writer append(CharSequence, int, int)
- Writer append(CharSequence)
- Appendable append(char)
- Appendable append(CharSequence, int, int)
- Appendable append(CharSequence)

### Class: org.apache.commons.io.output.ProxyCollectionWriter
Type: Class
Extends: org.apache.commons.io.output.FilterCollectionWriter

Methods:
- void flush()
- void write(char[])
- void write(char[], int, int)
- void write(int)
- void write(String)
- void write(String, int, int)
- void close()
- Writer append(char)
- Writer append(CharSequence)
- Writer append(CharSequence, int, int)
- Appendable append(char)
- Appendable append(CharSequence, int, int)
- Appendable append(CharSequence)

### Class: org.apache.commons.io.output.ProxyOutputStream
Type: Class
Extends: java.io.FilterOutputStream

Methods:
- void flush()
- void close()
- void write(int)
- void write(byte[])
- void write(byte[], int, int)

### Class: org.apache.commons.io.output.ProxyWriter
Type: Class
Extends: java.io.FilterWriter

Methods:
- void flush()
- void close()
- void write(int)
- void write(char[])
- void write(char[], int, int)
- void write(String)
- void write(String, int, int)
- Writer append(char)
- Writer append(CharSequence, int, int)
- Writer append(CharSequence)
- Appendable append(char)
- Appendable append(CharSequence, int, int)
- Appendable append(CharSequence)

### Class: org.apache.commons.io.output.QueueOutputStream
Type: Class
Extends: java.io.OutputStream

Constructors:
- QueueOutputStream(BlockingQueue<Integer> blockingQueue)

Methods:
- QueueInputStream newQueueInputStream()
- void write(int)

### Class: org.apache.commons.io.output.StringBuilderWriter
Type: Class
Extends: java.io.Writer
Implements: java.io.Serializable

Constructors:
- StringBuilderWriter(int builder)
- StringBuilderWriter(StringBuilder builder)

Methods:
- StringBuilder getBuilder()
- void flush()
- String toString()
- void write(String)
- void write(char[], int, int)
- void close()
- Writer append(char)
- Writer append(CharSequence)
- Writer append(CharSequence, int, int)
- Appendable append(char)
- Appendable append(CharSequence, int, int)
- Appendable append(CharSequence)

### Class: org.apache.commons.io.output.TaggedOutputStream
Type: Class
Extends: org.apache.commons.io.output.ProxyOutputStream

Constructors:
- TaggedOutputStream(OutputStream tag)

Methods:
- boolean isCauseOf(Exception)
- void throwIfCauseOf(Exception)

### Class: org.apache.commons.io.output.TaggedWriter
Type: Class
Extends: org.apache.commons.io.output.ProxyWriter

Constructors:
- TaggedWriter(Writer tag)

Methods:
- boolean isCauseOf(Exception)
- void throwIfCauseOf(Exception)

### Class: org.apache.commons.io.output.TeeOutputStream
Type: Class
Extends: org.apache.commons.io.output.ProxyOutputStream

Constructors:
- TeeOutputStream(OutputStream, OutputStream branch)

Methods:
- void flush()
- void close()
- void write(byte[])
- void write(byte[], int, int)
- void write(int)

### Class: org.apache.commons.io.output.TeeWriter
Type: Class
Extends: org.apache.commons.io.output.ProxyCollectionWriter

No public methods found

### Class: org.apache.commons.io.output.ThresholdingOutputStream
Type: Class
Extends: java.io.OutputStream

Constructors:
- ThresholdingOutputStream(int threshold, IOConsumer<ThresholdingOutputStream> thresholdConsumer, IOFunction<ThresholdingOutputStream, OutputStream> outputStreamGetter)

Methods:
- void flush()
- boolean isThresholdExceeded()
- int getThreshold()
- void write(byte[])
- void write(byte[], int, int)
- void write(int)
- void close()
- long getByteCount()

### Class: org.apache.commons.io.output.UnsynchronizedByteArrayOutputStream
Type: Class
Extends: org.apache.commons.io.output.AbstractByteArrayOutputStream

Methods:
- void writeTo(OutputStream)
- int size()
- byte[] toByteArray()
- **static** InputStream toBufferedInputStream(InputStream)
- **static** InputStream toBufferedInputStream(InputStream, int)
- void reset()
- InputStream toInputStream()
- void write(byte[], int, int)
- void write(int)
- int write(InputStream)

### Class: org.apache.commons.io.output.WriterOutputStream
Type: Class
Extends: java.io.OutputStream

Constructors:
- WriterOutputStream(Writer writer, CharsetDecoder decoder, int decoderOut, boolean writeImmediately)

Methods:
- void flush()
- void close()
- void write(byte[], int, int)
- void write(byte[])
- void write(int)

### Class: org.apache.commons.io.output.XmlStreamWriter
Type: Class
Extends: java.io.Writer

Constructors:
- XmlStreamWriter(OutputStream out, String defaultEncoding)

Methods:
- String getEncoding()
- void flush()
- String getDefaultEncoding()
- void write(char[], int, int)
- void close()

## Package: org.apache.commons.io.serialization

### Class: org.apache.commons.io.serialization.ClassNameMatcher
Type: Interface

Methods:
- boolean matches(String)

### Class: org.apache.commons.io.serialization.ValidatingObjectInputStream
Type: Class
Extends: java.io.ObjectInputStream

Constructors:
- ValidatingObjectInputStream(InputStream acceptMatchers)

Methods:
- ValidatingObjectInputStream reject(Class<*>)
- ValidatingObjectInputStream reject(String[])
- ValidatingObjectInputStream reject(Pattern)
- ValidatingObjectInputStream reject(ClassNameMatcher)
- ValidatingObjectInputStream accept(Class<*>)
- ValidatingObjectInputStream accept(String[])
- ValidatingObjectInputStream accept(Pattern)
- ValidatingObjectInputStream accept(ClassNameMatcher)

## Package: world.ofunny.bpm.Floodgate

### Class: world.ofunny.bpm.Floodgate.Floodgate
Type: Interface

Methods:
- boolean isBedrockPlayer(Player)

### Class: world.ofunny.bpm.Floodgate.FloodgateAPI
Type: Class

Methods:
- boolean isClass(String)
- **static** Floodgate get()

