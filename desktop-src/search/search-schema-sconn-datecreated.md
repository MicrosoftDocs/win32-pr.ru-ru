---
description: Необязательный <dateCreated> элемент определяет дату и время создания соединителя поиска, используя стандарт ISO 8601. У него нет дочерних элементов и атрибутов.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Элемент dateCreated (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808908"
---
# <a name="datecreated-element-search-connector-schema"></a><span data-ttu-id="6afad-104">Элемент dateCreated (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="6afad-104">dateCreated Element (Search Connector Schema)</span></span>

<span data-ttu-id="6afad-105">Необязательный <dateCreated> элемент определяет дату и время создания соединителя поиска, используя стандарт ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="6afad-105">The optional <dateCreated> element identifies the date and the time when this search connector was created, using the ISO 8601 standard.</span></span> <span data-ttu-id="6afad-106">У него нет дочерних элементов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="6afad-106">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6afad-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6afad-107">Syntax</span></span>


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="6afad-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6afad-108">Element Information</span></span>



| <span data-ttu-id="6afad-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="6afad-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="6afad-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6afad-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="6afad-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="6afad-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="6afad-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6afad-112">Remarks</span></span>

<span data-ttu-id="6afad-113">Формат значения этого элемента соответствует стандарту ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="6afad-113">The format of the value of this element follows the ISO 8601 standard.</span></span> <span data-ttu-id="6afad-114">Обычно используется один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="6afad-114">A common use would be either of the following:</span></span>

-   <span data-ttu-id="6afad-115">\[Гггг \] - \[ мм \] - \[ дд \] T \[ чч \] : \[ мм \] : \[ СС \] ± \[ чч \] : \[ мм \] ("1981-04-05T14:30:30-05:00")</span><span class="sxs-lookup"><span data-stu-id="6afad-115">\[YYYY\]-\[MM\]-\[DD\]T\[hh\]:\[mm\]:\[ss\]±\[hh\]:\[mm\] ("1981-04-05T14:30:30-05:00")</span></span>
-   <span data-ttu-id="6afad-116">\[ГГГГ \] \[ мм \] \[ дд \] T \[ чч \] \[ mm \] \[ SS \] Z ("19810405T193030Z")</span><span class="sxs-lookup"><span data-stu-id="6afad-116">\[YYYY\]\[MM\]\[DD\]T\[hh\]\[mm\]\[ss\]Z ("19810405T193030Z")</span></span>

## <a name="example"></a><span data-ttu-id="6afad-117">Пример</span><span class="sxs-lookup"><span data-stu-id="6afad-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



