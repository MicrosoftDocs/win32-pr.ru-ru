---
description: <name>Элемент указывает имя этой библиотеки. Этот элемент является обязательным и не имеет атрибутов или дочерних элементов.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Элемент Name (схема библиотеки)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997955"
---
# <a name="name-element-library-schema"></a><span data-ttu-id="62f11-104">Элемент Name (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="62f11-104">name Element (Library Schema)</span></span>

<span data-ttu-id="62f11-105"><name>Элемент указывает имя этой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="62f11-105">The <name> element specifies the name of this library.</span></span> <span data-ttu-id="62f11-106">Этот элемент является обязательным и не имеет атрибутов или дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="62f11-106">This element is required and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f11-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62f11-107">Syntax</span></span>

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a><span data-ttu-id="62f11-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62f11-108">Element Information</span></span>



| <span data-ttu-id="62f11-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62f11-109">Parent Element</span></span>                                                               | <span data-ttu-id="62f11-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62f11-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="62f11-111">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="62f11-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="62f11-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="62f11-112">Remarks</span></span>

<span data-ttu-id="62f11-113">Имя — это понятное имя библиотеки, отображаемое в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="62f11-113">The name is the friendly library name that is displayed in Windows Explorer.</span></span> <span data-ttu-id="62f11-114">Имя можно указать в <dllname> формате, как показано <index> в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="62f11-114">The name can be specified in a <dllname>,<index> format, as in the following example.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="62f11-115">См. также</span><span class="sxs-lookup"><span data-stu-id="62f11-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62f11-116">Элемент Либраридескриптион (схема библиотеки)</span><span class="sxs-lookup"><span data-stu-id="62f11-116">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="62f11-117">Схема описания соединителя поиска</span><span class="sxs-lookup"><span data-stu-id="62f11-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
