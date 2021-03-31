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
# <a name="extracting-patch-information-as-xml"></a><span data-ttu-id="752a6-103">Извлечение сведений об исправлениях в формате XML</span><span class="sxs-lookup"><span data-stu-id="752a6-103">Extracting Patch Information as XML</span></span>

<span data-ttu-id="752a6-104">Сведения о последовательности исправлений и применимости, возвращаемые функцией [**мсиекстрактпатчксмлдата**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) или методом [**екстрактпатчксмлдата**](installer-extractpatchxmldata.md) , представлены в формате большого двоичного объекта XML, который содержит элементы и атрибуты, определенные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="752a6-104">The patch sequencing and applicability information that is returned by the [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) function or the [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) method is in the format of an XML blob that contains the elements and attributes that are identified in this topic.</span></span> <span data-ttu-id="752a6-105">Вместо полного файла исправления можно предоставить XML-большой двоичный объект для [**мсидетерминепатчсекуенце**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) и [**мсидетерминеаппликаблепатчес**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) .</span><span class="sxs-lookup"><span data-stu-id="752a6-105">The XML blob can be provided to [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) and [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) instead of the full patch file.</span></span>

-   <span data-ttu-id="752a6-106">Элемент Мсипатч является верхним элементом большого двоичного объекта XML и содержит сведения об этом исправлении.</span><span class="sxs-lookup"><span data-stu-id="752a6-106">The MsiPatch element is the top element of the XML blob, and contains information about the patch.</span></span>

    <span data-ttu-id="752a6-107">Атрибут SchemaVersion указывает версию определения схемы.</span><span class="sxs-lookup"><span data-stu-id="752a6-107">The SchemaVersion attribute specifies the version of the schema definition.</span></span> <span data-ttu-id="752a6-108">Схема указывается Мсипатчаппликабилити. xsd, а текущая версия схемы — 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="752a6-108">The schema is specified by MSIPatchApplicability.xsd and the current schema version is 1.0.0.0.</span></span> <span data-ttu-id="752a6-109">Значение атрибута Патчгуид — это код исправления GUID для пакета обновления, полученного из свойства [**Сводка номера редакции**](revision-number-summary.md) в [информационном потоке сводки](summary-information-stream.md) исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-109">The value of the PatchGUID attribute is the GUID patch code for the patch package obtained from the [**Revision Number Summary**](revision-number-summary.md) Property in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span> <span data-ttu-id="752a6-110">Минмсиверсион — это минимальная версия установщик Windows, необходимая для установки исправления, полученного из свойства [**сводки слов**](word-count-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="752a6-110">The MinMsiVersion is the minimum version of the Windows Installer required to install the patch obtained from the [**Word Count Summary**](word-count-summary.md) Property.</span></span>

-   <span data-ttu-id="752a6-111">Элемент Таржетпродукт является элементом контейнера для получения сведений о приложении, для которого предназначено исправление.</span><span class="sxs-lookup"><span data-stu-id="752a6-111">The TargetProduct element is a container element for information about an application that a patch targets.</span></span>

    <span data-ttu-id="752a6-112">Можно использовать несколько элементов Таржетпродукт, если исправление можно применить к нескольким приложениям.</span><span class="sxs-lookup"><span data-stu-id="752a6-112">There can be multiple TargetProduct elements if the patch can be applied to multiple applications.</span></span> <span data-ttu-id="752a6-113">Сведения в элементе Таржетпродукт извлекаются из преобразований, внедренных в исправление.</span><span class="sxs-lookup"><span data-stu-id="752a6-113">The information in the TargetProduct element is extracted from transforms that are embedded within the patch.</span></span>

-   <span data-ttu-id="752a6-114">Элемент Таржетпродукткоде содержит значение свойства [**ProductCode**](productcode.md) целевого приложения до применения исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-114">The TargetProductCode element contains the value of the [**ProductCode**](productcode.md) property of the target application before the patch has been applied.</span></span>

    <span data-ttu-id="752a6-115">Можно использовать несколько элементов Таржетпродукткоде, если исправление можно применить к нескольким приложениям.</span><span class="sxs-lookup"><span data-stu-id="752a6-115">There can be multiple TargetProductCode elements if the patch can be applied to multiple applications.</span></span>

-   <span data-ttu-id="752a6-116">Элемент Упдатедпродукткоде содержит идентификатор GUID кода продукта целевого приложения после применения исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-116">The UpdatedProductCode element contains the product code GUID of the target application after the patch is applied.</span></span>

    <span data-ttu-id="752a6-117">Этот элемент имеется только в том случае, если исправление изменяет значение свойства [**ProductCode**](productcode.md) .</span><span class="sxs-lookup"><span data-stu-id="752a6-117">This element is only present if the patch changes the value of the [**ProductCode**](productcode.md) property.</span></span> <span data-ttu-id="752a6-118">Исправление, которое изменяет **код продукта** , называется [основным обновлением](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="752a6-118">A patch that changes the **ProductCode** is referred to as a [Major Upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="752a6-119">Элемент TargetVersion содержит свойство [**ProductVersion**](productversion.md) целевого приложения до применения исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-119">The TargetVersion element contains the [**ProductVersion**](productversion.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="752a6-120">Элемент Упдатеверсион содержит значение свойства [**ProductVersion**](productversion.md) целевого приложения после применения исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-120">The UpdateVersion element contains the value of the [**ProductVersion**](productversion.md) property of the target application after the patch is applied.</span></span>

    <span data-ttu-id="752a6-121">Этот элемент имеется только в том случае, если исправление изменяет значение свойства [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="752a6-121">This element is only present if the patch changes the value of the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="752a6-122">Большой двоичный объект XML для исправления, которое реализует [небольшое обновление](small-updates.md), также НАЗЫВАЕМое исправлением QFE, не будет включать этот элемент.</span><span class="sxs-lookup"><span data-stu-id="752a6-122">The XML blob for a patch that implements a [Small Update](small-updates.md), also referred to as a QFE, will not include this element.</span></span> <span data-ttu-id="752a6-123">Этот элемент будет включен в большой двоичный объект XML для исправления, которое реализует незначительное обновление, также называемое пакетом обновления.</span><span class="sxs-lookup"><span data-stu-id="752a6-123">The XML blob for a patch that implements a minor upgrade, also referred to as a service pack, will include this element.</span></span>

-   <span data-ttu-id="752a6-124">Элемент Таржетлангуаже содержит значение свойства [**продуктлангуаже**](productlanguage.md) целевого приложения до применения исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-124">The TargetLanguage element contains the value of the [**ProductLanguage**](productlanguage.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="752a6-125">Элемент Упдатедлангуажес содержит значение свойства [**продуктлангуаже**](productlanguage.md) после применения исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-125">The UpdatedLanguages element contains the value of the [**ProductLanguage**](productlanguage.md) property after the patch has been applied.</span></span>
-   <span data-ttu-id="752a6-126">Элемент UpgradeCode содержит значение свойства [**UpgradeCode**](upgradecode.md) целевого приложения.</span><span class="sxs-lookup"><span data-stu-id="752a6-126">The UpgradeCode element contains the value of the [**UpgradeCode**](upgradecode.md) property of the target application.</span></span>
-   <span data-ttu-id="752a6-127">Элемент Обсолетедпатч содержит коды исправлений (GUID) исправлений, которые указаны как устаревшие данным исправлением.</span><span class="sxs-lookup"><span data-stu-id="752a6-127">The ObsoletedPatch element contains the patch codes (GUIDs) of the patches that are specified as obsolete by this patch.</span></span>

    <span data-ttu-id="752a6-128">Список устаревших исправлений вы получили по [**номеру редакции**](revision-number-summary.md) в [информационном потоке сводки](summary-information-stream.md) исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-128">The list of obsolete patches is obtained from [**Revision Number Summary**](revision-number-summary.md) in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span>

-   <span data-ttu-id="752a6-129">Элемент Секуенцедата содержит сведения о последовательности исправлений для исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-129">The SequenceData element contains patch sequencing information for the patch.</span></span>

    <span data-ttu-id="752a6-130">В большом двоичном объекте XML может быть несколько элементов Секуенцедата.</span><span class="sxs-lookup"><span data-stu-id="752a6-130">There can be multiple SequenceData elements in the XML blob.</span></span> <span data-ttu-id="752a6-131">Каждый элемент Секуенцедата содержит сведения в одной строке [таблицы мсипатчсекуенце](msipatchsequence-table.md) исправления.</span><span class="sxs-lookup"><span data-stu-id="752a6-131">Each SequenceData element contains the information in one row of the [MsiPatchSequence table](msipatchsequence-table.md) of the patch.</span></span> <span data-ttu-id="752a6-132">Элемент Секуенцедата содержит элемент ProductCode, Sequence и Attributes для сведений в соответствующих полях таблицы Мсипатчсекуенце.</span><span class="sxs-lookup"><span data-stu-id="752a6-132">The SequenceData element contains a ProductCode, Sequence, and Attributes subelement for the information in the corresponding fields in the MsiPatchSequence table.</span></span> <span data-ttu-id="752a6-133">Описание каждого поля см. в разделе [таблицы мсипатчсекуенце](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="752a6-133">See the [MsiPatchSequence table](msipatchsequence-table.md) section for a description of each field.</span></span>

## <a name="extracting-applicability-information"></a><span data-ttu-id="752a6-134">Извлечение сведений о применимости</span><span class="sxs-lookup"><span data-stu-id="752a6-134">Extracting Applicability Information</span></span>

<span data-ttu-id="752a6-135">В следующем примере показано, как извлечь сведения о применимости для исправления установщик Windows (MSP-файл) с помощью [**мсиекстрактпатчксмлдата**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="752a6-135">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) using [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span> <span data-ttu-id="752a6-136">Извлеченный большой двоичный объект XML основан на определении схемы в Мсипатчаппликабилити. xsd и возвращается в Сзксмлдата.</span><span class="sxs-lookup"><span data-stu-id="752a6-136">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned to szXMLData.</span></span>


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



<span data-ttu-id="752a6-137">В следующем примере показано, как извлечь сведения о применимости для исправления установщик Windows (MSP-файл) в форме XML.</span><span class="sxs-lookup"><span data-stu-id="752a6-137">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) in XML form.</span></span> <span data-ttu-id="752a6-138">Извлеченный большой двоичный объект XML основан на определении схемы в Мсипатчаппликабилити. xsd и возвращается в Стрпатчксмл.</span><span class="sxs-lookup"><span data-stu-id="752a6-138">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned in strPatchXML.</span></span>

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a><span data-ttu-id="752a6-139">Определение схемы применимости исправлений</span><span class="sxs-lookup"><span data-stu-id="752a6-139">Patch Applicability Schema Definition</span></span>

<span data-ttu-id="752a6-140">Скопируйте следующий текст в Блокнот или другой текстовый редактор, чтобы создать файл определения схемы для сведений об особенностях применения исправления в большом двоичном объекте XML.</span><span class="sxs-lookup"><span data-stu-id="752a6-140">Copy the following text into Notepad or another text editor to create the schema definition file for the patch applicability information in the XML blob.</span></span> <span data-ttu-id="752a6-141">Назовите этот файл Мсипатчаппликабилити. XSD.</span><span class="sxs-lookup"><span data-stu-id="752a6-141">Name this file MSIPatchApplicability.XSD.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="752a6-142">См. также</span><span class="sxs-lookup"><span data-stu-id="752a6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="752a6-143">**екстрактпатчксмлдата**</span><span class="sxs-lookup"><span data-stu-id="752a6-143">**ExtractPatchXMLData**</span></span>](installer-extractpatchxmldata.md)
</dt> <dt>

[<span data-ttu-id="752a6-144">**мсидетерминепатчсекуенце**</span><span class="sxs-lookup"><span data-stu-id="752a6-144">**MsiDeterminePatchSequence**</span></span>](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[<span data-ttu-id="752a6-145">**мсидетерминеаппликаблепатчес**</span><span class="sxs-lookup"><span data-stu-id="752a6-145">**MsiDetermineApplicablePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[<span data-ttu-id="752a6-146">**мсиекстрактпатчксмлдата**</span><span class="sxs-lookup"><span data-stu-id="752a6-146">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



