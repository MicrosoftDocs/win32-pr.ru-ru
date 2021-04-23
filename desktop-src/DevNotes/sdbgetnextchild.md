---
description: Выполняет поиск следующего дочернего ТЕГА в указанном родителе и возвращает TAGID следующего дочернего элемента.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: Функция Сдбжетнекстчилд
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895817"
---
# <a name="sdbgetnextchild-function"></a><span data-ttu-id="f2813-103">Функция Сдбжетнекстчилд</span><span class="sxs-lookup"><span data-stu-id="f2813-103">SdbGetNextChild function</span></span>

<span data-ttu-id="f2813-104">Выполняет поиск следующего дочернего ТЕГА в указанном родителе и возвращает **TAGID** следующего дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="f2813-104">Searches for the next child TAG within the specified parent and returns the **TAGID** of the next child.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2813-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2813-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="f2813-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2813-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2813-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="f2813-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2813-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="f2813-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="f2813-109">*типарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2813-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2813-110">**TAGID** начала поиска.</span><span class="sxs-lookup"><span data-stu-id="f2813-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="f2813-111">Этот параметр может иметь **тип TAGID \_ root** или **Tag \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="f2813-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="f2813-112">*типрев* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2813-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2813-113">**TAGID** предыдущего дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="f2813-113">The **TAGID** of the previous child.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2813-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2813-114">Return value</span></span>

<span data-ttu-id="f2813-115">**TAGID** дочернего элемента или **TAGID \_ null** , если дочерний элемент не найден.</span><span class="sxs-lookup"><span data-stu-id="f2813-115">The **TAGID** of the child or **TAGID\_NULL** if no child is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2813-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2813-116">Remarks</span></span>

<span data-ttu-id="f2813-117">Перед вызовом этой функции вызовите функцию [**сдбжетфирстчилд**](sdbgetfirstchild.md) .</span><span class="sxs-lookup"><span data-stu-id="f2813-117">Before calling this function, call the [**SdbGetFirstChild**](sdbgetfirstchild.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2813-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f2813-118">Requirements</span></span>



| <span data-ttu-id="f2813-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f2813-119">Requirement</span></span> | <span data-ttu-id="f2813-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f2813-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2813-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2813-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f2813-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2813-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f2813-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2813-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f2813-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2813-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f2813-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f2813-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2813-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2813-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2813-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2813-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2813-128">**сдбфиндфирсттаг**</span><span class="sxs-lookup"><span data-stu-id="f2813-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="f2813-129">**сдбфинднексттаг**</span><span class="sxs-lookup"><span data-stu-id="f2813-129">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="f2813-130">**сдбжетфирстчилд**</span><span class="sxs-lookup"><span data-stu-id="f2813-130">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
</dt> </dl>

 

 




