---
title: Base2DCloudRenderer
layout: reference
---
class simul::clouds::Base2DCloudRenderer
===
void EnsureEffectsAreBuilt(r)
------

void InvalidateDeviceObjects()
------

void PreRenderUpdate(deviceContext,real_time)
------

void RecompileShaders()
------

bool Render(deviceContext,exposure,renderMode,nearFarPass,depth_alpha_tex,sc,write_alpha,viewportTextureRegionXYWH,amortizationStruct,fb,localFadeTextures)
------

void RenderAuxiliaryTextures(deviceContext,x0,y0,width,height)
------

void RenderCrossSections(deviceContext,x0,y0,width,height)
------

void RestoreDeviceObjects(renderPlatform)
------

void SetIlluminationTexture(i)
------

void SetLightTableTexture(i)
------

void SetMaxFadeAltitudeKm(ma_km)
------

void SetMaxFadeDistanceKm(dist_km)
------

Distance for fade texture lookups:
void SetSkyInterface(si)
------

void SetWindVelocity(x,y)
------

