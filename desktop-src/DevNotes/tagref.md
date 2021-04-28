---
description: ТАГРЕФ — содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: тагреф
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096632"
---
# <a name="tagref"></a><span data-ttu-id="d7357-103">тагреф</span><span class="sxs-lookup"><span data-stu-id="d7357-103">TAGREF</span></span>

<span data-ttu-id="d7357-104">Содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="d7357-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="d7357-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="d7357-105">Remarks</span></span>

<span data-ttu-id="d7357-106">**Тагреф** относится к базе данных оболочек совместимости и допустима в нескольких базах данных.</span><span class="sxs-lookup"><span data-stu-id="d7357-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="d7357-107">Это может быть целочисленное значение, представляющее индекс, или одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d7357-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="d7357-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>ТАГРЕФ \_ null (0)</span><span class="sxs-lookup"><span data-stu-id="d7357-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="d7357-109">**Тагреф** не существует.</span><span class="sxs-lookup"><span data-stu-id="d7357-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="d7357-110">Это значение возвращается из функции, если оно не может возвращать допустимый **тагреф**.</span><span class="sxs-lookup"><span data-stu-id="d7357-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="d7357-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Корневой тагреф (0)</span><span class="sxs-lookup"><span data-stu-id="d7357-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="d7357-112">Указывает тег корневого списка, который можно использовать в качестве родителя для получения дочернего **тагреф**.</span><span class="sxs-lookup"><span data-stu-id="d7357-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7357-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d7357-113">Requirements</span></span>



| <span data-ttu-id="d7357-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d7357-114">Requirement</span></span> | <span data-ttu-id="d7357-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d7357-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7357-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7357-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d7357-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7357-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d7357-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7357-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d7357-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7357-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7357-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d7357-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7357-121">**сдбтагрефтотагид**</span><span class="sxs-lookup"><span data-stu-id="d7357-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="d7357-122">**ТЕГАМИ**</span><span class="sxs-lookup"><span data-stu-id="d7357-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="d7357-123">Типы тегов</span><span class="sxs-lookup"><span data-stu-id="d7357-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="d7357-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="d7357-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




