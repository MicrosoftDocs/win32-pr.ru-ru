---
title: Схема общих типов профилей, цветовой системы Windows, стратегии управления версиями и локализации
description: Схема общих типов профилей, цветовой системы Windows, стратегии управления версиями и локализации
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Цветовая система Windows (WCS), общие типы профилей
- WCS (цветовая система Windows), типы общих профилей
- Управление цветом изображений, общие типы профилей
- Управление цветом, типы общих профилей
- цвета, типы общих профилей
- Цветовая система Windows (WCS), профили
- WCS (цветовая система Windows), профили
- Управление цветом изображений, профили
- Управление цветом, профили
- цвета, профили
- Цветовая система Windows (WCS), управление версиями
- WCS (цветовая система Windows), управление версиями
- Управление цветом изображений, контроль версий
- Управление цветом, контроль версий
- цвета, управление версиями
- Цветовая система Windows (WCS), локализация
- WCS (цветовая система Windows), локализация
- Управление цветом изображений, локализация
- Управление цветом, локализация
- цвета, локализация
- Стандартные типы профилей WCS
- потребители профилей
- Общие типы профилей
- схемы, общие типы профилей
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814b652b654b6416b42a7a3484950273a93ea96
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105720839"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a><span data-ttu-id="417ce-127">Схема общих типов профилей, цветовой системы Windows, стратегии управления версиями и локализации</span><span class="sxs-lookup"><span data-stu-id="417ce-127">Windows Color System Common Profile Types schema, Versioning and Localization Strategies</span></span>

-   [<span data-ttu-id="417ce-128">Схема 1 общих типов профилей WCS</span><span class="sxs-lookup"><span data-stu-id="417ce-128">WCS Common Profile Types Schema V1</span></span>](#wcs-common-profile-types-schema-v1)
-   [<span data-ttu-id="417ce-129">Дополнения схемы типов общих профилей WCS v2</span><span class="sxs-lookup"><span data-stu-id="417ce-129">WCS Common Profile Types Schema V2 Additions</span></span>](#wcs-common-profile-types-schema-v2-additions)
-   [<span data-ttu-id="417ce-130">Управление версиями схемы профиля WCS</span><span class="sxs-lookup"><span data-stu-id="417ce-130">WCS Profile Schema Versioning</span></span>](#wcs-profile-schema-versioning)
-   [<span data-ttu-id="417ce-131">Локализация профиля WCS</span><span class="sxs-lookup"><span data-stu-id="417ce-131">WCS Profile Localization</span></span>](#wcs-profile-localization)
    -   [<span data-ttu-id="417ce-132">Выражать локализуемые элементы</span><span class="sxs-lookup"><span data-stu-id="417ce-132">Expressing localizable elements</span></span>](#expressing-localizable-elements)
    -   [<span data-ttu-id="417ce-133">Поддержка схемы</span><span class="sxs-lookup"><span data-stu-id="417ce-133">Schema Support</span></span>](#schema-support)
    -   [<span data-ttu-id="417ce-134">Выбор языка</span><span class="sxs-lookup"><span data-stu-id="417ce-134">Selecting the Language</span></span>](#selecting-the-language)
    -   [<span data-ttu-id="417ce-135">Встроенные профили</span><span class="sxs-lookup"><span data-stu-id="417ce-135">Built-in profiles</span></span>](#built-in-profiles)
-   [<span data-ttu-id="417ce-136">См. также</span><span class="sxs-lookup"><span data-stu-id="417ce-136">Related topics</span></span>](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a><span data-ttu-id="417ce-137">Схема 1 общих типов профилей WCS</span><span class="sxs-lookup"><span data-stu-id="417ce-137">WCS Common Profile Types Schema V1</span></span>

<span data-ttu-id="417ce-138">Ниже приведено определение схемы версии 1.0 для общих типов профилей WCS.</span><span class="sxs-lookup"><span data-stu-id="417ce-138">The following provides the v1.0 schema definition for the WCS Common Profile Types.</span></span>


```XML
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:import namespace="http://www.w3.org/XML/1998/namespace" />

  <xs:annotation>
    <xs:documentation xml:lang="en">
      Common types used in WCS profile schemas.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:simpleType name="NonNegativeFloatType">
    <xs:restriction base="xs:float">
      <xs:minInclusive value="0"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="NonNegativeCIEXYZType">
    <xs:attribute name="X" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Z" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:simpleType name="GUIDType">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="LocalizedTextType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute ref="xml:lang" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="MultiLocalizedTextType">
    <xs:sequence>
      <xs:element name="Text" type="wcs:LocalizedTextType" minOccurs="1" />
    </xs:sequence>
  </xs:complexType>

</xs:schema>

```



<span data-ttu-id="417ce-139">Поддерживаются только кодировки UTF-8 или UTF-16.</span><span class="sxs-lookup"><span data-stu-id="417ce-139">Only UTF-8 or UTF-16 encodings are supported.</span></span> <span data-ttu-id="417ce-140">Все остальные кодировки XML настоятельно не рекомендуются для обеспечения оптимального взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="417ce-140">All other XML encodings are strongly discouraged in order to preserve optimum interoperability.</span></span>

## <a name="wcs-common-profile-types-schema-v2-additions"></a><span data-ttu-id="417ce-141">Дополнения схемы типов общих профилей WCS v2</span><span class="sxs-lookup"><span data-stu-id="417ce-141">WCS Common Profile Types Schema V2 Additions</span></span>

<span data-ttu-id="417ce-142">В Windows 7 Схема общих типов профилей WCS была обновлена для включения типов для поддержки [схемы калибровки WCS](wcs-calibration-schema.md).</span><span class="sxs-lookup"><span data-stu-id="417ce-142">In Windows 7, the WCS Common Profile Types schema has been updated to include types to support the [WCS Calibration schema](wcs-calibration-schema.md).</span></span>


```XML
  <xs:complexType name="ParameterizedCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="GreenTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="BlueTRC" type="wcs:ParameterizedCurveType"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="ParameterizedCurveType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset1" type="xs:float" use="optional"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset2" type="xs:float " use="optional"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset3" type="xs:float" use="optional"/>
  </xs:complexType>

  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="wcs:FloatList"/>
      <xs:element name="Output" type="wcs:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="wcs:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="2" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
```



## <a name="wcs-profile-schema-versioning"></a><span data-ttu-id="417ce-143">Управление версиями схемы профиля WCS</span><span class="sxs-lookup"><span data-stu-id="417ce-143">WCS Profile Schema Versioning</span></span>

<span data-ttu-id="417ce-144">В этом приложении термин «потребитель профиля» относится к программному обеспечению WCS или к программному компоненту стороннего производителя, использующему профили WCS.</span><span class="sxs-lookup"><span data-stu-id="417ce-144">In this Appendix, the term "profile consumer" refers to the WCS software, or to a third-party software component that consumes WCS profiles.</span></span>

<span data-ttu-id="417ce-145">Более новые версии потребителей профилей могут использовать профили WCS, написанные в соответствии с более старыми версиями схем.</span><span class="sxs-lookup"><span data-stu-id="417ce-145">Newer versions of profile consumers will be able to consume WCS profiles written according to older versions of the schemas.</span></span> <span data-ttu-id="417ce-146">Чтобы воспользоваться всеми преимуществами функций, определенных в последней версии схем, обычно требуется последняя версия клиента профиля.</span><span class="sxs-lookup"><span data-stu-id="417ce-146">To take full advantage of features defined in the newest version of the schemas, the newest version of a profile consumer will generally be required.</span></span> <span data-ttu-id="417ce-147">Однако старые клиенты профиля могут использовать профили, написанные в соответствии с более новыми версиями схем.</span><span class="sxs-lookup"><span data-stu-id="417ce-147">However, older profile consumers can consume profiles written according to newer versions of the schemas.</span></span> <span data-ttu-id="417ce-148">Потребитель профиля может игнорировать XML-элементы и атрибуты, которые они не понимают.</span><span class="sxs-lookup"><span data-stu-id="417ce-148">The profile consumer can ignore XML elements and attributes that it does not understand.</span></span> <span data-ttu-id="417ce-149">Результаты будут верными, но производительность или точность могут снизиться по сравнению с результатами, полученными с помощью последней версии клиента профиля.</span><span class="sxs-lookup"><span data-stu-id="417ce-149">The results will be correct, but performance or fidelity may degraded as compared to the results achieved with the newest version of the profile consumer.</span></span>

<span data-ttu-id="417ce-150">Ниже приведены рекомендации по использованию версий для потребителей профилей.</span><span class="sxs-lookup"><span data-stu-id="417ce-150">The following are versioning guidelines for profile consumers:</span></span>

-   <span data-ttu-id="417ce-151">Данная версия клиента профиля должна распознавать либо все элементы и атрибуты из пространства имен версии, либо ни одно из них.</span><span class="sxs-lookup"><span data-stu-id="417ce-151">A given version of a profile consumer must recognize either all of the elements and attributes from a version namespace, or none of them.</span></span>
-   <span data-ttu-id="417ce-152">Если пользователь профиля встречает элемент или атрибут из пространства имен, который он не понимает, он должен обрабатывать это как условие ошибки, если только профиль не содержит явных инструкций по обработке резервных.</span><span class="sxs-lookup"><span data-stu-id="417ce-152">If a profile consumer encounters an element or attribute from a namespace that it does not understand, it must treat this as an error condition, unless the profile contains explicit guidance on fallback processing.</span></span>
-   <span data-ttu-id="417ce-153">[Открытая спецификация упаковки](https://www.microsoft.com/whdc/xps/xpspkg.mspx) определяет дополнительный URI пространства имен, пространство имен совместимости разметки, которое определяет элементы и атрибуты, обеспечивающие это руководство по обеспечению резервной обработки.</span><span class="sxs-lookup"><span data-stu-id="417ce-153">The [Open Packaging Specification](https://www.microsoft.com/whdc/xps/xpspkg.mspx) defines an additional namespace URI, the markup compatibility namespace, which defines elements and attributes that provide this fallback processing guidance.</span></span>
-   <span data-ttu-id="417ce-154">Все версии всех потребителей профиля должны распознать и учитывать все элементы и атрибуты в пространстве имен совместимости разметки.</span><span class="sxs-lookup"><span data-stu-id="417ce-154">All versions of all profile consumers must recognize and respect all the elements and attributes in the markup compatibility namespace.</span></span>
-   <span data-ttu-id="417ce-155">Потребители профилей, основанные на новой версии схем профилей, должны поддерживать все ранее определенные пространства имен версий.</span><span class="sxs-lookup"><span data-stu-id="417ce-155">Profile consumers based on a new version of the profile schemas must support all previously defined version namespaces.</span></span>

<span data-ttu-id="417ce-156">В выпуске версии 1.0 WCS распознает элементы и атрибуты из следующих пространств имен:</span><span class="sxs-lookup"><span data-stu-id="417ce-156">In the v1.0 release, WCS recognizes elements and attributes from the following namespaces:</span></span>

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

<span data-ttu-id="417ce-157">Ниже показан пример совместимости разметки.</span><span class="sxs-lookup"><span data-stu-id="417ce-157">The following demonstrates an example of markup compatibility.</span></span>


```XML
<?xml version="1.0" encoding="utf-8" ?>
<ColorAppearanceModel
  xmlns=http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
  xmlns:cam2=http://schemas.microsoft.com/windows/2007/08/color/ColorAppearanceModel
  xmlns:mc=http://schemas.microsoft.com/winfx/2005/02/markup-compatibility
  xs:schemaLocation="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel ColorAppearanceModel.xsd"
  xmlns:xs='http://www.w3.org/2001/XMLSchema-instance'
  mc:Ignorable="cam2">

  <ProfileName>Default profile for ICC viewing conditions</ProfileName>
  <mc:AlternateContent>
    <mc:Choice Requires="cam2">
      <cam2:AudioDescription source="ProfileExplanation.wav"/>
    </mc:Choice>
    <mc:Fallback>
      <Description>Appropriate for a print in a D50 viewing booth</Description>
        </mc:Fallback>
  </mc:AlternateContent>
  <Author>Microsoft</Author>

  <ViewingConditions>
    <WhitePointName>D50</WhitePointName>
    <Background X="19.3" Y="20.0" Z="16.5" />
    <Surround>Average</Surround>
    <LuminanceOfAdaptingField>31.8</LuminanceOfAdaptingField>
    <DegreeOfAdaptation>-1</DegreeOfAdaptation>
    <cam2:Humidity>30%</cam2:Humidity>
  </ViewingConditions>

</ColorAppearanceModel>
```



## <a name="wcs-profile-localization"></a><span data-ttu-id="417ce-158">Локализация профиля WCS</span><span class="sxs-lookup"><span data-stu-id="417ce-158">WCS Profile Localization</span></span>

<span data-ttu-id="417ce-159">**Требования**</span><span class="sxs-lookup"><span data-stu-id="417ce-159">**Requirements**</span></span>

<span data-ttu-id="417ce-160">Профили WCS содержат определенные элементы, такие как имя файла и описание, которые содержат понятный для человека текст.</span><span class="sxs-lookup"><span data-stu-id="417ce-160">WCS profiles contain certain elements such as ProfileName and Description which contain human-readable text.</span></span> <span data-ttu-id="417ce-161">Этот текст является локализуемое.</span><span class="sxs-lookup"><span data-stu-id="417ce-161">This text is localizable.</span></span>

<span data-ttu-id="417ce-162">Ниже приведены рекомендации по использованию версий для авторов профилей.</span><span class="sxs-lookup"><span data-stu-id="417ce-162">The following are versioning guidelines for profile creators:</span></span>

-   <span data-ttu-id="417ce-163">Для профилей, созданных сторонними производителями, такими как производители принтеров, Автор профиля должен включать описательный текст на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="417ce-163">For profiles created by 3rd parties such as printer manufacturers, the profile author should incorporate descriptive text in multiple languages.</span></span>
-   <span data-ttu-id="417ce-164">Следующие элементы должны быть локализуемые:</span><span class="sxs-lookup"><span data-stu-id="417ce-164">The following elements should be localizable:</span></span> 

    | <span data-ttu-id="417ce-165">Элемент</span><span class="sxs-lookup"><span data-stu-id="417ce-165">Element</span></span>     | <span data-ttu-id="417ce-166">кдмп</span><span class="sxs-lookup"><span data-stu-id="417ce-166">CDMP</span></span> | <span data-ttu-id="417ce-167">гммп</span><span class="sxs-lookup"><span data-stu-id="417ce-167">GMMP</span></span> | <span data-ttu-id="417ce-168">CAMP</span><span class="sxs-lookup"><span data-stu-id="417ce-168">CAMP</span></span> |
    |-------------|------|------|------|
    | <span data-ttu-id="417ce-169">ProfileName</span><span class="sxs-lookup"><span data-stu-id="417ce-169">ProfileName</span></span> | <span data-ttu-id="417ce-170">x</span><span class="sxs-lookup"><span data-stu-id="417ce-170">x</span></span>    | <span data-ttu-id="417ce-171">x</span><span class="sxs-lookup"><span data-stu-id="417ce-171">x</span></span>    | <span data-ttu-id="417ce-172">x</span><span class="sxs-lookup"><span data-stu-id="417ce-172">x</span></span>    |
    | <span data-ttu-id="417ce-173">Описание</span><span class="sxs-lookup"><span data-stu-id="417ce-173">Description</span></span> | <span data-ttu-id="417ce-174">x</span><span class="sxs-lookup"><span data-stu-id="417ce-174">x</span></span>    | <span data-ttu-id="417ce-175">x</span><span class="sxs-lookup"><span data-stu-id="417ce-175">x</span></span>    | <span data-ttu-id="417ce-176">x</span><span class="sxs-lookup"><span data-stu-id="417ce-176">x</span></span>    |
    | <span data-ttu-id="417ce-177">Автор</span><span class="sxs-lookup"><span data-stu-id="417ce-177">Author</span></span>      | <span data-ttu-id="417ce-178">x</span><span class="sxs-lookup"><span data-stu-id="417ce-178">x</span></span>    | <span data-ttu-id="417ce-179">x</span><span class="sxs-lookup"><span data-stu-id="417ce-179">x</span></span>    | <span data-ttu-id="417ce-180">x</span><span class="sxs-lookup"><span data-stu-id="417ce-180">x</span></span>    |

    

     

### <a name="expressing-localizable-elements"></a><span data-ttu-id="417ce-181">Выражать локализуемые элементы</span><span class="sxs-lookup"><span data-stu-id="417ce-181">Expressing localizable elements</span></span>

<span data-ttu-id="417ce-182">Вместо непосредственного текста каждый локализуемый элемент содержит один или несколько вложенных элементов WCS: Text, каждый из которых должен указывать атрибут XML: lang.</span><span class="sxs-lookup"><span data-stu-id="417ce-182">Instead of directly containing text, each localizable element contains one or more wcs:Text sub-elements, each of which must specify the xml:lang attribute.</span></span> <span data-ttu-id="417ce-183">Как описано в разделе [спецификации xml](http://www.w3.org/TR/REC-xml/) 2,12 ("Идентификация языка"), значение атрибута XML: lang должно быть идентификатором языка IETF RFC 3066, например "en-US", "en" или "FR-FR".</span><span class="sxs-lookup"><span data-stu-id="417ce-183">As described in the [XML specification](http://www.w3.org/TR/REC-xml/) Section 2.12 ("Language Identification"), the value of the xml:lang attribute must be an IETF RFC 3066 language identifier such as "en-US", "en", or "fr-FR".</span></span> <span data-ttu-id="417ce-184">В схемах WCS значение атрибута XML: lang не должно быть пустой строкой "", хотя XML разрешает это в общем случае.</span><span class="sxs-lookup"><span data-stu-id="417ce-184">In WCS schemas, the value of the xml:lang attribute must not be the empty string "", even though XML allows this in the general case.</span></span> <span data-ttu-id="417ce-185">Пример:</span><span class="sxs-lookup"><span data-stu-id="417ce-185">For example:</span></span>


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



<span data-ttu-id="417ce-186">Нет двух элементов WCS: текстовые элементы могут иметь один и тот же атрибут XML: lang.</span><span class="sxs-lookup"><span data-stu-id="417ce-186">No two wcs:Text elements can have the same xml:lang attribute.</span></span> <span data-ttu-id="417ce-187">Каждая схема профиля WCS должна применять это ограничение отдельно для каждого локализуемого элемента.</span><span class="sxs-lookup"><span data-stu-id="417ce-187">Each WCS profile schema must enforce this constraint separately for each localizable element.</span></span> <span data-ttu-id="417ce-188">Поддерживаются только кодировки UTF-8 и UTF-16.</span><span class="sxs-lookup"><span data-stu-id="417ce-188">Only UTF-8 and UTF-16 encodings are supported.</span></span>

### <a name="schema-support"></a><span data-ttu-id="417ce-189">Поддержка схемы</span><span class="sxs-lookup"><span data-stu-id="417ce-189">Schema Support</span></span>

<span data-ttu-id="417ce-190">В проекте используются типы XSD WCS: LocalizedText и WCS: Мултилокализедтипе, определенные в схеме общего типа профиля WCS:</span><span class="sxs-lookup"><span data-stu-id="417ce-190">The design makes use of the XSD types wcs:LocalizedText and wcs:MultiLocalizedType defined in the WCS Common Profile Type schema:</span></span>


```XML
    <xs:complexType name="LocalizedText">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="xml:lang" type="xs:string" use="required"/>
            <xs:extension/>
        <xs:simpleContent/>
    </xs:complexType/>

    <xs:complexType name="MultiLocalizedType">
        <xs:element name="Text" type="cam:LocalizedText" minOccurs="1"/>
    </xs:complexType>
```



<span data-ttu-id="417ce-191">Каждая схема профиля WCS объявляет каждый локализуемый элемент типа Мултилокализедтипе, например:</span><span class="sxs-lookup"><span data-stu-id="417ce-191">Each WCS profile schema declares each localizable element to be of type MultiLocalizedType, for example:</span></span>


```XML
<xs:schema 
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
    targetNamespace=
        "http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    version="1.0">
    <xs:import namespace=
        "http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"/>

    <xs:element name="cdm:Description" type="wcs:MultiLocalizableType" minOccurs="0"/>

    <xs:unique name="uniqueDescriptionLanguage">
      <xs:selector xpath="cdm:ColorDeviceModel/cdm:Description/wcs:Text"/>
      <xs:field xpath="@xml:lang"/>
    </unique>

    ...
</xs:schema>
```



<span data-ttu-id="417ce-192">Схема КДМП применяет ограничение, которое каждый дочерний элемент WCS: Text элемента CDM: Description должен иметь уникальный атрибут XML: lang.</span><span class="sxs-lookup"><span data-stu-id="417ce-192">The CDMP schema enforces the constraint that each wcs:Text child of the cdm:Description element must have a unique xml:lang attribute.</span></span> <span data-ttu-id="417ce-193">Он обеспечивает то же самое ограничение для других локализуемых элементов.</span><span class="sxs-lookup"><span data-stu-id="417ce-193">It enforces the same constraint for the other localizable elements.</span></span> <span data-ttu-id="417ce-194">Схемы CAMP и ГММП одинаковы.</span><span class="sxs-lookup"><span data-stu-id="417ce-194">The CAMP and GMMP schemas do the same.</span></span>

### <a name="selecting-the-language"></a><span data-ttu-id="417ce-195">Выбор языка</span><span class="sxs-lookup"><span data-stu-id="417ce-195">Selecting the Language</span></span>

<span data-ttu-id="417ce-196">При принятии решения о том, какая языковая версия локализуемого элемента должна отображаться, код приложения должен выбрать "ближайшую версию" к "текущему языку".</span><span class="sxs-lookup"><span data-stu-id="417ce-196">When deciding which language version of a localizable element to display, application code should select the "closest version" to the "current language".</span></span> <span data-ttu-id="417ce-197">То, что означает «ближайшую версию» и «текущий язык», на самом деле зависит от платформы; см. ниже.</span><span class="sxs-lookup"><span data-stu-id="417ce-197">What "closest version" and "current language" actually mean is platform-dependent; see below.</span></span> <span data-ttu-id="417ce-198">Если профиль не содержит языковую версию, соответствующую текущему языку, приложение должно выбрать первую версию в профиле (первый дочерний элемент WCS: Text элемента Localizable).</span><span class="sxs-lookup"><span data-stu-id="417ce-198">If the profile does not contain a language version that matches the current language, the application should select the first version in the profile (the first wcs:Text child element of the localizable element).</span></span>

<span data-ttu-id="417ce-199">В Windows Vista выбор языка выполняется следующим образом: каждый поток имеет связанный список "предпочтительные языки интерфейса пользователя", который можно получить путем вызова [**жетсреадпреферредуилангуажес**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="417ce-199">On Windows Vista, the language selection is done as follows: Each thread has an associated list of "preferred UI languages", which can be obtained by calling [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span></span> <span data-ttu-id="417ce-200">Список возвращается в порядке предпочтения пользователя.</span><span class="sxs-lookup"><span data-stu-id="417ce-200">The list is returned in order of user preference.</span></span> <span data-ttu-id="417ce-201">Например, в системе, настроенной для английского языка (США), список, возвращенный **жетсреадпреферредуилангуажес** , — это {en-US, EN,}.</span><span class="sxs-lookup"><span data-stu-id="417ce-201">For instance, on a system set up for US English, the list returned by **GetThreadPreferredUILanguages** is { "en-US", "en" }.</span></span> <span data-ttu-id="417ce-202">Это означает: 1) английский (США), если он есть.</span><span class="sxs-lookup"><span data-stu-id="417ce-202">This means: 1) US English if present.</span></span> <span data-ttu-id="417ce-203">2) в противном случае используйте любой региональный вариант английского языка, например "en-GB" или просто "en".</span><span class="sxs-lookup"><span data-stu-id="417ce-203">2) Otherwise, use any regional variant of English, such as "en-GB" or just plain "en".</span></span>

<span data-ttu-id="417ce-204">Для каждого языка в списке в порядке перечисления код пользовательского интерфейса ищет элемент WCS: Text, атрибут XML: lang которого является точным совпадением.</span><span class="sxs-lookup"><span data-stu-id="417ce-204">For each language in that list, in list order, the UI code looks for a wcs:Text element whose xml:lang attribute is an exact match.</span></span> <span data-ttu-id="417ce-205">Используется первая совпадающая версия.</span><span class="sxs-lookup"><span data-stu-id="417ce-205">The first matching version is used.</span></span> <span data-ttu-id="417ce-206">Если версия не совпадает, используется первый элемент WCS: Text.</span><span class="sxs-lookup"><span data-stu-id="417ce-206">If no version matches, the first wcs:Text element is used.</span></span>

### <a name="built-in-profiles"></a><span data-ttu-id="417ce-207">Встроенные профили</span><span class="sxs-lookup"><span data-stu-id="417ce-207">Built-in profiles</span></span>

<span data-ttu-id="417ce-208">Стандартные профили WCS, поставляемые с Windows Vista, такие как sRGB. КДМП, имеют те же локализуемые свойства, что и другие профили.</span><span class="sxs-lookup"><span data-stu-id="417ce-208">The standard WCS profiles shipped with Windows Vista, such as sRGB.cdmp, have the same localizable properties as other profiles.</span></span>

<span data-ttu-id="417ce-209">Стандартным решением Windows было бы разместить локализованные строки в DLL MUI и ссылаться на них следующим образом:</span><span class="sxs-lookup"><span data-stu-id="417ce-209">The standard Windows solution would be to put the localized strings in a MUI DLL, and refer to them like this:</span></span>


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



<span data-ttu-id="417ce-210">В системе Windows текст описания будет извлечен из ресурса с ИДЕНТИФИКАТОРом 101 в соответствующей локализованной версии ресурсов MUI для mscms.dll.</span><span class="sxs-lookup"><span data-stu-id="417ce-210">On a Windows system, the description text would be extracted from resource ID 101 in the appropriate localized version of the MUI resources for mscms.dll.</span></span> <span data-ttu-id="417ce-211">В системах, отличных от Windows, будут использоваться вложенные элементы WCS: Text, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="417ce-211">Non-Windows systems would use the wcs:Text sub-elements as described above.</span></span>

<span data-ttu-id="417ce-212">Мы представляем необязательный глобальный уникальный атрибут идентификатора в корневом элементе каждой схемы профиля WCS.</span><span class="sxs-lookup"><span data-stu-id="417ce-212">We introduce an optional, globally unique ID attribute on the root element of each WCS profile schema.</span></span> <span data-ttu-id="417ce-213">Стандартный профиль Вксргб. КДМП может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="417ce-213">The standard profile wcsRGB.cdmp might look like this:</span></span>


```XML
<cdm:ColorDeviceModel
    ID=http://schemas.microsoft.com/2005/02/color/profiles/wcsRGB.cdmp
    ... >
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello.</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour.</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceModel>
```



<span data-ttu-id="417ce-214">Для цветовых профилей WCS, поставляемых с Windows, в палитре цветов отображаются описательные сведения из ресурсов, а не элементы WCS: Text в профилях.</span><span class="sxs-lookup"><span data-stu-id="417ce-214">For the WCS color profiles shipped with windows, the Color CPL displays descriptive information from the resources, rather than from the wcs:Text elements in the profiles.</span></span> <span data-ttu-id="417ce-215">Это позволяет Windows отображать локализованные сведения для этих профилей на всех поддерживаемых языках, не требуя от профилей семлселвес содержать описательные сведения на всех языках.</span><span class="sxs-lookup"><span data-stu-id="417ce-215">This allows Windows to display localized information for these profiles in all supported languages, without requiring the profiles themlselves to contain descriptive information in all languages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="417ce-216">См. также</span><span class="sxs-lookup"><span data-stu-id="417ce-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="417ce-217">Основные понятия управления цветом</span><span class="sxs-lookup"><span data-stu-id="417ce-217">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="417ce-218">Схемы и алгоритмы цветовой системы Windows</span><span class="sxs-lookup"><span data-stu-id="417ce-218">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 