---
description: Этот необязательный <templateInfo> элемент указывает тип папки для отображения результатов запроса через этот соединитель поиска. У этого элемента нет атрибутов и только один обязательный дочерний элемент.
ms.assetid: fe42f589-5c47-4629-94eb-78dbaffa4112
title: Элемент Темплатеинфо (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fd28780689b4d544f251bbaf1542bc379ecdaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692164"
---
# <a name="templateinfo-element-search-connector-schema"></a><span data-ttu-id="2fe55-104">Элемент Темплатеинфо (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="2fe55-104">templateInfo Element (Search Connector Schema)</span></span>

<span data-ttu-id="2fe55-105">Этот необязательный <templateInfo> элемент указывает тип папки для отображения результатов запроса через этот соединитель поиска.</span><span class="sxs-lookup"><span data-stu-id="2fe55-105">This optional <templateInfo> element specifies a folder type for displaying the results from a query over this search connector.</span></span> <span data-ttu-id="2fe55-106">У этого элемента нет атрибутов и только один обязательный дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="2fe55-106">This element has no attributes and only one mandatory child.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fe55-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fe55-107">Syntax</span></span>


```
<!-- templateInfo -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="templateInfo" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="folderType" minOccurs="0"/>
                    </xs:all>
                </xs:complexType>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="2fe55-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2fe55-108">Element Information</span></span>



| <span data-ttu-id="2fe55-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="2fe55-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="2fe55-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2fe55-110">Child Elements</span></span>                                                                     |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fe55-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="2fe55-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="2fe55-112">Элемент Фолдертипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="2fe55-112">folderType Element (Search Connector Schema)</span></span>](search-schema-sconn-foldertype.md) |



 

## <a name="remarks"></a><span data-ttu-id="2fe55-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2fe55-113">Remarks</span></span>

<span data-ttu-id="2fe55-114">Если в элементе не указан определенный тип папки <templateInfo> , Windows использует тип папки "общий соединитель поиска" {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span><span class="sxs-lookup"><span data-stu-id="2fe55-114">If you don't specify a particular folder type in the <templateInfo> element, Windows uses the general search connector folder type {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}.</span></span>

## <a name="example-of-a-templateinfo-element"></a><span data-ttu-id="2fe55-115">Пример элемента Темплатеинфо</span><span class="sxs-lookup"><span data-stu-id="2fe55-115">Example of a templateInfo Element</span></span>


```
<!-- templateInfo -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



