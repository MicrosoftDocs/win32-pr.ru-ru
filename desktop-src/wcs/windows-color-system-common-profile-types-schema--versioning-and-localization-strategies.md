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
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a>Схема общих типов профилей, цветовой системы Windows, стратегии управления версиями и локализации

-   [Схема 1 общих типов профилей WCS](#wcs-common-profile-types-schema-v1)
-   [Дополнения схемы типов общих профилей WCS v2](#wcs-common-profile-types-schema-v2-additions)
-   [Управление версиями схемы профиля WCS](#wcs-profile-schema-versioning)
-   [Локализация профиля WCS](#wcs-profile-localization)
    -   [Выражать локализуемые элементы](#expressing-localizable-elements)
    -   [Поддержка схемы](#schema-support)
    -   [Выбор языка](#selecting-the-language)
    -   [Встроенные профили](#built-in-profiles)
-   [См. также](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a>Схема 1 общих типов профилей WCS

Ниже приведено определение схемы версии 1.0 для общих типов профилей WCS.


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



Поддерживаются только кодировки UTF-8 или UTF-16. Все остальные кодировки XML настоятельно не рекомендуются для обеспечения оптимального взаимодействия.

## <a name="wcs-common-profile-types-schema-v2-additions"></a>Дополнения схемы типов общих профилей WCS v2

В Windows 7 Схема общих типов профилей WCS была обновлена для включения типов для поддержки [схемы калибровки WCS](wcs-calibration-schema.md).


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



## <a name="wcs-profile-schema-versioning"></a>Управление версиями схемы профиля WCS

В этом приложении термин «потребитель профиля» относится к программному обеспечению WCS или к программному компоненту стороннего производителя, использующему профили WCS.

Более новые версии потребителей профилей могут использовать профили WCS, написанные в соответствии с более старыми версиями схем. Чтобы воспользоваться всеми преимуществами функций, определенных в последней версии схем, обычно требуется последняя версия клиента профиля. Однако старые клиенты профиля могут использовать профили, написанные в соответствии с более новыми версиями схем. Потребитель профиля может игнорировать XML-элементы и атрибуты, которые они не понимают. Результаты будут верными, но производительность или точность могут снизиться по сравнению с результатами, полученными с помощью последней версии клиента профиля.

Ниже приведены рекомендации по использованию версий для потребителей профилей.

-   Данная версия клиента профиля должна распознавать либо все элементы и атрибуты из пространства имен версии, либо ни одно из них.
-   Если пользователь профиля встречает элемент или атрибут из пространства имен, который он не понимает, он должен обрабатывать это как условие ошибки, если только профиль не содержит явных инструкций по обработке резервных.
-   [Открытая спецификация упаковки](https://www.microsoft.com/whdc/xps/xpspkg.mspx) определяет дополнительный URI пространства имен, пространство имен совместимости разметки, которое определяет элементы и атрибуты, обеспечивающие это руководство по обеспечению резервной обработки.
-   Все версии всех потребителей профиля должны распознать и учитывать все элементы и атрибуты в пространстве имен совместимости разметки.
-   Потребители профилей, основанные на новой версии схем профилей, должны поддерживать все ранее определенные пространства имен версий.

В выпуске версии 1.0 WCS распознает элементы и атрибуты из следующих пространств имен:

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

Ниже показан пример совместимости разметки.


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



## <a name="wcs-profile-localization"></a>Локализация профиля WCS

**Требования**

Профили WCS содержат определенные элементы, такие как имя файла и описание, которые содержат понятный для человека текст. Этот текст является локализуемое.

Ниже приведены рекомендации по использованию версий для авторов профилей.

-   Для профилей, созданных сторонними производителями, такими как производители принтеров, Автор профиля должен включать описательный текст на нескольких языках.
-   Следующие элементы должны быть локализуемые: 

    | Элемент     | кдмп | гммп | CAMP |
    |-------------|------|------|------|
    | ProfileName | x    | x    | x    |
    | Описание | x    | x    | x    |
    | Автор      | x    | x    | x    |

    

     

### <a name="expressing-localizable-elements"></a>Выражать локализуемые элементы

Вместо непосредственного текста каждый локализуемый элемент содержит один или несколько вложенных элементов WCS: Text, каждый из которых должен указывать атрибут XML: lang. Как описано в разделе [спецификации xml](http://www.w3.org/TR/REC-xml/) 2,12 ("Идентификация языка"), значение атрибута XML: lang должно быть идентификатором языка IETF RFC 3066, например "en-US", "en" или "FR-FR". В схемах WCS значение атрибута XML: lang не должно быть пустой строкой "", хотя XML разрешает это в общем случае. Пример:


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



Нет двух элементов WCS: текстовые элементы могут иметь один и тот же атрибут XML: lang. Каждая схема профиля WCS должна применять это ограничение отдельно для каждого локализуемого элемента. Поддерживаются только кодировки UTF-8 и UTF-16.

### <a name="schema-support"></a>Поддержка схемы

В проекте используются типы XSD WCS: LocalizedText и WCS: Мултилокализедтипе, определенные в схеме общего типа профиля WCS:


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



Каждая схема профиля WCS объявляет каждый локализуемый элемент типа Мултилокализедтипе, например:


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



Схема КДМП применяет ограничение, которое каждый дочерний элемент WCS: Text элемента CDM: Description должен иметь уникальный атрибут XML: lang. Он обеспечивает то же самое ограничение для других локализуемых элементов. Схемы CAMP и ГММП одинаковы.

### <a name="selecting-the-language"></a>Выбор языка

При принятии решения о том, какая языковая версия локализуемого элемента должна отображаться, код приложения должен выбрать "ближайшую версию" к "текущему языку". То, что означает «ближайшую версию» и «текущий язык», на самом деле зависит от платформы; см. ниже. Если профиль не содержит языковую версию, соответствующую текущему языку, приложение должно выбрать первую версию в профиле (первый дочерний элемент WCS: Text элемента Localizable).

В Windows Vista выбор языка выполняется следующим образом: каждый поток имеет связанный список "предпочтительные языки интерфейса пользователя", который можно получить путем вызова [**жетсреадпреферредуилангуажес**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages). Список возвращается в порядке предпочтения пользователя. Например, в системе, настроенной для английского языка (США), список, возвращенный **жетсреадпреферредуилангуажес** , — это {en-US, EN,}. Это означает: 1) английский (США), если он есть. 2) в противном случае используйте любой региональный вариант английского языка, например "en-GB" или просто "en".

Для каждого языка в списке в порядке перечисления код пользовательского интерфейса ищет элемент WCS: Text, атрибут XML: lang которого является точным совпадением. Используется первая совпадающая версия. Если версия не совпадает, используется первый элемент WCS: Text.

### <a name="built-in-profiles"></a>Встроенные профили

Стандартные профили WCS, поставляемые с Windows Vista, такие как sRGB. КДМП, имеют те же локализуемые свойства, что и другие профили.

Стандартным решением Windows было бы разместить локализованные строки в DLL MUI и ссылаться на них следующим образом:


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



В системе Windows текст описания будет извлечен из ресурса с ИДЕНТИФИКАТОРом 101 в соответствующей локализованной версии ресурсов MUI для mscms.dll. В системах, отличных от Windows, будут использоваться вложенные элементы WCS: Text, как описано выше.

Мы представляем необязательный глобальный уникальный атрибут идентификатора в корневом элементе каждой схемы профиля WCS. Стандартный профиль Вксргб. КДМП может выглядеть следующим образом:


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



Для цветовых профилей WCS, поставляемых с Windows, в палитре цветов отображаются описательные сведения из ресурсов, а не элементы WCS: Text в профилях. Это позволяет Windows отображать локализованные сведения для этих профилей на всех поддерживаемых языках, не требуя от профилей семлселвес содержать описательные сведения на всех языках.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные понятия управления цветом](basic-color-management-concepts.md)
</dt> <dt>

[Схемы и алгоритмы цветовой системы Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 