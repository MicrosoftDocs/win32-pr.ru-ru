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
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>Схема и алгоритмы профиля модели цветового устройства WCS

В этом разделе содержатся сведения о схеме профиля модели цветового устройства WCS и связанных с ней алгоритмах.

В этом разделе содержатся следующие подразделы.

-   [Обзор](#overview)
-   [Архитектура профиля модели цветового устройства](#color-device-model-profile-architecture)
-   [Схема КДМП](#the-cdmp-schema)
-   [Добавление калибровки WCS КДМП v 2.0](#wcs-cdmp-v20-calibration-addition)
-   [Элементы схемы КДМП](#the-cdmp-schema-elements)
    -   [колордевицемоделпрофиле](#colordevicemodelprofile)
    -   [колордевицемодел](#colordevicemodelprofile)
    -   [намеспацеверсион](#namespaceversion)
    -   [Version](#namespaceversion)
    -   [Документация](#documentation)
    -   [Кртдевице, элемент](#crtdevice-element)
    -   [Лкддевице, элемент](#lcddevice-element)
    -   [Прожектордевице, элемент](#projectordevice-element)
    -   [Сканнердевице, элемент](#scannerdevice-element)
    -   [Камерадевице, элемент](#cameradevice-element)
    -   [Ргбпринтердевице, элемент](#rgbprinterdevice-element)
    -   [Кмикпринтердевице, элемент](#cmykprinterdevice-element)
    -   [Ргбвиртуалдевице, элемент](#rgbvirtualdevice-element)
    -   [плугиндевицетипе](#plugindevicetype)
    -   [ргбвиртуалмеасуременттипе](#rgbvirtualmeasurementtype)
    -   [гамматипе](#gammatype)
    -   [гаммаоффсетгаинтипе](#gammaoffsetgaintype)
    -   [гаммаоффсетгаинлинеаргаинтипе](#gammaoffsetgainlineargaintype)
    -   [тонереспонсекурвестипе](#toneresponsecurvestype)
    -   [гамутбаундарисамплестипе](#gamutboundarysamplestype)
    -   [флоатпаирлист](#floatpairlist)
    -   [кмикпринтермеасуременттипе](#cmykprintermeasurementtype)
    -   [ргбпринтермеасуременттипе](#rgbprintermeasurementtype)
    -   [ргбкаптуремеасуременттипе](#rgbcapturemeasurementtype)
    -   [онебасединдекс](#onebasedindex)
    -   [ргбпрожектормеасуременттипе](#rgbprojectormeasurementtype)
    -   [дисплаймеасуременттипе](#displaymeasurementtype)
    -   [меасуременткондитионстипе](#measurementconditionstype)
    -   [жеометритипе](#geometrytype)
    -   [ргбпримариесграуп](#rgbprimariesgroup)
    -   [ноннегативекмиксамплетипе](#nonnegativecmyksampletype)
    -   [ноннегативергбсамплетипе](#nonnegativergbsampletype)
    -   [ноннегативекмиктипе](#nonnegativecmyktype)
    -   [ноннегативергбтипе](#nonnegativergbtype)
    -   [ExtensionType](#extensiontype)
    -   [ноннегативексизтипе](#nonnegativexyztype)
    -   [ксизтипе](#nonnegativexyztype)
-   [Базовые алгоритмы КДМП](#the-cdmp-baseline-algorithms)
    -   [Базовый план модели устройства CRT](#crt-device-model-baseline)
    -   [Базовая модель устройства LCD](#lcd-device-model-baseline)
    -   [Базовый план модели устройства принтера RGB](#rgb-printer-device-model-baseline)
    -   [Базовый план модели виртуального устройства RGB](#rgb-virtual-device-model-baseline)
    -   [Базовая модель устройства принтера CMYK](#cmyk-printer-device-model-baseline)
    -   [Базовый план модели устройства с проектором RGB](#rgb-projector-device-model-baseline)
    -   [Базовый план модели устройства ICC](#icc-device-model-baseline)
-   [См. также](#related-topics)

## <a name="overview"></a>Обзор

Эта схема используется для указания содержимого профиля модели цветового устройства (КДМП). Связанные базовые алгоритмы описаны ниже.

Базовая схема профиля модели устройства (DMP) состоит из данных измерения выборки.

Компонент выборки в схеме XML DMP обеспечивает поддержку базовых целей измерения цвета, что сосредоточено на стандартных целевых объектах и целевых объектах, оптимизированных для моделей базовых устройств.

Кроме того, профиль устройства предоставляет определенную информацию о модели целевого устройства и предоставляет политику, которую модель базового резервного устройства может использовать, если Целевая модель недоступна. Экземпляры профиля могут включать частные расширения с помощью стандартных механизмов расширения XML.

## <a name="color-device-model-profile-architecture"></a>Архитектура профиля модели цветового устройства

![Схема, на которой показаны сведения, составляющие профиль модели устройства.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a>Схема КДМП


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



## <a name="wcs-cdmp-v20-calibration-addition"></a>Добавление калибровки WCS КДМП v 2.0

Элемент **колордевицемодел** схемы КДМП был обновлен в Windows 7 для включения нового элемента калибровки. Ниже показано изменение схемы КДМП.


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



## <a name="the-cdmp-schema-elements"></a>Элементы схемы КДМП

> [!Note]  
> Первичные цвета — это основные примеры красного, зеленого, синего, Черного и белого цветов. Основная шкала — это тональная шкала от наименьшей светимости до полного основного значения. Максимальное число записей в пандусе тонового элемента — 4096.

 

> [!Note]  
> Дмпс должны иметь данные измерения.

 

### <a name="colordevicemodelprofile"></a>колордевицемоделпрофиле

Этот элемент имеет тип Колордевицемодел.

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.

### <a name="colordevicemodel"></a>колордевицемодел

Этот элемент является последовательностью следующих вложенных элементов

1.  Строка имени файла,
2.  Необязательная строка описания
3.  Необязательная строка автора
4.  Необязательный Меасуременткондитионс Меасуременткондитионстипе,
5.  Self-Luminous Boolean,
6.  Максколорант float,
7.  Минколорант float,
8.  Выбора элементов
    1.  Кртдевице,
    2.  Лкддевице,
    3.  Ргбпрожектордевице,
    4.  Сканнердевице,
    5.  Камерадевице,
    6.  Ргбпринтердевице,
    7.  Кмикпринтердевице,
    8.  Ргбвиртуалдевице,
9.  Плугиндевице,
10. необязательное расширение ExtensionType

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу. Вложенные элементы строки содержат не более 10 000 символов. Вложенный элемент Максколорант должен быть больше или равен нулю (0) и больше, чем вложенный элемент Минколорант. Минколорант может быть отрицательным.

### <a name="namespaceversion"></a>намеспацеверсион

xmlns: CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Версия

Version = "1,0" в Windows Vista.

**Условия проверки:** Любое значение версии &gt; 0,1 или &lt; = 2,0 допустимо для поддержки некритических изменений в формате.

### <a name="documentation"></a>Документация

Схема профиля модели устройства.

(C) корпорация Майкрософт (Microsoft Corporation). Все права защищены.

### <a name="crtdevice-element"></a>Кртдевице, элемент

Этот элемент является последовательностью вложенных элементов Меасурементдата Дисплаймеасуременттипе.

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.

### <a name="lcddevice-element"></a>Лкддевице, элемент

Этот элемент является последовательностью вложенных элементов Меасурементдата Дисплаймеасуременттипе.

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.

### <a name="projectordevice-element"></a>Прожектордевице, элемент

Этот элемент является последовательностью вложенных элементов Меасурементдата Ргбпрожектормеасуременттипе.

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.

### <a name="scannerdevice-element"></a>Сканнердевице, элемент

Этот элемент является последовательностью вложенных элементов объекта Меасурементдата Ргбкаптуремеасуременттипе

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.

### <a name="cameradevice-element"></a>Камерадевице, элемент

Этот элемент является последовательностью вложенных элементов объекта Меасурементдата Ргбкаптуремеасуременттипе

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.

### <a name="rgbprinterdevice-element"></a>Ргбпринтердевице, элемент

Этот элемент является последовательностью вложенных элементов Меасурементдата Ргбпринтермеасуременттипе.

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.

### <a name="cmykprinterdevice-element"></a>Кмикпринтердевице, элемент

Этот элемент является последовательностью вложенных элементов Меасурементдата Кмикпринтермеасуременттипе.

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.

### <a name="rgbvirtualdevice-element"></a>Ргбвиртуалдевице, элемент

Этот элемент является последовательностью вложенных элементов объекта Ргбвиртуалмеасурементдататипе.

**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.

### <a name="plugindevicetype"></a>плугиндевицетипе

Этот элемент является последовательностью Гуидтипе GUID и всех вложенных элементов.

**Условия проверки:** Идентификатор GUID используется для сопоставления GUID подключаемого модуля DM DLL. Существует не более 100 000 настраиваемых вложенных элементов.

### <a name="rgbvirtualmeasurementtype"></a>ргбвиртуалмеасуременттипе

Этот элемент представляет собой последовательность, состоящую из

1.  Группа Ргбпримариесграуп
2.  Один из вариантов
3.  -   Gamma
    -   гаммаоффсетгаин
    -   гаммаоффсетгаинлинеаргам
    -   Элементы Тонереспонсекурвес

4.  Необязательный Гамутбаундарисамплес Гамутбаундарисамплестипе
5.  Метка времени (dateTime)

**Условия проверки:** Каждый вложенный элемент этих типов имеет свои собственные условия проверки.

### <a name="gammatype"></a>гамматипе

Этот элемент представляет собой сложный тип, состоящий из атрибута

-   Гамма-Ноннегативефлоаттипе

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="gammaoffsetgaintype"></a>гаммаоффсетгаинтипе

Этот элемент представляет собой сложный тип, состоящий из атрибутов

-   Гамма-Ноннегативефлоаттипе
-   Смещение Ноннегативефлоаттипе
-   Получить Ноннегативефлоаттипе

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="gammaoffsetgainlineargaintype"></a>гаммаоффсетгаинлинеаргаинтипе

Этот элемент представляет собой сложный тип, состоящий из атрибутов

-   Гамма-Ноннегативефлоаттипе
-   Смещение Ноннегативефлоаттипе
-   Получить Ноннегативефлоаттипе
-   Линеаргаин Ноннегативефлоаттипе
-   Транситионпоинт Ноннегативефлоаттипе.

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="toneresponsecurvestype"></a>тонереспонсекурвестипе

Этот элемент является последовательностью

1.  Редтрк Флоатпаирлист
2.  Гринтрк Флоатпаирлист
3.  Блуетрк Флоатпаирлист

Элемент также имеет атрибут Тркленгс типа unsignedInt.

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="gamutboundarysamplestype"></a>гамутбаундарисамплестипе

Этот элемент является последовательностью RGB Ргбтипес.

**Условия проверки:** В настоящее время не ограничено максимальное число повторений, которое должно быть ограничено на основе отзывов отрасли.

### <a name="floatpairlist"></a>флоатпаирлист

Этот элемент представляет собой простой тип списка пар float.

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="cmykprintermeasurementtype"></a>кмикпринтермеасуременттипе

Этот элемент является

1. последовательность элементов Колоркубе, состоящая из последовательности примеров Ноннегативекмиксамплетипе

2. Атрибут TimeStamp dateTime.

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="rgbprintermeasurementtype"></a>ргбпринтермеасуременттипе

Этот элемент является

1. последовательность элементов Колоркубе, состоящая из последовательности примеров Ноннегативергбсамплетипе

2. Атрибут TimeStamp dateTime.

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="rgbcapturemeasurementtype"></a>ргбкаптуремеасуременттипе

Этот элемент является последовательностью

1.  Примариндекс complexType
2.  1.  Белый Онебасединдекс
    2.  Необязательный черный Онебасединдекс
    3.  Необязательный красный Онебасединдекс
    4.  Необязательное зеленое Онебасединдекс
    5.  Необязательные синие Онебасединдекс
    6.  Необязательный голубой Онебасединдекс
    7.  Необязательный пурпурный Онебасединдекс
    8.  Необязательный желтый Онебасединдекс

3.  Неутралиндицес строк Онебасединдекс
4.  Колорсамплес последовательность примеров Ноннегативергбсамплетипе

Элемент также имеет атрибут TimeStamp dateTime.

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="onebasedindex"></a>онебасединдекс

Этот элемент является простым типом базового типа без знака int с minInclusive значением = "1".

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="rgbprojectormeasurementtype"></a>ргбпрожектормеасуременттипе

Этот элемент является последовательностью

1.  Группа Ргбпримариесграуп
2.  элемент Колорсамплес, состоящий из последовательности примеров Ноннегативергбсамплетипе

Элемент также имеет атрибут TimeStamp dateTime.

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="displaymeasurementtype"></a>дисплаймеасуременттипе

Этот элемент является последовательностью

1.  Ргбпримариесграуп группы
2.  Грайрамп последовательности примеров Ноннегативергбтипе
3.  Редрамп последовательности примеров Ноннегативергбтипе
4.  Гринрамп последовательности примеров Ноннегативергбтипе
5.  Блуерамп последовательности примеров Ноннегативергбтипе

Элемент Дисплаймеасуременттипе также имеет атрибут TimeStamp dateTime.

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="measurementconditionstype"></a>меасуременткондитионстипе

Меасуременткондитионстипе — это последовательность вложенных элементов, которая содержит:

1.  Колорспаце ограниченное строковое значение перечисления "ЦИЕКСИЗ"
2.  Необязательный вариант перечисления Вхитепоинт Ноннегативексизтипе или Вхитепоинтнаме String для значений D50, D65, A или F2
3.  Геометрическая Жеометритипе
4.  Апертуресизе целое число в миллиметрах

Значения по умолчанию:

1.  Принтеры RGB и CMYK:
    1.  ЦИЕКСИЗ Меасурементспацетипе
    2.  D50 Вхитепоинтвалуе
    3.  0/45 Жеометритипе
    4.  10mm Апертуресизе
2.  Сканеры
    1.  ЦИЕКСИЗ Меасурементспацетипе
    2.  D50 Вхитепоинтвалуе
    3.  0/45 Жеометритипе
    4.  10mm Апертуресизе
3.  Отображает и RGB виртуальное устройство:
    1.  ЦИЕКСИЗ Меасурементспацетипе
    2.  D65 Вхитепоинтвалуе
    3.  0/45 Жеометритипе
    4.  10mm Апертуресизе
4.  Цифровой
    1.  ЦИЕКСИЗ Меасурементспацетипе
    2.  D65 Вхитепоинтвалуе
    3.  Прямой Жеометритипе
    4.  10mm Апертуресизе

**Условия проверки:** Проверка каждого вложенного элемента определяется условиями проверки для этих вложенных элементов. Если какой-либо из вложенных элементов отсутствует, используется тип модели устройства по умолчанию.

### <a name="geometrytype"></a>жеометритипе

Строка

Значения перечисления:

-   "0/45"
-   "0/диффузный"
-   "диффузия/0"
-   Направлений

**Условия проверки:** Любое значение, за исключением указанных значений енумбератион, является недопустимым. Эта информация не изменит поведение базовой обработки.

### <a name="rgbprimariesgroup"></a>ргбпримариесграуп

Этот элемент является последовательностью

1.  Вхитепримари Ноннегативексизтипе
2.  Редпримари Ноннегативексизтипе
3.  Гринпримари Ноннегативексизтипе
4.  Блуепримари Ноннегативексизтипе
5.  Блаккпримари Ноннегативексизтипе

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="nonnegativecmyksampletype"></a>ноннегативекмиксамплетипе

Этот элемент является последовательностью

1.  CMYK Ноннегативекмиктипе
2.  ЦИЕКСИЗ Ноннегативексизтипе

Элемент также имеет необязательную строку тега атрибута

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="nonnegativergbsampletype"></a>ноннегативергбсамплетипе

Этот элемент является последовательностью

1.  Ноннегативергбтипе RGB
2.  ЦИЕКСИЗ Ноннегативексизтипе

Элемент также имеет необязательную строку тега атрибута

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="nonnegativecmyktype"></a>ноннегативекмиктипе

Этот элемент состоит из атрибутов

1.  С плавающей запятой
2.  С плавающей запятой M
3.  Y с плавающей запятой
4.  K с плавающей запятой

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="nonnegativergbtype"></a>ноннегативергбтипе

Этот элемент состоит из атрибутов

1.  R float
2.  С плавающей запятой
3.  B с плавающей запятой

**Условия проверки:** Для определения на основе отзывов отрасли.

### <a name="extensiontype"></a>ExtensionType

Элемент ExtensionType является последовательностью любого типа вложенного элемента и используется для собственной информации от сторонних приложений.

**Условия проверки:** Этот элемент является необязательным. Допускается не более 1000 вложенных элементов расширения.

### <a name="nonnegativexyztype"></a>ноннегативексизтипе

Элемент Ноннегативексизтипе состоит из Ноннегативефлоаттипе трех элементов с плавающей запятой одиночной точности с именами "X", "Y" и "Z". Эти значения ограничиваются значениями измерений профилей DMP. Эти измерения могут быть абсолютными (не относительными) ЦИЕКСИЗ 1931 отражающими значениями или абсолютными (не относительными) ЦИЕКСИЗ 1931 прямыми (передаваемые) значениями в Канделас на единицы измерения с квадратом.

**Условия проверки:** Допустимы только реальные значения, а отрицательные значения измерения ЦИЕКСИЗ недопустимы. Так как это абсолютные значения, значения могут быть больше 1,0 f. Разумное ограничение для любых "X", "Y" или "Z". для значения произвольно задано значение 10000.0 f.

### <a name="xyztype"></a>ксизтипе

Элемент Ксизтипе состоит из трех значений с плавающей запятой одиночной точности: "X", "Y" и "Z".

## <a name="the-cdmp-baseline-algorithms"></a>Базовые алгоритмы КДМП

### <a name="crt-device-model-baseline"></a>Базовый план модели устройства CRT

Чтобы понять эту модель, необходимо учитывать как процесс обработки символов, так и моделирование устройств. В процессе обработки символов измерения XYZ сначала выполняются на цветах, полученных путем заполнения буферов экрана ЭЛТ-устройства. В следующих примерах значения будут созданы хорошие данные для модели базовых устройств CRT:

Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Нейтральные: R = G = B = 0, 8, 16, 32, 64, 128, 192, 255

Также можно использовать приращение, отличное от 15 и нелинейного приращения. Каждый красный, зеленый, синий и нейтральный пандус должны содержать по крайней мере три выборки, но рекомендуется предоставить больше образцов. Необходимо предоставить образцы для чисто красного, зеленого, синего, Черного и белого цветов. Примеры не обязательно должны иметь одинаковое пространство.

Процесс создания матрицы тристимулус состоит из двух этапов. Сначала следует оценить значение черной точки XYZ или Блик. Этот шаг в основном основан на работе Бернс \[ 3 \] с немного измененной функцией цели для нелинейной оптимизации. Во-вторых, вычислите тристимулус матрицу на основе результата, полученного на шаге 1, а также вычисления усреднения по всем измерениям для каждого канала, а не только для максимального числа цифр.

Каждый из этих шагов содержит подробные процедуры. Начальная точка — это пандус (17 шагов в нашем примере) для каждого канала R, G и B. При отображении измерений XYZ на плоскости *XY* -нолики типичная ситуация показана на рис. 1. Шаг 1 состоит в решении проблемы нелинейной оптимизации, которая позволяет найти «наилучшее» направление черного цвета, что снизит смещение в глубине насыщенности по каналам R, G и B. На основе Бернс \[ 3 \] мы будем искать ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ), что позволяет максимально сокращать следующую целевую функцию:

![Показывает целевую функцию, где SR, SG и SB являются набором точек данных в каналах R, G и B.](images/cdmp-formula1.png)

где *s <sub>R</sub>*,*s <sub>G</sub>* и *s <sub>B</sub>* — это набор точек данных, соответствующих точкам в каналах R, G и b. Для *любого набора определите*:

![Показывает формулу для определения любого набора.](images/cdmp-formula2.png)

В предыдущих \|  \| версиях s — кратность *s*, т. е. количество точек в наборе.  ![ Показывает формулу для цветности точки.](images/cdmp-formula3.png) — Это координаты цветовой области точки, ![ которая показывает формаула для точки.](images/cdmp-formula4.png) , то ![ есть формула для среднего или центрирования массы, ](images/cdmp-formula5.png) — это среднее значение или центр массы всех точек *в* наборе в плоскости цветовой области. Таким же результатом является ![ Формула суммы секунды в секундах.](images/cdmp-formula6.png) сумма, равная сумме второго секунды относительно центра массы и представляющая степень распределения очков между ними. Наконец, ![ показывает формулу для общей меры распределения из трех кластеров точек.](images/cdmp-formula7.png) представляет собой общую меру распределения трех кластеров точек о соответствующих центрах.

В вычислении ![ показывает формулу f (X, Y, Z; КСК, ИК, ZK).](images/cdmp-formula8.png) , если ![ выражение содержит формулу для X. ](images/cdmp-formula9.png) , то вычисление пропускается, а кратность *S* корректируется соответствующим образом.

Несмотря на очевидную сложность функции задания, это сумма квадратов многих дифферентиабле функций в *X <sub>k</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 точек 2 *XY* -компоненты 3 канала = 102, в примере) и, следовательно, податлива к стандартным нелинейным методам, таким как алгоритм Levenberg-Marquardt, который является алгоритмом, используемым в WCS. Обратите внимание, что Предыдущая функция-цель отличается от предложенной в Бернс \[ 3 \] в том, что последняя функция измеряет дисперсию расстояния от центра массы, так что дисперсия равна нулю, когда точки эквидистантная от центра массы, даже если они могут распределяться довольно немного. В этом примере распределенность точек осуществляется напрямую с помощью второго секунды.

Как и в случае с любыми последовательными алгоритмами для проблемы с нелинейной наименее квадратами, Levenberg-Marquardt требует первоначального предположения. Существует два очевидных кандидата. Один — (0, 0, 0); второй — измеряемая черная точка. Для выражения CTE измеряемая черная точка сначала используется в качестве начального предположения. Если превышено максимальное число итераций 100 без достижения среднего расстояния в 0,001 каждой точки от центра массы (что соответствует пороговому значению (0,001) 17 3 = 0,000051 для функции цели), то выполняется еще один цикл итераций с первоначальным предположением (0, 0, 0). Результирующая оценка черной точки — XYZ по сравнению с лучшей оценкой из предыдущего цикла итераций (с измеряемой черной точкой в качестве первоначального предположения). Используйте оценку, которая возвращает наименьшее значение для целевой функции. Выбор из 100 итераций и расстояние ошибки 0,001 были выбраны многопроходно. В будущих версиях может быть целесообразно параметризовать расстояние ошибки.

Результатом первого шага является предполагаемая черная точка ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ). Второй шаг состоит из определения тристимулус матрицы путем усреднения цветового значения точек в трех кластерах, полученных на шаге 1. Для библиотек CRT это делается в основном для снижения влияния ошибок измерения. Точки, используемые для усреднения цветовой области, должны быть одной и той же точкой, используемой в процессе оптимизации на первом шаге. Иными словами, если первая точка (цифровое число 15, в примере) в каждом пандусе отбрасывается на шаге оптимизации, то то же самое необходимо сделать в усреднении. ![Значение, если содержит формулы среднего цвета для координат красного и зеленого каналов.](images/cdmp-formula10.png) и ![ отображает формулу среднего цвета для координат в синем канале.](images/cdmp-formula11.png) — Это средние координаты цветовых каналов красного, зеленого и синего цветов, а следующая процедура определяет матрицу тристимулус. Сначала решите систему 3? 3 Линейная:

![Показывает первую часть процедуры для решения линейной системы 3? 3.](images/cdmp-formula12.png)

![Показывает вторую часть линейной системы 3? 3.](images/cdmp-formula13.gif)![Отображение значения t подстрочной b в конце второй части линейной системы 3? 3.](images/cdmp-formula14.gif)

*X <sub>w</sub>*,*Y <sub>W</sub>*,*Z <sub>w</sub>*

![Показывает последнюю часть процедуры для решения линейной системы 3? 3.](images/cdmp-formula15.png)

После определения матрицы тристимулус определение кривых тонов соответствует стандартному подходу. Для отображения CRT предполагается, что отдельные каналы соответствуют модели "Гог":

![Показывает формулу для модели "G O G".](images/cdmp-formula16.png)

где *k <sub>g</sub>* — это "прибыль", 1-*k <sub>g</sub>* — "offset" и? — это «гамма». Обратная матрица тристимулус матрицы применяется к данным XYZ нейтральных элементов, чтобы получить линейные данные RGB, которые затем сопоставляются с цифровым значением RGB с использованием нелинейной регрессии в модели Гог. Эти характеристики не обязательно должны быть одинаковыми для каналов R, G и B и обычно не совпадают.

Бернс \[ 1 \] : Бернс, *Биллмэйер и салтзман принципы цветовой технологии*, 3 <sub>RD</sub> ED. Джон Wiley & сыновьями (2000).

Бернс \[ 2 \] : Бернс и катох, функция Digital to радиометрик для обмена с управляемыми компьютерами CRT, *Цие эксперт Symposium ' 97 цветовые стандарты для технологии создания образов*, Ноя. 1997.

Бернс \[ 3 \] : Бернс, Фернандес и Таплин, оценка Black-Level выбросов Computer-Controlled, просмотр *цветов и приложения*, 28:379-383 Wiley периодов, Inc. (2003)

Канг \[ 1 \] : Канг, *цветовая технология для устройств электронных изображений*, Спие (1997)

Катох \[ 1 \] : Катох, Дегучи и Бернс, точная кодировка предложения CRT Monitor (II) для расширения в метод Цие и его проверки, *OPT. Rev.* 8:397-408 (2001)

### <a name="lcd-device-model-baseline"></a>Базовая модель устройства LCD

Базовый план модели ЖК-устройства подобен базовому плану модели устройства CRT. В этом разделе рассматриваются способы, с помощью которых ЖК-моделирование отличается от моделирования CRT.

Одно отличие заключается в том, что ЖК-дисплеи должны следовать за моделью Гог, используемой для библиотек CRT, а кривые тона получаются путем интерполяции измеряемых данных. По этой причине независимая ось устройства должна быть выборке чаще.

Ниже приведены некоторые типичные примеры значений, которые могут формировать хорошие данные для базового показателя модели ЖК-устройства.

Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Нейтральные: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

Вычисление среднего цветового цвета для получения цветов для первичных элементов устройств является более важным для LCDs, чем для библиотек CRT. При отображении единиц измерения "XYZ" на плоскости *XY* -нолики типичная ситуация показана на рис. 1. Обратите внимание на смещение цветовой области к черной точке. Это обусловлено тем, что все LCDs имеют определенный уровень утечки освещения.

![Схема, показывающая график цветовой области с помощью необработанных данных без исправления.](images/cdmp-lcd-dmp-figure1.png)

**Рис. 1** . схема цветовой области, использующая необработанные данные без исправления

При вычитании из необработанных измерений XYZ типичная ситуация показана на рис. 2. Теперь точки Tне кластеризованы по трем центрам, хотя они не идентичны. Процесс усреднения, описанный для библиотек CRT, значительно улучшает результаты для LCDs.

![Схема, показывающая график насыщенности с помощью необработанных данных с настроенной черной точкой.](images/cdmp-lcd-dmp-figure2.png)

**Рис. 2** . схема цветовой области с использованием данных с скорректированной черной точкой

### <a name="rgb-capture-device-model-baseline"></a>Базовая модель устройства для записи RGB

Базовая модель устройства отслеживания RGB является подклассом класса Идевицемодел. В кодировке для устройств записи цветов, таких как сканеры и Цифровые камеры, используется следующий подход. Целевой объект, состоящий из цветовых исправлений с известными значениями ЦИЕКСИЗ, захватывается с помощью устройства записи. Результатом захвата является растровое изображение RGB, в котором цвет каждого исправления кодируется в значении RGB. Значения RGB для устройства зависят от конкретного устройства записи. Цель кодировки «+ +» заключается в том, чтобы установить многообразную связь между значениями RGB устройства и значениями ЦИЕКСИЗ, а также математическим преобразованием из RGB в XYZ, чтобы точно определить, насколько возможно поведение устройства записи.

Такое математическое преобразование может быть смоделировано с учетом степени полинома низкого угла. Эта процедура описана в литературе, например Канг \[ 92 \] , Канг \[ 97 \] . В Канг \[ 97 используется \] подход, в котором используется набор из трех значений полинома с 3, 6, 8, 9, 11, 14 или 20 терминами в переменных R, G и B, тогда как три свойства регрессии, соответственно, в компоненты X, Y и Z Циексиз пространства. Для 20-словного полинома используется форма:

![Показывает 20-условный полином.](images/cdmp-formula20.png)

Существуют похожие выражения для Y и Z. Математическая методика для подгонки полиномов попадает в «многофакторная линейную регрессию» и описывается в любом простейшем тексте в статистике.

Этот метод линейной регрессии имеет значение, не уменьшая правую функцию цели. Линейная регрессия находит наименьшее из квадратов, что означает, что коэффициенты, полученные в результате, уменьшают общую сумму квадратов ошибок в базовом пространстве или эквивалентно сумме квадратов евклидово расстояний. На практике требуется максимально сокращать сумму квадратов? Откуда? E — один из принятых стандартов, таких как CIE94. Минимизация этой целевой функции — это нелинейная задача регрессии.

В новом подсистеме в качестве лабораторного к XYZ используется ЦИЕ цветовое пространство, а в качестве модели для устройства захвата используется 20-термный коэффициент кубического уровня, а для использования в качестве подсчета, в котором следующие полиномы уменьшают сумму квадратов? E <sub>CIE94</sub> s.

![Отображает набор формул полинома.](images/cdmp-formula21.png)

Решение ( *l <sub>i</sub>*, *а <sub></sub>* я, *b <sub>i</sub>* ) в 60-мерный вещественном числовом пространстве **R** 203 должно быть таким, чтобы следующая общая ошибка была минимальна:

![Показывает общую ошибку для сворачивания.](images/cdmp-formula22.png)

где суммирование проходит через все пары точек данных (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub></sub>*,*v <sub>i</sub>* ) в наборе данных выборки, а также дополнительные контрольные точки, которые должны быть подробно описаны в следующем примере. Это нелинейная задача регрессии, *поскольку параметры <sub> я</sub>*, *a <sub></sub>*, * <sub>i</sub>* вводит в функцию цели нелинейный способ (не в виде квадратичного).

Поскольку функция задания? является нелинейной (и неквадратичной) функцией параметров *?<sub> я</sub>*, *а <sub>i</sub>* и * <sub>i</sub>*, чтобы решить проблему оптимизации, необходимо прибегнуть к итеративным методам. Поскольку форма функции задания является суммой квадратов, используется стандартный метод оптимизации, называемый алгоритмом Levenberg-Marquardt. Он считается методом выбора для проблем с нелинейным наименьшим числом квадратов. Для итеративных алгоритмов, таких как Левенберг-Маркварт, необходимо указать начальное предположение. Хорошее первоначальное предположение обычно является критически важным при поиске правильного минимального значения. В этом случае один хороший кандидат на первоначальное предположение — решение проблемы линейной регрессии. Сначала Сократите сумму квадрата евклидово расстояний в лабораторном пространстве, определив функцию, определяющую целевое значение.

![Показывает определенную функцию для квадратичной цели.](images/cdmp-formula23.png)

Математическое решение такого типа «линейная и наименьшая квадраты» хорошо известно. Так как *?<sub> я</sub>* появился только в модели *L* , а *<sub>i</sub>* отображается только в модели *u* , а * <sub>i</sub>* отображается только в модели *v* . проблему оптимизации можно разложить на три подзадачи: одну для *L*, одну для *u* и одну для *v*. Рассмотрим « *L* уравнения». (Уравнения *u* и *v* уравнения соответствуют точно одному аргументу.) Проблема минимизации суммы квадратов ошибок в *L* может быть обпоставлена следующим уравнением матрицы в некотором смысле наименее квадратов:

![Показывает уравнение матрицы для L.](images/cdmp-formula24.png)

где *N* — общее количество точек данных (исходные образцы точек плюс контрольные точки, созданные описанными ниже способами). Как правило, *N* гораздо больше 20, поэтому предыдущее уравнение было чрезмерно определено, что требует наименьшего решения в виде квадратов. Это решение для закрытых форм **?** доступен:

![Отображает решение закрытой формы.](images/cdmp-formula25.png)

На практике прямое вычисление с помощью решения закрытой формы не используется, так как оно имеет неудовлетворительные числовые свойства. Вместо этого некоторый тип алгоритма факторинга матрицы применяется к матрице коэффициента, которая сокращает систему уравнений до канонической формы. В текущей реализации для матрицы **R** применяется декомпозиция единственного значения (SVD), а затем разрешается полученная декомпозиция системы.

Решение проблемы линейной регрессии, обозначенное, ![ показывает решение проблемы линейной регрессии.](images/cdmp-formula26.png) , используется в качестве начальной точки алгоритма Levenberg-Marquardt. В этом алгоритме вычисляются шаги пробной версии, которые должны двигаться ближе к оптимальному решению. Этап пробной версии удовлетворяет набору линейных уравнений, зависящих от функционального значения и значений производных элементов в текущей точке. По этой причине производные от функции цели? в отношении параметров *?<sub> i</sub>*, *я <sub></sub> <sub></sub>* потребовал входные данные для алгоритма Levenberg-Marquardt. Хотя существует 60 параметров, существует ярлык, позволяющий вычислять гораздо меньше. По правилу цепочки математического анализа за,

![Показывает уравнение, которое позволяет использовать ярлык с помощью правила цепочки математического анализа за.](images/cdmp-formula27.png)

где *j* = 1, 2,, 20, *L <sub>i</sub>*,*u <sub>я</sub>*,*v <sub>i</sub>* *— это значение Циелаб в качестве* образца, а *R <sub>ИЖ</sub>* — это запись (*i*,*j* ), определенная **выше матрицы** . Таким образом, вместо вычисления производных для параметров 60 можно вычислять производные для *L*,*a* и *b* , используя числовые разностные вычисления.

Также необходимо настроить критерий остановки для итерационных алгоритмов. В текущей реализации итерации завершаются, если среднее значение квадрата DECIE94 меньше 1 или число выполненных итераций превысило 10. Число 10 поступает из практического опыта, если первые несколько итераций не уменьшают ошибку значительно, а дальнейшие итерации не будут настолько полезны, как перемещение точки осЦиллатори способом, т. е. алгоритм может не сходится. Даже в том случае, если алгоритм сходится, мы можем убедиться, что DECIE94 не хуже того, что мы начали, т. е. с параметрами, полученными из линейной регрессии.

Даже при использовании предыдущего метода нелинейной регрессии возникает несколько проблем с подгонками. Одна из проблем заключается в том, что степень сложности обычно отклонение или с неисправностью за точками данных. Искусственные локальные прыжка и прыжка могут быть введены в процесс подгонки. Это можно запретить с помощью полиномов низкого уровня, что является причиной, по которой не следует использовать более трех градусов. Более серьезный аспект снижения или прокрутки заключается в том, что, хотя степень серьезности может принимать любое вещественное значение теоретически, пространство, которое он пытается смоделировать, обычно имеет физические ограничения и практические ограничения. ЦИЕКСИЗ должен иметь все координаты X, Y и Z, не являющиеся отрицательными, которые являются физическими ограничениями. На практике они принимают значения только с сотнями, а не с тысячами и выше. Аналогичным образом, ЦИЕЛАБ или ЦИЕЛУВ имеет собственные физические и практические ограничения. Если пространство RGB заполнено с точки выборки, проблема с прокруткой или прокруткой не является серьезной. Однако захваченные точки RGB из устройства записи обычно не заполняют пространство RGB единообразно. Точки могут заполнить только внутренний 80% Куба RGB, или, что более того, они могут находиться в более низком эта функция предназначена. В этом случае при экстраполяции значений за пределами точек данных нереалистичные прогнозы могут оказаться неудовлетворительными. Необходимо, чтобы модель всегда возвращала разумные значения. Для этого требуется метод, который может эффективно управлять поведением границ регрессивной регрессии, установления дополнительные затраты на эти степени, которые работают нестабильно, близко к границе Куба RGB. Еще одной мерой, гарантирующей, что полиномы всегда возвращают реалистичные значения, применяются путем усечения выходных данных в ЦИЕ Спектрал очага.

На этом этапе моделирование сканера и моделирование камеры расходят друг от друга. Предполагается, что модель камеры будет выделена до регионов за пределами выбранных точек, включая «отраженные блики», для модели сканера не требуется одинаковая экстраполяция. Предполагается, что цель сканера охватывает сходство, похожее на печатные материалы, которые должны быть проверены. Модель сканера все еще должна быть надежной в том смысле, что она не должна возвращать нереалистичные значения, но экстраполяция далеко за пределы целевого объекта не требуется. Чтобы обеспечить надежность, значение L-полинома, приведенное выше, обрезается в 100, то есть модель полинома не должна высекаться за пределами "DMin" целевого объекта сканера.

Предполагается, что модель камеры будет обрезана до отраженных светов, поэтому обрезка в 100 нежелательна. Вместо этого используется следующий алгоритм.

Для управления поведением свойств полиномов в регионах с недостаточным объемом выборки появились контрольные точки искусственного интеллекта. Стратегические размещение этих контрольных точек с соответствующими значениями позволяет «извлекать» степень полинома в требуемом направлении. В текущей реализации используются восемь контрольных точек, соответствующих углам Куба RGB. Если значения устройства нормализованы до Unity, то используются следующие моменты:

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

За исключением белого *R*  = *G*  = *B* = 1, связанного со значением Циелаб *L* = 100, *u*  = *v* = 0, для определения подходящего значения Циелаб используется следующий алгоритм экстраполяции. Как правило, для конкретного (*r*,*g*,*b* ) вес связан с каждым из (*r <sub>i</sub>*,*g <sub>i</sub>*,*B <sub>i</sub>* ) в наборе данных выборки. Существует две цели для назначения веса. Во-первых, вес обратно пропорционален расстоянию между (*r*,*g*,*b* ) и (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ). Во-вторых, вы хотите отбросить или присвоить весовой коэффициент 0 к точкам, цвет которых отличается от оттенка данной точки (*R*,*G*,*B* ). Чтобы сделать оттенок учетной записи, рассмотрите точки, находящиеся внутри конуса, вершина которого равна (0, 0, 0), ось которой совпадает со строкой, соединяющей (0, 0, 0) и (*R*,*G*,*B* ) и вертикальным углом? соответствует COS? = 0,9. Иллюстрация этого конуса показана на рис. 3.

![Схема, показывающая форму окружения.](images/cdmp-lcd-dmp-figure3.png)

**Рис. 3** . Фильтрация образцов точек по угла и расстоянию. Форма окружения показана только для иллюстрации. Фактическая фигура зависит от используемого расстояния; Это одноромбное окружение, если используется 1 норма.

В этом конусе выполняется вторая фильтрация, основанная на расстоянии RGB, который использует 1-норму, определенную

![Показывает формулу для второй фильтрации в конусе.](images/cdmp-formula28.png)

При текущем конусе первоначальный поиск осуществляется для точек, которые находятся в пределах расстояния от 0,1 (*R*,*G*,*B* ). Если в радиусе не найдено ни одной точки, радиус увеличивается на 0,1, а поиск перезапускается. Если следующая скругленная некоторая точка не имеет ни одного, радиус увеличивается на 0,1. Этот процесс будет продолжен до тех пор, пока радиус не превысит Максдист/5, где Максдист = 3, в случае 1-нормы. Если точка не найдена, конус увеличивается за счет уменьшения COS? к 0,05, т. е. увеличить угол? и перезапускает весь процесс с увеличивающимся радиусом. Этот процесс будет продолжен до тех пор, пока не будет найден непустой набор точек или COS? достигает значения 0, то есть конус открыт, чтобы стать плоскостью. На этом этапе Поиск перезапускается путем увеличения радиуса, за исключением того, что поиск будет продолжен до тех пор, пока радиус не достигнет Максдист. Это гарантирует, что в худшем случае будет найден непустой набор точек. Этот алгоритм суммируется на схеме Flow на рис. 4.

![Схема, показывающая последовательность алгоритма.](images/cdmp-lcd-dmp-figure4.png)

**Рисунок 4** . Схема потока для определения набора точек выборки, используемых в экстраполяции для входного значения RGB

При условии, что предыдущий процесс *выдает непустой набор точек* (*R <sub>i</sub>*,*G <sub>i</sub>*,*b <sub>i</sub>* ) и соответствующий (*L <sub>i</sub>*,*а <sub>я</sub>*,*b <sub>i</sub>* ), то для каждой такой точки назначается *вес,<sub></sub>* присвоенный

![Показывает формулу для веса для каждой точки.](images/cdmp-formula29.png)

Наконец, екстраполант определяется

![Показывает определение для екстраполант.](images/cdmp-formula30.png)

Предыдущие уравнения составляют экземпляр "взвешенных методов обратного расстояния", обычно называемых методами Шепард. Выполняя каждую из восьми точек с EQ (6) через алгоритм, получаются восемь контрольных точек, каждая из которых имеет значения *R*,*G*,*B* и *L*,*a*,*b* , которые помещаются в пул с исходными образцами данных.

Чтобы гарантировать, что модель всегда формирует допустимые значения цвета, и целостность системы и стабильность всего конвейера обработки цветов, необходимо выполнить окончательную отсечение с выходными данными модели полинома. Визуальный охват ЦИЕ описывается компонентом ачроматик (*Y* или *L* ) и компонентом цветового элемента (*XY* или *а'б*), которые связаны с пространством XYZ с помощью многопроектного преобразования). В текущей реализации используется цвет « *а'б»* , так как он напрямую связан с Циелув пространством. Для любого значения *Циелаб* сначала Clip *L* в неотрицательное значение:

![Показывает отсечение L с неотрицательным значением.](images/cdmp-formula31.png)

Чтобы разрешить экстраполяцию для отраженных светов, *L* не обрезается в 100, "обычной" верхней границы для *L* в пространстве лаборатории.

Затем, если *L* = 0, то *a* и *b* обрезаются таким, что a *= b =* 0. Если *L* ? 0, вычислить

![Показывает формулу, если L = 0.](images/cdmp-formula32.png)

Это компоненты вектора в схеме *а'б* из белого пункта (*u? "*,*v?"* ) к рассматриваемому цвету. Определите ЦИЕ Спектрал очага как выпуклой поверхности всех точек (*a "*,*b"* ), параметризованных вавеленгс?:

![Показывает формулу для вавеленгс.](images/cdmp-formula33.png)

где ![ отображаются функции для сопоставления цветов Цие.](images/cdmp-formula34.png) — Это ЦИЕ функции сопоставления цветов для наблюдателя с 2 градусами. Если вектор находится за пределами ЦИЕ очага, он обрезается до точки на ЦИЕ очага, которая является пересечением очага и линией, определенной вектором. См. рис. 5. Если обрезка произошла, значение *a* и *b* перестраивается с помощью первого вычитания *?* и *b? '* из обрезанного *типа "* и *b"* и затем умножения на 13 *L*.

![Схема, на которой показан график для алгоритма обрезки.](images/cdmp-lcd-dmp-figure5.png)

**Рис. 5** . Алгоритм обрезки для значений Lab, которые выходят за пределы визуального элемента Цие

В текущей реализации ЦИЕ Спектрал очага в плоскости *а'б* представляет собой кусочно-линейную кривую с 35 сегментами (соответствующей вавеленгс от 360 nm до 700 nm включительно). При упорядочении сегментов линии таким образом, чтобы их часть в белой точке была в порядке возрастания, что эквивалентно убыванию вавеленгсс, сегмент линии, пересекающийся с лучом, сформированный приведенным выше вектором, может быть обнаружен простым двоичным поиском.

### <a name="rgb-printer-device-model-baseline"></a>Базовый план модели устройства принтера RGB

Устройство печати RGB-принтера состоит из создания многообразовой модели устройства, которая прогнозирует независимый от устройства ЦИЕЛУВ цвет для любого значения RGB.

Существует два способа создания многовариантной модели. Один из способов — использовать данные устройства для принтера RGB, а другой — использовать аналитические данные параметров. В первом случае данные измерения, предоставленные пользователем для устройства принтера RGB, используются для создания таблицы 3-D Lookup (LUT). Данные измерения состоят из значений XYZ для одинаковых выборочных исправлений RGB. Стандартные размеры выборки — 9 или 17 для каждого компонента. Каждое исправление измеряется с помощью колориметер или спектрофотометер в ЦИЕКСИЗ пространстве. Затем значение XYZ для исправления преобразуется в значение ЦИЕЛУВ, формирующее трехмерную LUT. В модели устройства метод интерполяции тетрахедрал Сакамото применяется к трехмерной LUT для прогнозирования данных ЦИЕЛУВ для данных RGB. (Сакамото США, патент 4275413 (Сакамото) 4511989, Канг \[ 1 \] . Истек срок действия двух упомянутых патентов.). Аналитические параметры, переданные во втором методе, — это просто LUT, который был построен ранее. Как правило, этот LUT был создан с помощью первого метода, хотя он может быть создан вручную.

В текущем управлении цветом исходная схема определяется как схема, которая перемещается из пространства RGB в аппаратно-независимое цветовое пространство ЦИЕКСИЗ. Целевая схема определяется как схема, которая перемещается из аппаратно-независимого ЦИЕКСИЗ цветового пространства в пространство RGB. Это обратная схема исходного кода.

Модель с использованием модели используется непосредственно в исходной карте. Сначала он сопоставляет данные RGB с данными ЦИЕЛУВ, которые преобразуются в данные типа XYZ. В целевой карте данные независимых от устройства ЦИЕКСИЗ сначала преобразуются в данные ЦИЕЛУВ. Затем для прогнозирования оптимальных данных в формате RGB для данных ЦИЕЛУВ используются модель и классический метод Newton-Raphson. Ниже приведены сведения о преобразовании из Циелув в данные RGB.

После создания трехмерного LUT из RGB в Циелув карту из RGB в Лув создается с использованием тетрахедрал интерполяции в RGB. Эта схема обозначается следующими уравнениями:

![Отображение уравнений для схемы с R G B до L U.](images/cdmp-image125.png)

Инверсия схемы состоит из решения для любого цвета ![Показывает L U.](images/cdmp-image127.png) , следующая система нелинейных уравнений:

![Показывает нелинейные уравнения для лолвинг любого цвета L.](images/cdmp-image129.png)

В новом CTE-выражении используется нелинейное уравнение, основанное на классического Newton-Raphson метода. Начальное предположение (или *приори* ), <sub>предшествующее</sub> (R 0, G 0, B 0), получается путем поиска по «начальной матрице», состоящей из унифицированной сетки 8x8x8 для предварительно вычисленных пар (RGB, Лув). Выбирается соответствующий Лув RGB, ближайший к L \* u \* \* . Каждая точка в матрице заполнения соответствует центру ячейки, так что итерации не начинаются с точки на границе границы Куба RGB. Иными словами, RGB начальных значений определяется следующим образом: шаг = 1/8 s <sub>ИЖК</sub> = (шаг/2 + (i-1) шаг, шаг/2 + (j-1) шаг, шаг/2 + (k-1) шаг) с i, j, k = 1... *8 на первом* шаге Ньютона-Рафсона, Следующая оценка ![ показывает переменные для следующей оценки.](images/cdmp-image133.png) получается по формуле:

![Показывает формулу для оценки.](images/cdmp-image135.png)

Итерация останавливается, когда ошибка (расстояние в ЦИЕЛУВ пространстве) меньше, чем предварительно установленный уровень допуска (0,1 в CTE-выражении), или когда число итераций превышает максимально допустимое число итераций (10 в CTE-выражении). Значения для допуска и количества итераций были определены эффективно. В будущих версиях значение допуска может быть изменено.

Матрица Жакобиан вычисляется с использованием прямой разницы, за исключением точки границы (один или несколько значений R, G, B — 1), где используется обратная разница. Вместо того чтобы рассчитывать обратную матрицу Жакобиан, линейная система разрешается напрямую с помощью Gauss-Jordanного удаления с полной сводкой.

В конце итераций схождение все равно может быть не достигнутым, так как Newton-Raphson является локальным алгоритмом, то есть хорошо работает только в том случае, если вы начинаете с первого предположения, близкого к истинному решению. Если, в конце Newton-Raphson итераций, конвергенция в предопределенной отказоустойчивости не была достигнута, итерации перезапускаются с новым набором начальных значений, определенным следующим образом.

Например, лучшим решением, полученным до сих пор, является (r, g, b). Из этого решения N постериори начальные значения являются производными, где N = 4. Интуитивно, решение перемещается по центру в соответствии с размером шага, который зависит от N. См. рис. 6.

![Схема, на которой показаны пертурбатион направления решения.](images/cdmp-image136.png)

**Рис. 6** . Направление пертурбатион решения зависит от того, в каком октет он находится.

Иными словами, если r &gt; 0,5, значение в канале r уменьшается, в противном случае значение увеличивается. Существует аналогичная логика для каналов G и B. Точные определения:

ПЕРТУРБАТИОН = 0,5/(N + 1)

Dir (r) =-1, если r &gt; 0,5; + 1 в противном случае. Аналогично для DIR (g) и dir (b)

ЖС постериори SEED, s????, имеет значение (r + dir (r) \* j \* пертурбатион, g + dir (g) \* j \* Пертурбатион, b + dir (b) \* j \* пертурбатион)

Попробуйте первые s???? и если оно предоставляет новое решение в пределах допустимой допускки ошибок, его можно прекратить. В противном случае попробуйте второй???? и т. д. до n????.

Схема всего алгоритма показана на рис. 7.

![Схема, показывающая последовательность инвертирования модели устройства.](images/cdmp-image138.png)

**Рис. 7. схема** инвертирования модели устройства

### <a name="rgb-virtual-device-model-baseline"></a>Базовый план модели виртуального устройства RGB

Эта модель устройств (DM) — это простой алгоритм воспроизведения матрицы и тона. Матрица является производной от белого пункта и первичного цвета с использованием стандартных алгоритмов обработки и анализа. Кривая воспроизведения является производной от параметров измерения в соответствии с ICC-описаниями Курветипе и Параметриктипе (или инверсией по мере необходимости). Подробные сведения о внутренних алгоритмах будут предоставлены после дополнительной проверки высоких проблем с динамическим диапазоном.

Модель виртуального устройства RGB — это идеальное значение кривой воспроизведения матрицы и тона RGB, аналогичное структуре профиля на основе матрицы из трех компонентов ICC. Параметры виртуального измерения в DM включают значение белой точки (абсолютное ЦИЕКСИЗ), первичные значения RGB (абсолютное ЦИЕКСИЗ) и кривую воспроизведения на основе ICC Параметриккурветипе и Курветипе в формате XML, совместимом с схемами DMP.

В следующей таблице показаны типы функций ICC Параметриккурветипе Encoding и соответствующая поддержка в Иргбвиртуалдевицемоделбасе.



| Тип функции                                         | Параметры                          | Тип                                     | Примечание                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Показывает функцию "Гамматипе".](images/cdmp-image154.png)<br/> | н<br/>              | гамматипе<br/>                 | Общая реализация<br/>           |
| ![Показывает функцию "Гаммаоффсетгаинтипе".](images/cdmp-image156.png)<br/> | общедоступная версия b<br/>           | гаммаоффсетгаинтипе<br/>       | ЦИЕ 122-1966<br/>                    |
| ![Показывает функцию "Гаммаоффсетгаиноффсеттипе".](images/cdmp-image158.png)<br/> | общедоступная версия b c<br/>         | гаммаоффсетгаиноффсеттипе<br/> | IEC 61966-3<br/>                     |
| ![Показывает функцию "Гаммаоффсетгаингаинтипе".](images/cdmp-image160.png)<br/> | общедоступная версия b c d<br/>       | гаммаоффсетгаингаинтипе<br/>   | IEC 61966-2.1<br/> sRGB<br/> |
| ![Показывает функцию для параметров "g a b c d e f".](images/cdmp-image162.png)<br/> | GA b c d е е<br/>   | Н/Д<br/>                       | Не поддерживается в WCS<br/>            |



 

Кривая тона для виртуальных устройств RGB применяется в Девицетоколориметрик между входными данными, Пдевицеколорс и матрицей. Для Колориметриктодевице необходимо использовать метод для инвертирования кривой тона. В базовой реализации это делается путем непосредственной интерполяции в той же кривой тона, которая используется для Девицетоколориметрик.

Кривые должны быть указаны в профилях как пары чисел в пространстве с плавающей запятой. Первое число представляет значения в Пдевицеколорс. Второе число представляет выход кривой тонов. Все значения в кривой тона должны находиться между Минколорантусед и Максколорантусед. Кривые тона должны содержать по крайней мере две записи: один для Минколорантусед и один для Максколорантусед. Максимальное число записей в Тонекурве — 2048. В целом, чем больше записей в таблице, тем точнее вы сможете моделировать кривизну. Между записями выполняется линейная интерполяция кусочно-.

Вы можете рассмотреть альтернативные методы интерполяции. Если вы знакомы с базовым поведением устройства, вы можете более точно использовать меньшее число выборок и модель, используя кривую с более высоким порядком. Но при использовании неправильного типа кривой вы будете очень неточны. Без дополнительных сведений вы не можете угадать тип кривой. Таким образом, используйте линейную интерполяцию и предоставьте много точек данных.

### <a name="cmyk-printer-device-model-baseline"></a>Базовая модель устройства принтера CMYK

Устройство печати CMYK принтера состоит из создания многообразной модели устройства, которая прогнозирует распечатанный цвет для любого значения CMYK. Подобная кодировка также включает в себя инверсию этой модели, чтобы можно было получить рецепт значения CMYK для печати для данного цвета. Обычно это определяется с точки зрения значения ЦИЕКСИЗ или ЦИЕЛАБ.

Как правило, используется целевой объект 8,7/3, содержащий исправления CMYK. Исправления состоят из выборки пространства CMYK в четко определенном виде, чтобы была сформирована прямоугольная сетка (с неоднородными интервалами в C, M, Y и K). Каждое исправление затем измеряется с помощью колориметер или спектрофотометер. Измерения в значениях ЦИЕКСИЗ затем формируют таблицу подстановки (LUT), из которой строится модель принтера с помощью метода интерполяции Сакамото. Патент 4275413 США (Сакамото et al.), патент США 4511989 (Сакамото), Канг \[ 1 \] . Истек срок действия двух упомянутых патентов.

Конкретные требования к примерам измерения CMYK, необходимым для использования профиля модели устройства в соответствии с моделью базового устройства принтера CMYK, приведены ниже. (Образец набора проще всего описать как набор образцов кубов КМИ, каждый из которых связан с конкретным уровнем K.)

-   Для уровней K = 0 и K = 100 должны быть указаны как минимум допустимые Кубы КМИ.
-   Промежуточные уровни K могут иметь неоднородное пространство.
-   Любой промежуточный уровень K без допустимого Куба КМИ будет проигнорирован.
-   Кубы КМИ могут использовать неоднородные интервалы выборки (междустрочный интервал), но один и тот же набор интервалов выборки должен использоваться во всех измерениях C, M и Y в Кубе КМИ для данного уровня K.
-   Каждый куб K уровня КМИ может использовать разное число и интервалы выборки.
-   Все Кубы КМИ должны содержать "углы" Куба КМИ, т. е. КМИ Samples имеет значение \[ 0, 0, 0 \] , \[ 0, 0100 \] , \[ 0100, 0 \] , \[ 100, 0, 0 \] , \[ 0100 100 \] , \[ 100, 0100 \] , \[ 100 100, 0 \] , \[ 100 100 100 \] .
-   Все промежуточные уровни сетки КМИ должны быть полностью выборке в каждом канале. Иными словами, пример должен существовать на каждом трехмерном пересечении сетки в Кубе КМИ.
-   Для кубов K = 0 и K = 100 КМИ, 2x2x2 «только углы» являются минимально допустимыми.

    \[Примечание. для K = 0 и K = 100 уровней куб 3x3x3 КМИ будет обрабатываться как куб с 2x2x2 только угловыми углами; промежуточный пример уровня не учитывается. в 4x4x4 и более крупных кубах будут использоваться все примеры использования сетки.\]

-   Для уровней "промежуточный K" 4x4x4 КМИ Кубы — это минимальный допустимый уровень.

Профиль высокого качества будет использовать более детализированные сетки выборки, чем минимум, необходимый для допустимости, обычно 9x9x9x9 или выше. Образцы из ИТ-8,7/3, IT 8,7/4 и ECI создают допустимые профили модели устройств (Дмпс) для модели базового устройства принтера CMYK. Несмотря на то, что эта модель устройства может игнорировать внешние (недоступные) примеры в этих целевых объектах, не гарантируется, что она сможет сделать это для других целей, и поэтому рекомендуется удалить лишние образцы из наборов измерений, поступающих в профили для этой модели устройства.

Некоторая версия модели принтера предоставляет больше проблем. Учитывая цвет ввода в ЦИЕКАМ, существует вопрос, находится ли этот цвет в цветовой гамме принтера. Существуют также проблемы, связанные с расположением точек в области отображения цвета. Несмотря на то, что значения CMYK можно расположить на прямоугольной сетке, как это делается в целевом объекте "8,7/3", то то же самое невозможно сказать из итогового напечатанного цвета, так как они расположены в области отображения цвета. Как правило, они разбросаны в области отображения цвета без определенного шаблона.

Обычно существует два подхода к проблеме устранения неисправностей в разбросанных точках. Одним из подходов является использование геометрического деления цветового охвата принтера с помощью простейших трехмерных сплошных трехмерных фрагментов, например тетрахедра. Подразделение цветового охвата принтера в области отображения цвета может быть вызвано соответствующим подразделением пространства КМИ (K), см \[ \] . 93, Канг \[ 97 \] . Этот подход имеет преимущество вычислительной простоты. В случае с тетрахедрон в интерполяции используются только четыре точки. С другой стороны, результат зависит от нескольких точек, что означает, что ошибка измерения оказывает значительное воздействие на результат. Интерполант также обычно не так гладко. Второй подход не предполагает наличия подразделений и основан на методе интерполяции рассеивания данных. Классическим примером является метод интерполяции Шепард или метод обратного взвешенного метода (см \[ . шепард 68 \] ). Здесь несколько точек, окружающих точку ввода, выбираются каким-либо образом, каждый из которых имеет вес, обычно обратно пропорционально расстоянию, а интерполант принимается в качестве взвешенного среднего по соседним точкам. При таком подходе выбирать соседние точки имеет первостепенное значение для производительности. Хотя слишком мало точек может визуализировать интерполант неточные и негладкие, слишком большое количество точек накладывает высокую вычислительную стоимость, так как весовые коэффициенты обычно являются нелинейными функциями и требуют вычислений.

Два подхода, описанных выше, имеют проблемы. Подход подразделений имеет критически важное значение для данных, которые, как правило, являются недостаточными для шума, и обычно интерполант не очень гладко. Рассеивание рассеивания данных более чувствительна к шумам данных и, как правило, предоставляет более гладкий интерполант, но он является более затратным.

Новое ОТВ использует другой подход. Устройство CMYK обрабатывается как коллекция из нескольких КМИ устройств, каждое из которых имеет определенное значение черного (K). При использовании алгоритма выбора, который принимает параметры Light и чрома, выбирается уровень черного. Значения КМИ получаются путем инверсии соответствующей таблицы КМИ в Лув с помощью методов Ньютона, используемых в других случаях алгоритмом принтера RGB.

Выполните следующие действия.

1.  Распечатайте целевой объект, который является либо целевым объектом для ИТ-8,7/3, либо целевым объектом, содержащим выборку пространства CMYK в обычном или непостоянном промежутке времени.
2.  Измерьте целевой объект с помощью спектрофотометер и преобразуйте измерения в ЦИЕЛУВ пространство.
3.  Создайте прямую карту из CMYK в Лув.
4.  Используйте прямую карту для создания набора КМИ для Лув Maps для диапазона значений K.
5.  Для любого входного значения Лув соответствующее значение CMYK получается путем выбора одного из карт, созданных на шаге 4 выше, и инверсии с помощью метода Ньютона для получения КМИ колорант, сопровождающего выбранное значение K.

Шаги 1 и 2, которые являются стандартными процедурами, выполняются программой профилирования, которая не является частью нового CTE-выражения. Цель IT 8,7/3 содержит достаточно детализированную выборку всех значений CMYK на различных уровнях C, M, Y и K. Кроме того, можно использовать пользовательский целевой объект с единообразной выборкой каналов C, M, Y и K. После печати целевого объекта спектрофотометер или колориметер можно использовать для измерения значения XYZ каждого исправления, а значение XYZ можно преобразовать в значение Лув с помощью модели ЦИЕЛУВ.

Шаг 3. Создание прямой схемы из CMYK в Лув может быть достигнуто применением любой известной методики интерполяции, например тетрахедрал или многолинейного метода, в прямоугольной сетке в пространстве CMYK. В новом CTE-выражении используется 4-мерный тетрахедрал интерполяция. Так как сетки выборки КМИ обычно отличаются на каждом уровне K, мы используем метод Super-выборки, как описано ниже. Для заданной точки CMYK сначала определяются южные уровни K, основанные на значении K. Затем введите «супер-Grid» для каждого уровня K, который представляет собой объединение сеток КМИ на каждом из двух уровней K. На каждом уровне K значение Лув любой вновь введенной точки сетки получается трехмерной тетрахедрал интерполяцией на уровне K. Наконец, в этой новой сетке выполняется 4-мерный тетрахедрал интерполяция для определенной точки CMYK.

![Схема, показывающая ресамплинг.](images/cdmp-image163.png)

**Рис. 8** . ресамплинг

На шаге 4 создается набор таблиц подстановки КМИ-Лув (Лутс). Прямая схема, созданная на шаге 3, вызывается многократно для повторной выборки пространства CMYK. Цветовое пространство CMYK выделено с помощью четного интервала в K и другого, но по-прежнему равномерного выделения пространства, выборка КМИ.

Шаг 5 — это процедура получения значения CMYK с помощью Лутс, созданного на шаге 4 для любой входной точки Лув. Чтобы выбрать соответствующее значение K, можно проанализировать освещение, а также степень цвета в запрошенном Лув. После выбора таблицы значения КМИ извлекаются из таблицы с помощью метода Ньютона (как описано в разделе модель устройства принтера RGB выше).

ЦИЕЛУВ пространство используется в модели принтера вместо Циежаб, так как модель устройства должна основываться исключительно на цвете данных, доступной в DMP. В DMP содержатся изображения для каждого измеряемого исправления, включая белую точку мультимедиа, поэтому можно преобразовать ЦИЕКСИЗ данные в данные ЦИЕЛУВ. Однако преобразование в CIECAM02 ЖЧ или Jab невозможно, так как нет доступа к сведениям о условии просмотра в DMP.

### <a name="rgb-projector-device-model-baseline"></a>Базовый план модели устройства с проектором RGB

Примечание. Многие Проекторы RGB имеют более одного режима работы. В одном режиме, который часто используется по умолчанию и может называться нечто вроде «презентация», цветовой ответ проектора оптимизирован для максимальной яркости. Однако в этом режиме проектор теряет возможность воспроизводить освещение, слегка разноцветные цвета, например бледно-желтые и некоторые звуки. В другом режиме, который часто называется «пленка», «видео» или «sRGB», проектор оптимизирован для воспроизведения реалистичных изображений и естественных сцен. В этом режиме для повышения общего качества воспроизведения цвета выдается максимальная яркость. Чтобы получить удовлетворительное воспроизведение цвета с помощью проекторов RGB, необходимо разместить проектор в режиме, где можно воссоздать плавный охват цветов.

![Схема, на которой показана модель устройства D L P.](images/cdmp-image167.png)

**Рис. 9** . модель устройства DLP

Значение входящего значения RGB проходит через два вычислительных пути. Первая — это модель матрицы, результатом которой является значение XYZ. После этого сразу же следует преобразование из XYZ в Лув. Второй является неоднородной LUT интерполяцией с помощью интерполяции тетрахедрал. Выходные данные интерполяции уже находятся в Лув пространстве по конструкции. Для получения прогнозируемого значения Лув добавляются два выхода. В итоге он преобразуется в XYZ, что является ожидаемым выходом модели "+ +" для устройства DLP.

Так как проекторы являются устройствами вывода, они также поддерживают инверсию модели, то есть преобразование из XYZ в RGB. Так как модель устройства преобразует пространство RGB в XYZ-пространство, которое состоит из трех измерений, инверсия эквивалентна решению трех нелинейных уравнений в трех неизвестных. Это можно сделать с помощью стандартных методов решения уравнений, например Ньютона-Рафсона. Однако предпочтительнее сначала преобразовать XYZ в Лув, а затем инвертировать Лув в преобразование RGB, так как Лув пространство больше перцептуалли, чем в пространстве XYZ.

### <a name="icc-device-model-baseline"></a>Базовый план модели устройства ICC

Совместимость рабочих процессов ICC включается путем создания специального профиля модели устройства ICC, в котором хранится объект профиля, и для создания преобразования ICC с помощью профиля No-Op XYZ. Это преобразование затем используется для преобразования цветов устройств и ЦИЕКСИЗ.

![Схема, на которой показано взаимодействие с рабочим процессом c I T E c c.](images/cdmp-image168.png)

**Рис. 10** . Совместимость рабочих процессов ICC

## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные понятия управления цветом](basic-color-management-concepts.md)
</dt> <dt>

[Схемы и алгоритмы цветовой системы Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





