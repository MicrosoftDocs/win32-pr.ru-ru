---
title: Схема и алгоритмы профиля модели цветового устройства WCS
description: В этом разделе содержатся сведения о схеме профиля модели цветового устройства WCS и связанных с ней алгоритмах. В этом разделе содержатся следующие разделы Овервиевколор профиль модели устройства Арчитектуресе КДМП Счемавкс КДМП v 2.0 калибровка Аддитионсе КДМП Schema Елементсколордевицемоделпрофилеколордевицемоделнамеспацеверсионверсиондокументатионкртдевице elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice elementCMYKPrinterDevice elementRGBVirtualDevice Елементплугиндевицетипергбвиртуалмеасуременттипегамматипегаммаоффсетгаинтипегаммаоффсетгаинлинеаргаинтипетонереспонсекурвестипегамутбаундарисамплестипефлоатпаирлисткмикпринтермеасуременттипергбпринтермеасуременттипергбкаптуремеасуременттипеонебасединдексргбпрожектормеасуременттипедисплаймеасурементти peMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe CDMP базовое AlgorithmsCRT модель устройства BaselineLCD устройство модель BaselineRGB принтер модель BaselineRGB виртуальное устройство модель BaselineCMYK Printer устройство модель BaselineRGB проектор устройство модель BaselineICC устройство BaselineRelated разделы
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- Цветовая система Windows (WCS), профиль модели цветового устройства (КДМП)
- WCS (цветовая система Windows), профиль модели цветового устройства (КДМП)
- Управление цветом изображений, профиль модели цветового устройства (КДМП)
- Управление цветом, профиль модели цветового устройства (КДМП)
- цвета, профиль модели цветового устройства (КДМП)
- Цветовая система Windows (WCS), профили
- WCS (цветовая система Windows), профили
- Управление цветом изображений, профили
- Управление цветом, профили
- цвета, профили
- схемы, профиль модели цветового устройства (КДМП)
- алгоритмы, профиль модели цветового устройства (КДМП)
- Профиль модели цветового устройства (КДМП)
- КДМП (профиль модели цветового устройства)
- Профиль модели цветового устройства WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b671bf97625b00c99060e65be4d39c44e5b35f
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104565929"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a><span data-ttu-id="fe4b7-118">Схема и алгоритмы профиля модели цветового устройства WCS</span><span class="sxs-lookup"><span data-stu-id="fe4b7-118">WCS Color Device Model Profile Schema and Algorithms</span></span>

<span data-ttu-id="fe4b7-119">В этом разделе содержатся сведения о схеме профиля модели цветового устройства WCS и связанных с ней алгоритмах.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-119">This topic provides information about the WCS Color Device Model Profile Schema and its associated algorithms.</span></span>

<span data-ttu-id="fe4b7-120">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-120">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="fe4b7-121">Обзор</span><span class="sxs-lookup"><span data-stu-id="fe4b7-121">Overview</span></span>](#overview)
-   [<span data-ttu-id="fe4b7-122">Архитектура профиля модели цветового устройства</span><span class="sxs-lookup"><span data-stu-id="fe4b7-122">Color Device Model Profile Architecture</span></span>](#color-device-model-profile-architecture)
-   [<span data-ttu-id="fe4b7-123">Схема КДМП</span><span class="sxs-lookup"><span data-stu-id="fe4b7-123">The CDMP Schema</span></span>](#the-cdmp-schema)
-   [<span data-ttu-id="fe4b7-124">Добавление калибровки WCS КДМП v 2.0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-124">WCS CDMP v2.0 Calibration Addition</span></span>](#wcs-cdmp-v20-calibration-addition)
-   [<span data-ttu-id="fe4b7-125">Элементы схемы КДМП</span><span class="sxs-lookup"><span data-stu-id="fe4b7-125">The CDMP Schema Elements</span></span>](#the-cdmp-schema-elements)
    -   [<span data-ttu-id="fe4b7-126">колордевицемоделпрофиле</span><span class="sxs-lookup"><span data-stu-id="fe4b7-126">ColorDeviceModelProfile</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="fe4b7-127">колордевицемодел</span><span class="sxs-lookup"><span data-stu-id="fe4b7-127">ColorDeviceModel</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="fe4b7-128">намеспацеверсион</span><span class="sxs-lookup"><span data-stu-id="fe4b7-128">NamespaceVersion</span></span>](#namespaceversion)
    -   [<span data-ttu-id="fe4b7-129">Version</span><span class="sxs-lookup"><span data-stu-id="fe4b7-129">Version</span></span>](#namespaceversion)
    -   [<span data-ttu-id="fe4b7-130">Документация</span><span class="sxs-lookup"><span data-stu-id="fe4b7-130">Documentation</span></span>](#documentation)
    -   [<span data-ttu-id="fe4b7-131">Кртдевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-131">CRTDevice element</span></span>](#crtdevice-element)
    -   [<span data-ttu-id="fe4b7-132">Лкддевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-132">LCDDevice element</span></span>](#lcddevice-element)
    -   [<span data-ttu-id="fe4b7-133">Прожектордевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-133">ProjectorDevice element</span></span>](#projectordevice-element)
    -   [<span data-ttu-id="fe4b7-134">Сканнердевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-134">ScannerDevice element</span></span>](#scannerdevice-element)
    -   [<span data-ttu-id="fe4b7-135">Камерадевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-135">CameraDevice element</span></span>](#cameradevice-element)
    -   [<span data-ttu-id="fe4b7-136">Ргбпринтердевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-136">RGBPrinterDevice element</span></span>](#rgbprinterdevice-element)
    -   [<span data-ttu-id="fe4b7-137">Кмикпринтердевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-137">CMYKPrinterDevice element</span></span>](#cmykprinterdevice-element)
    -   [<span data-ttu-id="fe4b7-138">Ргбвиртуалдевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-138">RGBVirtualDevice element</span></span>](#rgbvirtualdevice-element)
    -   [<span data-ttu-id="fe4b7-139">плугиндевицетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-139">PlugInDeviceType</span></span>](#plugindevicetype)
    -   [<span data-ttu-id="fe4b7-140">ргбвиртуалмеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-140">RGBVirtualMeasurementType</span></span>](#rgbvirtualmeasurementtype)
    -   [<span data-ttu-id="fe4b7-141">гамматипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-141">GammaType</span></span>](#gammatype)
    -   [<span data-ttu-id="fe4b7-142">гаммаоффсетгаинтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-142">GammaOffsetGainType</span></span>](#gammaoffsetgaintype)
    -   [<span data-ttu-id="fe4b7-143">гаммаоффсетгаинлинеаргаинтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-143">GammaOffsetGainLinearGainType</span></span>](#gammaoffsetgainlineargaintype)
    -   [<span data-ttu-id="fe4b7-144">тонереспонсекурвестипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-144">ToneResponseCurvesType</span></span>](#toneresponsecurvestype)
    -   [<span data-ttu-id="fe4b7-145">гамутбаундарисамплестипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-145">GamutBoundarySamplesType</span></span>](#gamutboundarysamplestype)
    -   [<span data-ttu-id="fe4b7-146">флоатпаирлист</span><span class="sxs-lookup"><span data-stu-id="fe4b7-146">FloatPairList</span></span>](#floatpairlist)
    -   [<span data-ttu-id="fe4b7-147">кмикпринтермеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-147">CMYKPrinterMeasurementType</span></span>](#cmykprintermeasurementtype)
    -   [<span data-ttu-id="fe4b7-148">ргбпринтермеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-148">RGBPrinterMeasurementType</span></span>](#rgbprintermeasurementtype)
    -   [<span data-ttu-id="fe4b7-149">ргбкаптуремеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-149">RGBCaptureMeasurementType</span></span>](#rgbcapturemeasurementtype)
    -   [<span data-ttu-id="fe4b7-150">онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-150">OneBasedIndex</span></span>](#onebasedindex)
    -   [<span data-ttu-id="fe4b7-151">ргбпрожектормеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-151">RGBProjectorMeasurementType</span></span>](#rgbprojectormeasurementtype)
    -   [<span data-ttu-id="fe4b7-152">дисплаймеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-152">DisplayMeasurementType</span></span>](#displaymeasurementtype)
    -   [<span data-ttu-id="fe4b7-153">меасуременткондитионстипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-153">MeasurementConditionsType</span></span>](#measurementconditionstype)
    -   [<span data-ttu-id="fe4b7-154">жеометритипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-154">GeometryType</span></span>](#geometrytype)
    -   [<span data-ttu-id="fe4b7-155">ргбпримариесграуп</span><span class="sxs-lookup"><span data-stu-id="fe4b7-155">RGBPrimariesGroup</span></span>](#rgbprimariesgroup)
    -   [<span data-ttu-id="fe4b7-156">ноннегативекмиксамплетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-156">NonNegativeCMYKSampleType</span></span>](#nonnegativecmyksampletype)
    -   [<span data-ttu-id="fe4b7-157">ноннегативергбсамплетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-157">NonNegativeRGBSampleType</span></span>](#nonnegativergbsampletype)
    -   [<span data-ttu-id="fe4b7-158">ноннегативекмиктипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-158">NonNegativeCMYKType</span></span>](#nonnegativecmyktype)
    -   [<span data-ttu-id="fe4b7-159">ноннегативергбтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-159">NonNegativeRGBType</span></span>](#nonnegativergbtype)
    -   [<span data-ttu-id="fe4b7-160">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="fe4b7-160">ExtensionType</span></span>](#extensiontype)
    -   [<span data-ttu-id="fe4b7-161">ноннегативексизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-161">NonNegativeXYZType</span></span>](#nonnegativexyztype)
    -   [<span data-ttu-id="fe4b7-162">ксизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-162">XYZType</span></span>](#nonnegativexyztype)
-   [<span data-ttu-id="fe4b7-163">Базовые алгоритмы КДМП</span><span class="sxs-lookup"><span data-stu-id="fe4b7-163">The CDMP Baseline Algorithms</span></span>](#the-cdmp-baseline-algorithms)
    -   [<span data-ttu-id="fe4b7-164">Базовый план модели устройства CRT</span><span class="sxs-lookup"><span data-stu-id="fe4b7-164">CRT Device Model Baseline</span></span>](#crt-device-model-baseline)
    -   [<span data-ttu-id="fe4b7-165">Базовая модель устройства LCD</span><span class="sxs-lookup"><span data-stu-id="fe4b7-165">LCD Device Model Baseline</span></span>](#lcd-device-model-baseline)
    -   [<span data-ttu-id="fe4b7-166">Базовый план модели устройства принтера RGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-166">RGB Printer Device Model Baseline</span></span>](#rgb-printer-device-model-baseline)
    -   [<span data-ttu-id="fe4b7-167">Базовый план модели виртуального устройства RGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-167">RGB Virtual Device Model Baseline</span></span>](#rgb-virtual-device-model-baseline)
    -   [<span data-ttu-id="fe4b7-168">Базовая модель устройства принтера CMYK</span><span class="sxs-lookup"><span data-stu-id="fe4b7-168">CMYK Printer Device Model Baseline</span></span>](#cmyk-printer-device-model-baseline)
    -   [<span data-ttu-id="fe4b7-169">Базовый план модели устройства с проектором RGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-169">RGB Projector Device Model Baseline</span></span>](#rgb-projector-device-model-baseline)
    -   [<span data-ttu-id="fe4b7-170">Базовый план модели устройства ICC</span><span class="sxs-lookup"><span data-stu-id="fe4b7-170">ICC Device Model Baseline</span></span>](#icc-device-model-baseline)
-   [<span data-ttu-id="fe4b7-171">См. также</span><span class="sxs-lookup"><span data-stu-id="fe4b7-171">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="fe4b7-172">Обзор</span><span class="sxs-lookup"><span data-stu-id="fe4b7-172">Overview</span></span>

<span data-ttu-id="fe4b7-173">Эта схема используется для указания содержимого профиля модели цветового устройства (КДМП).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-173">This schema is used to specify the content of a color device model profile(CDMP).</span></span> <span data-ttu-id="fe4b7-174">Связанные базовые алгоритмы описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-174">The associated baseline algorithms are described below.</span></span>

<span data-ttu-id="fe4b7-175">Базовая схема профиля модели устройства (DMP) состоит из данных измерения выборки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-175">The basic device model profile (DMP) schema consists of the sampling measurement data.</span></span>

<span data-ttu-id="fe4b7-176">Компонент выборки в схеме XML DMP обеспечивает поддержку базовых целей измерения цвета, что сосредоточено на стандартных целевых объектах и целевых объектах, оптимизированных для моделей базовых устройств.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-176">The sampling component of the DMP XML schema provides support for basic color measurement targets, focusing on common standard targets and targets optimized for the baseline device models.</span></span>

<span data-ttu-id="fe4b7-177">Кроме того, профиль устройства предоставляет определенную информацию о модели целевого устройства и предоставляет политику, которую модель базового резервного устройства может использовать, если Целевая модель недоступна.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-177">In addition, the device profile provides specific information on the targeted device model and provides a policy that the baseline fallback device model can use if the targeted model is unavailable.</span></span> <span data-ttu-id="fe4b7-178">Экземпляры профиля могут включать частные расширения с помощью стандартных механизмов расширения XML.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-178">The profile instances can include private extensions using standard XML extension mechanisms.</span></span>

## <a name="color-device-model-profile-architecture"></a><span data-ttu-id="fe4b7-179">Архитектура профиля модели цветового устройства</span><span class="sxs-lookup"><span data-stu-id="fe4b7-179">Color Device Model Profile Architecture</span></span>

![Схема, на которой показаны сведения, составляющие профиль модели устройства.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a><span data-ttu-id="fe4b7-181">Схема КДМП</span><span class="sxs-lookup"><span data-stu-id="fe4b7-181">The CDMP Schema</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="RGBType">
    <xs:attribute name="R" type="xs:float" use="required"/>
    <xs:attribute name="G" type="xs:float" use="required"/>
    <xs:attribute name="B" type="xs:float" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeRGBType">
    <xs:attribute name="R" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="G" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="B" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeCMYKType">
    <xs:attribute name="C" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="M" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="K" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeRGBSampleType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:NonNegativeRGBType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeCMYKSampleType">
    <xs:sequence>
      <xs:element name="CMYK" type="cdm:NonNegativeCMYKType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:group name="RGBPrimariesGroup">
    <xs:sequence>
      <xs:element name="WhitePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="RedPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="GreenPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BluePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BlackPrimary" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
  </xs:group> 
  
  <xs:complexType name="MeasurementConditionsType">
    <xs:annotation>
      <xs:documentation>
      Optional measurement conditions. 
       
      We only support CIEXYZ for measurement color space in this version. 
      If the white point value from the measurement conditions is not available, 
      the default processing will use
        - "D50" for printer and scanners
        - "D65" for camera and displays.          
      </xs:documentation>
    </xs:annotation>
    <xs:sequence>
      <xs:element name="ColorSpace" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="CIEXYZ"/>
          </xs:restriction>
        </xs:simpleType>    
      </xs:element>
      <xs:choice minOccurs="0">
        <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
        <xs:element name="WhitePointName">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="D50"/>
              <xs:enumeration value="D65"/>
              <xs:enumeration value="A"/>
              <xs:enumeration value="F2"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:choice>
      <xs:element name="Geometry" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="0/45"/>
            <xs:enumeration value="0/diffuse"/>
            <xs:enumeration value="diffuse/0"/>
            <xs:enumeration value="direct"/>
          </xs:restriction>
        </xs:simpleType>   
      </xs:element>
      <xs:element name="ApertureSize" type="xs:int" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="DisplayMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="GrayRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="RedRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GreenRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="BlueRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBProjectorMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:simpleType name="OneBasedIndex">
    <xs:restriction base="xs:int">
      <xs:minInclusive value="1"/>
    </xs:restriction>
  </xs:simpleType>
    
  <xs:complexType name="RGBCaptureMeasurementType">
    <xs:sequence>
      <xs:element name="PrimaryIndex">
        <xs:complexType>
          <xs:all>
            <xs:element name="White" type="cdm:OneBasedIndex"/>
            <xs:element name="Black" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Red" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Green" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Blue" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Cyan" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Magenta" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Yellow" type="cdm:OneBasedIndex" minOccurs="0"/>
          </xs:all>
        </xs:complexType>
      </xs:element>
      <xs:element name="NeutralIndices">
        <xs:simpleType>
          <xs:list itemType="cdm:OneBasedIndex"/>
        </xs:simpleType>
      </xs:element>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:complexType name="CMYKPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeCMYKSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="GammaType">
    <xs:attribute name="value" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="GammaOffsetGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="GammaOffsetGainLinearGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="LinearGain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="cdm:FloatList"/>
      <xs:element name="Output" type="cdm:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="cdm:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="0" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="GamutBoundarySamplesType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:RGBType" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="RGBVirtualMeasurementType">
    <xs:sequence>
      <xs:element name="MaxColorantUsed" type="xs:float"/>
      <xs:element name="MinColorantUsed" type="xs:float"/>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:choice>
        <xs:element name="Gamma" type="cdm:GammaType"/>
        <xs:element name="GammaOffsetGain" type="cdm:GammaOffsetGainType"/>
        <xs:element name="GammaOffsetGainLinearGain" type="cdm:GammaOffsetGainLinearGainType"/>
        <xs:element name="HDRToneResponseCurves" type="cdm:HDRToneResponseCurvesType"/>
      </xs:choice>
      <xs:element name="GamutBoundarySamples" type="cdm:GamutBoundarySamplesType" minOccurs="0"/>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="MeasurementConditions" type="cdm:MeasurementConditionsType" minOccurs="0"/>
        <xs:element name="SelfLuminous" type="xs:boolean" />
        <xs:element name="MaxColorant" type="xs:float"/>
        <xs:element name="MinColorant" type="xs:float"/>
        <xs:choice>
          <xs:element name="CRTDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="LCDDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBProjectorDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBProjectorMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="ScannerDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CameraDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CMYKPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:CMYKPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBVirtualDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBVirtualMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
        </xs:choice>
        <xs:element name="PlugInDevice" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>

```



## <a name="wcs-cdmp-v20-calibration-addition"></a><span data-ttu-id="fe4b7-182">Добавление калибровки WCS КДМП v 2.0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-182">WCS CDMP v2.0 Calibration Addition</span></span>

<span data-ttu-id="fe4b7-183">Элемент **колордевицемодел** схемы КДМП был обновлен в Windows 7 для включения нового элемента калибровки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-183">The **ColorDeviceModel** element of the CDMP schema has been updated in Windows 7 to include the new calibration element.</span></span> <span data-ttu-id="fe4b7-184">Ниже показано изменение схемы КДМП.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-184">The following shows the change to the CDMP schema.</span></span>


```C++
  ...
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        ...
        <xs:element name="PlugInDevice" minOccurs="0">
             ...
        </xs:element>
        <xs:element name="Calibration" type="cal:Calibration" minOccurs="0"/>
        ...
      <xs:sequence>
    ...
    <xs:complexType>
  ...
```



## <a name="the-cdmp-schema-elements"></a><span data-ttu-id="fe4b7-185">Элементы схемы КДМП</span><span class="sxs-lookup"><span data-stu-id="fe4b7-185">The CDMP Schema Elements</span></span>

> [!Note]  
> <span data-ttu-id="fe4b7-186">Первичные цвета — это основные примеры красного, зеленого, синего, Черного и белого цветов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-186">Primaries are primary samples of red, green, blue, black, and white.</span></span> <span data-ttu-id="fe4b7-187">Основная шкала — это тональная шкала от наименьшей светимости до полного основного значения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-187">A primary ramp is a tonal ramp from least luminance to full primary value.</span></span> <span data-ttu-id="fe4b7-188">Максимальное число записей в пандусе тонового элемента — 4096.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-188">The maximum number of entries in a tone ramp is 4096.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe4b7-189">Дмпс должны иметь данные измерения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-189">DMPs are required to have measurement data.</span></span>

 

### <a name="colordevicemodelprofile"></a><span data-ttu-id="fe4b7-190">колордевицемоделпрофиле</span><span class="sxs-lookup"><span data-stu-id="fe4b7-190">ColorDeviceModelProfile</span></span>

<span data-ttu-id="fe4b7-191">Этот элемент имеет тип Колордевицемодел.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-191">This element is of type ColorDeviceModel.</span></span>

<span data-ttu-id="fe4b7-192">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-192">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="colordevicemodel"></a><span data-ttu-id="fe4b7-193">колордевицемодел</span><span class="sxs-lookup"><span data-stu-id="fe4b7-193">ColorDeviceModel</span></span>

<span data-ttu-id="fe4b7-194">Этот элемент является последовательностью следующих вложенных элементов</span><span class="sxs-lookup"><span data-stu-id="fe4b7-194">This element is a sequence of the following sub-elements</span></span>

1.  <span data-ttu-id="fe4b7-195">Строка имени файла,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-195">ProfileName string,</span></span>
2.  <span data-ttu-id="fe4b7-196">Необязательная строка описания</span><span class="sxs-lookup"><span data-stu-id="fe4b7-196">optional Description string,</span></span>
3.  <span data-ttu-id="fe4b7-197">Необязательная строка автора</span><span class="sxs-lookup"><span data-stu-id="fe4b7-197">optional Author string,</span></span>
4.  <span data-ttu-id="fe4b7-198">Необязательный Меасуременткондитионс Меасуременткондитионстипе,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-198">optional MeasurementConditions MeasurementConditionsType,</span></span>
5.  <span data-ttu-id="fe4b7-199">Self-Luminous Boolean,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-199">Self-Luminous Boolean,</span></span>
6.  <span data-ttu-id="fe4b7-200">Максколорант float,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-200">MaxColorant float,</span></span>
7.  <span data-ttu-id="fe4b7-201">Минколорант float,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-201">MinColorant float,</span></span>
8.  <span data-ttu-id="fe4b7-202">Выбора элементов</span><span class="sxs-lookup"><span data-stu-id="fe4b7-202">Choice of elements</span></span>
    1.  <span data-ttu-id="fe4b7-203">Кртдевице,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-203">CRTDevice,</span></span>
    2.  <span data-ttu-id="fe4b7-204">Лкддевице,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-204">LCDDevice,</span></span>
    3.  <span data-ttu-id="fe4b7-205">Ргбпрожектордевице,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-205">RGBProjectorDevice,</span></span>
    4.  <span data-ttu-id="fe4b7-206">Сканнердевице,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-206">ScannerDevice,</span></span>
    5.  <span data-ttu-id="fe4b7-207">Камерадевице,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-207">CameraDevice,</span></span>
    6.  <span data-ttu-id="fe4b7-208">Ргбпринтердевице,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-208">RGBPrinterDevice,</span></span>
    7.  <span data-ttu-id="fe4b7-209">Кмикпринтердевице,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-209">CMYKPrinterDevice,</span></span>
    8.  <span data-ttu-id="fe4b7-210">Ргбвиртуалдевице,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-210">RGBVirtualDevice,</span></span>
9.  <span data-ttu-id="fe4b7-211">Плугиндевице,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-211">PlugInDevice,</span></span>
10. <span data-ttu-id="fe4b7-212">необязательное расширение ExtensionType</span><span class="sxs-lookup"><span data-stu-id="fe4b7-212">optional Extension ExtensionType</span></span>

<span data-ttu-id="fe4b7-213">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-213">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="fe4b7-214">Вложенные элементы строки содержат не более 10 000 символов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-214">String sub-elements have a maximum of 10,000 characters.</span></span> <span data-ttu-id="fe4b7-215">Вложенный элемент Максколорант должен быть больше или равен нулю (0) и больше, чем вложенный элемент Минколорант.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-215">The MaxColorant sub-element must be greater than or equal to zero (0) and greater than the MinColorant sub-element.</span></span> <span data-ttu-id="fe4b7-216">Минколорант может быть отрицательным.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-216">The MinColorant can be negative.</span></span>

### <a name="namespaceversion"></a><span data-ttu-id="fe4b7-217">намеспацеверсион</span><span class="sxs-lookup"><span data-stu-id="fe4b7-217">NamespaceVersion</span></span>

<span data-ttu-id="fe4b7-218">xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="fe4b7-218">xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

<span data-ttu-id="fe4b7-219">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="fe4b7-219">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

### <a name="version"></a><span data-ttu-id="fe4b7-220">Версия</span><span class="sxs-lookup"><span data-stu-id="fe4b7-220">Version</span></span>

<span data-ttu-id="fe4b7-221">Version = "1,0" в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-221">Version = "1.0" with Windows Vista.</span></span>

<span data-ttu-id="fe4b7-222">**Условия проверки:** Любое значение версии &gt; 0,1 или &lt; = 2,0 допустимо для поддержки некритических изменений в формате.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-222">**Validation conditions:** Any version value &gt;0.1 or &lt;=2.0 is valid to support non-breaking changes to the format.</span></span>

### <a name="documentation"></a><span data-ttu-id="fe4b7-223">Документация</span><span class="sxs-lookup"><span data-stu-id="fe4b7-223">Documentation</span></span>

<span data-ttu-id="fe4b7-224">Схема профиля модели устройства.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-224">Device Model Profile schema.</span></span>

<span data-ttu-id="fe4b7-225">(C) корпорация Майкрософт (Microsoft Corporation).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-225">Copyright (C) Microsoft.</span></span> <span data-ttu-id="fe4b7-226">Все права защищены.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-226">All rights reserved.</span></span>

### <a name="crtdevice-element"></a><span data-ttu-id="fe4b7-227">Кртдевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-227">CRTDevice element</span></span>

<span data-ttu-id="fe4b7-228">Этот элемент является последовательностью вложенных элементов Меасурементдата Дисплаймеасуременттипе.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-228">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="fe4b7-229">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-229">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="lcddevice-element"></a><span data-ttu-id="fe4b7-230">Лкддевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-230">LCDDevice element</span></span>

<span data-ttu-id="fe4b7-231">Этот элемент является последовательностью вложенных элементов Меасурементдата Дисплаймеасуременттипе.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-231">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="fe4b7-232">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-232">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="projectordevice-element"></a><span data-ttu-id="fe4b7-233">Прожектордевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-233">ProjectorDevice element</span></span>

<span data-ttu-id="fe4b7-234">Этот элемент является последовательностью вложенных элементов Меасурементдата Ргбпрожектормеасуременттипе.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-234">This element is a sequence of sub-elements of a MeasurementData RGBProjectorMeasurementType.</span></span>

<span data-ttu-id="fe4b7-235">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-235">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="scannerdevice-element"></a><span data-ttu-id="fe4b7-236">Сканнердевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-236">ScannerDevice element</span></span>

<span data-ttu-id="fe4b7-237">Этот элемент является последовательностью вложенных элементов объекта Меасурементдата Ргбкаптуремеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-237">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="fe4b7-238">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-238">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cameradevice-element"></a><span data-ttu-id="fe4b7-239">Камерадевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-239">CameraDevice element</span></span>

<span data-ttu-id="fe4b7-240">Этот элемент является последовательностью вложенных элементов объекта Меасурементдата Ргбкаптуремеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-240">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="fe4b7-241">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-241">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbprinterdevice-element"></a><span data-ttu-id="fe4b7-242">Ргбпринтердевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-242">RGBPrinterDevice element</span></span>

<span data-ttu-id="fe4b7-243">Этот элемент является последовательностью вложенных элементов Меасурементдата Ргбпринтермеасуременттипе.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-243">This element is a sequence of sub-elements of a MeasurementData RGBPrinterMeasurementType.</span></span>

<span data-ttu-id="fe4b7-244">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-244">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cmykprinterdevice-element"></a><span data-ttu-id="fe4b7-245">Кмикпринтердевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-245">CMYKPrinterDevice element</span></span>

<span data-ttu-id="fe4b7-246">Этот элемент является последовательностью вложенных элементов Меасурементдата Кмикпринтермеасуременттипе.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-246">This element is a sequence of sub-elements of a MeasurementData CMYKPrinterMeasurementType.</span></span>

<span data-ttu-id="fe4b7-247">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-247">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbvirtualdevice-element"></a><span data-ttu-id="fe4b7-248">Ргбвиртуалдевице, элемент</span><span class="sxs-lookup"><span data-stu-id="fe4b7-248">RGBVirtualDevice element</span></span>

<span data-ttu-id="fe4b7-249">Этот элемент является последовательностью вложенных элементов объекта Ргбвиртуалмеасурементдататипе.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-249">This element is a sequence of sub-elements of a RGBVirtualMeasurementDataType.</span></span>

<span data-ttu-id="fe4b7-250">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-250">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="plugindevicetype"></a><span data-ttu-id="fe4b7-251">плугиндевицетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-251">PlugInDeviceType</span></span>

<span data-ttu-id="fe4b7-252">Этот элемент является последовательностью Гуидтипе GUID и всех вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-252">This element is a sequence of a GUID GUIDType and any sub-elements.</span></span>

<span data-ttu-id="fe4b7-253">**Условия проверки:** Идентификатор GUID используется для сопоставления GUID подключаемого модуля DM DLL.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-253">**Validation conditions:** The GUID is used to match the DM PlugIn Dll GUID.</span></span> <span data-ttu-id="fe4b7-254">Существует не более 100 000 настраиваемых вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-254">There are a maximum of 100,000 custom sub-elements.</span></span>

### <a name="rgbvirtualmeasurementtype"></a><span data-ttu-id="fe4b7-255">ргбвиртуалмеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-255">RGBVirtualMeasurementType</span></span>

<span data-ttu-id="fe4b7-256">Этот элемент представляет собой последовательность, состоящую из</span><span class="sxs-lookup"><span data-stu-id="fe4b7-256">This element is a sequence consisting of</span></span>

1.  <span data-ttu-id="fe4b7-257">Группа Ргбпримариесграуп</span><span class="sxs-lookup"><span data-stu-id="fe4b7-257">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="fe4b7-258">Один из вариантов</span><span class="sxs-lookup"><span data-stu-id="fe4b7-258">A choice of</span></span>
3.  -   <span data-ttu-id="fe4b7-259">Gamma</span><span class="sxs-lookup"><span data-stu-id="fe4b7-259">Gamma</span></span>
    -   <span data-ttu-id="fe4b7-260">гаммаоффсетгаин</span><span class="sxs-lookup"><span data-stu-id="fe4b7-260">GammaOffsetGain</span></span>
    -   <span data-ttu-id="fe4b7-261">гаммаоффсетгаинлинеаргам</span><span class="sxs-lookup"><span data-stu-id="fe4b7-261">GammaOffsetGainLinearGam</span></span>
    -   <span data-ttu-id="fe4b7-262">Элементы Тонереспонсекурвес</span><span class="sxs-lookup"><span data-stu-id="fe4b7-262">ToneResponseCurves elements</span></span>

4.  <span data-ttu-id="fe4b7-263">Необязательный Гамутбаундарисамплес Гамутбаундарисамплестипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-263">optional GamutBoundarySamples GamutBoundarySamplesType</span></span>
5.  <span data-ttu-id="fe4b7-264">Метка времени (dateTime)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-264">TimeStamp dateTime</span></span>

<span data-ttu-id="fe4b7-265">**Условия проверки:** Каждый вложенный элемент этих типов имеет свои собственные условия проверки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-265">**Validation conditions:** Each sub-element of these types has its own validation conditions.</span></span>

### <a name="gammatype"></a><span data-ttu-id="fe4b7-266">гамматипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-266">GammaType</span></span>

<span data-ttu-id="fe4b7-267">Этот элемент представляет собой сложный тип, состоящий из атрибута</span><span class="sxs-lookup"><span data-stu-id="fe4b7-267">This element is a complex type consisting of the attribute</span></span>

-   <span data-ttu-id="fe4b7-268">Гамма-Ноннегативефлоаттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-268">Gamma NonNegativeFloatType</span></span>

<span data-ttu-id="fe4b7-269">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-269">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgaintype"></a><span data-ttu-id="fe4b7-270">гаммаоффсетгаинтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-270">GammaOffsetGainType</span></span>

<span data-ttu-id="fe4b7-271">Этот элемент представляет собой сложный тип, состоящий из атрибутов</span><span class="sxs-lookup"><span data-stu-id="fe4b7-271">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="fe4b7-272">Гамма-Ноннегативефлоаттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-272">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="fe4b7-273">Смещение Ноннегативефлоаттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-273">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="fe4b7-274">Получить Ноннегативефлоаттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-274">Gain NonNegativeFloatType</span></span>

<span data-ttu-id="fe4b7-275">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-275">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgainlineargaintype"></a><span data-ttu-id="fe4b7-276">гаммаоффсетгаинлинеаргаинтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-276">GammaOffsetGainLinearGainType</span></span>

<span data-ttu-id="fe4b7-277">Этот элемент представляет собой сложный тип, состоящий из атрибутов</span><span class="sxs-lookup"><span data-stu-id="fe4b7-277">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="fe4b7-278">Гамма-Ноннегативефлоаттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-278">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="fe4b7-279">Смещение Ноннегативефлоаттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-279">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="fe4b7-280">Получить Ноннегативефлоаттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-280">Gain NonNegativeFloatType</span></span>
-   <span data-ttu-id="fe4b7-281">Линеаргаин Ноннегативефлоаттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-281">LinearGain NonNegativeFloatType</span></span>
-   <span data-ttu-id="fe4b7-282">Транситионпоинт Ноннегативефлоаттипе.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-282">TransitionPoint NonNegativeFloatType.</span></span>

<span data-ttu-id="fe4b7-283">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-283">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="toneresponsecurvestype"></a><span data-ttu-id="fe4b7-284">тонереспонсекурвестипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-284">ToneResponseCurvesType</span></span>

<span data-ttu-id="fe4b7-285">Этот элемент является последовательностью</span><span class="sxs-lookup"><span data-stu-id="fe4b7-285">This element is a sequence of</span></span>

1.  <span data-ttu-id="fe4b7-286">Редтрк Флоатпаирлист</span><span class="sxs-lookup"><span data-stu-id="fe4b7-286">RedTRC FloatPairList</span></span>
2.  <span data-ttu-id="fe4b7-287">Гринтрк Флоатпаирлист</span><span class="sxs-lookup"><span data-stu-id="fe4b7-287">GreenTRC FloatPairList</span></span>
3.  <span data-ttu-id="fe4b7-288">Блуетрк Флоатпаирлист</span><span class="sxs-lookup"><span data-stu-id="fe4b7-288">BlueTRC FloatPairList</span></span>

<span data-ttu-id="fe4b7-289">Элемент также имеет атрибут Тркленгс типа unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-289">The element also has an attribute TRCLength of unsignedint type.</span></span>

<span data-ttu-id="fe4b7-290">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-290">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gamutboundarysamplestype"></a><span data-ttu-id="fe4b7-291">гамутбаундарисамплестипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-291">GamutBoundarySamplesType</span></span>

<span data-ttu-id="fe4b7-292">Этот элемент является последовательностью RGB Ргбтипес.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-292">This element is a sequence of RGB RGBTypes.</span></span>

<span data-ttu-id="fe4b7-293">**Условия проверки:** В настоящее время не ограничено максимальное число повторений, которое должно быть ограничено на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-293">**Validation conditions:** Currently unbounded maximum occurences, to be capped based on industry feedback.</span></span>

### <a name="floatpairlist"></a><span data-ttu-id="fe4b7-294">флоатпаирлист</span><span class="sxs-lookup"><span data-stu-id="fe4b7-294">FloatPairList</span></span>

<span data-ttu-id="fe4b7-295">Этот элемент представляет собой простой тип списка пар float.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-295">This element is a simple type of list of pairs of floats.</span></span>

<span data-ttu-id="fe4b7-296">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-296">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="cmykprintermeasurementtype"></a><span data-ttu-id="fe4b7-297">кмикпринтермеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-297">CMYKPrinterMeasurementType</span></span>

<span data-ttu-id="fe4b7-298">Этот элемент является</span><span class="sxs-lookup"><span data-stu-id="fe4b7-298">This element is a</span></span>

1. <span data-ttu-id="fe4b7-299">последовательность элементов Колоркубе, состоящая из последовательности примеров Ноннегативекмиксамплетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-299">sequence of ColorCube element consisting of a sequence of Sample NonNegativeCMYKSampleType</span></span>

2. <span data-ttu-id="fe4b7-300">Атрибут TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-300">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="fe4b7-301">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-301">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprintermeasurementtype"></a><span data-ttu-id="fe4b7-302">ргбпринтермеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-302">RGBPrinterMeasurementType</span></span>

<span data-ttu-id="fe4b7-303">Этот элемент является</span><span class="sxs-lookup"><span data-stu-id="fe4b7-303">This element is a</span></span>

1. <span data-ttu-id="fe4b7-304">последовательность элементов Колоркубе, состоящая из последовательности примеров Ноннегативергбсамплетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-304">sequence of ColorCube element consisting of a sequence of Sample NonNegativeRGBSampleType</span></span>

2. <span data-ttu-id="fe4b7-305">Атрибут TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-305">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="fe4b7-306">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-306">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbcapturemeasurementtype"></a><span data-ttu-id="fe4b7-307">ргбкаптуремеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-307">RGBCaptureMeasurementType</span></span>

<span data-ttu-id="fe4b7-308">Этот элемент является последовательностью</span><span class="sxs-lookup"><span data-stu-id="fe4b7-308">This element is a sequence of</span></span>

1.  <span data-ttu-id="fe4b7-309">Примариндекс complexType</span><span class="sxs-lookup"><span data-stu-id="fe4b7-309">PrimaryIndex complexType of</span></span>
2.  1.  <span data-ttu-id="fe4b7-310">Белый Онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-310">White OneBasedIndex</span></span>
    2.  <span data-ttu-id="fe4b7-311">Необязательный черный Онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-311">Optional Black OneBasedIndex</span></span>
    3.  <span data-ttu-id="fe4b7-312">Необязательный красный Онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-312">Optional Red OneBasedIndex</span></span>
    4.  <span data-ttu-id="fe4b7-313">Необязательное зеленое Онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-313">Optional Green OneBasedIndex</span></span>
    5.  <span data-ttu-id="fe4b7-314">Необязательные синие Онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-314">Optional Blue OneBasedIndex</span></span>
    6.  <span data-ttu-id="fe4b7-315">Необязательный голубой Онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-315">Optional Cyan OneBasedIndex</span></span>
    7.  <span data-ttu-id="fe4b7-316">Необязательный пурпурный Онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-316">Optional Magenta OneBasedIndex</span></span>
    8.  <span data-ttu-id="fe4b7-317">Необязательный желтый Онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-317">Optional Yellow OneBasedIndex</span></span>

3.  <span data-ttu-id="fe4b7-318">Неутралиндицес строк Онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-318">NeutralIndices of lines of OneBasedIndex</span></span>
4.  <span data-ttu-id="fe4b7-319">Колорсамплес последовательность примеров Ноннегативергбсамплетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-319">ColorSamples sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="fe4b7-320">Элемент также имеет атрибут TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-320">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="fe4b7-321">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-321">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="onebasedindex"></a><span data-ttu-id="fe4b7-322">онебасединдекс</span><span class="sxs-lookup"><span data-stu-id="fe4b7-322">OneBasedIndex</span></span>

<span data-ttu-id="fe4b7-323">Этот элемент является простым типом базового типа без знака int с minInclusive значением = "1".</span><span class="sxs-lookup"><span data-stu-id="fe4b7-323">This element is a simple type of restriction base unsigned int with minInclusive value = "1."</span></span>

<span data-ttu-id="fe4b7-324">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-324">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprojectormeasurementtype"></a><span data-ttu-id="fe4b7-325">ргбпрожектормеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-325">RGBProjectorMeasurementType</span></span>

<span data-ttu-id="fe4b7-326">Этот элемент является последовательностью</span><span class="sxs-lookup"><span data-stu-id="fe4b7-326">This element is a sequence of</span></span>

1.  <span data-ttu-id="fe4b7-327">Группа Ргбпримариесграуп</span><span class="sxs-lookup"><span data-stu-id="fe4b7-327">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="fe4b7-328">элемент Колорсамплес, состоящий из последовательности примеров Ноннегативергбсамплетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-328">element ColorSamples consisting of sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="fe4b7-329">Элемент также имеет атрибут TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-329">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="fe4b7-330">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-330">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="displaymeasurementtype"></a><span data-ttu-id="fe4b7-331">дисплаймеасуременттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-331">DisplayMeasurementType</span></span>

<span data-ttu-id="fe4b7-332">Этот элемент является последовательностью</span><span class="sxs-lookup"><span data-stu-id="fe4b7-332">This element is a sequence of</span></span>

1.  <span data-ttu-id="fe4b7-333">Ргбпримариесграуп группы</span><span class="sxs-lookup"><span data-stu-id="fe4b7-333">group RGBPrimariesGroup</span></span>
2.  <span data-ttu-id="fe4b7-334">Грайрамп последовательности примеров Ноннегативергбтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-334">GrayRamp of sequence of Sample NonNegativeRGBType</span></span>
3.  <span data-ttu-id="fe4b7-335">Редрамп последовательности примеров Ноннегативергбтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-335">RedRamp of sequence of Sample NonNegativeRGBType</span></span>
4.  <span data-ttu-id="fe4b7-336">Гринрамп последовательности примеров Ноннегативергбтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-336">GreenRamp of sequence of Sample NonNegativeRGBType</span></span>
5.  <span data-ttu-id="fe4b7-337">Блуерамп последовательности примеров Ноннегативергбтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-337">BlueRamp of sequence of Sample NonNegativeRGBType</span></span>

<span data-ttu-id="fe4b7-338">Элемент Дисплаймеасуременттипе также имеет атрибут TimeStamp dateTime.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-338">The DisplayMeasurementType element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="fe4b7-339">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-339">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="measurementconditionstype"></a><span data-ttu-id="fe4b7-340">меасуременткондитионстипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-340">MeasurementConditionsType</span></span>

<span data-ttu-id="fe4b7-341">Меасуременткондитионстипе — это последовательность вложенных элементов, которая содержит:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-341">The MeasurementConditionsType is a sequence of sub-elements that contains:</span></span>

1.  <span data-ttu-id="fe4b7-342">Колорспаце ограниченное строковое значение перечисления "ЦИЕКСИЗ"</span><span class="sxs-lookup"><span data-stu-id="fe4b7-342">ColorSpace restricted string enumeration value of "CIEXYZ"</span></span>
2.  <span data-ttu-id="fe4b7-343">Необязательный вариант перечисления Вхитепоинт Ноннегативексизтипе или Вхитепоинтнаме String для значений D50, D65, A или F2</span><span class="sxs-lookup"><span data-stu-id="fe4b7-343">optional choice of WhitePoint NonNegativeXYZType or WhitePointName string enumeration of values D50, D65, A, or F2</span></span>
3.  <span data-ttu-id="fe4b7-344">Геометрическая Жеометритипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-344">Geometry GeometryType</span></span>
4.  <span data-ttu-id="fe4b7-345">Апертуресизе целое число в миллиметрах</span><span class="sxs-lookup"><span data-stu-id="fe4b7-345">ApertureSize integer in millimeters</span></span>

<span data-ttu-id="fe4b7-346">Значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-346">Defaults are:</span></span>

1.  <span data-ttu-id="fe4b7-347">Принтеры RGB и CMYK:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-347">RGB and CMYK Printers:</span></span>
    1.  <span data-ttu-id="fe4b7-348">ЦИЕКСИЗ Меасурементспацетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-348">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="fe4b7-349">D50 Вхитепоинтвалуе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-349">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="fe4b7-350">0/45 Жеометритипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-350">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="fe4b7-351">10mm Апертуресизе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-351">10mm ApertureSize</span></span>
2.  <span data-ttu-id="fe4b7-352">Сканеры</span><span class="sxs-lookup"><span data-stu-id="fe4b7-352">Scanners:</span></span>
    1.  <span data-ttu-id="fe4b7-353">ЦИЕКСИЗ Меасурементспацетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-353">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="fe4b7-354">D50 Вхитепоинтвалуе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-354">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="fe4b7-355">0/45 Жеометритипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-355">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="fe4b7-356">10mm Апертуресизе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-356">10mm ApertureSize</span></span>
3.  <span data-ttu-id="fe4b7-357">Отображает и RGB виртуальное устройство:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-357">Displays and RGB Virtual Device:</span></span>
    1.  <span data-ttu-id="fe4b7-358">ЦИЕКСИЗ Меасурементспацетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-358">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="fe4b7-359">D65 Вхитепоинтвалуе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-359">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="fe4b7-360">0/45 Жеометритипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-360">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="fe4b7-361">10mm Апертуресизе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-361">10mm ApertureSize</span></span>
4.  <span data-ttu-id="fe4b7-362">Цифровой</span><span class="sxs-lookup"><span data-stu-id="fe4b7-362">Cameras:</span></span>
    1.  <span data-ttu-id="fe4b7-363">ЦИЕКСИЗ Меасурементспацетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-363">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="fe4b7-364">D65 Вхитепоинтвалуе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-364">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="fe4b7-365">Прямой Жеометритипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-365">Direct GeometryType</span></span>
    4.  <span data-ttu-id="fe4b7-366">10mm Апертуресизе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-366">10mm ApertureSize</span></span>

<span data-ttu-id="fe4b7-367">**Условия проверки:** Проверка каждого вложенного элемента определяется условиями проверки для этих вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-367">**Validation conditions:** Validation of each sub-element is determined by validation conditions for those sub-elements.</span></span> <span data-ttu-id="fe4b7-368">Если какой-либо из вложенных элементов отсутствует, используется тип модели устройства по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-368">If any sub-element is missing, the device model type specific default is used.</span></span>

### <a name="geometrytype"></a><span data-ttu-id="fe4b7-369">жеометритипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-369">GeometryType</span></span>

<span data-ttu-id="fe4b7-370">Строка</span><span class="sxs-lookup"><span data-stu-id="fe4b7-370">String</span></span>

<span data-ttu-id="fe4b7-371">Значения перечисления:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-371">Enumeration values:</span></span>

-   <span data-ttu-id="fe4b7-372">"0/45"</span><span class="sxs-lookup"><span data-stu-id="fe4b7-372">"0/45"</span></span>
-   <span data-ttu-id="fe4b7-373">"0/диффузный"</span><span class="sxs-lookup"><span data-stu-id="fe4b7-373">"0/diffuse"</span></span>
-   <span data-ttu-id="fe4b7-374">"диффузия/0"</span><span class="sxs-lookup"><span data-stu-id="fe4b7-374">"diffuse/0"</span></span>
-   <span data-ttu-id="fe4b7-375">Направлений</span><span class="sxs-lookup"><span data-stu-id="fe4b7-375">"Direct"</span></span>

<span data-ttu-id="fe4b7-376">**Условия проверки:** Любое значение, за исключением указанных значений енумбератион, является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-376">**Validation conditions:** Any value except the enumberation values listed is invalid.</span></span> <span data-ttu-id="fe4b7-377">Эта информация не изменит поведение базовой обработки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-377">This information will not change baseline processing behavior.</span></span>

### <a name="rgbprimariesgroup"></a><span data-ttu-id="fe4b7-378">ргбпримариесграуп</span><span class="sxs-lookup"><span data-stu-id="fe4b7-378">RGBPrimariesGroup</span></span>

<span data-ttu-id="fe4b7-379">Этот элемент является последовательностью</span><span class="sxs-lookup"><span data-stu-id="fe4b7-379">This element is a sequence of</span></span>

1.  <span data-ttu-id="fe4b7-380">Вхитепримари Ноннегативексизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-380">WhitePrimary NonNegativeXYZType</span></span>
2.  <span data-ttu-id="fe4b7-381">Редпримари Ноннегативексизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-381">RedPrimary NonNegativeXYZType</span></span>
3.  <span data-ttu-id="fe4b7-382">Гринпримари Ноннегативексизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-382">GreenPrimary NonNegativeXYZType</span></span>
4.  <span data-ttu-id="fe4b7-383">Блуепримари Ноннегативексизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-383">BluePrimary NonNegativeXYZTYpe</span></span>
5.  <span data-ttu-id="fe4b7-384">Блаккпримари Ноннегативексизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-384">BlackPrimary NonNegativeXYZType</span></span>

<span data-ttu-id="fe4b7-385">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-385">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyksampletype"></a><span data-ttu-id="fe4b7-386">ноннегативекмиксамплетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-386">NonNegativeCMYKSampleType</span></span>

<span data-ttu-id="fe4b7-387">Этот элемент является последовательностью</span><span class="sxs-lookup"><span data-stu-id="fe4b7-387">This element is a sequence of</span></span>

1.  <span data-ttu-id="fe4b7-388">CMYK Ноннегативекмиктипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-388">CMYK NonNegativeCMYKType</span></span>
2.  <span data-ttu-id="fe4b7-389">ЦИЕКСИЗ Ноннегативексизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-389">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="fe4b7-390">Элемент также имеет необязательную строку тега атрибута</span><span class="sxs-lookup"><span data-stu-id="fe4b7-390">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="fe4b7-391">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-391">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbsampletype"></a><span data-ttu-id="fe4b7-392">ноннегативергбсамплетипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-392">NonNegativeRGBSampleType</span></span>

<span data-ttu-id="fe4b7-393">Этот элемент является последовательностью</span><span class="sxs-lookup"><span data-stu-id="fe4b7-393">This element is a sequence of</span></span>

1.  <span data-ttu-id="fe4b7-394">Ноннегативергбтипе RGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-394">RGB NonNegativeRGBType</span></span>
2.  <span data-ttu-id="fe4b7-395">ЦИЕКСИЗ Ноннегативексизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-395">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="fe4b7-396">Элемент также имеет необязательную строку тега атрибута</span><span class="sxs-lookup"><span data-stu-id="fe4b7-396">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="fe4b7-397">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-397">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyktype"></a><span data-ttu-id="fe4b7-398">ноннегативекмиктипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-398">NonNegativeCMYKType</span></span>

<span data-ttu-id="fe4b7-399">Этот элемент состоит из атрибутов</span><span class="sxs-lookup"><span data-stu-id="fe4b7-399">This element consisting of attributes</span></span>

1.  <span data-ttu-id="fe4b7-400">С плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="fe4b7-400">C float</span></span>
2.  <span data-ttu-id="fe4b7-401">С плавающей запятой M</span><span class="sxs-lookup"><span data-stu-id="fe4b7-401">M float</span></span>
3.  <span data-ttu-id="fe4b7-402">Y с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="fe4b7-402">Y float</span></span>
4.  <span data-ttu-id="fe4b7-403">K с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="fe4b7-403">K float</span></span>

<span data-ttu-id="fe4b7-404">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-404">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbtype"></a><span data-ttu-id="fe4b7-405">ноннегативергбтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-405">NonNegativeRGBType</span></span>

<span data-ttu-id="fe4b7-406">Этот элемент состоит из атрибутов</span><span class="sxs-lookup"><span data-stu-id="fe4b7-406">This element consisting of attributes</span></span>

1.  <span data-ttu-id="fe4b7-407">R float</span><span class="sxs-lookup"><span data-stu-id="fe4b7-407">R float</span></span>
2.  <span data-ttu-id="fe4b7-408">С плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="fe4b7-408">G float</span></span>
3.  <span data-ttu-id="fe4b7-409">B с плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="fe4b7-409">B float</span></span>

<span data-ttu-id="fe4b7-410">**Условия проверки:** Для определения на основе отзывов отрасли.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-410">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="extensiontype"></a><span data-ttu-id="fe4b7-411">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="fe4b7-411">ExtensionType</span></span>

<span data-ttu-id="fe4b7-412">Элемент ExtensionType является последовательностью любого типа вложенного элемента и используется для собственной информации от сторонних приложений.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-412">The ExtensionType element is a sequence of any sub-element type and is used for proprietary information from non-Microsoft applications.</span></span>

<span data-ttu-id="fe4b7-413">**Условия проверки:** Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-413">**Validation conditions:** This element is optional.</span></span> <span data-ttu-id="fe4b7-414">Допускается не более 1000 вложенных элементов расширения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-414">There can be a maximum of 1000 extension sub-elements.</span></span>

### <a name="nonnegativexyztype"></a><span data-ttu-id="fe4b7-415">ноннегативексизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-415">NonNegativeXYZType</span></span>

<span data-ttu-id="fe4b7-416">Элемент Ноннегативексизтипе состоит из Ноннегативефлоаттипе трех элементов с плавающей запятой одиночной точности с именами "X", "Y" и "Z".</span><span class="sxs-lookup"><span data-stu-id="fe4b7-416">The NonNegativeXYZType element is composed of NonNegativeFloatType three single-precision IEEE floating-point elements named "X," "Y," and "Z."</span></span> <span data-ttu-id="fe4b7-417">Эти значения ограничиваются значениями измерений профилей DMP.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-417">These values are limited to the DMP profiles measurement values.</span></span> <span data-ttu-id="fe4b7-418">Эти измерения могут быть абсолютными (не относительными) ЦИЕКСИЗ 1931 отражающими значениями или абсолютными (не относительными) ЦИЕКСИЗ 1931 прямыми (передаваемые) значениями в Канделас на единицы измерения с квадратом.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-418">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="fe4b7-419">**Условия проверки:** Допустимы только реальные значения, а отрицательные значения измерения ЦИЕКСИЗ недопустимы.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-419">**Validation conditions:** Only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="fe4b7-420">Так как это абсолютные значения, значения могут быть больше 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-420">Because these are absolute values, values can be greater than 1.0f.</span></span> <span data-ttu-id="fe4b7-421">Разумное ограничение для любых "X", "Y" или "Z".</span><span class="sxs-lookup"><span data-stu-id="fe4b7-421">A reasonable limit for any "X," "Y," or "Z."</span></span> <span data-ttu-id="fe4b7-422">для значения произвольно задано значение 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-422">value is arbitrarily set to 10000.0f.</span></span>

### <a name="xyztype"></a><span data-ttu-id="fe4b7-423">ксизтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-423">XYZType</span></span>

<span data-ttu-id="fe4b7-424">Элемент Ксизтипе состоит из трех значений с плавающей запятой одиночной точности: "X", "Y" и "Z".</span><span class="sxs-lookup"><span data-stu-id="fe4b7-424">The XYZType element is composed of three single-precision IEEE floating-point values: "X," "Y," and "Z."</span></span>

## <a name="the-cdmp-baseline-algorithms"></a><span data-ttu-id="fe4b7-425">Базовые алгоритмы КДМП</span><span class="sxs-lookup"><span data-stu-id="fe4b7-425">The CDMP Baseline Algorithms</span></span>

### <a name="crt-device-model-baseline"></a><span data-ttu-id="fe4b7-426">Базовый план модели устройства CRT</span><span class="sxs-lookup"><span data-stu-id="fe4b7-426">CRT Device Model Baseline</span></span>

<span data-ttu-id="fe4b7-427">Чтобы понять эту модель, необходимо учитывать как процесс обработки символов, так и моделирование устройств.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-427">To understand this model, you must consider both the characterization process and the device modeling.</span></span> <span data-ttu-id="fe4b7-428">В процессе обработки символов измерения XYZ сначала выполняются на цветах, полученных путем заполнения буферов экрана ЭЛТ-устройства.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-428">In the characterization process, XYZ measurements are first performed on the colors obtained by filling the display buffer of a CRT display device.</span></span> <span data-ttu-id="fe4b7-429">В следующих примерах значения будут созданы хорошие данные для модели базовых устройств CRT:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-429">The following example values will generate good data for the baseline CRT device model:</span></span>

<span data-ttu-id="fe4b7-430">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-430">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="fe4b7-431">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-431">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="fe4b7-432">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-432">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="fe4b7-433">Нейтральные: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255</span><span class="sxs-lookup"><span data-stu-id="fe4b7-433">Neutrals: R = G= B = 0, 8, 16, 32, 64, 128, 192, 255</span></span>

<span data-ttu-id="fe4b7-434">Также можно использовать приращение, отличное от 15 и нелинейного приращения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-434">Increments other than 15 and nonlinear increments can also be used.</span></span> <span data-ttu-id="fe4b7-435">Каждый красный, зеленый, синий и нейтральный пандус должны содержать по крайней мере три выборки, но рекомендуется предоставить больше образцов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-435">Each red, green, blue, and neutral ramp must contain at least three samples, but providing more samples is recommended.</span></span> <span data-ttu-id="fe4b7-436">Необходимо предоставить образцы для чисто красного, зеленого, синего, Черного и белого цветов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-436">You must provide samples for pure red, green, blue, black, and white.</span></span> <span data-ttu-id="fe4b7-437">Примеры не обязательно должны иметь одинаковое пространство.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-437">The samples do not have to be uniformly spaced.</span></span>

<span data-ttu-id="fe4b7-438">Процесс создания матрицы тристимулус состоит из двух этапов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-438">The process of building the tristimulus matrix consists of two steps.</span></span> <span data-ttu-id="fe4b7-439">Сначала следует оценить значение черной точки XYZ или Блик.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-439">First, estimate the black point XYZ value, or the flare.</span></span> <span data-ttu-id="fe4b7-440">Этот шаг в основном основан на работе Бернс \[ 3 \] с немного измененной функцией цели для нелинейной оптимизации.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-440">This step is based largely on work of Berns\[3\] with a slightly modified objective function for the nonlinear optimization.</span></span> <span data-ttu-id="fe4b7-441">Во-вторых, вычислите тристимулус матрицу на основе результата, полученного на шаге 1, а также вычисления усреднения по всем измерениям для каждого канала, а не только для максимального числа цифр.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-441">Second, calculate tristimulus matrix based on the result from step one and also from an averaging calculation on all of the per-channel measurements, not just the one for maximum digital count.</span></span>

<span data-ttu-id="fe4b7-442">Каждый из этих шагов содержит подробные процедуры.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-442">Each of these steps contains detailed procedures.</span></span> <span data-ttu-id="fe4b7-443">Начальная точка — это пандус (17 шагов в нашем примере) для каждого канала R, G и B.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-443">The starting point is the ramps (17 steps in our example) for each of R, G, and B channels.</span></span> <span data-ttu-id="fe4b7-444">При отображении измерений XYZ на плоскости *XY* -нолики типичная ситуация показана на рис. 1.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-444">When the XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="fe4b7-445">Шаг 1 состоит в решении проблемы нелинейной оптимизации, которая позволяет найти «наилучшее» направление черного цвета, что снизит смещение в глубине насыщенности по каналам R, G и B.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-445">Step one consists of solving a nonlinear optimization problem to find the "best fit" black point that will minimize the drift in chromaticity as one traverses along the R, G, and B channels.</span></span> <span data-ttu-id="fe4b7-446">На основе Бернс \[ 3 \] мы будем искать ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ), что позволяет максимально сокращать следующую целевую функцию:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-446">Based on Berns\[3\], we seek ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ) that minimizes the following objective function:</span></span>

![Показывает целевую функцию, где SR, SG и SB являются набором точек данных в каналах R, G и B.](images/cdmp-formula1.png)

<span data-ttu-id="fe4b7-448">где *s <sub>R</sub>*,*s <sub>G</sub>* и *s <sub>B</sub>* — это набор точек данных, соответствующих точкам в каналах R, G и b.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-448">where *S <sub>R</sub>*,*S <sub>G</sub>*, and *S<sub>B</sub>* are the set of data points corresponding to the points on the R, G, and B channels.</span></span> <span data-ttu-id="fe4b7-449">Для *любого набора определите*:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-449">For any set *S*, define:</span></span>

![Показывает формулу для определения любого набора.](images/cdmp-formula2.png)

<span data-ttu-id="fe4b7-451">В предыдущих \|  \| версиях s — кратность *s*, т. е. количество точек в наборе.  ![ Показывает формулу для цветности точки.](images/cdmp-formula3.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-451">In the preceding, \| *S* \| is the cardinality of *S*, i.e., the number of points in the set *S*. ![Shows a formula for the chromaticity of a point.](images/cdmp-formula3.png)</span></span> <span data-ttu-id="fe4b7-452">— Это координаты цветовой области точки, ![ которая показывает формаула для точки.](images/cdmp-formula4.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-452">is the chromaticity coordinates of the point ![Shows a formaula for a point.](images/cdmp-formula4.png)</span></span> <span data-ttu-id="fe4b7-453">, то ![ есть формула для среднего или центрирования массы, ](images/cdmp-formula5.png) — это среднее значение или центр массы всех точек *в* наборе в плоскости цветовой области.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-453">, so ![Shows a formula for the average or center of mass.](images/cdmp-formula5.png), is the average, or center of mass, of all the points in the set *S* in the chromaticity plane.</span></span> <span data-ttu-id="fe4b7-454">Таким же результатом является ![ Формула суммы секунды в секундах.](images/cdmp-formula6.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-454">Thus, ![Shows a formula for the sum of a second moments of points.](images/cdmp-formula6.png)</span></span> <span data-ttu-id="fe4b7-455">сумма, равная сумме второго секунды относительно центра массы и представляющая степень распределения очков между ними.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-455">is the sum of second moments of the points about the center of mass and is a measure of how spread out the points are about it.</span></span> <span data-ttu-id="fe4b7-456">Наконец, ![ показывает формулу для общей меры распределения из трех кластеров точек.](images/cdmp-formula7.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-456">Finally, ![Shows a formula for the total measure of the spread of three clusters of points.](images/cdmp-formula7.png)</span></span> <span data-ttu-id="fe4b7-457">представляет собой общую меру распределения трех кластеров точек о соответствующих центрах.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-457">is a total measure of how spread out the three clusters of points are about their respective centers of mass.</span></span>

<span data-ttu-id="fe4b7-458">В вычислении ![ показывает формулу f (X, Y, Z; КСК, ИК, ZK).](images/cdmp-formula8.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-458">In the calculation of ![Shows a formula of f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png)</span></span> <span data-ttu-id="fe4b7-459">, если ![ выражение содержит формулу для X. ](images/cdmp-formula9.png) , то вычисление пропускается, а кратность *S* корректируется соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-459">, if ![Shows a formula for X.](images/cdmp-formula9.png) , then the calculation is skipped, and the cardinality of *S* is adjusted accordingly.</span></span>

<span data-ttu-id="fe4b7-460">Несмотря на очевидную сложность функции задания, это сумма квадратов многих дифферентиабле функций в *X <sub>k</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 точек 2 *XY* -компоненты 3 канала = 102, в примере) и, следовательно, податлива к стандартным нелинейным методам, таким как алгоритм Levenberg-Marquardt, который является алгоритмом, используемым в WCS.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-460">Despite the apparent complexity of the objective function, it is a sum of the squares of many differentiable functions in *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K</sub>* (17 points   2 *xy* -components   3 channels = 102, in the example), and, therefore, is amenable to standard nonlinear least squares techniques, such as the Levenberg-Marquardt algorithm, which is the algorithm used in WCS.</span></span> <span data-ttu-id="fe4b7-461">Обратите внимание, что Предыдущая функция-цель отличается от предложенной в Бернс \[ 3 \] в том, что последняя функция измеряет дисперсию расстояния от центра массы, так что дисперсия равна нулю, когда точки эквидистантная от центра массы, даже если они могут распределяться довольно немного.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-461">Note that the preceding objective function is different from the one suggested in Berns\[3\] in that the latter function measures the variance of the distances from the center of mass, so that the variance is zero when the points are equidistant from the center of mass, even though they may spread out quite a bit about it.</span></span> <span data-ttu-id="fe4b7-462">В этом примере распределенность точек осуществляется напрямую с помощью второго секунды.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-462">In the example, the dispersion of points is contolled directly using the second moments.</span></span>

<span data-ttu-id="fe4b7-463">Как и в случае с любыми последовательными алгоритмами для проблемы с нелинейной наименее квадратами, Levenberg-Marquardt требует первоначального предположения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-463">As with any iterative algorithm for the nonlinear least squares problem, Levenberg-Marquardt requires an initial guess.</span></span> <span data-ttu-id="fe4b7-464">Существует два очевидных кандидата.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-464">There are two obvious candidates.</span></span> <span data-ttu-id="fe4b7-465">Один — (0, 0, 0); второй — измеряемая черная точка.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-465">One is (0, 0, 0); the other is the measured black point.</span></span> <span data-ttu-id="fe4b7-466">Для выражения CTE измеряемая черная точка сначала используется в качестве начального предположения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-466">For the CTE, the measured black point is first used as the initial guess.</span></span> <span data-ttu-id="fe4b7-467">Если превышено максимальное число итераций 100 без достижения среднего расстояния в 0,001 каждой точки от центра массы (что соответствует пороговому значению (0,001) 17 3 = 0,000051 для функции цели), то выполняется еще один цикл итераций с первоначальным предположением (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-467">If a maximum of 100 iterations is exceeded without achieving a threshold of an average distance of 0.001 of each point from its center of mass (which corresponds to a threshold value of (0.001)    17   3 = 0.000051 for the objective function), then another round of iterations with the initial guess of (0, 0, 0) is performed.</span></span> <span data-ttu-id="fe4b7-468">Результирующая оценка черной точки — XYZ по сравнению с лучшей оценкой из предыдущего цикла итераций (с измеряемой черной точкой в качестве первоначального предположения).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-468">The resulting estimate of the black point is XYZ compared with the best estimate from the previous round of iterations (with the measured black point as the initial guess).</span></span> <span data-ttu-id="fe4b7-469">Используйте оценку, которая возвращает наименьшее значение для целевой функции.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-469">Use the estimate that gives the smallest value for the objective function.</span></span> <span data-ttu-id="fe4b7-470">Выбор из 100 итераций и расстояние ошибки 0,001 были выбраны многопроходно.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-470">The choice of 100 iterations and the error distance of 0.001 were each selected empirically.</span></span> <span data-ttu-id="fe4b7-471">В будущих версиях может быть целесообразно параметризовать расстояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-471">In future versions, it might be reasonable to parameterize the error distance.</span></span>

<span data-ttu-id="fe4b7-472">Результатом первого шага является предполагаемая черная точка ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-472">The result of step one is the estimated black point ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ).</span></span> <span data-ttu-id="fe4b7-473">Второй шаг состоит из определения тристимулус матрицы путем усреднения цветового значения точек в трех кластерах, полученных на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-473">Step two consists of determining the tristimulus matrix by averaging the chromaticity of the points in the three clusters obtained in step one.</span></span> <span data-ttu-id="fe4b7-474">Для библиотек CRT это делается в основном для снижения влияния ошибок измерения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-474">For CRTs, this is done primarily to minimize the effects of measurement errors.</span></span> <span data-ttu-id="fe4b7-475">Точки, используемые для усреднения цветовой области, должны быть одной и той же точкой, используемой в процессе оптимизации на первом шаге.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-475">The points used in averaging the chromaticity must be the same points used in the optimization in step one.</span></span> <span data-ttu-id="fe4b7-476">Иными словами, если первая точка (цифровое число 15, в примере) в каждом пандусе отбрасывается на шаге оптимизации, то то же самое необходимо сделать в усреднении.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-476">In other words, if the first point (digital count 15, in the example) in each ramp is discarded in the optimization step, then the same must be done in the averaging.</span></span> <span data-ttu-id="fe4b7-477">![Значение, если содержит формулы среднего цвета для координат красного и зеленого каналов.](images/cdmp-formula10.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-477">If ![Shows formulas of averaged chromaticity for coordinates in the red and green channels.](images/cdmp-formula10.png)</span></span> <span data-ttu-id="fe4b7-478">и ![ отображает формулу среднего цвета для координат в синем канале.](images/cdmp-formula11.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-478">, and ![Shows a formula of averaged chromaticity for coordinates in the blue channel.](images/cdmp-formula11.png)</span></span> <span data-ttu-id="fe4b7-479">— Это средние координаты цветовых каналов красного, зеленого и синего цветов, а следующая процедура определяет матрицу тристимулус.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-479">are the averaged chromaticity coordinates of the red, green, and blue channels, then the following procedure determines the tristimulus matrix.</span></span> <span data-ttu-id="fe4b7-480">Сначала решите систему 3? 3 Линейная:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-480">First, solve the 3?3 linear system:</span></span>

![Показывает первую часть процедуры для решения линейной системы 3? 3.](images/cdmp-formula12.png)

![Показывает вторую часть линейной системы 3? 3.](images/cdmp-formula13.gif)![Отображение значения t подстрочной b в конце второй части линейной системы 3? 3.](images/cdmp-formula14.gif)

<span data-ttu-id="fe4b7-484">*X <sub>w</sub>*,*Y <sub>W</sub>*,*Z <sub>w</sub>*</span><span class="sxs-lookup"><span data-stu-id="fe4b7-484">*X <sub>W</sub>*,*Y <sub>W</sub>*,*Z<sub>W</sub>*</span></span>

![Показывает последнюю часть процедуры для решения линейной системы 3? 3.](images/cdmp-formula15.png)

<span data-ttu-id="fe4b7-486">После определения матрицы тристимулус определение кривых тонов соответствует стандартному подходу.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-486">After the tristimulus matrix is determined, the determination of tone curves follows the standard approach.</span></span> <span data-ttu-id="fe4b7-487">Для отображения CRT предполагается, что отдельные каналы соответствуют модели "Гог":</span><span class="sxs-lookup"><span data-stu-id="fe4b7-487">For CRT displays, the individual channels are assumed to follow the "GOG" model:</span></span>

![Показывает формулу для модели "G O G".](images/cdmp-formula16.png)

<span data-ttu-id="fe4b7-489">где *k <sub>g</sub>* — это "прибыль", 1-*k <sub>g</sub>* — "offset" и?</span><span class="sxs-lookup"><span data-stu-id="fe4b7-489">where *k <sub>g</sub>* is the "gain",1 -*k<sub>g</sub>* is the "offset", and ?</span></span> <span data-ttu-id="fe4b7-490">— это «гамма».</span><span class="sxs-lookup"><span data-stu-id="fe4b7-490">is the "gamma."</span></span> <span data-ttu-id="fe4b7-491">Обратная матрица тристимулус матрицы применяется к данным XYZ нейтральных элементов, чтобы получить линейные данные RGB, которые затем сопоставляются с цифровым значением RGB с использованием нелинейной регрессии в модели Гог.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-491">The inverse matrix of the tristimulus matrix is applied to the XYZ data of the neutrals to obtain the linear RGB data, which is then correlated with the digital RGB values using nonlinear regression on the GOG model.</span></span> <span data-ttu-id="fe4b7-492">Эти характеристики не обязательно должны быть одинаковыми для каналов R, G и B и обычно не совпадают.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-492">These characteristics do not have to be the same for the R, G, and B channels, and generally are not the same.</span></span>

<span data-ttu-id="fe4b7-493">Бернс \[ 1 \] : Бернс, *Биллмэйер и салтзман принципы цветовой технологии*, 3 <sub>RD</sub> ED.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-493">Berns\[1\]: Berns, *Billmeyer and Saltzman's Principles of Color Technology*, 3 <sub>rd</sub> Ed.</span></span> <span data-ttu-id="fe4b7-494">Джон Wiley & сыновьями (2000).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-494">John Wiley & Sons (2000).</span></span>

<span data-ttu-id="fe4b7-495">Бернс \[ 2 \] : Бернс и катох, функция Digital to радиометрик для обмена с управляемыми компьютерами CRT, *Цие эксперт Symposium ' 97 цветовые стандарты для технологии создания образов*, Ноя. 1997.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-495">Berns\[2\]: Berns and Katoh, The digital to radiometric transfer function for computer controlled CRT displays, *CIE Expert Symposium '97 Colour Standards for Imaging Technology*, Nov. 1997.</span></span>

<span data-ttu-id="fe4b7-496">Бернс \[ 3 \] : Бернс, Фернандес и Таплин, оценка Black-Level выбросов Computer-Controlled, просмотр *цветов и приложения*, 28:379-383 Wiley периодов, Inc. (2003)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-496">Berns\[3\]: Berns, Fernandez and Taplin, Estimating Black-Level Emissions of Computer-Controlled Displays, *Color Research and Application*, 28: 379-383 Wiley Periodicals, Inc. (2003)</span></span>

<span data-ttu-id="fe4b7-497">Канг \[ 1 \] : Канг, *цветовая технология для устройств электронных изображений*, Спие (1997)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-497">Kang\[1\]: Kang, *Color Technology for Electronic Imaging Devices*, SPIE (1997)</span></span>

<span data-ttu-id="fe4b7-498">Катох \[ 1 \] : Катох, Дегучи и Бернс, точная кодировка предложения CRT Monitor (II) для расширения в метод Цие и его проверки, *OPT. Rev.* 8:397-408 (2001)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-498">Katoh\[1\]: Katoh, Deguchi and Berns, An accurate characterization of CRT monitor (II) proposal for an extension to CIE method and its verification, *Opt. Rev.* 8: 397-408 (2001)</span></span>

### <a name="lcd-device-model-baseline"></a><span data-ttu-id="fe4b7-499">Базовая модель устройства LCD</span><span class="sxs-lookup"><span data-stu-id="fe4b7-499">LCD Device Model Baseline</span></span>

<span data-ttu-id="fe4b7-500">Базовый план модели ЖК-устройства подобен базовому плану модели устройства CRT.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-500">The LCD Device Model Baseline is similar to the CRT Device Model Baseline.</span></span> <span data-ttu-id="fe4b7-501">В этом разделе рассматриваются способы, с помощью которых ЖК-моделирование отличается от моделирования CRT.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-501">This section will explain the ways in which LCD modeling differs from CRT modeling.</span></span>

<span data-ttu-id="fe4b7-502">Одно отличие заключается в том, что ЖК-дисплеи должны следовать за моделью Гог, используемой для библиотек CRT, а кривые тона получаются путем интерполяции измеряемых данных.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-502">One difference is that you cannot assume that LCD displays follow the GOG model used for CRTs, and the tone curves are obtained by interpolation of measured data.</span></span> <span data-ttu-id="fe4b7-503">По этой причине независимая ось устройства должна быть выборке чаще.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-503">Because of that, the device neutral axis should be sampled more frequently.</span></span>

<span data-ttu-id="fe4b7-504">Ниже приведены некоторые типичные примеры значений, которые могут формировать хорошие данные для базового показателя модели ЖК-устройства.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-504">Here are some typical example values that can generate good data for the LCD device model baseline:</span></span>

<span data-ttu-id="fe4b7-505">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-505">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="fe4b7-506">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-506">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="fe4b7-507">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-507">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="fe4b7-508">Нейтральные: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span></span>

<span data-ttu-id="fe4b7-509">Вычисление среднего цветового цвета для получения цветов для первичных элементов устройств является более важным для LCDs, чем для библиотек CRT.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-509">The process of averaging measured color chromaticies to obtain the chromaticities for the device primaries is more critical for LCDs than it is for CRTs.</span></span> <span data-ttu-id="fe4b7-510">При отображении единиц измерения "XYZ" на плоскости *XY* -нолики типичная ситуация показана на рис. 1.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-510">When XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="fe4b7-511">Обратите внимание на смещение цветовой области к черной точке.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-511">Notice how the chromaticity drifts toward the black point.</span></span> <span data-ttu-id="fe4b7-512">Это обусловлено тем, что все LCDs имеют определенный уровень утечки освещения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-512">This is because all LCDs have a certain amount of light leakage.</span></span>

![Схема, показывающая график цветовой области с помощью необработанных данных без исправления.](images/cdmp-lcd-dmp-figure1.png)

<span data-ttu-id="fe4b7-514">**Рис. 1** . схема цветовой области, использующая необработанные данные без исправления</span><span class="sxs-lookup"><span data-stu-id="fe4b7-514">**Figure 1** : The chromaticity diagram using raw data with no correction</span></span>

<span data-ttu-id="fe4b7-515">При вычитании из необработанных измерений XYZ типичная ситуация показана на рис. 2.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-515">When this is subtracted from the raw XYZ measurements, a typical situation is depicted in Figure 2.</span></span> <span data-ttu-id="fe4b7-516">Теперь точки Tне кластеризованы по трем центрам, хотя они не идентичны.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-516">Tthe points are now clustered about three centers, although they don't fall identically on them.</span></span> <span data-ttu-id="fe4b7-517">Процесс усреднения, описанный для библиотек CRT, значительно улучшает результаты для LCDs.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-517">The averaging process described for CRTs greatly improves the results for LCDs.</span></span>

![Схема, показывающая график насыщенности с помощью необработанных данных с настроенной черной точкой.](images/cdmp-lcd-dmp-figure2.png)

<span data-ttu-id="fe4b7-519">**Рис. 2** . схема цветовой области с использованием данных с скорректированной черной точкой</span><span class="sxs-lookup"><span data-stu-id="fe4b7-519">**Figure 2** : The chromaticity diagram using data with adjusted black point</span></span>

### <a name="rgb-capture-device-model-baseline"></a><span data-ttu-id="fe4b7-520">Базовая модель устройства для записи RGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-520">RGB Capture Device Model Baseline</span></span>

<span data-ttu-id="fe4b7-521">Базовая модель устройства отслеживания RGB является подклассом класса Идевицемодел.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-521">The baseline RGB capture device model is a subclass of the IDeviceModel class.</span></span> <span data-ttu-id="fe4b7-522">В кодировке для устройств записи цветов, таких как сканеры и Цифровые камеры, используется следующий подход.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-522">In the colorimetric characterization of color capture devices, such as scanners and digital cameras, the following approach is used.</span></span> <span data-ttu-id="fe4b7-523">Целевой объект, состоящий из цветовых исправлений с известными значениями ЦИЕКСИЗ, захватывается с помощью устройства записи.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-523">A target consisting of color patches with known CIEXYZ values is captured using the capture device.</span></span> <span data-ttu-id="fe4b7-524">Результатом захвата является растровое изображение RGB, в котором цвет каждого исправления кодируется в значении RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-524">The result of the capture is an RGB bitmap image in which the color of each patch is encoded in an RGB value.</span></span> <span data-ttu-id="fe4b7-525">Значения RGB для устройства зависят от конкретного устройства записи.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-525">These device RGB values are specific to a particular capture device.</span></span> <span data-ttu-id="fe4b7-526">Цель кодировки «+ +» заключается в том, чтобы установить многообразную связь между значениями RGB устройства и значениями ЦИЕКСИЗ, а также математическим преобразованием из RGB в XYZ, чтобы точно определить, насколько возможно поведение устройства записи.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-526">The goal of colorimetric characterization is to establish an empirical relationship between the device RGB values and CIEXYZ values, or a mathematical transformation from RGB to XYZ that models as accurately as possible the behavior of the capture device.</span></span>

<span data-ttu-id="fe4b7-527">Такое математическое преобразование может быть смоделировано с учетом степени полинома низкого угла.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-527">Such a mathematical transformation can be modeled reasonably by polynomials of low degrees.</span></span> <span data-ttu-id="fe4b7-528">Эта процедура описана в литературе, например Канг \[ 92 \] , Канг \[ 97 \] .</span><span class="sxs-lookup"><span data-stu-id="fe4b7-528">This procedure is detailed in the literature, for example Kang\[92\], Kang\[97\].</span></span> <span data-ttu-id="fe4b7-529">В Канг \[ 97 используется \] подход, в котором используется набор из трех значений полинома с 3, 6, 8, 9, 11, 14 или 20 терминами в переменных R, G и B, тогда как три свойства регрессии, соответственно, в компоненты X, Y и Z Циексиз пространства.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-529">In Kang\[97\], an approach is reported that uses a set of three polynomials with 3, 6, 8, 9, 11, 14 or 20 terms in the R, G, and B variables, while the three polynomials regress respectively into the X, Y, Z components of the CIEXYZ space.</span></span> <span data-ttu-id="fe4b7-530">Для 20-словного полинома используется форма:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-530">For the 20-term polynomial, the form is:</span></span>

![Показывает 20-условный полином.](images/cdmp-formula20.png)

<span data-ttu-id="fe4b7-532">Существуют похожие выражения для Y и Z. Математическая методика для подгонки полиномов попадает в «многофакторная линейную регрессию» и описывается в любом простейшем тексте в статистике.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-532">There are similar expressions for Y and Z. The mathematical technique for fitting the polynomials falls within "Multivariate Linear Regression" and is described in any elementary text in Statistics.</span></span>

<span data-ttu-id="fe4b7-533">Этот метод линейной регрессии имеет значение, не уменьшая правую функцию цели.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-533">This method of linear regression suffers from not minimizing the "right" objective function.</span></span> <span data-ttu-id="fe4b7-534">Линейная регрессия находит наименьшее из квадратов, что означает, что коэффициенты, полученные в результате, уменьшают общую сумму квадратов ошибок в базовом пространстве или эквивалентно сумме квадратов евклидово расстояний.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-534">By design, linear regression finds the least squares solution, which implies that the coefficients obtained will minimize the total sum of squares of errors in the underlying space, or equivalently, the sum of squares of the Euclidean distances.</span></span> <span data-ttu-id="fe4b7-535">На практике требуется максимально сокращать сумму квадратов? Откуда? E — один из принятых стандартов, таких как CIE94.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-535">In practice, you want to minimize the sum of squares of ?Es, where ?E is one of the accepted standards such as CIE94.</span></span> <span data-ttu-id="fe4b7-536">Минимизация этой целевой функции — это нелинейная задача регрессии.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-536">Minimizing this objective function is a nonlinear regression problem.</span></span>

<span data-ttu-id="fe4b7-537">В новом подсистеме в качестве лабораторного к XYZ используется ЦИЕ цветовое пространство, а в качестве модели для устройства захвата используется 20-термный коэффициент кубического уровня, а для использования в качестве подсчета, в котором следующие полиномы уменьшают сумму квадратов? E <sub>CIE94</sub> s.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-537">In the new engine, Lab to XYZ is the CIE color space that is regressed into, and the 20-term cubic polynomial is used as the model for the capture device, or coefficients ls,as,bs such that the following polynomials minimize the sum of squares of ?E <sub>CIE94</sub> s.</span></span>

![Отображает набор формул полинома.](images/cdmp-formula21.png)

<span data-ttu-id="fe4b7-539">Решение ( *l <sub>i</sub>*, *а <sub></sub>* я, *b <sub>i</sub>* ) в 60-мерный вещественном числовом пространстве **R** 203 должно быть таким, чтобы следующая общая ошибка была минимальна:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-539">The solution ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) in the 60-dimensional real numeric space **R** 203 must be such that the following total error is minimized:</span></span>

![Показывает общую ошибку для сворачивания.](images/cdmp-formula22.png)

<span data-ttu-id="fe4b7-541">где суммирование проходит через все пары точек данных (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub></sub>*,*v <sub>i</sub>* ) в наборе данных выборки, а также дополнительные контрольные точки, которые должны быть подробно описаны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-541">where the summation is through all the data point pairs (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v<sub>i</sub>* ) in the sampled data set plus additional control points to be detailed in the following.</span></span> <span data-ttu-id="fe4b7-542">Это нелинейная задача регрессии, *поскольку параметры <sub> я</sub>*, *a <sub></sub>*, \* <sub>i</sub>\* вводит в функцию цели нелинейный способ (не в виде квадратичного).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-542">This is a nonlinear regression problem because the parameters *?<sub>i</sub>*, *a<sub>i</sub>*, \* <sub>i</sub>\* enter into the objective function in a nonlinear way (not quadratically).</span></span>

<span data-ttu-id="fe4b7-543">Поскольку функция задания?</span><span class="sxs-lookup"><span data-stu-id="fe4b7-543">Because the objective function ?</span></span> <span data-ttu-id="fe4b7-544">является нелинейной (и неквадратичной) функцией параметров *?<sub> я</sub>*, *а <sub>i</sub>* и \* <sub>i</sub>\*, чтобы решить проблему оптимизации, необходимо прибегнуть к итеративным методам.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-544">is a nonlinear (and nonquadratic) function of the parameters *?<sub>i</sub>*, *a<sub>i</sub>* and \* <sub>i</sub>\*, you must resort to iterative techniques to solve the optimization problem.</span></span> <span data-ttu-id="fe4b7-545">Поскольку форма функции задания является суммой квадратов, используется стандартный метод оптимизации, называемый алгоритмом Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-545">Because the form of the objective function is a sum of squares, a standard optimization technique called the Levenberg-Marquardt algorithm is used.</span></span> <span data-ttu-id="fe4b7-546">Он считается методом выбора для проблем с нелинейным наименьшим числом квадратов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-546">It is considered the method of choice for nonlinear least squares problems.</span></span> <span data-ttu-id="fe4b7-547">Для итеративных алгоритмов, таких как Левенберг-Маркварт, необходимо указать начальное предположение.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-547">For iterative algorithms such as Levenberg-Marquardt, you must supply an initial guess.</span></span> <span data-ttu-id="fe4b7-548">Хорошее первоначальное предположение обычно является критически важным при поиске правильного минимального значения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-548">A good initial guess is usually critical in finding the correct minimum value.</span></span> <span data-ttu-id="fe4b7-549">В этом случае один хороший кандидат на первоначальное предположение — решение проблемы линейной регрессии.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-549">In this case, one good candidate for the initial guess is the solution of the linear regression problem.</span></span> <span data-ttu-id="fe4b7-550">Сначала Сократите сумму квадрата евклидово расстояний в лабораторном пространстве, определив функцию, определяющую целевое значение.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-550">First, minimize the sum of the square of Euclidean distances in Lab space, by defining a quadratic objective function:</span></span>

![Показывает определенную функцию для квадратичной цели.](images/cdmp-formula23.png)

<span data-ttu-id="fe4b7-552">Математическое решение такого типа «линейная и наименьшая квадраты» хорошо известно.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-552">The mathematical solution to such "linear least squares" problem is well known.</span></span> <span data-ttu-id="fe4b7-553">Так как *?<sub> я</sub>* появился только в модели *L* , а *<sub>i</sub>* отображается только в модели *u* , а \* <sub>i</sub>\* отображается только в модели *v* . проблему оптимизации можно разложить на три подзадачи: одну для *L*, одну для *u* и одну для *v*.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-553">Because *?<sub>i</sub>* only appears in the *L* modeling, *a <sub>i</sub>* only appears in the *u* modeling, and \* <sub>i</sub>\* only appears in the *v* modeling; the optimization problem can be decomposed into three subproblems: one for *L*, one for *u* and one for *v*.</span></span> <span data-ttu-id="fe4b7-554">Рассмотрим « *L* уравнения».</span><span class="sxs-lookup"><span data-stu-id="fe4b7-554">Consider the *L* equations.</span></span> <span data-ttu-id="fe4b7-555">(Уравнения *u* и *v* уравнения соответствуют точно одному аргументу.) Проблема минимизации суммы квадратов ошибок в *L* может быть обпоставлена следующим уравнением матрицы в некотором смысле наименее квадратов:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-555">(The *u* equations and the *v* equations follow exactly the same argument.) The problem of minimizing the sum of squares of errors in *L* can be stated as solving the following matrix equation in the least squares sense:</span></span>

![Показывает уравнение матрицы для L.](images/cdmp-formula24.png)

<span data-ttu-id="fe4b7-557">где *N* — общее количество точек данных (исходные образцы точек плюс контрольные точки, созданные описанными ниже способами).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-557">where *N* is the total number of data points (original sampled points plus control points created in a manner described below).</span></span> <span data-ttu-id="fe4b7-558">Как правило, *N* гораздо больше 20, поэтому предыдущее уравнение было чрезмерно определено, что требует наименьшего решения в виде квадратов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-558">Typically, *N* is much larger than 20, so the preceding equation is over-determined, requiring a least squares solution.</span></span> <span data-ttu-id="fe4b7-559">Это решение для закрытых форм **?**</span><span class="sxs-lookup"><span data-stu-id="fe4b7-559">A closed form solution for **?**</span></span> <span data-ttu-id="fe4b7-560">доступен:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-560">is available:</span></span>

![Отображает решение закрытой формы.](images/cdmp-formula25.png)

<span data-ttu-id="fe4b7-562">На практике прямое вычисление с помощью решения закрытой формы не используется, так как оно имеет неудовлетворительные числовые свойства.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-562">In practice, direct evaluation using the closed form solution is not used because it has poor numerical properties.</span></span> <span data-ttu-id="fe4b7-563">Вместо этого некоторый тип алгоритма факторинга матрицы применяется к матрице коэффициента, которая сокращает систему уравнений до канонической формы.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-563">Instead, some kind of matrix factorization algorithm is applied to the coefficient matrix which reduces the system of equations to a canonical form.</span></span> <span data-ttu-id="fe4b7-564">В текущей реализации для матрицы **R** применяется декомпозиция единственного значения (SVD), а затем разрешается полученная декомпозиция системы.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-564">In the current implementation, Singular Value Decomposition (SVD) is applied to the matrix **R** and then the resulting decomposed system is solved.</span></span>

<span data-ttu-id="fe4b7-565">Решение проблемы линейной регрессии, обозначенное, ![ показывает решение проблемы линейной регрессии.](images/cdmp-formula26.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-565">The solution to the linear regression problem, denoted by ![Shows the solution to the linear regression problem.](images/cdmp-formula26.png)</span></span> <span data-ttu-id="fe4b7-566">, используется в качестве начальной точки алгоритма Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-566">, is used as the starting point of the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="fe4b7-567">В этом алгоритме вычисляются шаги пробной версии, которые должны двигаться ближе к оптимальному решению.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-567">In this algorithm, a trial step is computed that should move the point closer to the optimal solution.</span></span> <span data-ttu-id="fe4b7-568">Этап пробной версии удовлетворяет набору линейных уравнений, зависящих от функционального значения и значений производных элементов в текущей точке.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-568">The trial step satisfies a set of linear equations dependent on the functional value and values of the derivatives at the current point.</span></span> <span data-ttu-id="fe4b7-569">По этой причине производные от функции цели?</span><span class="sxs-lookup"><span data-stu-id="fe4b7-569">For this reason, the derivatives of the objective function ?</span></span> <span data-ttu-id="fe4b7-570">в отношении параметров *?<sub> i</sub>*, *я <sub></sub> <sub></sub>* потребовал входные данные для алгоритма Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-570">with respect to the parameters *?<sub>i</sub>*, *a<sub>i</sub> <sub>i</sub>* are required inputs to the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="fe4b7-571">Хотя существует 60 параметров, существует ярлык, позволяющий вычислять гораздо меньше.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-571">Although there are 60 parameters, there is a shortcut that allows you to compute a lot less.</span></span> <span data-ttu-id="fe4b7-572">По правилу цепочки математического анализа за,</span><span class="sxs-lookup"><span data-stu-id="fe4b7-572">By the Chain Rule of Calculus,</span></span>

![Показывает уравнение, которое позволяет использовать ярлык с помощью правила цепочки математического анализа за.](images/cdmp-formula27.png)

<span data-ttu-id="fe4b7-574">где *j* = 1, 2,, 20, *L <sub>i</sub>*,*u <sub>я</sub>*,*v <sub>i</sub>* *— это значение Циелаб в качестве* образца, а *R <sub>ИЖ</sub>* — это запись (*i*,*j* ), определенная **выше матрицы** .</span><span class="sxs-lookup"><span data-stu-id="fe4b7-574">where *j* = 1, 2,  , 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* are the CIELAB value of the *i* th sample point, and *R <sub>ij</sub>* is the (*i*,*j* )th entry of the matrix **R** defined above.</span></span> <span data-ttu-id="fe4b7-575">Таким образом, вместо вычисления производных для параметров 60 можно вычислять производные для *L*,*a* и *b* , используя числовые разностные вычисления.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-575">So instead of computing derivatives for 60 parameters, you can compute derivatives for *L*,*a*, and *b* using numerical forward differencing.</span></span>

<span data-ttu-id="fe4b7-576">Также необходимо настроить критерий остановки для итерационных алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-576">It is also necessary to set up a stopping criterion for iterative algorithms.</span></span> <span data-ttu-id="fe4b7-577">В текущей реализации итерации завершаются, если среднее значение квадрата DECIE94 меньше 1 или число выполненных итераций превысило 10.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-577">In the current implementation, the iterations are terminated if the mean square DECIE94 is less than 1, or the number of iterations performed has exceeded 10.</span></span> <span data-ttu-id="fe4b7-578">Число 10 поступает из практического опыта, если первые несколько итераций не уменьшают ошибку значительно, а дальнейшие итерации не будут настолько полезны, как перемещение точки осЦиллатори способом, т. е. алгоритм может не сходится.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-578">The number 10 comes from the practical experience that if the first few iterations do not reduce the error significantly, further iterations would not help much other than moving the point in an oscillatory manner, i.e., the algorithm may not converge.</span></span> <span data-ttu-id="fe4b7-579">Даже в том случае, если алгоритм сходится, мы можем убедиться, что DECIE94 не хуже того, что мы начали, т. е. с параметрами, полученными из линейной регрессии.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-579">Even in the case that the algorithm diverges, we can be sure that the DECIE94 is no worse than what we started, i.e. with the parameters obtained from linear regression.</span></span>

<span data-ttu-id="fe4b7-580">Даже при использовании предыдущего метода нелинейной регрессии возникает несколько проблем с подгонками.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-580">Even with the preceding method of nonlinear regression, there are several problems with the fitting.</span></span> <span data-ttu-id="fe4b7-581">Одна из проблем заключается в том, что степень сложности обычно отклонение или с неисправностью за точками данных.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-581">One problem is that the polynomials tend to overshoot or undershoot beyond the data points.</span></span> <span data-ttu-id="fe4b7-582">Искусственные локальные прыжка и прыжка могут быть введены в процесс подгонки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-582">Artificial local maxima and minima may be introduced in the fitting process.</span></span> <span data-ttu-id="fe4b7-583">Это можно запретить с помощью полиномов низкого уровня, что является причиной, по которой не следует использовать более трех градусов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-583">This can be counteracted by using polynomials of low degree, which is the reason you should not use higher than three degrees.</span></span> <span data-ttu-id="fe4b7-584">Более серьезный аспект снижения или прокрутки заключается в том, что, хотя степень серьезности может принимать любое вещественное значение теоретически, пространство, которое он пытается смоделировать, обычно имеет физические ограничения и практические ограничения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-584">A more serious aspect of overshooting or undershooting is that, while a polynomial can take any real value theoretically, the space it tries to model typically has physical constraints and practical constraints.</span></span> <span data-ttu-id="fe4b7-585">ЦИЕКСИЗ должен иметь все координаты X, Y и Z, не являющиеся отрицательными, которые являются физическими ограничениями.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-585">CIEXYZ must have all of X, Y, Z non-negative, which is a physical constraint.</span></span> <span data-ttu-id="fe4b7-586">На практике они принимают значения только с сотнями, а не с тысячами и выше.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-586">In practice, they only take values in the magnitude of hundreds, not thousands or higher.</span></span> <span data-ttu-id="fe4b7-587">Аналогичным образом, ЦИЕЛАБ или ЦИЕЛУВ имеет собственные физические и практические ограничения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-587">Similarly, CIELAB or CIELUV has its own physical and practical constraints.</span></span> <span data-ttu-id="fe4b7-588">Если пространство RGB заполнено с точки выборки, проблема с прокруткой или прокруткой не является серьезной.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-588">When the RGB space is filled sufficiently with sample points, the problem of overshooting or undershooting is not serious.</span></span> <span data-ttu-id="fe4b7-589">Однако захваченные точки RGB из устройства записи обычно не заполняют пространство RGB единообразно.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-589">However, the captured RGB points from the capture device do not usually fill up the RGB space uniformly.</span></span> <span data-ttu-id="fe4b7-590">Точки могут заполнить только внутренний 80% Куба RGB, или, что более того, они могут находиться в более низком эта функция предназначена.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-590">The points may fill up only inner the 80% of the RGB cube, or worse, they may reside in a lower dimensional manifold.</span></span> <span data-ttu-id="fe4b7-591">В этом случае при экстраполяции значений за пределами точек данных нереалистичные прогнозы могут оказаться неудовлетворительными.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-591">When this happens, the regressed polynomials may do a poor job at extrapolating the values beyond the data points, sometimes returning unrealistic predictions.</span></span> <span data-ttu-id="fe4b7-592">Необходимо, чтобы модель всегда возвращала разумные значения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-592">You want a model that always returns reasonably realistic values.</span></span> <span data-ttu-id="fe4b7-593">Для этого требуется метод, который может эффективно управлять поведением границ регрессивной регрессии, установления дополнительные затраты на эти степени, которые работают нестабильно, близко к границе Куба RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-593">This requires a method that can effectively control the boundary behavior of regression polynomials by imposing additional cost to those polynomials that behave erratically near the boundary of the RGB cube.</span></span> <span data-ttu-id="fe4b7-594">Еще одной мерой, гарантирующей, что полиномы всегда возвращают реалистичные значения, применяются путем усечения выходных данных в ЦИЕ Спектрал очага.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-594">A further measure to ensure that the polynomials always return realistic values is applied by clipping the output to within the CIE spectral locus.</span></span>

<span data-ttu-id="fe4b7-595">На этом этапе моделирование сканера и моделирование камеры расходят друг от друга.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-595">It is at this point that the scanner modeling and camera modeling diverge from each other.</span></span> <span data-ttu-id="fe4b7-596">Предполагается, что модель камеры будет выделена до регионов за пределами выбранных точек, включая «отраженные блики», для модели сканера не требуется одинаковая экстраполяция.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-596">The camera model is expected to extrapolate to regions beyond the sampled points including the "specular highlights," the same extrapolation is not required for the scanner model.</span></span> <span data-ttu-id="fe4b7-597">Предполагается, что цель сканера охватывает сходство, похожее на печатные материалы, которые должны быть проверены.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-597">The scanner target is expected to cover a characterization that is similar to the printed materials to be scanned.</span></span> <span data-ttu-id="fe4b7-598">Модель сканера все еще должна быть надежной в том смысле, что она не должна возвращать нереалистичные значения, но экстраполяция далеко за пределы целевого объекта не требуется.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-598">The scanner model is still required to be robust in the sense that it should not return unrealistic values, but extrapolation far beyond the characterization target is not required.</span></span> <span data-ttu-id="fe4b7-599">Чтобы обеспечить надежность, значение L-полинома, приведенное выше, обрезается в 100, то есть модель полинома не должна высекаться за пределами "DMin" целевого объекта сканера.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-599">To ensure robustness, the L-polynomial above is clipped at 100, that is, the polynomial model is forced not to extrapolate beyond "Dmin" of the scanner target.</span></span>

<span data-ttu-id="fe4b7-600">Предполагается, что модель камеры будет обрезана до отраженных светов, поэтому обрезка в 100 нежелательна.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-600">The camera model is expected to extrapolate to specular highlights, so clipping at 100 is undesirable.</span></span> <span data-ttu-id="fe4b7-601">Вместо этого используется следующий алгоритм.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-601">Instead, the following algorithm is used.</span></span>

<span data-ttu-id="fe4b7-602">Для управления поведением свойств полиномов в регионах с недостаточным объемом выборки появились контрольные точки искусственного интеллекта.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-602">Artificial control points are introduced to control the behavior of the polynomials in regions with insufficient sampling.</span></span> <span data-ttu-id="fe4b7-603">Стратегические размещение этих контрольных точек с соответствующими значениями позволяет «извлекать» степень полинома в требуемом направлении.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-603">By strategically placing these control points with appropriate values, they serve to "pull" the polynomials in the required direction.</span></span> <span data-ttu-id="fe4b7-604">В текущей реализации используются восемь контрольных точек, соответствующих углам Куба RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-604">In the current implementation, eight control points corresponding to the corners of the RGB cube are used.</span></span> <span data-ttu-id="fe4b7-605">Если значения устройства нормализованы до Unity, то используются следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-605">If the device values are normalized to unity, then these points are:</span></span>

<span data-ttu-id="fe4b7-606">*R* = 0, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-606">*R* = 0, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="fe4b7-607">*R* = 0, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="fe4b7-607">*R* = 0, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="fe4b7-608">*R* = 0, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-608">*R* = 0, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="fe4b7-609">*R* = 0.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-609">*R* = 0.</span></span> <span data-ttu-id="fe4b7-610">*G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="fe4b7-610">*G* = 1, *B* = 1</span></span>

<span data-ttu-id="fe4b7-611">*R* = 1, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-611">*R* = 1, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="fe4b7-612">*R* = 1, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="fe4b7-612">*R* = 1, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="fe4b7-613">*R* = 1, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="fe4b7-613">*R* = 1, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="fe4b7-614">*R* = 1, *G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="fe4b7-614">*R* = 1, *G* = 1, *B* = 1</span></span>

<span data-ttu-id="fe4b7-615">За исключением белого *R*  = *G*  = *B* = 1, связанного со значением Циелаб *L* = 100, *u*  = *v* = 0, для определения подходящего значения Циелаб используется следующий алгоритм экстраполяции.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-615">Except for the white *R* =*G* =*B* = 1, which is associated with a CIELAB value of *L* = 100, *u* =*v* = 0, the following extrapolation algorithm is used to determine the appropriate CIELAB value to be associated with.</span></span> <span data-ttu-id="fe4b7-616">Как правило, для конкретного (*r*,*g*,*b* ) вес связан с каждым из (*r <sub>i</sub>*,*g <sub>i</sub>*,*B <sub>i</sub>* ) в наборе данных выборки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-616">Generally, for a given (*R*,*G*,*B* ), a weight is associated with each of the (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ) in the sampled data set.</span></span> <span data-ttu-id="fe4b7-617">Существует две цели для назначения веса.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-617">There are two goals to assigning the weight.</span></span> <span data-ttu-id="fe4b7-618">Во-первых, вес обратно пропорционален расстоянию между (*r*,*g*,*b* ) и (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-618">First, the weight is inversely proportional to the distance between (*R*,*G*,*B* ) and (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ).</span></span> <span data-ttu-id="fe4b7-619">Во-вторых, вы хотите отбросить или присвоить весовой коэффициент 0 к точкам, цвет которых отличается от оттенка данной точки (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-619">Second, you want to discard, or assign weight 0 to, points that have a different hue than the given point (*R*,*G*,*B* ).</span></span> <span data-ttu-id="fe4b7-620">Чтобы сделать оттенок учетной записи, рассмотрите точки, находящиеся внутри конуса, вершина которого равна (0, 0, 0), ось которой совпадает со строкой, соединяющей (0, 0, 0) и (*R*,*G*,*B* ) и вертикальным углом?</span><span class="sxs-lookup"><span data-stu-id="fe4b7-620">To take the hue into account, consider points that lie within a cone whose vertex is at (0, 0, 0), whose axis coincides with the line joining (0, 0, 0) to (*R*,*G*,*B* ), and whose semi-vertical angle ?</span></span> <span data-ttu-id="fe4b7-621">соответствует COS?</span><span class="sxs-lookup"><span data-stu-id="fe4b7-621">satisfies cos ?</span></span> <span data-ttu-id="fe4b7-622">= 0,9.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-622">= 0.9.</span></span> <span data-ttu-id="fe4b7-623">Иллюстрация этого конуса показана на рис. 3.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-623">See Figure 3 for an illustration of this cone.</span></span>

![Схема, показывающая форму окружения.](images/cdmp-lcd-dmp-figure3.png)

<span data-ttu-id="fe4b7-625">**Рис. 3** . Фильтрация образцов точек по угла и расстоянию.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-625">**Figure 3** : Filtering the sample points by angle and distance.</span></span> <span data-ttu-id="fe4b7-626">Форма окружения показана только для иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-626">The shape of the neighborhood depicted is for illustration purpose only.</span></span> <span data-ttu-id="fe4b7-627">Фактическая фигура зависит от используемого расстояния; Это одноромбное окружение, если используется 1 норма.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-627">The actual shape depends on the distance used; it is a diamond-shaped neighborhood if the 1-norm is used.</span></span>

<span data-ttu-id="fe4b7-628">В этом конусе выполняется вторая фильтрация, основанная на расстоянии RGB, который использует 1-норму, определенную</span><span class="sxs-lookup"><span data-stu-id="fe4b7-628">Within this cone, a second filtering is performed that is based on the RGB distance, which uses the 1-norm, defined by</span></span>

![Показывает формулу для второй фильтрации в конусе.](images/cdmp-formula28.png)

<span data-ttu-id="fe4b7-630">При текущем конусе первоначальный поиск осуществляется для точек, которые находятся в пределах расстояния от 0,1 (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-630">With the current cone, the initial search is for points that are within a distance of 0.1 from (*R*,*G*,*B* ).</span></span> <span data-ttu-id="fe4b7-631">Если в радиусе не найдено ни одной точки, радиус увеличивается на 0,1, а поиск перезапускается.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-631">If no point is found within this radius, the radius is increased by 0.1, and the search is restarted.</span></span> <span data-ttu-id="fe4b7-632">Если следующая скругленная некоторая точка не имеет ни одного, радиус увеличивается на 0,1.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-632">If the next round nets no point either, the radius is increased by 0.1.</span></span> <span data-ttu-id="fe4b7-633">Этот процесс будет продолжен до тех пор, пока радиус не превысит Максдист/5, где Максдист = 3, в случае 1-нормы.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-633">This process continues until the radius exceeds MaxDist/5, where MaxDist = 3, in the case of 1-norm.</span></span> <span data-ttu-id="fe4b7-634">Если точка не найдена, конус увеличивается за счет уменьшения COS?</span><span class="sxs-lookup"><span data-stu-id="fe4b7-634">If no point is found, the cone is enlarged by decreasing the cos ?</span></span> <span data-ttu-id="fe4b7-635">к 0,05, т. е. увеличить угол?</span><span class="sxs-lookup"><span data-stu-id="fe4b7-635">by 0.05, that is, increasing the angle ?</span></span> <span data-ttu-id="fe4b7-636">и перезапускает весь процесс с увеличивающимся радиусом.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-636">and restarting the whole process with an increasing radius.</span></span> <span data-ttu-id="fe4b7-637">Этот процесс будет продолжен до тех пор, пока не будет найден непустой набор точек или COS?</span><span class="sxs-lookup"><span data-stu-id="fe4b7-637">This process continues until a non-empty set of points is found, or cos ?</span></span> <span data-ttu-id="fe4b7-638">достигает значения 0, то есть конус открыт, чтобы стать плоскостью.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-638">reaches 0, that is, the cone has opened up to become a plane.</span></span> <span data-ttu-id="fe4b7-639">На этом этапе Поиск перезапускается путем увеличения радиуса, за исключением того, что поиск будет продолжен до тех пор, пока радиус не достигнет Максдист.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-639">At this point, the search is restarted by increasing the radius, except that the search continues until the radius reaches MaxDist.</span></span> <span data-ttu-id="fe4b7-640">Это гарантирует, что в худшем случае будет найден непустой набор точек.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-640">This guarantees that in the worst-case scenario, a non-empty set of points will be found.</span></span> <span data-ttu-id="fe4b7-641">Этот алгоритм суммируется на схеме Flow на рис. 4.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-641">The algorithm is summarized in the flow diagram in Figure 4.</span></span>

![Схема, показывающая последовательность алгоритма.](images/cdmp-lcd-dmp-figure4.png)

<span data-ttu-id="fe4b7-643">**Рисунок 4** . Схема потока для определения набора точек выборки, используемых в экстраполяции для входного значения RGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-643">**Figure 4** : Flow diagram for determining the set S of sample points used in the extrapolation for an input RGB value</span></span>

<span data-ttu-id="fe4b7-644">При условии, что предыдущий процесс *выдает непустой набор точек* (*R <sub>i</sub>*,*G <sub>i</sub>*,*b <sub>i</sub>* ) и соответствующий (*L <sub>i</sub>*,*а <sub>я</sub>*,*b <sub>i</sub>* ), то для каждой такой точки назначается *вес,<sub></sub>* присвоенный</span><span class="sxs-lookup"><span data-stu-id="fe4b7-644">Assuming that the preceding process yields a non-empty set *S* of points (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) and corresponding (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), then for each such point, a weight *w<sub>i</sub>* is assigned, given by</span></span>

![Показывает формулу для веса для каждой точки.](images/cdmp-formula29.png)

<span data-ttu-id="fe4b7-646">Наконец, екстраполант определяется</span><span class="sxs-lookup"><span data-stu-id="fe4b7-646">Finally, the extrapolant is defined by</span></span>

![Показывает определение для екстраполант.](images/cdmp-formula30.png)

<span data-ttu-id="fe4b7-648">Предыдущие уравнения составляют экземпляр "взвешенных методов обратного расстояния", обычно называемых методами Шепард.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-648">The preceding equations constitute an instance of the "inverse-distance weighted methods," commonly called the Shepard methods.</span></span> <span data-ttu-id="fe4b7-649">Выполняя каждую из восьми точек с EQ (6) через алгоритм, получаются восемь контрольных точек, каждая из которых имеет значения *R*,*G*,*B* и *L*,*a*,*b* , которые помещаются в пул с исходными образцами данных.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-649">By running each of the eight points from eq (6) through the algorithm, eight control points are obtained, each with *R*,*G*,*B* and *L*,*a*,*b* values, which are put into the pool with the original sample data.</span></span>

<span data-ttu-id="fe4b7-650">Чтобы гарантировать, что модель всегда формирует допустимые значения цвета, и целостность системы и стабильность всего конвейера обработки цветов, необходимо выполнить окончательную отсечение с выходными данными модели полинома.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-650">To ensure that the model always produces valid color values and for system integrity and stability down the whole color processing pipeline, you must perform a final clipping to the output of the polynomial model.</span></span> <span data-ttu-id="fe4b7-651">Визуальный охват ЦИЕ описывается компонентом ачроматик (*Y* или *L* ) и компонентом цветового элемента (*XY* или *а'б*), которые связаны с пространством XYZ с помощью многопроектного преобразования).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-651">The CIE visual gamut is described by the achromatic component (*Y* or *L* ) and the chromatic component (*xy* or *a'b'*, which are related to the XYZ space by a projective transformation).</span></span> <span data-ttu-id="fe4b7-652">В текущей реализации используется цвет « *а'б»* , так как он напрямую связан с Циелув пространством.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-652">In the current implementation, the *a'b'* chromaticity is used because it is directly related to the CIELUV space.</span></span> <span data-ttu-id="fe4b7-653">Для любого значения *Циелаб* сначала Clip *L* в неотрицательное значение:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-653">For any *CIELAB* value, first clip *L* to a non-negative value:</span></span>

![Показывает отсечение L с неотрицательным значением.](images/cdmp-formula31.png)

<span data-ttu-id="fe4b7-655">Чтобы разрешить экстраполяцию для отраженных светов, *L* не обрезается в 100, "обычной" верхней границы для *L* в пространстве лаборатории.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-655">To allow extrapolation for specular highlights, *L* is not clipped at 100, the "conventional" upper bound for *L* in Lab space.</span></span>

<span data-ttu-id="fe4b7-656">Затем, если *L* = 0, то *a* и *b* обрезаются таким, что a *= b =* 0.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-656">Next, if *L* = 0, then *a* and *b* are clipped such that a *= b =* 0.</span></span> <span data-ttu-id="fe4b7-657">Если *L* ?</span><span class="sxs-lookup"><span data-stu-id="fe4b7-657">If *L* ?</span></span> <span data-ttu-id="fe4b7-658">0, вычислить</span><span class="sxs-lookup"><span data-stu-id="fe4b7-658">0, calculate</span></span>

![Показывает формулу, если L = 0.](images/cdmp-formula32.png)

<span data-ttu-id="fe4b7-660">Это компоненты вектора в схеме *а'б* из белого пункта (*u? "*,*v?"*</span><span class="sxs-lookup"><span data-stu-id="fe4b7-660">These are the components of a vector in the *a'b'* diagram from the white point (*u?'*,*v?'*</span></span> <span data-ttu-id="fe4b7-661">) к рассматриваемому цвету.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-661">) to the color in question.</span></span> <span data-ttu-id="fe4b7-662">Определите ЦИЕ Спектрал очага как выпуклой поверхности всех точек (*a "*,*b"* ), параметризованных вавеленгс?:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-662">Define the CIE spectral locus as the convex hull of all the points (*a'*,*b'* ), parameterized by the wavelength ?:</span></span>

![Показывает формулу для вавеленгс.](images/cdmp-formula33.png)

<span data-ttu-id="fe4b7-664">где ![ отображаются функции для сопоставления цветов Цие.](images/cdmp-formula34.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-664">where ![Shows the functions for CIE color-matching.](images/cdmp-formula34.png)</span></span> <span data-ttu-id="fe4b7-665">— Это ЦИЕ функции сопоставления цветов для наблюдателя с 2 градусами.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-665">are the CIE color-matching functions for the 2-degree observer.</span></span> <span data-ttu-id="fe4b7-666">Если вектор находится за пределами ЦИЕ очага, он обрезается до точки на ЦИЕ очага, которая является пересечением очага и линией, определенной вектором.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-666">If the vector lies outside the CIE locus, the color is clipped to the point on the CIE locus that is the intersection of the locus and the line defined by the vector.</span></span> <span data-ttu-id="fe4b7-667">См. рис. 5.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-667">See Figure 5.</span></span> <span data-ttu-id="fe4b7-668">Если обрезка произошла, значение *a* и *b* перестраивается с помощью первого вычитания *?*</span><span class="sxs-lookup"><span data-stu-id="fe4b7-668">If clipping has occurred, the *a* and *b* value is reconstructed by first subtracting *a?'*</span></span> <span data-ttu-id="fe4b7-669">и *b? '*</span><span class="sxs-lookup"><span data-stu-id="fe4b7-669">and *b?'*</span></span> <span data-ttu-id="fe4b7-670">из обрезанного *типа "* и *b"* и затем умножения на 13 *L*.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-670">from the clipped *a'* and *b'*, and then multiplying by 13 *L*.</span></span>

![Схема, на которой показан график для алгоритма обрезки.](images/cdmp-lcd-dmp-figure5.png)

<span data-ttu-id="fe4b7-672">**Рис. 5** . Алгоритм обрезки для значений Lab, которые выходят за пределы визуального элемента Цие</span><span class="sxs-lookup"><span data-stu-id="fe4b7-672">**Figure 5** : Clipping algorithm for Lab values that are outside the CIE visual gamut</span></span>

<span data-ttu-id="fe4b7-673">В текущей реализации ЦИЕ Спектрал очага в плоскости *а'б* представляет собой кусочно-линейную кривую с 35 сегментами (соответствующей вавеленгс от 360 nm до 700 nm включительно).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-673">In the current implementation, the CIE spectral locus in the *a'b'* plane is represented by a piecewise linear curve with 35 segments (corresponding to a wavelength from 360 nm to 700 nm inclusive).</span></span> <span data-ttu-id="fe4b7-674">При упорядочении сегментов линии таким образом, чтобы их часть в белой точке была в порядке возрастания, что эквивалентно убыванию вавеленгсс, сегмент линии, пересекающийся с лучом, сформированный приведенным выше вектором, может быть обнаружен простым двоичным поиском.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-674">By ordering the line segments so that their subtended angles at the white point are ascending, which is equivalent to descending wavelengths, the line segment that intersects with the ray formed by the above vector can be found by a simple binary search.</span></span>

### <a name="rgb-printer-device-model-baseline"></a><span data-ttu-id="fe4b7-675">Базовый план модели устройства принтера RGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-675">RGB Printer Device Model Baseline</span></span>

<span data-ttu-id="fe4b7-676">Устройство печати RGB-принтера состоит из создания многообразовой модели устройства, которая прогнозирует независимый от устройства ЦИЕЛУВ цвет для любого значения RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-676">A device characterization of a RGB printer consists of constructing an empirical model of the device that predicts the device-independent CIELUV color for any given RGB value</span></span>

<span data-ttu-id="fe4b7-677">Существует два способа создания многовариантной модели.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-677">There are two ways to construct the empirical model.</span></span> <span data-ttu-id="fe4b7-678">Один из способов — использовать данные устройства для принтера RGB, а другой — использовать аналитические данные параметров.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-678">One way is to use the device data for a RGB printer, and the other is to use analytical parameter data.</span></span> <span data-ttu-id="fe4b7-679">В первом случае данные измерения, предоставленные пользователем для устройства принтера RGB, используются для создания таблицы 3-D Lookup (LUT).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-679">In the first one, measurement data provided by a user for a RGB printer device is used to construct 3-D lookup table (LUT).</span></span> <span data-ttu-id="fe4b7-680">Данные измерения состоят из значений XYZ для одинаковых выборочных исправлений RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-680">The measurement data consists of XYZ values for uniformly sampled RGB patches.</span></span> <span data-ttu-id="fe4b7-681">Стандартные размеры выборки — 9 или 17 для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-681">Typical sampling sizes are 9 or 17 for each component.</span></span> <span data-ttu-id="fe4b7-682">Каждое исправление измеряется с помощью колориметер или спектрофотометер в ЦИЕКСИЗ пространстве.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-682">Each patch is measured with a colorimeter or spectrophotometer in CIEXYZ space.</span></span> <span data-ttu-id="fe4b7-683">Затем значение XYZ для исправления преобразуется в значение ЦИЕЛУВ, формирующее трехмерную LUT.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-683">The XYZ value for a patch is then converted into CIELUV value, forming a 3-D LUT.</span></span> <span data-ttu-id="fe4b7-684">В модели устройства метод интерполяции тетрахедрал Сакамото применяется к трехмерной LUT для прогнозирования данных ЦИЕЛУВ для данных RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-684">In the device model, the Sakamoto's tetrahedral interpolation method is applied to the 3-D LUT in order to predict the CIELUV data for a given RGB data.</span></span> <span data-ttu-id="fe4b7-685">(Сакамото США, патент 4275413 (Сакамото) 4511989, Канг \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fe4b7-685">(Confer US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="fe4b7-686">Истек срок действия двух упомянутых патентов.).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-686">The two patents mentioned have expired.).</span></span> <span data-ttu-id="fe4b7-687">Аналитические параметры, переданные во втором методе, — это просто LUT, который был построен ранее.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-687">The analytical parameter data passed in the second method is simply a LUT that was built previously.</span></span> <span data-ttu-id="fe4b7-688">Как правило, этот LUT был создан с помощью первого метода, хотя он может быть создан вручную.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-688">Typically, that LUT was built using the first method, although it could be hand-built.</span></span>

<span data-ttu-id="fe4b7-689">В текущем управлении цветом исходная схема определяется как схема, которая перемещается из пространства RGB в аппаратно-независимое цветовое пространство ЦИЕКСИЗ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-689">In the current color management, the source map is defined as the map that goes from RGB space to a device-independent CIEXYZ color space.</span></span> <span data-ttu-id="fe4b7-690">Целевая схема определяется как схема, которая перемещается из аппаратно-независимого ЦИЕКСИЗ цветового пространства в пространство RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-690">The destination map is defined as the map that goes from the device-independent CIEXYZ color space to RGB space.</span></span> <span data-ttu-id="fe4b7-691">Это обратная схема исходного кода.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-691">It is the inverse of the source map.</span></span>

<span data-ttu-id="fe4b7-692">Модель с использованием модели используется непосредственно в исходной карте.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-692">The empirical model is directly used in the source map.</span></span> <span data-ttu-id="fe4b7-693">Сначала он сопоставляет данные RGB с данными ЦИЕЛУВ, которые преобразуются в данные типа XYZ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-693">It first maps a given RGB data into a CIELUV data, which is converted into XYZ data.</span></span> <span data-ttu-id="fe4b7-694">В целевой карте данные независимых от устройства ЦИЕКСИЗ сначала преобразуются в данные ЦИЕЛУВ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-694">In the destination map, device-independent CIEXYZ data is first converted into CIELUV data.</span></span> <span data-ttu-id="fe4b7-695">Затем для прогнозирования оптимальных данных в формате RGB для данных ЦИЕЛУВ используются модель и классический метод Newton-Raphson.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-695">Then, the empirical model and the classical Newton-Raphson method are used to predict the best RGB data for the CIELUV data.</span></span> <span data-ttu-id="fe4b7-696">Ниже приведены сведения о преобразовании из Циелув в данные RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-696">The details about conversion from CieLUV to RGB data are as follows:</span></span>

<span data-ttu-id="fe4b7-697">После создания трехмерного LUT из RGB в Циелув карту из RGB в Лув создается с использованием тетрахедрал интерполяции в RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-697">After generating a 3-D LUT from RGB to CieLUV, the map from RGB to LUV is built using tetrahedral interpolation on RGB.</span></span> <span data-ttu-id="fe4b7-698">Эта схема обозначается следующими уравнениями:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-698">This map is denoted by the following equations:</span></span>

![Отображение уравнений для схемы с R G B до L U.](images/cdmp-image125.png)

<span data-ttu-id="fe4b7-700">Инверсия схемы состоит из решения для любого цвета</span><span class="sxs-lookup"><span data-stu-id="fe4b7-700">Inversion of the map consists of solving, for any color</span></span> ![Показывает L U.](images/cdmp-image127.png) <span data-ttu-id="fe4b7-702">, следующая система нелинейных уравнений:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-702">, the following system of nonlinear equations:</span></span>

![Показывает нелинейные уравнения для лолвинг любого цвета L.](images/cdmp-image129.png)

<span data-ttu-id="fe4b7-704">В новом CTE-выражении используется нелинейное уравнение, основанное на классического Newton-Raphson метода.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-704">A nonlinear equation that is based on the classical Newton-Raphson method is used in the new CTE.</span></span> <span data-ttu-id="fe4b7-705">Начальное предположение (или *приори* ), <sub>предшествующее</sub> (R 0, G 0, B 0), получается путем поиска по «начальной матрице», состоящей из унифицированной сетки 8x8x8 для предварительно вычисленных пар (RGB, Лув).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-705">An initial guess, or *a priori* see, s <sub>prior</sub> -(R 0, G 0, B 0 ) is obtained by searching through a "seed matrix" consisting of a uniform 8x8x8 grid of pre-computed (RGB,Luv) pairs.</span></span> <span data-ttu-id="fe4b7-706">Выбирается соответствующий Лув RGB, ближайший к L \* u \* \* .</span><span class="sxs-lookup"><span data-stu-id="fe4b7-706">The RGB corresponding Luv that is closest to the L\*u\*v\* is chosen.</span></span> <span data-ttu-id="fe4b7-707">Каждая точка в матрице заполнения соответствует центру ячейки, так что итерации не начинаются с точки на границе границы Куба RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-707">Each point in the seed matrix corresponds to the center of a cell so that the iterations don't start with a point on the boundary face of the RGB cube.</span></span> <span data-ttu-id="fe4b7-708">Иными словами, RGB начальных значений определяется следующим образом: шаг = 1/8 s <sub>ИЖК</sub> = (шаг/2 + (i-1) шаг, шаг/2 + (j-1) шаг, шаг/2 + (k-1) шаг) с i, j, k = 1... *8 на первом* шаге Ньютона-Рафсона, Следующая оценка ![ показывает переменные для следующей оценки.](images/cdmp-image133.png)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-708">In other words, the RGB of the seeds is defined by: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) with i,j,k = 1...8 At the *i* th step of Newton-Raphson, the next estimate ![Shows the variables for the next estimate.](images/cdmp-image133.png)</span></span> <span data-ttu-id="fe4b7-709">получается по формуле:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-709">is obtained by the formula:</span></span>

![Показывает формулу для оценки.](images/cdmp-image135.png)

<span data-ttu-id="fe4b7-711">Итерация останавливается, когда ошибка (расстояние в ЦИЕЛУВ пространстве) меньше, чем предварительно установленный уровень допуска (0,1 в CTE-выражении), или когда число итераций превышает максимально допустимое число итераций (10 в CTE-выражении).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-711">Iteration stops when the error (distance in the CIELUV space) is less than a pre-set tolerance level (0.1 in the CTE), or when the number of iterations has exceeded the maximum allowed number of iterations (10 in the CTE).</span></span> <span data-ttu-id="fe4b7-712">Значения для допуска и количества итераций были определены эффективно.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-712">The values for the tolerance and the number of iterations were empirically determined to be effective.</span></span> <span data-ttu-id="fe4b7-713">В будущих версиях значение допуска может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-713">In future versions, the tolerance value may be changed.</span></span>

<span data-ttu-id="fe4b7-714">Матрица Жакобиан вычисляется с использованием прямой разницы, за исключением точки границы (один или несколько значений R, G, B — 1), где используется обратная разница.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-714">The Jacobian matrix is calculated using forward difference, except at a boundary point (one or more of the R, G, B is 1) where backward difference is used instead.</span></span> <span data-ttu-id="fe4b7-715">Вместо того чтобы рассчитывать обратную матрицу Жакобиан, линейная система разрешается напрямую с помощью Gauss-Jordanного удаления с полной сводкой.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-715">Instead of calculating the inverse of the Jacobian matrix, the linear system is solved directly using Gauss-Jordan elimination with full pivoting.</span></span>

<span data-ttu-id="fe4b7-716">В конце итераций схождение все равно может быть не достигнутым, так как Newton-Raphson является локальным алгоритмом, то есть хорошо работает только в том случае, если вы начинаете с первого предположения, близкого к истинному решению.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-716">At the end of the iterations, convergence still might not be achieved because Newton-Raphson is a "local" algorithm, that is, it only works well if you start with an initial guess that is close to the true solution.</span></span> <span data-ttu-id="fe4b7-717">Если, в конце Newton-Raphson итераций, конвергенция в предопределенной отказоустойчивости не была достигнута, итерации перезапускаются с новым набором начальных значений, определенным следующим образом.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-717">If, at the end of the Newton-Raphson iterations, convergence within the pre-defined error tolerance has not been achieved, the iterations are restarted with a new set of seeds, defined as follows.</span></span>

<span data-ttu-id="fe4b7-718">Например, лучшим решением, полученным до сих пор, является (r, g, b).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-718">For example, the best solution obtained so far is (r, g, b).</span></span> <span data-ttu-id="fe4b7-719">Из этого решения N постериори начальные значения являются производными, где N = 4.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-719">From this solution, N a posteriori seeds are derived, where N = 4.</span></span> <span data-ttu-id="fe4b7-720">Интуитивно, решение перемещается по центру в соответствии с размером шага, который зависит от N. См. рис. 6.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-720">Intuitively, the solution is moved "toward the center" in a step size that depends on N. See Figure 6.</span></span>

![Схема, на которой показаны пертурбатион направления решения.](images/cdmp-image136.png)

<span data-ttu-id="fe4b7-722">**Рис. 6** . Направление пертурбатион решения зависит от того, в каком октет он находится.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-722">**Figure 6** : Perturbation direction of the solution depends on which octant it is in.</span></span>

<span data-ttu-id="fe4b7-723">Иными словами, если r &gt; 0,5, значение в канале r уменьшается, в противном случае значение увеличивается.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-723">In other words, if r &gt; 0.5, the value on the R channel is decreased, otherwise the value is increased.</span></span> <span data-ttu-id="fe4b7-724">Существует аналогичная логика для каналов G и B.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-724">There is similar logic for the G and B channels.</span></span> <span data-ttu-id="fe4b7-725">Точные определения:</span><span class="sxs-lookup"><span data-stu-id="fe4b7-725">The precise definitions are:</span></span>

<span data-ttu-id="fe4b7-726">ПЕРТУРБАТИОН = 0,5/(N + 1)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-726">PERTURBATION = 0.5/(N+1)</span></span>

<span data-ttu-id="fe4b7-727">Dir (r) =-1, если r &gt; 0,5; + 1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-727">Dir(r) = -1 if r &gt; 0.5; +1 otherwise.</span></span> <span data-ttu-id="fe4b7-728">Аналогично для DIR (g) и dir (b)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-728">Similarly for Dir(g) and Dir(b)</span></span>

<span data-ttu-id="fe4b7-729">ЖС постериори SEED, s????, имеет значение (r + dir (r) \* j \* пертурбатион, g + dir (g) \* j \* Пертурбатион, b + dir (b) \* j \* пертурбатион)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-729">The jth a posteriori seed, s ????, is (r + Dir(r) \*j \* PERTURBATION, g + Dir(g) \* j \* PERTURBATION, b + Dir(b) \* j \* PERTURBATION)</span></span>

<span data-ttu-id="fe4b7-730">Попробуйте первые s????</span><span class="sxs-lookup"><span data-stu-id="fe4b7-730">Try the first s ????</span></span> <span data-ttu-id="fe4b7-731">и если оно предоставляет новое решение в пределах допустимой допускки ошибок, его можно прекратить.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-731">and if it gives a new solution within error tolerance, you can stop.</span></span> <span data-ttu-id="fe4b7-732">В противном случае попробуйте второй????</span><span class="sxs-lookup"><span data-stu-id="fe4b7-732">Otherwise, try the second s ????</span></span> <span data-ttu-id="fe4b7-733">и т. д. до n????.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-733">and so on until the Nth s ????.</span></span>

<span data-ttu-id="fe4b7-734">Схема всего алгоритма показана на рис. 7.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-734">The schematics of the whole algorithm is shown in Figure 7.</span></span>

![Схема, показывающая последовательность инвертирования модели устройства.](images/cdmp-image138.png)

<span data-ttu-id="fe4b7-736">**Рис. 7. схема** инвертирования модели устройства</span><span class="sxs-lookup"><span data-stu-id="fe4b7-736">**Figure 7** : Schematics of inverting the device model</span></span>

### <a name="rgb-virtual-device-model-baseline"></a><span data-ttu-id="fe4b7-737">Базовый план модели виртуального устройства RGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-737">RGB Virtual Device Model Baseline</span></span>

<span data-ttu-id="fe4b7-738">Эта модель устройств (DM) — это простой алгоритм воспроизведения матрицы и тона.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-738">This device model(DM) is a simple matrix/tone reproduction algorithm.</span></span> <span data-ttu-id="fe4b7-739">Матрица является производной от белого пункта и первичного цвета с использованием стандартных алгоритмов обработки и анализа.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-739">The matrix is derived from the white point and primaries using standard color science algorithms.</span></span> <span data-ttu-id="fe4b7-740">Кривая воспроизведения является производной от параметров измерения в соответствии с ICC-описаниями Курветипе и Параметриктипе (или инверсией по мере необходимости).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-740">The tone reproduction curve is derived from the measurement parameters according to the ICC descriptions of CurveType and ParametricType (or inverted as required).</span></span> <span data-ttu-id="fe4b7-741">Подробные сведения о внутренних алгоритмах будут предоставлены после дополнительной проверки высоких проблем с динамическим диапазоном.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-741">Details of the internal algorithms will be provided after additional validation of high dynamic range issues.</span></span>

<span data-ttu-id="fe4b7-742">Модель виртуального устройства RGB — это идеальное значение кривой воспроизведения матрицы и тона RGB, аналогичное структуре профиля на основе матрицы из трех компонентов ICC.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-742">The RGB virtual device model is an idealized matrix/tone reproduction curve RGB similar to the ICC three-component matrix-based profile design.</span></span> <span data-ttu-id="fe4b7-743">Параметры виртуального измерения в DM включают значение белой точки (абсолютное ЦИЕКСИЗ), первичные значения RGB (абсолютное ЦИЕКСИЗ) и кривую воспроизведения на основе ICC Параметриккурветипе и Курветипе в формате XML, совместимом с схемами DMP.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-743">The "virtual measurement" parameters of the DM include a white point value (absolute CIEXYZ), RGB primary values (absolute CIEXYZ), and a tone reproduction curve that is based on the ICC ParametricCurveType and CurveType in XML formatting consistent with the DMP schemas.</span></span>

<span data-ttu-id="fe4b7-744">В следующей таблице показаны типы функций ICC Параметриккурветипе Encoding и соответствующая поддержка в Иргбвиртуалдевицемоделбасе.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-744">ICC parametricCurveType function type encoding and corresponding support in IRGBVirtualDeviceModelBase are shown in the following table.</span></span>



| <span data-ttu-id="fe4b7-745">Тип функции</span><span class="sxs-lookup"><span data-stu-id="fe4b7-745">Function type</span></span>                                         | <span data-ttu-id="fe4b7-746">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe4b7-746">Parameters</span></span>                          | <span data-ttu-id="fe4b7-747">Тип</span><span class="sxs-lookup"><span data-stu-id="fe4b7-747">Type</span></span>                                     | <span data-ttu-id="fe4b7-748">Примечание</span><span class="sxs-lookup"><span data-stu-id="fe4b7-748">Note</span></span>                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Показывает функцию "Гамматипе".](images/cdmp-image154.png)<br/> | <span data-ttu-id="fe4b7-750">н</span><span class="sxs-lookup"><span data-stu-id="fe4b7-750">g</span></span><br/>              | <span data-ttu-id="fe4b7-751">гамматипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-751">GammaType</span></span><br/>                 | <span data-ttu-id="fe4b7-752">Общая реализация</span><span class="sxs-lookup"><span data-stu-id="fe4b7-752">Common implementation</span></span><br/>           |
| ![Показывает функцию "Гаммаоффсетгаинтипе".](images/cdmp-image156.png)<br/> | <span data-ttu-id="fe4b7-754">общедоступная версия b</span><span class="sxs-lookup"><span data-stu-id="fe4b7-754">ga b</span></span><br/>           | <span data-ttu-id="fe4b7-755">гаммаоффсетгаинтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-755">GammaOffsetGainType</span></span><br/>       | <span data-ttu-id="fe4b7-756">ЦИЕ 122-1966</span><span class="sxs-lookup"><span data-stu-id="fe4b7-756">CIE 122-1966</span></span><br/>                    |
| ![Показывает функцию "Гаммаоффсетгаиноффсеттипе".](images/cdmp-image158.png)<br/> | <span data-ttu-id="fe4b7-758">общедоступная версия b c</span><span class="sxs-lookup"><span data-stu-id="fe4b7-758">ga b c</span></span><br/>         | <span data-ttu-id="fe4b7-759">гаммаоффсетгаиноффсеттипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-759">GammaOffsetGainOffsetType</span></span><br/> | <span data-ttu-id="fe4b7-760">IEC 61966-3</span><span class="sxs-lookup"><span data-stu-id="fe4b7-760">IEC 61966-3</span></span><br/>                     |
| ![Показывает функцию "Гаммаоффсетгаингаинтипе".](images/cdmp-image160.png)<br/> | <span data-ttu-id="fe4b7-762">общедоступная версия b c d</span><span class="sxs-lookup"><span data-stu-id="fe4b7-762">ga b c d</span></span><br/>       | <span data-ttu-id="fe4b7-763">гаммаоффсетгаингаинтипе</span><span class="sxs-lookup"><span data-stu-id="fe4b7-763">GammaOffsetGainGainType</span></span><br/>   | <span data-ttu-id="fe4b7-764">IEC 61966-2.1</span><span class="sxs-lookup"><span data-stu-id="fe4b7-764">IEC 61966-2.1</span></span><br/> <span data-ttu-id="fe4b7-765">sRGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-765">(sRGB)</span></span><br/> |
| ![Показывает функцию для параметров "g a b c d e f".](images/cdmp-image162.png)<br/> | <span data-ttu-id="fe4b7-767">GA b c d е е</span><span class="sxs-lookup"><span data-stu-id="fe4b7-767">ga b c d e f</span></span><br/>   | <span data-ttu-id="fe4b7-768">Н/Д</span><span class="sxs-lookup"><span data-stu-id="fe4b7-768">N/A</span></span><br/>                       | <span data-ttu-id="fe4b7-769">Не поддерживается в WCS</span><span class="sxs-lookup"><span data-stu-id="fe4b7-769">Not supported in WCS</span></span><br/>            |



 

<span data-ttu-id="fe4b7-770">Кривая тона для виртуальных устройств RGB применяется в Девицетоколориметрик между входными данными, Пдевицеколорс и матрицей.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-770">The tone curve for RGB virtual devices is applied in DeviceToColorimetric between the input data, pDeviceColors, and the matrix multiply.</span></span> <span data-ttu-id="fe4b7-771">Для Колориметриктодевице необходимо использовать метод для инвертирования кривой тона.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-771">For ColorimetricToDevice, a method must be used to invert the tone curve.</span></span> <span data-ttu-id="fe4b7-772">В базовой реализации это делается путем непосредственной интерполяции в той же кривой тона, которая используется для Девицетоколориметрик.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-772">In the baseline implementation, this is done by direct interpolation in the same tone curve used for DeviceToColorimetric.</span></span>

<span data-ttu-id="fe4b7-773">Кривые должны быть указаны в профилях как пары чисел в пространстве с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-773">The curves should be specified in the profiles as pairs of numbers in float space.</span></span> <span data-ttu-id="fe4b7-774">Первое число представляет значения в Пдевицеколорс.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-774">The first number represents values in pDeviceColors.</span></span> <span data-ttu-id="fe4b7-775">Второе число представляет выход кривой тонов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-775">The second number represents the output of the tone curve.</span></span> <span data-ttu-id="fe4b7-776">Все значения в кривой тона должны находиться между Минколорантусед и Максколорантусед.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-776">All values in the tone curve must be between minColorantUsed and maxColorantUsed.</span></span> <span data-ttu-id="fe4b7-777">Кривые тона должны содержать по крайней мере две записи: один для Минколорантусед и один для Максколорантусед.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-777">Tone curves must contain at least two entries: one for minColorantUsed and one for maxColorantUsed.</span></span> <span data-ttu-id="fe4b7-778">Максимальное число записей в Тонекурве — 2048.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-778">The maximum number of entries in the ToneCurve is 2048.</span></span> <span data-ttu-id="fe4b7-779">В целом, чем больше записей в таблице, тем точнее вы сможете моделировать кривизну.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-779">In general, the more entries in the table, the more accurately you can model curvature.</span></span> <span data-ttu-id="fe4b7-780">Между записями выполняется линейная интерполяция кусочно-.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-780">A piecewise linear interpolation is performed between the entries.</span></span>

<span data-ttu-id="fe4b7-781">Вы можете рассмотреть альтернативные методы интерполяции.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-781">You might consider alternative interpolation methods.</span></span> <span data-ttu-id="fe4b7-782">Если вы знакомы с базовым поведением устройства, вы можете более точно использовать меньшее число выборок и модель, используя кривую с более высоким порядком.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-782">If you know something about the underlying behavior of the device, you can use fewer samples and model more accurately with a higher order curve.</span></span> <span data-ttu-id="fe4b7-783">Но при использовании неправильного типа кривой вы будете очень неточны.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-783">But if you use the wrong curve type, you will be very inaccurate.</span></span> <span data-ttu-id="fe4b7-784">Без дополнительных сведений вы не можете угадать тип кривой.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-784">Without more information, you cannot guess the curve type.</span></span> <span data-ttu-id="fe4b7-785">Таким образом, используйте линейную интерполяцию и предоставьте много точек данных.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-785">So, use linear interpolation and provide many data points.</span></span>

### <a name="cmyk-printer-device-model-baseline"></a><span data-ttu-id="fe4b7-786">Базовая модель устройства принтера CMYK</span><span class="sxs-lookup"><span data-stu-id="fe4b7-786">CMYK Printer Device Model Baseline</span></span>

<span data-ttu-id="fe4b7-787">Устройство печати CMYK принтера состоит из создания многообразной модели устройства, которая прогнозирует распечатанный цвет для любого значения CMYK.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-787">A device characterization of a CMYK printer consists of constructing an empirical model of the device that predicts the printed color for any given CMYK value.</span></span> <span data-ttu-id="fe4b7-788">Подобная кодировка также включает в себя инверсию этой модели, чтобы можно было получить рецепт значения CMYK для печати для данного цвета.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-788">The characterization also includes the inversion of this model so that a prescription of the CMYK value to us for a given color to be printed can be given.</span></span> <span data-ttu-id="fe4b7-789">Обычно это определяется с точки зрения значения ЦИЕКСИЗ или ЦИЕЛАБ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-789">This is typically defined in terms of CIEXYZ or CIELAB value.</span></span>

<span data-ttu-id="fe4b7-790">Как правило, используется целевой объект 8,7/3, содержащий исправления CMYK.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-790">Typically, an IT8.7/3 target containing CMYK patches is used.</span></span> <span data-ttu-id="fe4b7-791">Исправления состоят из выборки пространства CMYK в четко определенном виде, чтобы была сформирована прямоугольная сетка (с неоднородными интервалами в C, M, Y и K).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-791">The patches consist of sampling of the CMYK space in a well-defined manner so that a rectangular grid (with non-uniform spacing in C, M, Y and K) is formed.</span></span> <span data-ttu-id="fe4b7-792">Каждое исправление затем измеряется с помощью колориметер или спектрофотометер.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-792">Each patch is then measured with a colorimeter or spectrophotometer.</span></span> <span data-ttu-id="fe4b7-793">Измерения в значениях ЦИЕКСИЗ затем формируют таблицу подстановки (LUT), из которой строится модель принтера с помощью метода интерполяции Сакамото.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-793">The measurements in CIEXYZ values then form a lookup table (LUT), from which an empirical model of the printer is built using Sakamoto's interpolation method.</span></span> <span data-ttu-id="fe4b7-794">Патент 4275413 США (Сакамото et al.), патент США 4511989 (Сакамото), Канг \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fe4b7-794">US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="fe4b7-795">Истек срок действия двух упомянутых патентов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-795">The two patents mentioned have expired.</span></span>

<span data-ttu-id="fe4b7-796">Конкретные требования к примерам измерения CMYK, необходимым для использования профиля модели устройства в соответствии с моделью базового устройства принтера CMYK, приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-796">Specific requirements for the CMYK measurement samples necessary for a device model profile to be accepted as valid by the CMYK printer baseline device model are as follows.</span></span> <span data-ttu-id="fe4b7-797">(Образец набора проще всего описать как набор образцов кубов КМИ, каждый из которых связан с конкретным уровнем K.)</span><span class="sxs-lookup"><span data-stu-id="fe4b7-797">(The sample set is most clearly described as a set of CMY sample cubes, each associated with a specific K level.)</span></span>

-   <span data-ttu-id="fe4b7-798">Для уровней K = 0 и K = 100 должны быть указаны как минимум допустимые Кубы КМИ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-798">At minimum, valid CMY cubes must be provided for the K = 0 and K = 100 levels.</span></span>
-   <span data-ttu-id="fe4b7-799">Промежуточные уровни K могут иметь неоднородное пространство.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-799">Intermediate K levels may be non-uniformly spaced.</span></span>
-   <span data-ttu-id="fe4b7-800">Любой промежуточный уровень K без допустимого Куба КМИ будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-800">Any intermediate K level without a valid CMY cube will be ignored.</span></span>
-   <span data-ttu-id="fe4b7-801">Кубы КМИ могут использовать неоднородные интервалы выборки (междустрочный интервал), но один и тот же набор интервалов выборки должен использоваться во всех измерениях C, M и Y в Кубе КМИ для данного уровня K.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-801">The CMY cubes may use non-uniform sample intervals (grid spacing), but the same set of sample intervals must be used in all of the C,M, and Y dimensions in the CMY cube for a given K level.</span></span>
-   <span data-ttu-id="fe4b7-802">Каждый куб K уровня КМИ может использовать разное число и интервалы выборки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-802">Each K level CMY cube can use a different number and spacing of sample intervals.</span></span>
-   <span data-ttu-id="fe4b7-803">Все Кубы КМИ должны содержать "углы" Куба КМИ, т. е. КМИ Samples имеет значение \[ 0, 0, 0 \] , \[ 0, 0100 \] , \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100 100 \] , \[ 100, 0100 \] , \[ 100 100, 0 \] , \[ 100 100 100 \] .</span><span class="sxs-lookup"><span data-stu-id="fe4b7-803">All CMY cubes must contain the "corners" of the CMY cube, that is, CMY samples at \[0,0,0\], \[0,0,100\], \[0,100,0\], \[100,0,0\], \[0,100,100\], \[100,0,100\], \[100,100, 0\], \[100,100,100\].</span></span>
-   <span data-ttu-id="fe4b7-804">Все промежуточные уровни сетки КМИ должны быть полностью выборке в каждом канале.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-804">Any intermediate CMY grid levels must be fully sampled in each channel.</span></span> <span data-ttu-id="fe4b7-805">Иными словами, пример должен существовать на каждом трехмерном пересечении сетки в Кубе КМИ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-805">In other words, a sample must exist at each 3-D grid intersection within the CMY cube.</span></span>
-   <span data-ttu-id="fe4b7-806">Для кубов K = 0 и K = 100 КМИ, 2x2x2 «только углы» являются минимально допустимыми.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-806">For the K = 0 and K = 100 CMY cubes, 2x2x2 "corners-only" cubes are the minimum accepted as valid.</span></span>

    <span data-ttu-id="fe4b7-807">\[Примечание. для K = 0 и K = 100 уровней куб 3x3x3 КМИ будет обрабатываться как куб с 2x2x2 только угловыми углами; промежуточный пример уровня не учитывается.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-807">\[NOTE: for K=0 and K=100 levels, a 3x3x3 CMY cube will be processed as a 2x2x2 "corners-only" cube; the intermediate sample level is ignored.</span></span> <span data-ttu-id="fe4b7-808">в 4x4x4 и более крупных кубах будут использоваться все примеры использования сетки.\]</span><span class="sxs-lookup"><span data-stu-id="fe4b7-808">4x4x4 and larger cubes will have all on-grid samples used.\]</span></span>

-   <span data-ttu-id="fe4b7-809">Для уровней "промежуточный K" 4x4x4 КМИ Кубы — это минимальный допустимый уровень.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-809">For intermediate K levels, 4x4x4 CMY cubes are the minimum accepted as valid.</span></span>

<span data-ttu-id="fe4b7-810">Профиль высокого качества будет использовать более детализированные сетки выборки, чем минимум, необходимый для допустимости, обычно 9x9x9x9 или выше.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-810">A high-quality profile will use finer sampling grids than the minimum required for validity, usually 9x9x9x9 or higher.</span></span> <span data-ttu-id="fe4b7-811">Образцы из ИТ-8,7/3, IT 8,7/4 и ECI создают допустимые профили модели устройств (Дмпс) для модели базового устройства принтера CMYK.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-811">The samples from the IT8.7/3, IT8.7/4, and ECI targets produce valid device model profiles (DMPs)for the CMYK printer baseline device model.</span></span> <span data-ttu-id="fe4b7-812">Несмотря на то, что эта модель устройства может игнорировать внешние (недоступные) примеры в этих целевых объектах, не гарантируется, что она сможет сделать это для других целей, и поэтому рекомендуется удалить лишние образцы из наборов измерений, поступающих в профили для этой модели устройства.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-812">While this device model is able to ignore the extraneous (off-grid) samples in these targets, it is not guaranteed to be able to do so for other targets, and so, it is recommended that extraneous samples be removed from measurement sets going into profiles for this device model.</span></span>

<span data-ttu-id="fe4b7-813">Некоторая версия модели принтера предоставляет больше проблем.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-813">The inversion of the printer model presents more difficulties.</span></span> <span data-ttu-id="fe4b7-814">Учитывая цвет ввода в ЦИЕКАМ, существует вопрос, находится ли этот цвет в цветовой гамме принтера.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-814">Given an input color in CIECAM, there is a question of whether this color is within the printer gamut.</span></span> <span data-ttu-id="fe4b7-815">Существуют также проблемы, связанные с расположением точек в области отображения цвета.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-815">There is also the issue regarding the arrangement of points in the color appearance space.</span></span> <span data-ttu-id="fe4b7-816">Несмотря на то, что значения CMYK можно расположить на прямоугольной сетке, как это делается в целевом объекте "8,7/3", то то же самое невозможно сказать из итогового напечатанного цвета, так как они расположены в области отображения цвета.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-816">While we can arrange the CMYK values to fall on a rectangular grid, as is done in the IT8.7/3 target, the same cannot be said of the resulting printed colors as they are situated in the color appearance space.</span></span> <span data-ttu-id="fe4b7-817">Как правило, они разбросаны в области отображения цвета без определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-817">In general, they are scattered in the color appearance space with no particular pattern.</span></span>

<span data-ttu-id="fe4b7-818">Обычно существует два подхода к проблеме устранения неисправностей в разбросанных точках.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-818">There are generally two approaches to the inversion problem of scattered points.</span></span> <span data-ttu-id="fe4b7-819">Одним из подходов является использование геометрического деления цветового охвата принтера с помощью простейших трехмерных сплошных трехмерных фрагментов, например тетрахедра.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-819">One approach is to use a geometric subdivision of the printer gamut using elementary 3-dimensional solids, such as tetrahedra.</span></span> <span data-ttu-id="fe4b7-820">Подразделение цветового охвата принтера в области отображения цвета может быть вызвано соответствующим подразделением пространства КМИ (K), см \[ \] . 93, Канг \[ 97 \] . Этот подход имеет преимущество вычислительной простоты.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-820">A subdivision of the printer gamut in the color appearance space can be induced from the corresponding subdivision of the CMY(K) space, see Hung\[93\], Kang\[97\].This approach has the advantage of computational simplicity.</span></span> <span data-ttu-id="fe4b7-821">В случае с тетрахедрон в интерполяции используются только четыре точки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-821">In the case of a tetrahedron, only four points are used in an interpolation.</span></span> <span data-ttu-id="fe4b7-822">С другой стороны, результат зависит от нескольких точек, что означает, что ошибка измерения оказывает значительное воздействие на результат.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-822">On the other hand, the result depends heavily on a few points, which means that a measurement error will have a significant effect on the result.</span></span> <span data-ttu-id="fe4b7-823">Интерполант также обычно не так гладко.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-823">The interpolant also tends to be not as smooth.</span></span> <span data-ttu-id="fe4b7-824">Второй подход не предполагает наличия подразделений и основан на методе интерполяции рассеивания данных.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-824">The second approach does not assume any subdivision, and is based on the technique of scattered data interpolation.</span></span> <span data-ttu-id="fe4b7-825">Классическим примером является метод интерполяции Шепард или метод обратного взвешенного метода (см \[ . шепард 68 \] ).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-825">A classical example is the technique of Shepard interpolation, or inverse weighted method (See Shepard \[68\]).</span></span> <span data-ttu-id="fe4b7-826">Здесь несколько точек, окружающих точку ввода, выбираются каким-либо образом, каждый из которых имеет вес, обычно обратно пропорционально расстоянию, а интерполант принимается в качестве взвешенного среднего по соседним точкам.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-826">Here, several points surrounding the input point are chosen in some manner, each assigned a weight, usually inversely proportional to the distance, and the interpolant is taken as the weighted average of the neighboring points.</span></span> <span data-ttu-id="fe4b7-827">При таком подходе выбирать соседние точки имеет первостепенное значение для производительности.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-827">In this approach, the choice of neighboring points is paramount to performance.</span></span> <span data-ttu-id="fe4b7-828">Хотя слишком мало точек может визуализировать интерполант неточные и негладкие, слишком большое количество точек накладывает высокую вычислительную стоимость, так как весовые коэффициенты обычно являются нелинейными функциями и требуют вычислений.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-828">While too few points can render the interpolant inaccurate and non-smooth, too many points impose a high computational cost, as the weights are typically non-linear functions and costly to compute.</span></span>

<span data-ttu-id="fe4b7-829">Два подхода, описанных выше, имеют проблемы.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-829">The two approaches described above both have problems.</span></span> <span data-ttu-id="fe4b7-830">Подход подразделений имеет критически важное значение для данных, которые, как правило, являются недостаточными для шума, и обычно интерполант не очень гладко.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-830">The subdivision approach depends critically on the data being reasonably void of noise, and generally the interpolant is not very smooth.</span></span> <span data-ttu-id="fe4b7-831">Рассеивание рассеивания данных более чувствительна к шумам данных и, как правило, предоставляет более гладкий интерполант, но он является более затратным.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-831">The scattered data interpolation is more tolerant to data noise, and generally gives a smoother interpolant, but it is computationally more expensive.</span></span>

<span data-ttu-id="fe4b7-832">Новое ОТВ использует другой подход.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-832">The new CTE takes an alternative approach.</span></span> <span data-ttu-id="fe4b7-833">Устройство CMYK обрабатывается как коллекция из нескольких КМИ устройств, каждое из которых имеет определенное значение черного (K).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-833">The CMYK device is treated as a collection of several CMY devices, each of which has a specific value of black (K).</span></span> <span data-ttu-id="fe4b7-834">При использовании алгоритма выбора, который принимает параметры Light и чрома, выбирается уровень черного.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-834">Using a selection algorithm that takes as parameters lightness and chroma, a level of black is chosen.</span></span> <span data-ttu-id="fe4b7-835">Значения КМИ получаются путем инверсии соответствующей таблицы КМИ в Лув с помощью методов Ньютона, используемых в других случаях алгоритмом принтера RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-835">The CMY values are obtained by inversion of the corresponding CMY to Luv table using the Newton methods employed elsewhere by the RGB printer algorithm.</span></span>

<span data-ttu-id="fe4b7-836">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-836">Use the following steps.</span></span>

1.  <span data-ttu-id="fe4b7-837">Распечатайте целевой объект, который является либо целевым объектом для ИТ-8,7/3, либо целевым объектом, содержащим выборку пространства CMYK в обычном или непостоянном промежутке времени.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-837">Print the characterization target, which is either the IT8.7/3 target, or a target containing sampling of the CMYK space at regularly or irregularly spaced intervals.</span></span>
2.  <span data-ttu-id="fe4b7-838">Измерьте целевой объект с помощью спектрофотометер и преобразуйте измерения в ЦИЕЛУВ пространство.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-838">Measure the target using a spectrophotometer, and convert the measurements to CIELUV space.</span></span>
3.  <span data-ttu-id="fe4b7-839">Создайте прямую карту из CMYK в Лув.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-839">Construct the forward map from CMYK to Luv.</span></span>
4.  <span data-ttu-id="fe4b7-840">Используйте прямую карту для создания набора КМИ для Лув Maps для диапазона значений K.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-840">Use the forward map to construct a set of CMY to Luv maps for a range of K values.</span></span>
5.  <span data-ttu-id="fe4b7-841">Для любого входного значения Лув соответствующее значение CMYK получается путем выбора одного из карт, созданных на шаге 4 выше, и инверсии с помощью метода Ньютона для получения КМИ колорант, сопровождающего выбранное значение K.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-841">For any input Luv value, the corresponding CMYK value is obtained by selecting one of the maps constructed in step 4 above and inverting using Newton's method to obtain a CMY colorant set to accompany the K value selected.</span></span>

<span data-ttu-id="fe4b7-842">Шаги 1 и 2, которые являются стандартными процедурами, выполняются программой профилирования, которая не является частью нового CTE-выражения.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-842">Steps 1 and 2, which are standard procedures, are performed by a profiling program that is not part of the new CTE.</span></span> <span data-ttu-id="fe4b7-843">Цель IT 8,7/3 содержит достаточно детализированную выборку всех значений CMYK на различных уровнях C, M, Y и K. Кроме того, можно использовать пользовательский целевой объект с единообразной выборкой каналов C, M, Y и K.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-843">The IT8.7/3 target contains a reasonably detailed sampling of all the CMYK values at various levels of C, M, Y, and K. Alternatively, a custom target with uniform sampling of the C, M, Y, and K channels can be used.</span></span> <span data-ttu-id="fe4b7-844">После печати целевого объекта спектрофотометер или колориметер можно использовать для измерения значения XYZ каждого исправления, а значение XYZ можно преобразовать в значение Лув с помощью модели ЦИЕЛУВ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-844">After the target is printed, a spectrophotometer or colorimeter can be used to measure the XYZ value of each patch, and the XYZ value can be converted to the Luv value using the CIELUV model.</span></span>

<span data-ttu-id="fe4b7-845">Шаг 3. Создание прямой схемы из CMYK в Лув может быть достигнуто применением любой известной методики интерполяции, например тетрахедрал или многолинейного метода, в прямоугольной сетке в пространстве CMYK.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-845">Step 3, construction of the forward map from CMYK to Luv, can be achieved by applying any known interpolation technique, such as tetrahedral or multilinear method, on the rectangular grid in CMYK space.</span></span> <span data-ttu-id="fe4b7-846">В новом CTE-выражении используется 4-мерный тетрахедрал интерполяция.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-846">In the new CTE, a 4-dimensional tetrahedral interpolation is used.</span></span> <span data-ttu-id="fe4b7-847">Так как сетки выборки КМИ обычно отличаются на каждом уровне K, мы используем метод Super-выборки, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-847">Because the CMY sampling grids are generally different on each level of K, however, we use a technique of super-sampling, as detailed below.</span></span> <span data-ttu-id="fe4b7-848">Для заданной точки CMYK сначала определяются южные уровни K, основанные на значении K.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-848">For a given CMYK point, the sandwiching K levels are first determined based on the K value.</span></span> <span data-ttu-id="fe4b7-849">Затем введите «супер-Grid» для каждого уровня K, который представляет собой объединение сеток КМИ на каждом из двух уровней K.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-849">Then introduce a "super-grid" on each K level that is a union of the CMY grids on each of the two K levels.</span></span> <span data-ttu-id="fe4b7-850">На каждом уровне K значение Лув любой вновь введенной точки сетки получается трехмерной тетрахедрал интерполяцией на уровне K.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-850">On each K level, the Luv value of any newly introduced grid point is obtained by a 3-dimensional tetrahedral interpolation within that K level.</span></span> <span data-ttu-id="fe4b7-851">Наконец, в этой новой сетке выполняется 4-мерный тетрахедрал интерполяция для определенной точки CMYK.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-851">Finally, a 4-dimensional tetrahedral interpolation for the specific CMYK point is performed on this new grid.</span></span>

![Схема, показывающая ресамплинг.](images/cdmp-image163.png)

<span data-ttu-id="fe4b7-853">**Рис. 8** . ресамплинг</span><span class="sxs-lookup"><span data-stu-id="fe4b7-853">**Figure 8** : Supersampling</span></span>

<span data-ttu-id="fe4b7-854">На шаге 4 создается набор таблиц подстановки КМИ-Лув (Лутс).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-854">Step 4 constructs a set of CMY-to-Luv lookup tables (LUTs).</span></span> <span data-ttu-id="fe4b7-855">Прямая схема, созданная на шаге 3, вызывается многократно для повторной выборки пространства CMYK.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-855">The forward map constructed in Step 3 is called repeatedly to resample the CMYK space.</span></span> <span data-ttu-id="fe4b7-856">Цветовое пространство CMYK выделено с помощью четного интервала в K и другого, но по-прежнему равномерного выделения пространства, выборка КМИ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-856">The CMYK color space is sampled using an even spacing of K and a different, but still evenly spaced, sampling of CMY.</span></span>

<span data-ttu-id="fe4b7-857">Шаг 5 — это процедура получения значения CMYK с помощью Лутс, созданного на шаге 4 для любой входной точки Лув.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-857">Step 5 is a procedure to obtain the CMYK value using the LUTs constructed in Step 4 for any input Luv point.</span></span> <span data-ttu-id="fe4b7-858">Чтобы выбрать соответствующее значение K, можно проанализировать освещение, а также степень цвета в запрошенном Лув.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-858">The appropriate value of K is chosen by analyzing the lightness as well as the degree of color in the Luv requested.</span></span> <span data-ttu-id="fe4b7-859">После выбора таблицы значения КМИ извлекаются из таблицы с помощью метода Ньютона (как описано в разделе модель устройства принтера RGB выше).</span><span class="sxs-lookup"><span data-stu-id="fe4b7-859">After the table is selected, the CMY values are obtained from the table by using Newton's method (as documented under the RGB printer device model earlier).</span></span>

<span data-ttu-id="fe4b7-860">ЦИЕЛУВ пространство используется в модели принтера вместо Циежаб, так как модель устройства должна основываться исключительно на цвете данных, доступной в DMP.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-860">CIELUV space is used in the printer model instead of CIEJab because the device model should be based solely on colorimetric data available in the DMP.</span></span> <span data-ttu-id="fe4b7-861">В DMP содержатся изображения для каждого измеряемого исправления, включая белую точку мультимедиа, поэтому можно преобразовать ЦИЕКСИЗ данные в данные ЦИЕЛУВ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-861">The DMP contains colorimetric data for each measured patch, including the media white point, so it is possible to convert CIEXYZ data into CIELUV data.</span></span> <span data-ttu-id="fe4b7-862">Однако преобразование в CIECAM02 ЖЧ или Jab невозможно, так как нет доступа к сведениям о условии просмотра в DMP.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-862">However, it is not possible to convert to CIECAM02 JCh or Jab, because there is no access to the viewing condition information in the DMP.</span></span>

### <a name="rgb-projector-device-model-baseline"></a><span data-ttu-id="fe4b7-863">Базовый план модели устройства с проектором RGB</span><span class="sxs-lookup"><span data-stu-id="fe4b7-863">RGB Projector Device Model Baseline</span></span>

<span data-ttu-id="fe4b7-864">Примечание. Многие Проекторы RGB имеют более одного режима работы.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-864">Note: Many RGB projectors have more than one operating mode.</span></span> <span data-ttu-id="fe4b7-865">В одном режиме, который часто используется по умолчанию и может называться нечто вроде «презентация», цветовой ответ проектора оптимизирован для максимальной яркости.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-865">In one mode, which is often the default and might be called something like "presentation," the color response of the projector is optimized for maximum brightness.</span></span> <span data-ttu-id="fe4b7-866">Однако в этом режиме проектор теряет возможность воспроизводить освещение, слегка разноцветные цвета, например бледно-желтые и некоторые звуки.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-866">However, in this mode, the projector loses the ability to reproduce light, slightly chromatic colors such as pale yellows and some flesh tones.</span></span> <span data-ttu-id="fe4b7-867">В другом режиме, который часто называется «пленка», «видео» или «sRGB», проектор оптимизирован для воспроизведения реалистичных изображений и естественных сцен.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-867">In another mode, often called "film," "video," or "sRGB," the projector is optimized for reproduction of realistic images and natural scenes.</span></span> <span data-ttu-id="fe4b7-868">В этом режиме для повышения общего качества воспроизведения цвета выдается максимальная яркость.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-868">In this mode, maximum brightness is traded off to improve the overall quality of the color reproduction.</span></span> <span data-ttu-id="fe4b7-869">Чтобы получить удовлетворительное воспроизведение цвета с помощью проекторов RGB, необходимо разместить проектор в режиме, где можно воссоздать плавный охват цветов.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-869">To obtain satisfactory color reproduction with RGB projectors, it is necessary to place the projector in a mode where a smooth gamut of colors can be reproduced.</span></span>

![Схема, на которой показана модель устройства D L P.](images/cdmp-image167.png)

<span data-ttu-id="fe4b7-871">**Рис. 9** . модель устройства DLP</span><span class="sxs-lookup"><span data-stu-id="fe4b7-871">**Figure 9** : DLP device model</span></span>

<span data-ttu-id="fe4b7-872">Значение входящего значения RGB проходит через два вычислительных пути.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-872">An incoming RGB value passes through two computational pathways.</span></span> <span data-ttu-id="fe4b7-873">Первая — это модель матрицы, результатом которой является значение XYZ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-873">The first is the matrix model, which results in an XYZ value.</span></span> <span data-ttu-id="fe4b7-874">После этого сразу же следует преобразование из XYZ в Лув.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-874">This is immediately followed by the conversion from XYZ to Luv.</span></span> <span data-ttu-id="fe4b7-875">Второй является неоднородной LUT интерполяцией с помощью интерполяции тетрахедрал.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-875">The second is the non-uniform LUT interpolation using tetrahedral interpolation.</span></span> <span data-ttu-id="fe4b7-876">Выходные данные интерполяции уже находятся в Лув пространстве по конструкции.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-876">The output of the interpolation is already in Luv space by construction.</span></span> <span data-ttu-id="fe4b7-877">Для получения прогнозируемого значения Лув добавляются два выхода.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-877">The two outputs are added to obtain the predicted Luv value.</span></span> <span data-ttu-id="fe4b7-878">В итоге он преобразуется в XYZ, что является ожидаемым выходом модели "+ +" для устройства DLP.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-878">This is finally converted to XYZ, which is the expected output of the colorimetric model for the DLP device.</span></span>

<span data-ttu-id="fe4b7-879">Так как проекторы являются устройствами вывода, они также поддерживают инверсию модели, то есть преобразование из XYZ в RGB.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-879">Since projectors are display devices, they also support the inversion of the model, that is, the transform from XYZ to RGB.</span></span> <span data-ttu-id="fe4b7-880">Так как модель устройства преобразует пространство RGB в XYZ-пространство, которое состоит из трех измерений, инверсия эквивалентна решению трех нелинейных уравнений в трех неизвестных.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-880">Because the device model transforms RGB space to XYZ space, which are both three dimensional, inversion is equivalent to solving three nonlinear equations in three unknowns.</span></span> <span data-ttu-id="fe4b7-881">Это можно сделать с помощью стандартных методов решения уравнений, например Ньютона-Рафсона.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-881">This can done by standard equation solving techniques, such as Newton-Raphson.</span></span> <span data-ttu-id="fe4b7-882">Однако предпочтительнее сначала преобразовать XYZ в Лув, а затем инвертировать Лув в преобразование RGB, так как Лув пространство больше перцептуалли, чем в пространстве XYZ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-882">It is preferable, however, to first convert XYZ to Luv, and then invert the Luv To RGB transform, because Luv space is more perceptually linear than XYZ space.</span></span>

### <a name="icc-device-model-baseline"></a><span data-ttu-id="fe4b7-883">Базовый план модели устройства ICC</span><span class="sxs-lookup"><span data-stu-id="fe4b7-883">ICC Device Model Baseline</span></span>

<span data-ttu-id="fe4b7-884">Совместимость рабочих процессов ICC включается путем создания специального профиля модели устройства ICC, в котором хранится объект профиля, и для создания преобразования ICC с помощью профиля No-Op XYZ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-884">The CITE ICC workflow interoperability is enabled by creating a special ICC device baseline device model profile that stores the profile object and creates a ICC transform using a no-op XYZ profile.</span></span> <span data-ttu-id="fe4b7-885">Это преобразование затем используется для преобразования цветов устройств и ЦИЕКСИЗ.</span><span class="sxs-lookup"><span data-stu-id="fe4b7-885">This transform is then used to translate between device and CIEXYZ colors.</span></span>

![Схема, на которой показано взаимодействие с рабочим процессом c I T E c c.](images/cdmp-image168.png)

<span data-ttu-id="fe4b7-887">**Рис. 10** . Совместимость рабочих процессов ICC</span><span class="sxs-lookup"><span data-stu-id="fe4b7-887">**Figure 10** : CITE ICC Workflow Interoperability</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe4b7-888">См. также</span><span class="sxs-lookup"><span data-stu-id="fe4b7-888">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe4b7-889">Основные понятия управления цветом</span><span class="sxs-lookup"><span data-stu-id="fe4b7-889">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="fe4b7-890">Схемы и алгоритмы цветовой системы Windows</span><span class="sxs-lookup"><span data-stu-id="fe4b7-890">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





