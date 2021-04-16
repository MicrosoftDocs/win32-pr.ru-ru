---
description: Необязательный <iconReference> элемент указывает пользовательский значок для этого расположения. Этот элемент не имеет атрибутов и не содержит дочерних элементов.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Элемент Иконреференце (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540642"
---
# <a name="iconreference-element-search-connector-schema"></a><span data-ttu-id="dcd56-104">Элемент Иконреференце (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="dcd56-104">iconReference Element (Search Connector Schema)</span></span>

<span data-ttu-id="dcd56-105">Необязательный <iconReference> элемент указывает пользовательский значок для этого расположения.</span><span class="sxs-lookup"><span data-stu-id="dcd56-105">The optional <iconReference> element specifies a custom icon for this location.</span></span> <span data-ttu-id="dcd56-106">Этот элемент не имеет атрибутов и не содержит дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="dcd56-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcd56-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcd56-107">Syntax</span></span>


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="dcd56-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dcd56-108">Element Information</span></span>



| <span data-ttu-id="dcd56-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="dcd56-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="dcd56-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dcd56-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="dcd56-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="dcd56-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="dcd56-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcd56-112">Remarks</span></span>

<span data-ttu-id="dcd56-113">Формат ссылки должен быть указан в форме, подходящей для функции [паспарсеиконлокатион](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) : (например, <dll file name> <icon index> ).</span><span class="sxs-lookup"><span data-stu-id="dcd56-113">The format of the reference must be specified in a form suitable for the [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) function: (for example, <dll file name>,<icon index>).</span></span>

## <a name="example"></a><span data-ttu-id="dcd56-114">Пример</span><span class="sxs-lookup"><span data-stu-id="dcd56-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
