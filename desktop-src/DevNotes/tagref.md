---
description: Содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: тагреф
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8631811f101850b68bdbad1097c19b9a41737bd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538516"
---
# <a name="tagref"></a><span data-ttu-id="f47f1-103">тагреф</span><span class="sxs-lookup"><span data-stu-id="f47f1-103">TAGREF</span></span>

<span data-ttu-id="f47f1-104">Содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="f47f1-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="f47f1-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f47f1-105">Remarks</span></span>

<span data-ttu-id="f47f1-106">**Тагреф** относится к базе данных оболочек совместимости и допустима в нескольких базах данных.</span><span class="sxs-lookup"><span data-stu-id="f47f1-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="f47f1-107">Это может быть целочисленное значение, представляющее индекс, или одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f47f1-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f47f1-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>ТАГРЕФ \_ null (0)</span><span class="sxs-lookup"><span data-stu-id="f47f1-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="f47f1-109">**Тагреф** не существует.</span><span class="sxs-lookup"><span data-stu-id="f47f1-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="f47f1-110">Это значение возвращается из функции, если оно не может возвращать допустимый **тагреф**.</span><span class="sxs-lookup"><span data-stu-id="f47f1-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="f47f1-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Корневой тагреф (0)</span><span class="sxs-lookup"><span data-stu-id="f47f1-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="f47f1-112">Указывает тег корневого списка, который можно использовать в качестве родителя для получения дочернего **тагреф**.</span><span class="sxs-lookup"><span data-stu-id="f47f1-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f47f1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f47f1-113">Requirements</span></span>



| <span data-ttu-id="f47f1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f47f1-114">Requirement</span></span> | <span data-ttu-id="f47f1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f47f1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f47f1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f47f1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f47f1-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f47f1-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f47f1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f47f1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f47f1-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f47f1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f47f1-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f47f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f47f1-121">**сдбтагрефтотагид**</span><span class="sxs-lookup"><span data-stu-id="f47f1-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="f47f1-122">**ТЕГАМИ**</span><span class="sxs-lookup"><span data-stu-id="f47f1-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="f47f1-123">Типы тегов</span><span class="sxs-lookup"><span data-stu-id="f47f1-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="f47f1-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="f47f1-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




