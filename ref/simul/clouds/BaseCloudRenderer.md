---
title: BaseCloudRenderer
layout: reference
---
class simul::clouds::BaseCloudRenderer
===
CloudGeometryHelper CreateCloudGeometryHelper(m)
------

! Returns a new geometry helper.
BaseGpuCloudGenerator CreateGpuCloudGenerator(m)
------

void EnsureEffectsAreBuilt(renderPlatform)
------

! If possible, build all shader effect variations.
void ExportCloudVolume(target)
------

BaseGpuCloudGenerator GetBaseGpuCloudGenerator()
------

float GetCloudOffset()
------

! Get the xyz offset of the clouds (only xy are usually relevant).
CloudRenderingOptions GetCloudRenderingOptions()
------

/
float GetCloudScales()
------

! Get the xyz scales of the clouds in metres.
CloudShadowStruct GetCloudShadowStruct()
------

CloudWindow GetCloudWindow()
------

char GetDebugText()
------

! Get some per-frame text information for debugging - usually timing data.
char GetInfoForRaytrace()
------

char GetInfoForShouldRenderCloudShadowTexture()
------

META_ValueRangePropertyWithSetCall(float,MaxCloudDistanceKm,1.f,1000.f,DetailChanged    ,"Furthest distance, in km, to draw clouds.")
char GetInfoForUseSimulationTime()
------

LineQueryResult GetLineQuery(id,pos1_km,pos2_km)
------

! Set, or create a cloud query. This returns the previous results of the same query.
int GetMaxSlices(viewport_id)
------

!       Cloud rendering detail is determined by the number of slices. See SetMaxSlices.
unsigned int GetOrdinalOfRaytrace()
------

unsigned int GetOrdinalOfShouldRenderCloudShadowTexture()
------

META_ValueRangePropertyWithSetCall(float,MaxCloudDistanceKm,1.f,1000.f,DetailChanged    ,"Furthest distance, in km, to draw clouds.")
unsigned int GetOrdinalOfUseSimulationTime()
------

VolumeQueryResult GetPointQuery(id,pos_km)
------

! Set, or create a cloud query. This returns the previous results of the same query.
VolumeQueryResult GetPointQuery(id)
------

! Get results of a cloud query.
float GetPrecipitation()
------

int GetQueryIdForViewId(view_id)
------

! Get the query id for the specified view. If Render() has been called for the view, the query should have a valid set of results for the last frame rendered.
float GetRainToSnow()
------

crossplatform::Texture GetRandomTexture3D()
------

! Get the random 3D texture.
bool GetRaytrace()
------

bool GetShouldRenderCloudShadowTexture()
------

META_ValueRangePropertyWithSetCall(float,MaxCloudDistanceKm,1.f,1000.f,DetailChanged    ,"Furthest distance, in km, to draw clouds.")
float GetSunOcclusion(deviceContext,cam_pos)
------

! Get a value for how much the sun is blocked from the clouds.
bool GetUseSimulationTime()
------

void InitializePropertiesDefinition()
------

void InitRaytrace(value)
------

void InitShouldRenderCloudShadowTexture(value)
------

META_ValueRangePropertyWithSetCall(float,MaxCloudDistanceKm,1.f,1000.f,DetailChanged    ,"Furthest distance, in km, to draw clouds.")
void InitUseSimulationTime(value)
------

void InvalidateDeviceObjects()
------

! Call this Platform-dependent function when the 3D device has been lost.
bool IsCameraAboveCloudBase(cam_pos)
------

! Return true if the camera is above the cloudbase altitude.
void MakeCloudShadowTexture()
------

! Get an API-dependent identifier for the clouds' 2D shadow.
void PreRenderUpdate(deviceContext,real_time)
------

! Platform-dependent per-frame update, called by BaseWeatherRenderer.
void RecompileShaders()
------

! Platform-dependent function to reload the shaders - only use this for debug purposes.
bool Render(deviceContext,exposure,renderMode,nearFarPass,depth_tex,scatteringVolume,write_alpha,viewportTextureRegionXYWH,amortizationStruct,fb,localFadeTextures,ambientCubemap)
------

! Platform-dependent render function.
void RenderAuxiliaryTextures(context,x0,y0,width,height)
------

void RenderCloudGrid(deviceContext,ck)
------

void RenderCloudShadowTexture(deviceContext)
------

/ The cloud shadow texture:
/ Centred on the viewer
/ Aligned to the sun.
/ Output is km in front of or behind the view pos where shadow starts
void RenderCloudTool(deviceContext,ck,t,dir,press,size_km)
------

void RenderCloudVolumes(deviceContext,ck)
------

void RenderCloudWindow(deviceContext,x0,y0,width,height)
------

/ Show the cloud volume window on the lat-long sphere.
void RenderCrossSections(context,x0,y0,width,height)
------

! Show the cloud volumes onscreen by cross section.
void RenderDebugInfo(deviceContext,width,height)
------

void RenderQueries(deviceContext)
------

! Draw the queries in 3D
void RenderShapeMasks(deviceContext,ck)
------

void RestoreDeviceObjects(renderPlatform)
------

! Platform-dependent function to generate device objects for the renderer.
void SetCloudRenderingOptions(c)
------

void SetEnableStorms(s)
------

! Where supported, enable lightning generation.
void SetExternalCloudTexture()
------

/ Where we create the main volume texture for rendering elsewhere, we pass it in here.
/ This permits ESRAM on XboxOne for example, in a game engine.
void SetIlluminationTexture()
------

void SetLightTableTexture()
------

void SetMaxFadeAltitudeKm(ma_km)
------

void SetMaxFadeDistanceKm(dist_km)
------

Distance for fade texture lookups:
void SetMaxSlices(viewport_id,maxs)
------

!       Cloud rendering detail is determined by the number of slices. If not set the value from the CloudKeyframer will be used (GetDefaultNumSlices), but each viewport id can have a separate setting.
void SetNoiseTextureProperties(size,freq,octaves,persistence)
------

! Adjust the noise texture
void SetPointLight(id,pos,min_radius,max_radius,irradiance)
------

! Place a point light source.
void SetRaytrace(value)
------

void SetShouldRenderCloudShadowTexture(value)
------

META_ValueRangePropertyWithSetCall(float,MaxCloudDistanceKm,1.f,1000.f,DetailChanged    ,"Furthest distance, in km, to draw clouds.")
void SetSkyInterface(si)
------

! Set the sky interface.
void SetUseSimulationTime(value)
------

void StreamInAutoPropertiesDefinition(is)
------

void StreamOutAutoPropertiesDefinition(os)
------

void Templ_AccumulateSetInitialDefinition()
------

META_ValueRangePropertyWithSetCall(float,MaxCloudDistanceKm,1.f,1000.f,DetailChanged    ,"Furthest distance, in km, to draw clouds.")
void Templ_AccumulateSetInitialDefinition()
------

void Templ_AccumulateSetInitialDefinition()
------

void Templ_AccumulateStreamInDefinition(is)
------

META_ValueRangePropertyWithSetCall(float,MaxCloudDistanceKm,1.f,1000.f,DetailChanged    ,"Furthest distance, in km, to draw clouds.")
void Templ_AccumulateStreamInDefinition(is)
------

void Templ_AccumulateStreamInDefinition(is)
------

void Templ_AccumulateStreamOutDefinition(os)
------

META_ValueRangePropertyWithSetCall(float,MaxCloudDistanceKm,1.f,1000.f,DetailChanged    ,"Furthest distance, in km, to draw clouds.")
void Templ_AccumulateStreamOutDefinition(os)
------

void Templ_AccumulateStreamOutDefinition(os)
------

void ClearIterators()
------

void Create3DNoiseTexture(deviceContext)
------

void CreateGpuCloudGenerator()
------

void CreateNoiseTexture(deviceContext)
------

void DetailChanged()
------

void EnsureCorrectIlluminationTextureSizes()
------

void EnsureCorrectTextureSizes(deviceContext)
------

void EnsureIlluminationTexturesAreUpToDate()
------

void EnsureLayersAreInitialized()
------

void EnsureTextureCycle(L)
------

void EnsureTexturesAreUpToDate(deviceContext)
------

bool FailedNoiseChecksum()
------

void FillInQueries(deviceContext)
------

void Recompile()
------

void RenderCombinedCloudTexture(deviceContext)
------

void RenderPointSource(deviceContext,fb,exposure,viewportTextureRegionXYWH)
------

void SetCloudConstants(cloudConstants,real_time)
------

void SetCloudLightpassConstants(pos,min_radius,max_radius,irr,cam_pos)
------

void SetCloudPerViewConstants(cloudPerViewConstants,viewStruct,exposure,viewportTextureRegionXYWH,worldToScatteringVolumeMatrix,amortizationStruct)
------

void SetCloudShadowPerViewConstants(c)
------

