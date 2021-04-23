---
description: Выполняет поиск следующего ТЕГА в указанном родителе и возвращает TAGID совпадения.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: Функция Сдбфинднексттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895661"
---
# <a name="sdbfindnexttag-function"></a><span data-ttu-id="623b5-103">Функция Сдбфинднексттаг</span><span class="sxs-lookup"><span data-stu-id="623b5-103">SdbFindNextTag function</span></span>

<span data-ttu-id="623b5-104">Выполняет поиск следующего ТЕГА в указанном родителе и возвращает **TAGID** совпадения.</span><span class="sxs-lookup"><span data-stu-id="623b5-104">Searches for the next TAG match within the specified parent and returns the **TAGID** of the match.</span></span>

## <a name="syntax"></a><span data-ttu-id="623b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="623b5-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="623b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="623b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="623b5-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="623b5-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="623b5-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="623b5-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="623b5-109">*типарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="623b5-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="623b5-110">**TAGID** начала поиска.</span><span class="sxs-lookup"><span data-stu-id="623b5-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="623b5-111">Этот параметр может иметь **тип TAGID \_ root** или **Tag \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="623b5-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="623b5-112">*типрев* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="623b5-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="623b5-113">**TAGID** предыдущего совпадения.</span><span class="sxs-lookup"><span data-stu-id="623b5-113">The **TAGID** of the previous match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="623b5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="623b5-114">Return value</span></span>

<span data-ttu-id="623b5-115">**TAGID** совпадения.</span><span class="sxs-lookup"><span data-stu-id="623b5-115">The **TAGID** of the match.</span></span>

## <a name="remarks"></a><span data-ttu-id="623b5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="623b5-116">Remarks</span></span>

<span data-ttu-id="623b5-117">Перед вызовом этой функции вызовите функцию [**сдбфиндфирсттаг**](sdbfindfirsttag.md) .</span><span class="sxs-lookup"><span data-stu-id="623b5-117">Before calling this function, call the [**SdbFindFirstTag**](sdbfindfirsttag.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="623b5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="623b5-118">Requirements</span></span>



| <span data-ttu-id="623b5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="623b5-119">Requirement</span></span> | <span data-ttu-id="623b5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="623b5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="623b5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="623b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="623b5-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="623b5-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="623b5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="623b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="623b5-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="623b5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="623b5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="623b5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="623b5-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="623b5-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="623b5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="623b5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623b5-128">**сдбфиндфирсттаг**</span><span class="sxs-lookup"><span data-stu-id="623b5-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="623b5-129">**сдбтагрефтотагид**</span><span class="sxs-lookup"><span data-stu-id="623b5-129">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




