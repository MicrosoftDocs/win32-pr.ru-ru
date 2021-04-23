---
description: Содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990440"
---
# <a name="tagid"></a><span data-ttu-id="0d193-103">TAGID</span><span class="sxs-lookup"><span data-stu-id="0d193-103">TAGID</span></span>

<span data-ttu-id="0d193-104">Содержит индекс записи и сведения о ТЕГАХ в базе данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="0d193-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a><span data-ttu-id="0d193-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d193-105">Remarks</span></span>

<span data-ttu-id="0d193-106">**TAGID** зависит от базы данных.</span><span class="sxs-lookup"><span data-stu-id="0d193-106">A **TAGID** is specific to a database.</span></span> <span data-ttu-id="0d193-107">Это может быть целочисленное значение, представляющее индекс, или одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="0d193-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="0d193-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ null (0)</span><span class="sxs-lookup"><span data-stu-id="0d193-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="0d193-109">**TAGID** не существует.</span><span class="sxs-lookup"><span data-stu-id="0d193-109">The **TAGID** does not exist.</span></span> <span data-ttu-id="0d193-110">Это значение возвращается из функции, если оно не может возвращать допустимый **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="0d193-110">This value is returned from a function when it cannot return a valid **TAGID**.</span></span>

</dd> <dt>

<span data-ttu-id="0d193-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>\_Корневой TAGID (0)</span><span class="sxs-lookup"><span data-stu-id="0d193-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="0d193-112">Указывает тег корневого списка, который можно использовать в качестве родителя для получения дочернего **TAGID**.</span><span class="sxs-lookup"><span data-stu-id="0d193-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d193-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0d193-113">Requirements</span></span>



| <span data-ttu-id="0d193-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0d193-114">Requirement</span></span> | <span data-ttu-id="0d193-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0d193-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d193-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d193-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0d193-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d193-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0d193-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d193-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0d193-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d193-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d193-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d193-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d193-121">**ТЕГАМИ**</span><span class="sxs-lookup"><span data-stu-id="0d193-121">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="0d193-122">Типы тегов</span><span class="sxs-lookup"><span data-stu-id="0d193-122">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="0d193-123">**тагреф**</span><span class="sxs-lookup"><span data-stu-id="0d193-123">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




