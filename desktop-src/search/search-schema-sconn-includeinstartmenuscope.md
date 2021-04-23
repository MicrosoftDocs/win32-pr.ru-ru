---
description: Необязательный логический <includeInStartMenuScope> элемент указывает, следует ли включать этот соединитель поиска в область поиска меню "Пуск".
ms.assetid: 934a3834-9ddc-4c15-b738-68ea74adc24c
title: Элемент Инклудеинстартменускопе (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126d10a2b69dcec5057e732679c8531fd6e82bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692173"
---
# <a name="includeinstartmenuscope-element-search-connector-schema"></a><span data-ttu-id="d8118-103">Элемент Инклудеинстартменускопе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="d8118-103">includeInStartMenuScope Element (Search Connector Schema)</span></span>

<span data-ttu-id="d8118-104">Необязательный логический <includeInStartMenuScope> элемент указывает, следует ли включать этот соединитель поиска в область поиска меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="d8118-104">The optional Boolean <includeInStartMenuScope> element specifies whether this search connector should be included in the Start menu search scope.</span></span> <span data-ttu-id="d8118-105">Значение по умолчанию — true для соединителей поиска, использующих файловую систему в качестве источника данных, и false для соединителей поиска, используемых обработчиками свойств.</span><span class="sxs-lookup"><span data-stu-id="d8118-105">The default value is true for search connectors using the file system as a data source, and false for search connectors used by property handlers.</span></span> <span data-ttu-id="d8118-106">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d8118-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8118-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8118-107">Syntax</span></span>


```
<!-- includeInStartMenuScope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="d8118-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d8118-108">Element Information</span></span>



| <span data-ttu-id="d8118-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="d8118-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="d8118-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d8118-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="d8118-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="d8118-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="d8118-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8118-112">Remarks</span></span>

<span data-ttu-id="d8118-113">Если включить соединитель поиска в область меню "Пуск", пользователи смогут выполнять поиск в вашем расположении из поля поиска в меню "Пуск".</span><span class="sxs-lookup"><span data-stu-id="d8118-113">If you include the search connector in the Start menu scope, users can search your location from the search box in the Start menu.</span></span>

## <a name="example"></a><span data-ttu-id="d8118-114">Пример</span><span class="sxs-lookup"><span data-stu-id="d8118-114">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <includeinStartMenuScope>true</includeinStartMenuScope>
    ...
</searchConnectionDescription>
```



 

 



