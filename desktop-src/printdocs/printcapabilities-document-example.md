---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 86577c09-919b-4f07-9388-47879c656f32
title: Пример документа PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032958221f531186c5c6ec993102e574aefc315
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105656743"
---
# <a name="printcapabilities-document-example"></a><span data-ttu-id="35572-104">Пример документа PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="35572-104">PrintCapabilities Document Example</span></span>

<span data-ttu-id="35572-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="35572-105">This topic is not current.</span></span> <span data-ttu-id="35572-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="35572-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="35572-107">Примечания. пространство имен по умолчанию не применяется к XML-атрибутам.</span><span class="sxs-lookup"><span data-stu-id="35572-107">Notes: The default namespace does not apply to XML Attributes.</span></span> <span data-ttu-id="35572-108">Они должны быть явно уточнены префиксом.</span><span class="sxs-lookup"><span data-stu-id="35572-108">They must be explicitly prefix-qualified.</span></span> <span data-ttu-id="35572-109">Имена экземпляров, используемые в следующем примере, предназначены только для иллюстрации, хотя обычно соответствуют именам экземпляров, определенным в ключевых словах «Печать схемы».</span><span class="sxs-lookup"><span data-stu-id="35572-109">Instance names used in the following sample are for illustration only, although they generally conform to the instance names defined in the Print Schema Keywords.</span></span>

``` syntax
<psf:PrintCapabilities xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
                  xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" 
                  xmlns:xsd="https://www.w3.org/2001/XMLSchema" version="1" 
                  xmlns:ns0000="http://schemas.microsoft.com/windows/printing/oemdriverpt/ES_LNseries_PowerPrinter" 
                  xmlns:psk="https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords">
    <psf:ParameterDef name="ns0000:PageDevmodeSnapshot">
        <psf:Property name="psf:DataType">
            <psf:Value xsi:type="xsd:QName">xsd:string</psf:Value>
        </psf:Property>
        <psf:Property name="psf:UnitType">
            <psf:Value xsi:type="xsd:string">base64</psf:Value>
        </psf:Property>
        <psf:Property name="psf:DefaultValue">
            <psf:Value xsi:type="xsd:string">SABQACAARABlAHMDFDFJASKJFDUETgEAAAA=</psf:Value>
        </psf:Property>
        <psf:Property name="psf:Mandatory">
            <psf:Value xsi:type="xsd:QName">psk:Optional</psf:Value>
        </psf:Property>
        <psf:Property name="psf:MinLength">
            <psf:Value xsi:type="xsd:integer">0</psf:Value>
        </psf:Property>
        <psf:Property name="psf:MaxLength">
            <psf:Value xsi:type="xsd:integer">174760</psf:Value>
        </psf:Property>
    </psf:ParameterDef>
    <psf:Feature name="psk:PageICMRenderingIntent">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Default Image Color Matching Intent</psf:Value>
        </psf:Property>
        <psf:Option name="psk:AbsoluteColorimetric" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Match</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:RelativeColorimetric" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Proof</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:Photographs" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Pictures</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:BusinessGraphics" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Graphics</psf:Value>
            </psf:Property>
        </psf:Option>
    </psf:Feature>
    <psf:Feature name="psk:PageColorManagement">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Image Color Matching (ICM) Option</psf:Value>
        </psf:Property>
        <psf:Option name="psk:None" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">ICM Disabled</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:System" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">ICM Handled by Host System</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:Driver" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">ICM Handled by Printer</psf:Value>
            </psf:Property>
        </psf:Option>
    </psf:Feature>
    <psf:Feature name="psk:DocumentCollate">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Collate Copies</psf:Value>
        </psf:Property>
        <psf:Option name="psk:Collated" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Yes</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:Uncollated" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">No</psf:Value>
            </psf:Property>
        </psf:Option>
    </psf:Feature>
    <psf:ParameterDef name="psk:JobCopiesAllDocuments">
        <psf:Property name="psf:DataType">
            <psf:Value xsi:type="xsd:QName">xsd:integer</psf:Value>
        </psf:Property>
        <psf:Property name="psf:UnitType">
            <psf:Value xsi:type="xsd:string">copies</psf:Value>
        </psf:Property>
        <psf:Property name="psf:Multiple">
            <psf:Value xsi:type="xsd:integer">1</psf:Value>
        </psf:Property>
        <psf:Property name="psf:MaxValue">
            <psf:Value xsi:type="xsd:integer">9999</psf:Value>
        </psf:Property>
        <psf:Property name="psf:MinValue">
            <psf:Value xsi:type="xsd:integer">1</psf:Value>
        </psf:Property>
        <psf:Property name="psf:DefaultValue">
            <psf:Value xsi:type="xsd:integer">1</psf:Value>
        </psf:Property>
        <psf:Property name="psf:Mandatory">
            <psf:Value xsi:type="xsd:QName">psk:Unconditional</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Copy Count</psf:Value>
        </psf:Property>
    </psf:ParameterDef>
    <psf:Feature name="psk:JobNUpAllDocumentsContiguously">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Pages per Sheet</psf:Value>
        </psf:Property>
        <psf:Option constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">1</psf:Value>
            </psf:Property>
            <psf:ScoredProperty name="psk:PagesPerSheet">
                <psf:Value xsi:type="xsd:integer">1</psf:Value>
            </psf:ScoredProperty>
            <psf:Property name="psf:IdentityOption">
                <psf:Value xsi:type="xsd:string">True</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">2</psf:Value>
            </psf:Property>
            <psf:ScoredProperty name="psk:PagesPerSheet">
                <psf:Value xsi:type="xsd:integer">2</psf:Value>
            </psf:ScoredProperty>
        </psf:Option>
        <psf:Option constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">4</psf:Value>
            </psf:Property>
            <psf:ScoredProperty name="psk:PagesPerSheet">
                <psf:Value xsi:type="xsd:integer">4</psf:Value>
            </psf:ScoredProperty>
        </psf:Option>
        <psf:Option constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">6</psf:Value>
            </psf:Property>
            <psf:ScoredProperty name="psk:PagesPerSheet">
                <psf:Value xsi:type="xsd:integer">6</psf:Value>
            </psf:ScoredProperty>
        </psf:Option>
        <psf:Option constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">9</psf:Value>
            </psf:Property>
            <psf:ScoredProperty name="psk:PagesPerSheet">
                <psf:Value xsi:type="xsd:integer">9</psf:Value>
            </psf:ScoredProperty>
        </psf:Option>
        <psf:Option constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">16</psf:Value>
            </psf:Property>
            <psf:ScoredProperty name="psk:PagesPerSheet">
                <psf:Value xsi:type="xsd:integer">16</psf:Value>
            </psf:ScoredProperty>
        </psf:Option>
        <psf:Feature name="psk:PresentationDirection">
            <psf:Property name="psf:SelectionType">
                <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
            </psf:Property>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Pages per Sheet Layout</psf:Value>
            </psf:Property>
            <psf:Option name="psk:RightBottom" constrained="psk:None">
                <psf:Property name="psk:DisplayName">
                    <psf:Value xsi:type="xsd:string">Right then Down</psf:Value>
                </psf:Property>
            </psf:Option>
            <psf:Option name="psk:BottomRight" constrained="psk:None">
                <psf:Property name="psk:DisplayName">
                    <psf:Value xsi:type="xsd:string">Down then Right</psf:Value>
                </psf:Property>
            </psf:Option>
            <psf:Option name="psk:LeftBottom" constrained="psk:None">
                <psf:Property name="psk:DisplayName">
                    <psf:Value xsi:type="xsd:string">Left then Down</psf:Value>
                </psf:Property>
            </psf:Option>
            <psf:Option name="psk:BottomLeft" constrained="psk:None">
                <psf:Property name="psk:DisplayName">
                    <psf:Value xsi:type="xsd:string">Down then Left</psf:Value>
                </psf:Property>
            </psf:Option>
        </psf:Feature>
        <psf:Feature name="ns0000:Borders">
            <psf:Property name="psf:SelectionType">
                <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
            </psf:Property>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Border Drawing</psf:Value>
            </psf:Property>
            <psf:Option name="ns0000:Off" constrained="psk:None">
                <psf:Property name="psk:DisplayName">
                    <psf:Value xsi:type="xsd:string">No/OFF</psf:Value>
                </psf:Property>
            </psf:Option>
            <psf:Option name="ns0000:On" constrained="psk:None">
                <psf:Property name="psk:DisplayName">
                    <psf:Value xsi:type="xsd:string">Yes/ON</psf:Value>
                </psf:Property>
            </psf:Option>
        </psf:Feature>
    </psf:Feature>
    <psf:Feature name="psk:PageMediaSize">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Paper Size</psf:Value>
        </psf:Property>
        <psf:Option name="psk:NorthAmericaLetter" constrained="psk:None">
            <psf:ScoredProperty name="psk:MediaSizeWidth">
                <psf:Value xsi:type="xsd:integer">215900</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:MediaSizeHeight">
                <psf:Value xsi:type="xsd:integer">279400</psf:Value>
            </psf:ScoredProperty>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Letter</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:CustomMediaSize" constrained="psk:None">
            <psf:ScoredProperty name="psk:MediaSizeWidth">
                <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:MediaSizeHeight">
                <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
            </psf:ScoredProperty>
        </psf:Option>
    </psf:Feature>
    <psf:ParameterDef name="psk:PageMediaSizeMediaSizeWidth">
        <psf:Property name="psf:DataType">
            <psf:Value xsi:type="xsd:QName">xsd:integer</psf:Value>
        </psf:Property>
        <psf:Property name="psf:UnitType">
            <psf:Value xsi:type="xsd:string">microns</psf:Value>
        </psf:Property>
        <psf:Property name="psf:Multiple">
            <psf:Value xsi:type="xsd:integer">1</psf:Value>
        </psf:Property>
        <psf:Property name="psf:MaxValue">
            <psf:Value xsi:type="xsd:integer">203200</psf:Value>
        </psf:Property>
        <psf:Property name="psf:MinValue">
            <psf:Value xsi:type="xsd:integer">87291</psf:Value>
        </psf:Property>
        <psf:Property name="psf:DefaultValue">
            <psf:Value xsi:type="xsd:integer">87291</psf:Value>
        </psf:Property>
        <psf:Property name="psf:Mandatory">
            <psf:Value xsi:type="xsd:QName">psk:Optional</psf:Value>
        </psf:Property>
    </psf:ParameterDef>
    <psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
        <psf:Property name="psf:DataType">
            <psf:Value xsi:type="xsd:QName">xsd:integer</psf:Value>
        </psf:Property>
        <psf:Property name="psf:UnitType">
            <psf:Value xsi:type="xsd:string">microns</psf:Value>
        </psf:Property>
        <psf:Property name="psf:Multiple">
            <psf:Value xsi:type="xsd:integer">1</psf:Value>
        </psf:Property>
        <psf:Property name="psf:MaxValue">
            <psf:Value xsi:type="xsd:integer">342138</psf:Value>
        </psf:Property>
        <psf:Property name="psf:MinValue">
            <psf:Value xsi:type="xsd:integer">134535</psf:Value>
        </psf:Property>
        <psf:Property name="psf:DefaultValue">
            <psf:Value xsi:type="xsd:integer">134535</psf:Value>
        </psf:Property>
        <psf:Property name="psf:Mandatory">
            <psf:Value xsi:type="xsd:QName">psk:Optional</psf:Value>
        </psf:Property>
    </psf:ParameterDef>
    <psf:Feature name="psk:JobInputBin">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Paper Source</psf:Value>
        </psf:Property>
        <psf:Option name="psk:AutoSelect" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Automatically Select</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="ns0000:ESLDProBin" constrained="psk:None">
            <psf:ScoredProperty name="psk:BinType">
                <psf:Value xsi:type="xsd:QName">psk:Manual</psf:Value>
            </psf:ScoredProperty>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Manual Feed</psf:Value>
            </psf:Property>
        </psf:Option>
    </psf:Feature>
    <psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Two-sided Printing</psf:Value>
        </psf:Property>
        <psf:Option name="psk:OneSided" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">None</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:TwoSidedLongEdge" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Flip on long edge</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:TwoSidedShortEdge" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Flip on short edge</psf:Value>
            </psf:Property>
        </psf:Option>
    </psf:Feature>
    <psf:Feature name="psk:PageOrientation">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Orientation</psf:Value>
        </psf:Property>
        <psf:Option name="psk:Portrait" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Portrait</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:Landscape" constrained="psk:None">
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Landscape</psf:Value>
            </psf:Property>
        </psf:Option>
    </psf:Feature>
    <psf:Feature name="psk:PageResolution">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Resolution</psf:Value>
        </psf:Property>
        <psf:Option name="ns0000:ESLD300x300" constrained="psk:None">
            <psf:ScoredProperty name="psk:ResolutionX">
                <psf:Value xsi:type="xsd:integer">300</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:ResolutionY">
                <psf:Value xsi:type="xsd:integer">300</psf:Value>
            </psf:ScoredProperty>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">300 x 300 dots per inch</psf:Value>
            </psf:Property>
        </psf:Option>
    </psf:Feature>
    <psf:Feature name="psk:PageMediaType">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Media Type</psf:Value>
        </psf:Property>
        <psf:Option name="psk:Plain" constrained="psk:None">
            <psf:ScoredProperty name="psk:BackCoating">
                <psf:Value xsi:type="xsd:QName">psk:None</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:FrontCoating">
                <psf:Value xsi:type="xsd:QName">psk:None</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:Material">
                <psf:Value xsi:type="xsd:QName">psk:Paper</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:PrePrinted">
                <psf:Value xsi:type="xsd:QName">psk:None</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:PrePunched">
                <psf:Value xsi:type="xsd:QName">psk:None</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:Recycled">
                <psf:Value xsi:type="xsd:QName">psk:None</psf:Value>
            </psf:ScoredProperty>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Plain Paper</psf:Value>
            </psf:Property>
        </psf:Option>
    </psf:Feature>

    <psf:Feature name="psk:PageOutputColor">
        <psf:Property name="psf:SelectionType">
            <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value>
        </psf:Property>
        <psf:Property name="psk:DisplayName">
            <psf:Value xsi:type="xsd:string">Color Printing Mode</psf:Value>
        </psf:Property>
        <psf:Option name="psk:Monochrome" constrained="psk:PrintTicketSettings">
            <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
                <psf:Value xsi:type="xsd:integer">0</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:DriverBitsPerPixel">
                <psf:Value xsi:type="xsd:integer">1</psf:Value>
            </psf:ScoredProperty>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Monochrome</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:Color" constrained="psk:PrintTicketSettings">
            <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
                <psf:Value xsi:type="xsd:integer">0</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:DriverBitsPerPixel">
                <psf:Value xsi:type="xsd:integer">4</psf:Value>
            </psf:ScoredProperty>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">8 Color (Halftoned)</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:Monochrome" constrained="psk:PrintTicketSettings">
            <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
                <psf:Value xsi:type="xsd:integer">0</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:DriverBitsPerPixel">
                <psf:Value xsi:type="xsd:integer">8</psf:Value>
            </psf:ScoredProperty>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">Grayscale (8bpp)</psf:Value>
            </psf:Property>
        </psf:Option>
        <psf:Option name="psk:Color" constrained="psk:None">
            <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
                <psf:Value xsi:type="xsd:integer">0</psf:Value>
            </psf:ScoredProperty>
            <psf:ScoredProperty name="psk:DriverBitsPerPixel">
                <psf:Value xsi:type="xsd:integer">24</psf:Value>
            </psf:ScoredProperty>
            <psf:Property name="psk:DisplayName">
                <psf:Value xsi:type="xsd:string">True Color (24bpp)</psf:Value>
            </psf:Property>
        </psf:Option>
    </psf:Feature>
    <psf:Property name="psk:PageImageableSize">
        <psf:Property name="psk:ImageableSizeWidth">
            <psf:Value xsi:type="xsd:integer">215900</psf:Value>
        </psf:Property>
        <psf:Property name="psk:ImageableSizeHeight">
            <psf:Value xsi:type="xsd:integer">279400</psf:Value>
        </psf:Property>
        <psf:Property name="psk:ImageableArea">
            <psf:Property name="psk:OriginWidth">
                <psf:Value xsi:type="xsd:integer">6350</psf:Value>
            </psf:Property>
            <psf:Property name="psk:OriginHeight">
                <psf:Value xsi:type="xsd:integer">1693</psf:Value>
            </psf:Property>
            <psf:Property name="psk:ExtentWidth">
                <psf:Value xsi:type="xsd:integer">203200</psf:Value>
            </psf:Property>
            <psf:Property name="psk:ExtentHeight">
                <psf:Value xsi:type="xsd:integer">264837</psf:Value>
            </psf:Property>
        </psf:Property>
    </psf:Property>
</psf:PrintCapabilities>
```

## <a name="related-topics"></a><span data-ttu-id="35572-110">См. также</span><span class="sxs-lookup"><span data-stu-id="35572-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35572-111">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="35572-111">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



