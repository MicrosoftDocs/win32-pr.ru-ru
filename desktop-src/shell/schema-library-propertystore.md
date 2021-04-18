---
description: <propertyStore>Элемент указывает набор из одного или нескольких свойств, используемых этой библиотекой. Этот элемент является необязательным и не имеет атрибутов.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Элемент Пропертисторе (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985820"
---
# <a name="propertystore-element-library-schema"></a><span data-ttu-id="aea9c-104">Элемент Пропертисторе (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="aea9c-104">propertyStore Element (Library Schema)</span></span>

<span data-ttu-id="aea9c-105"><propertyStore>Элемент указывает набор из одного или нескольких свойств, используемых этой библиотекой.</span><span class="sxs-lookup"><span data-stu-id="aea9c-105">The <propertyStore> element specifies a set of one or more properties used by this library.</span></span> <span data-ttu-id="aea9c-106">Этот элемент является необязательным и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="aea9c-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea9c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aea9c-107">Syntax</span></span>

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="aea9c-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="aea9c-108">Element Information</span></span>



| <span data-ttu-id="aea9c-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="aea9c-109">Parent Element</span></span>                                                               | <span data-ttu-id="aea9c-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="aea9c-110">Child Elements</span></span>                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="aea9c-111">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="aea9c-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="aea9c-112">Элемент Property (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="aea9c-112">property Element (Library Schema)</span></span>](schema-library-property.md) |



 

## <a name="remarks"></a><span data-ttu-id="aea9c-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="aea9c-113">Remarks</span></span>

<span data-ttu-id="aea9c-114"><propertyStore>Элемент может иметь один или несколько <property> дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="aea9c-114">The <propertyStore> element can have one or more <property> child elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aea9c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="aea9c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aea9c-116">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="aea9c-116">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="aea9c-117">Схема описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="aea9c-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
