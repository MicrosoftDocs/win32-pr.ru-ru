---
title: Запрос для объектов схемы категории 1 или 2
description: Атрибут systemFlags объектов attributeSchema и classSchema представляет собой целочисленную битовую маску, которая содержит флаги, указывающие дополнительные системные характеристики атрибута или класса.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Запросы к объектам схемы категории 1 или 2
- объект Active Directory, запрос для объектов схемы категории 1 или 2
- схема AD, выполнение запросов к объектам схемы категории 1 или 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336788"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a><span data-ttu-id="293c6-106">Запрос для объектов схемы категории 1 или 2</span><span class="sxs-lookup"><span data-stu-id="293c6-106">Querying for Category 1 or 2 Schema Objects</span></span>

<span data-ttu-id="293c6-107">Атрибут **systemFlags** объектов **attributeSchema** и **classSchema** представляет собой целочисленную битовую маску, которая содержит флаги, указывающие дополнительные системные характеристики атрибута или класса.</span><span class="sxs-lookup"><span data-stu-id="293c6-107">The **systemFlags** attribute of **attributeSchema** and **classSchema** objects is an integer bitmask that contains flags that indicate additional system qualities of the attribute or class.</span></span> <span data-ttu-id="293c6-108">Перечисление [**ADS \_ системфлаг \_ enum**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) содержит значения, которые соответствуют битам, которые можно задать в атрибуте **systemFlags** .</span><span class="sxs-lookup"><span data-stu-id="293c6-108">The [**ADS\_SYSTEMFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) enumeration contains values that correspond to the bits you can set in the **systemFlags** attribute.</span></span> <span data-ttu-id="293c6-109">Можно задать дополнительные биты **systemFlags** , например 0x10 бит, указывающий, относится ли атрибут или класс к категории 1 или категории 2.</span><span class="sxs-lookup"><span data-stu-id="293c6-109">There are additional **systemFlags** bits that you cannot set, such as the 0x10 bit which indicates whether the attribute or class is category 1 or category 2.</span></span> <span data-ttu-id="293c6-110">Бит 0x10 установлен для объектов Category 1, которые являются классами и атрибутами, включенными в основную схему, включенную в систему.</span><span class="sxs-lookup"><span data-stu-id="293c6-110">The 0x10 bit is set for category 1 objects, which are the classes and attributes included in the base schema included with the system.</span></span> <span data-ttu-id="293c6-111">Бит не задан для атрибутов и классов категории 2, которые являются расширениями схемы.</span><span class="sxs-lookup"><span data-stu-id="293c6-111">The bit is not set for category 2 attributes and classes, which are extensions to the schema.</span></span> <span data-ttu-id="293c6-112">Если для объекта **attributeSchema** или **classSchema** не существует свойства **systemFlags** , это категория 2.</span><span class="sxs-lookup"><span data-stu-id="293c6-112">If no **systemFlags** property exists on an **attributeSchema** or **classSchema** object, it is category 2.</span></span>

<span data-ttu-id="293c6-113">**\_ \_ Бит правила сопоставления LDAP \_ \_ и** правило сопоставления можно использовать для поиска объектов, для которых в атрибуте **systemFlags** установлен флаг 0x10.</span><span class="sxs-lookup"><span data-stu-id="293c6-113">The **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule can be used to search for objects that have the 0x10 flag set in the **systemFlags** attribute.</span></span> <span data-ttu-id="293c6-114">Дополнительные сведения см. в разделе [синтаксис фильтра поиска](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="293c6-114">For more information, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

## <a name="querying-for-category-1"></a><span data-ttu-id="293c6-115">Запрос для категории 1</span><span class="sxs-lookup"><span data-stu-id="293c6-115">Querying for Category 1</span></span>

<span data-ttu-id="293c6-116">Следующая строка запроса ищет атрибуты категории 1 (объекты **attributeSchema** с битом 0x10, заданным в свойстве **systemFlags** ).</span><span class="sxs-lookup"><span data-stu-id="293c6-116">The following query string searches for category 1 attributes (**attributeSchema** objects with the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



<span data-ttu-id="293c6-117">Имейте в виду, что в приведенном выше примере синтаксис запроса LDAP требует наличия десятичных значений. Поэтому шестнадцатеричное значение флага должно быть преобразовано в тип Decimal.</span><span class="sxs-lookup"><span data-stu-id="293c6-117">Be aware that, in the example above, the LDAP query syntax requires decimal values; therefore, the hex value of the flag must be converted to decimal.</span></span> <span data-ttu-id="293c6-118">В этом случае категория 1 bit имеет значение 0x10, поэтому значением фильтра должно быть 16.</span><span class="sxs-lookup"><span data-stu-id="293c6-118">In this case, category 1 bit is 0x10 so the filter value must be specified as 16.</span></span>

## <a name="querying-for-category-2"></a><span data-ttu-id="293c6-119">Запрос для категории 2</span><span class="sxs-lookup"><span data-stu-id="293c6-119">Querying for Category 2</span></span>

<span data-ttu-id="293c6-120">Следующая строка запроса ищет атрибуты категории 2 (объекты **attributeSchema** , для которых в свойстве **systemFlags** не задан бит 0x10).</span><span class="sxs-lookup"><span data-stu-id="293c6-120">The following query string searches for category 2 attributes (**attributeSchema** objects that do not have the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



<span data-ttu-id="293c6-121">Имейте в виду, что этот запрос также возвращает объекты **attributeSchema** , у которых нет свойства **systemFlags** , и, следовательно, неявным образом не задан заданный флаг.</span><span class="sxs-lookup"><span data-stu-id="293c6-121">Be aware that this query also returns **attributeSchema** objects that do not have a **systemFlags** property, and, therefore, implicitly do not have the specified flag set.</span></span>

 

 