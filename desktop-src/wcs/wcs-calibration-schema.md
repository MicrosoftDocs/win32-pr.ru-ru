---
title: Схема калибровки WCS
description: В этом разделе описывается схема калибровки WCS, которая расширяет профиль модели цветового устройства WCS.
ms.assetid: 99f3e9e3-15b7-4bca-87cc-a3bf3b6d0112
keywords:
- Цветовая система Windows (WCS), калибровка
- WCS (цветовая система Windows), калибровка
- Управление цветом изображений, калибровка
- Управление цветом, калибровка
- цвета, калибровка
- схемы, калибровка
- Калибровка WCS
- монитора
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e859ab9d2b47355db063961004f17a8cc1537694
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "105719831"
---
# <a name="wcs-calibration-schema"></a><span data-ttu-id="dc972-111">Схема калибровки WCS</span><span class="sxs-lookup"><span data-stu-id="dc972-111">WCS Calibration Schema</span></span>

<span data-ttu-id="dc972-112">В этом разделе описывается схема калибровки WCS, которая расширяет [профиль модели цветового устройства WCS](wcs-color-device-model-profile-schema-and-algorithms.md).</span><span class="sxs-lookup"><span data-stu-id="dc972-112">This topic describes the WCS Calibration schema that expands the [WCS color device model profile](wcs-color-device-model-profile-schema-and-algorithms.md).</span></span>

## <a name="the-wcs-calibration-schema"></a><span data-ttu-id="dc972-113">Схема калибровки WCS</span><span class="sxs-lookup"><span data-stu-id="dc972-113">The WCS Calibration Schema</span></span>

<span data-ttu-id="dc972-114">Следующее определение схемы используется для указания новых определений Windows 7, которые поддерживают калибровку [профиля модели устройства цветового WCS](wcs-color-device-model-profile-schema-and-algorithms.md) .</span><span class="sxs-lookup"><span data-stu-id="dc972-114">The following schema definition is used to specify the new Windows 7 definitions that support [WCS color device model profile](wcs-color-device-model-profile-schema-and-algorithms.md) calibration.</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<!--
  Copyright (C) Microsoft. All rights reserved. The Windows Color System
  color profile schemas may be used according to the terms of the license agreement
  available at https://www.microsoft.com/whdc/device/display/color/wcs_license.mspx.
  -->
<xs:schema
  xmlns:cal="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2007/11/color/Calibration"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model Calibration profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="AdapterGammaConfiguration">
    <xs:choice>
      <xs:element name="ParameterizedCurves" type="wcs:ParameterizedCurvesType"/>
      <xs:element name="HDRToneResponseCurves" type="wcs:HDRToneResponseCurvesType"/>
    </xs:choice>
  </xs:complexType>

  <xs:complexType name="Calibration">
    <xs:sequence>
      <xs:element name="AdapterGammaConfiguration" type="cal:AdapterGammaConfiguration" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>

</xs:schema>
```



<span data-ttu-id="dc972-115">Для совместимости с Windows Vista Профили, содержащие теги калибровки, должны включать атрибут `mc:Ignoreable="cdm_calibration"` .</span><span class="sxs-lookup"><span data-stu-id="dc972-115">For compatibility with Windows Vista, profiles containing calibration tags should include the attribute `mc:Ignoreable="cdm_calibration"`.</span></span>

 

 




