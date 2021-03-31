---
description: Сведения о последовательности исправлений и применимости, возвращаемые функцией Мсиекстрактпатчксмлдата или методом Екстрактпатчксмлдата, представлены в формате большого двоичного объекта XML, который содержит элементы и атрибуты, определенные в этом разделе.
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: Извлечение сведений об исправлениях в формате XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e1e594d3ff2870ca1aaf87245c537045f95d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155526"
---
# <a name="extracting-patch-information-as-xml"></a>Извлечение сведений об исправлениях в формате XML

Сведения о последовательности исправлений и применимости, возвращаемые функцией [**мсиекстрактпатчксмлдата**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) или методом [**екстрактпатчксмлдата**](installer-extractpatchxmldata.md) , представлены в формате большого двоичного объекта XML, который содержит элементы и атрибуты, определенные в этом разделе. Вместо полного файла исправления можно предоставить XML-большой двоичный объект для [**мсидетерминепатчсекуенце**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) и [**мсидетерминеаппликаблепатчес**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) .

-   Элемент Мсипатч является верхним элементом большого двоичного объекта XML и содержит сведения об этом исправлении.

    Атрибут SchemaVersion указывает версию определения схемы. Схема указывается Мсипатчаппликабилити. xsd, а текущая версия схемы — 1.0.0.0. Значение атрибута Патчгуид — это код исправления GUID для пакета обновления, полученного из свойства [**Сводка номера редакции**](revision-number-summary.md) в [информационном потоке сводки](summary-information-stream.md) исправления. Минмсиверсион — это минимальная версия установщик Windows, необходимая для установки исправления, полученного из свойства [**сводки слов**](word-count-summary.md) .

-   Элемент Таржетпродукт является элементом контейнера для получения сведений о приложении, для которого предназначено исправление.

    Можно использовать несколько элементов Таржетпродукт, если исправление можно применить к нескольким приложениям. Сведения в элементе Таржетпродукт извлекаются из преобразований, внедренных в исправление.

-   Элемент Таржетпродукткоде содержит значение свойства [**ProductCode**](productcode.md) целевого приложения до применения исправления.

    Можно использовать несколько элементов Таржетпродукткоде, если исправление можно применить к нескольким приложениям.

-   Элемент Упдатедпродукткоде содержит идентификатор GUID кода продукта целевого приложения после применения исправления.

    Этот элемент имеется только в том случае, если исправление изменяет значение свойства [**ProductCode**](productcode.md) . Исправление, которое изменяет **код продукта** , называется [основным обновлением](major-upgrades.md).

-   Элемент TargetVersion содержит свойство [**ProductVersion**](productversion.md) целевого приложения до применения исправления.
-   Элемент Упдатеверсион содержит значение свойства [**ProductVersion**](productversion.md) целевого приложения после применения исправления.

    Этот элемент имеется только в том случае, если исправление изменяет значение свойства [**ProductVersion**](productversion.md) . Большой двоичный объект XML для исправления, которое реализует [небольшое обновление](small-updates.md), также НАЗЫВАЕМое исправлением QFE, не будет включать этот элемент. Этот элемент будет включен в большой двоичный объект XML для исправления, которое реализует незначительное обновление, также называемое пакетом обновления.

-   Элемент Таржетлангуаже содержит значение свойства [**продуктлангуаже**](productlanguage.md) целевого приложения до применения исправления.
-   Элемент Упдатедлангуажес содержит значение свойства [**продуктлангуаже**](productlanguage.md) после применения исправления.
-   Элемент UpgradeCode содержит значение свойства [**UpgradeCode**](upgradecode.md) целевого приложения.
-   Элемент Обсолетедпатч содержит коды исправлений (GUID) исправлений, которые указаны как устаревшие данным исправлением.

    Список устаревших исправлений вы получили по [**номеру редакции**](revision-number-summary.md) в [информационном потоке сводки](summary-information-stream.md) исправления.

-   Элемент Секуенцедата содержит сведения о последовательности исправлений для исправления.

    В большом двоичном объекте XML может быть несколько элементов Секуенцедата. Каждый элемент Секуенцедата содержит сведения в одной строке [таблицы мсипатчсекуенце](msipatchsequence-table.md) исправления. Элемент Секуенцедата содержит элемент ProductCode, Sequence и Attributes для сведений в соответствующих полях таблицы Мсипатчсекуенце. Описание каждого поля см. в разделе [таблицы мсипатчсекуенце](msipatchsequence-table.md) .

## <a name="extracting-applicability-information"></a>Извлечение сведений о применимости

В следующем примере показано, как извлечь сведения о применимости для исправления установщик Windows (MSP-файл) с помощью [**мсиекстрактпатчксмлдата**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa). Извлеченный большой двоичный объект XML основан на определении схемы в Мсипатчаппликабилити. xsd и возвращается в Сзксмлдата.


```C++
#include <windows.h>
#include <msi.h>

#pragma comment( lib, "msi.lib" )

void main()
{
     TCHAR szPatchPath[] = TEXT("c:\\scratch\\RTM-RTMQFE.msp");
    TCHAR* szXMLData = NULL;
    DWORD cchXMLData = 0;

    UINT uiStatus = ERROR_SUCCESS;

    // Determine size of XML blob buffer.
    if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
         /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
    {
        // cchXMLData now includes size of szXMLData in characters not including terminating NULL
        ++cchXMLData;

        szXMLData = new TCHAR[cchXMLData];
        if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
            /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
        {
            //
            // szXMLData now contains the XML patch applicability blob. This could be
            // provided to MsiDetermineApplicablePatches or MsiDeterminePatchSequence in the
            // proper format to evaluate patch applicability.
            //

        }

        delete [] szXMLData;
        szXMLData = NULL;
    }
}
```



В следующем примере показано, как извлечь сведения о применимости для исправления установщик Windows (MSP-файл) в форме XML. Извлеченный большой двоичный объект XML основан на определении схемы в Мсипатчаппликабилити. xsd и возвращается в Стрпатчксмл.

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a>Определение схемы применимости исправлений

Скопируйте следующий текст в Блокнот или другой текстовый редактор, чтобы создать файл определения схемы для сведений об особенностях применения исправления в большом двоичном объекте XML. Назовите этот файл Мсипатчаппликабилити. XSD.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema id="Applicability" 
    targetNamespace="https://www.microsoft.com/msi/patch_applicability.xsd" 
    elementFormDefault="qualified" 
    xmlns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:mstns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema">
    
    <xs:element name="MsiPatch">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="TargetProduct" minOccurs="1" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="TargetProductCode" type="ValidateGUID" />
                            <xs:element name="UpdatedProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetVersion" type="ValidateVersion" />
                            <xs:element name="UpdatedVersion" type="Version" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetLanguage" type="ValidateLanguage" />
                            <xs:element name="UpdatedLanguages" type="intList" minOccurs="0" maxOccurs="1" />
                            <xs:element name="UpgradeCode" type="ValidateGUID" />
                            <xs:element name="UpdatedUpgradeCode" type="GUID" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                        <xs:attribute name="MinMsiVersion" type="xs:int" />
                    </xs:complexType>
                </xs:element>
                <xs:element name="TargetProductCode" type="GUID" minOccurs="1" maxOccurs="unbounded" />
                <xs:element name="ObsoletedPatch" minOccurs="0" maxOccurs="unbounded" type="GUID" />
                <xs:element name="SequenceData" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="PatchFamily" type="Identifier" />
                            <xs:element name="ProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="Sequence" type="Version" />
                            <xs:element name="Attributes" type="xs:int" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:sequence>
            <xs:attribute name="SchemaVersion" type="Version" />
            <xs:attribute name="PatchGUID" type="GUID" />
            <xs:attribute name="MinMsiVersion" type="xs:int" />
            <xs:attribute name="TargetsRTM" type="xs:boolean" use="optional" />
        </xs:complexType>
    </xs:element>
    <xs:simpleType name="GUID">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{12}\}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:simpleType name="Version">
        <xs:restriction base="xs:string">
            <xs:pattern value="[0-9]{1,5}(\.[0-9]{1,5}){0,3}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:complexType name="ValidateGUID">
        <xs:simpleContent>
            <xs:extension base="GUID">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateVersion">
        <xs:simpleContent>
            <xs:extension base="Version">
                <xs:attribute name="ComparisonType">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="LessThan" />
                            <xs:enumeration value="LessThanOrEqual" />
                            <xs:enumeration value="Equal" />
                            <xs:enumeration value="GreaterThanOrEqual" />
                            <xs:enumeration value="GreaterThan" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="ComparisonFilter">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="Major" />
                            <xs:enumeration value="MajorMinor" />
                            <xs:enumeration value="MajorMinorUpdate" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateLanguage">
        <xs:simpleContent>
            <xs:extension base="xs:int">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:simpleType name="intList">
        <xs:list itemType="xs:int" />
    </xs:simpleType>
    <xs:simpleType name="Identifier">
        <xs:restriction base="xs:string">
            <xs:pattern value="[_a-zA-Z][_a-zA-Z0-9\.]*" />
        </xs:restriction>
    </xs:simpleType>
</xs:schema>
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[**екстрактпатчксмлдата**](installer-extractpatchxmldata.md)
</dt> <dt>

[**мсидетерминепатчсекуенце**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[**мсидетерминеаппликаблепатчес**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[**мсиекстрактпатчксмлдата**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



