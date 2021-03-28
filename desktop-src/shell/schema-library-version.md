---
description: <version>Элемент указывает версию содержимого этой библиотеки. Этот элемент не имеет атрибутов и не содержит дочерних элементов.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: Элемент Version (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984584"
---
# <a name="version-element-library-schema"></a><span data-ttu-id="2ce6e-104">Элемент Version (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="2ce6e-104">version Element (Library Schema)</span></span>

<span data-ttu-id="2ce6e-105"><version>Элемент указывает версию содержимого этой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="2ce6e-105">The <version> element specifies the content version of this library.</span></span> <span data-ttu-id="2ce6e-106">Этот элемент не имеет атрибутов и не содержит дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="2ce6e-106">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce6e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ce6e-107">Syntax</span></span>

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a><span data-ttu-id="2ce6e-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2ce6e-108">Element Information</span></span>



| <span data-ttu-id="2ce6e-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="2ce6e-109">Parent Element</span></span>                                                               | <span data-ttu-id="2ce6e-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2ce6e-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="2ce6e-111">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="2ce6e-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | <span data-ttu-id="2ce6e-112">None</span><span class="sxs-lookup"><span data-stu-id="2ce6e-112">None</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="2ce6e-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="2ce6e-113">Remarks</span></span>

<span data-ttu-id="2ce6e-114">Версия содержимого библиотеки отличается от версии в формате файла библиотеки ( \* . Library-MS).</span><span class="sxs-lookup"><span data-stu-id="2ce6e-114">The content version of the library is different from the library's file format (\*.library-ms) version.</span></span> <span data-ttu-id="2ce6e-115">Версия формата файла библиотеки указывается в [пространстве имен](library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="2ce6e-115">The library's file format version is specified in the [namespace](library-schema-entry.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ce6e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="2ce6e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ce6e-117">Схема описания библиотеки</span><span class="sxs-lookup"><span data-stu-id="2ce6e-117">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="2ce6e-118">Схема описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="2ce6e-118">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
