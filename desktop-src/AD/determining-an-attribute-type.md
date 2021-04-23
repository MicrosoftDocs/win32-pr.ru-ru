---
title: Определение типа атрибута
description: Атрибут systemFlags объекта attributeSchema содержит набор флагов, которые указывают различные значения качества объекта атрибута, например, создается или не реплицируется атрибут.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Определение типа атрибута Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069782"
---
# <a name="determining-an-attribute-type"></a><span data-ttu-id="08a01-104">Определение типа атрибута</span><span class="sxs-lookup"><span data-stu-id="08a01-104">Determining an Attribute Type</span></span>

<span data-ttu-id="08a01-105">Атрибут [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) содержит набор флагов, которые указывают различные значения качества объекта атрибута, например, создается или не реплицируется атрибут.</span><span class="sxs-lookup"><span data-stu-id="08a01-105">The [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object contains a set of flags that indicate various qualities of the attribute object, such as whether the attribute is constructed or non-replicated.</span></span> <span data-ttu-id="08a01-106">В следующей таблице перечислены флаги атрибута **systemFlags** , влияющие на тип хранения атрибута.</span><span class="sxs-lookup"><span data-stu-id="08a01-106">The following table lists the flags of the **systemFlags** attribute that affect the storage type of the attribute.</span></span> 

| <span data-ttu-id="08a01-107">Значение флага</span><span class="sxs-lookup"><span data-stu-id="08a01-107">Flag value</span></span> | <span data-ttu-id="08a01-108">Описание</span><span class="sxs-lookup"><span data-stu-id="08a01-108">Description</span></span>                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a01-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08a01-109">0x00000001</span></span> | <span data-ttu-id="08a01-110">Если этот флаг имеется в атрибуте [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , то этот атрибут не реплицируется.</span><span class="sxs-lookup"><span data-stu-id="08a01-110">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is not replicated.</span></span> |
| <span data-ttu-id="08a01-111">0x00000004</span><span class="sxs-lookup"><span data-stu-id="08a01-111">0x00000004</span></span> | <span data-ttu-id="08a01-112">Если этот флаг имеется в атрибуте [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , то создается атрибут.</span><span class="sxs-lookup"><span data-stu-id="08a01-112">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is constructed.</span></span>    |



 

<span data-ttu-id="08a01-113">Можно создать строку запроса, которая может использоваться для запроса созданных или нереплицируемых атрибутов.</span><span class="sxs-lookup"><span data-stu-id="08a01-113">It is possible to construct a query string that can be used to query for constructed or non-replicated attributes.</span></span> <span data-ttu-id="08a01-114">Например, следующая строка запроса находит все нереплицированные объекты [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) .</span><span class="sxs-lookup"><span data-stu-id="08a01-114">For example, the following query string finds all non-replicated [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects.</span></span> <span data-ttu-id="08a01-115">Имейте в виду, что строка запроса требует десятичного эквивалента значения, а не шестнадцатеричного эквивалента значения.</span><span class="sxs-lookup"><span data-stu-id="08a01-115">Be aware that the query string requires the decimal equivalent of the value, not the hexadecimal equivalent of the value.</span></span> <span data-ttu-id="08a01-116">Дополнительные сведения о идентификаторе OID правила сопоставления, используемом этой строкой запроса, см. [в разделе как указать значения для сравнения](how-to-specify-comparison-values.md).</span><span class="sxs-lookup"><span data-stu-id="08a01-116">For more information about the matching rule OID used by this query string, see [How to Specify Comparison Values](how-to-specify-comparison-values.md).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



<span data-ttu-id="08a01-117">Атрибут [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) каждого атрибута определяет, индексируется ли атрибут. индексированный атрибут имеет значение 1, неиндексированный атрибут имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="08a01-117">The [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is indexed; an indexed attribute has a value of 1, a non-indexed attribute has a value of 0.</span></span> <span data-ttu-id="08a01-118">Например, следующая строка запроса находит объекты **attributeSchema** , представляющие индексированные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="08a01-118">For example, the following query string finds the **attributeSchema** objects representing indexed attributes.</span></span>


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



<span data-ttu-id="08a01-119">Атрибут [**исмемберофпартиалаттрибутесет**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) объекта [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) каждого атрибута определяет, реплицируется ли атрибут в глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="08a01-119">The [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is replicated to the global catalog.</span></span> <span data-ttu-id="08a01-120">Этот атрибут имеет значение **true** , если атрибут является членом глобального каталога, или **значение false** , если атрибуты не находятся в глобальном каталоге.</span><span class="sxs-lookup"><span data-stu-id="08a01-120">This attribute has a value of **TRUE** if the attribute is a member of the global catalog or **FALSE** if the attributes is not in the global catalog.</span></span> <span data-ttu-id="08a01-121">Например, следующая строка запроса выполняет поиск объектов **attributeSchema** , которые реплицируются в глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="08a01-121">For example, the following query string searches the **attributeSchema** objects that are replicated to the global catalog.</span></span>


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 