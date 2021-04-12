---
description: Необязательный логический <isDefaultSaveLocation> элемент указывает, следует ли использовать расположение, описанное в соединителе поиска, в качестве расположения для сохранения по умолчанию. Этот элемент не имеет дочерних элементов и не имеет атрибутов.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Элемент Исдефаултсавелокатион (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b664e4cd6f7c88f1dfbeb44ba23faee5d24a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342912"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a><span data-ttu-id="f0781-104">Элемент Исдефаултсавелокатион (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="f0781-104">isDefaultSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="f0781-105">Необязательный логический <isDefaultSaveLocation> элемент указывает, следует ли использовать расположение, описанное в соединителе поиска, в качестве расположения для сохранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0781-105">The optional Boolean <isDefaultSaveLocation> element specifies whether the location described in the search connector should be used as the default save location.</span></span> <span data-ttu-id="f0781-106">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f0781-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0781-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0781-107">Syntax</span></span>


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="f0781-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f0781-108">Element Information</span></span>



| <span data-ttu-id="f0781-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="f0781-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="f0781-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f0781-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f0781-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="f0781-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="f0781-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0781-112">Remarks</span></span>

<span data-ttu-id="f0781-113">Когда пользователь выбирает сохранение элемента, проводник Windows сохраняет его в расположении, указанном в <simpleLocation> элементе.</span><span class="sxs-lookup"><span data-stu-id="f0781-113">When a user chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span> <span data-ttu-id="f0781-114">Пользователи могут изменить этот параметр, используя диалоговое окно свойств соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="f0781-114">Users can change this setting using the Properties dialog for the search connector.</span></span>

## <a name="example"></a><span data-ttu-id="f0781-115">Пример</span><span class="sxs-lookup"><span data-stu-id="f0781-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



