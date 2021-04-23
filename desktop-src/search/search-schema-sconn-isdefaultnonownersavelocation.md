---
description: Необязательный логический <isDefaultNonOwnerSaveLocation> элемент указывает, следует ли использовать расположение, описанное в соединителе поиска, в качестве расположения для сохранения по умолчанию, когда пользователь из другого компьютера в домашней группе выбирает сохранение элемента.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: Элемент Исдефаултноновнерсавелокатион (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edd39ab76ae1b99d6518ca40407d328f5da9778c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692172"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a><span data-ttu-id="701e8-103">Элемент Исдефаултноновнерсавелокатион (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="701e8-103">isDefaultNonOwnerSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="701e8-104">Необязательный логический <isDefaultNonOwnerSaveLocation> элемент указывает, следует ли использовать расположение, описанное в соединителе поиска, в качестве расположения для сохранения по умолчанию, когда пользователь из другого компьютера в домашней группе выбирает сохранение элемента.</span><span class="sxs-lookup"><span data-stu-id="701e8-104">The optional Boolean <isDefaultNonOwnerSaveLocation> element specifies whether the location described in the search connector should be used as the default save location when a user from another computer in a Homegroup chooses to save an item.</span></span> <span data-ttu-id="701e8-105">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="701e8-105">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="701e8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="701e8-106">Syntax</span></span>


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="701e8-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="701e8-107">Element Information</span></span>



| <span data-ttu-id="701e8-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="701e8-108">Parent Element</span></span>                                                                                                   | <span data-ttu-id="701e8-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="701e8-109">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="701e8-110">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="701e8-110">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="701e8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="701e8-111">Remarks</span></span>

<span data-ttu-id="701e8-112">Если задано значение true, то когда пользователь из другого компьютера в домашней группе выбирает сохранение элемента, проводник Windows сохраняет этот элемент в расположении, указанном в <simpleLocation> элементе.</span><span class="sxs-lookup"><span data-stu-id="701e8-112">If true, when a user from another computer in a Homegroup chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span>

## <a name="example"></a><span data-ttu-id="701e8-113">Пример</span><span class="sxs-lookup"><span data-stu-id="701e8-113">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



