---
description: Выполняет поиск дочернего ТЕГА в указанном родительском элементе и возвращает TAGID первого дочернего элемента.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: Функция Сдбжетфирстчилд
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538255"
---
# <a name="sdbgetfirstchild-function"></a><span data-ttu-id="4ce69-103">Функция Сдбжетфирстчилд</span><span class="sxs-lookup"><span data-stu-id="4ce69-103">SdbGetFirstChild function</span></span>

<span data-ttu-id="4ce69-104">Выполняет поиск дочернего ТЕГА в указанном родительском элементе и возвращает **TAGID** первого дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="4ce69-104">Searches for a child TAG within the specified parent and returns the **TAGID** of the first child.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce69-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ce69-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a><span data-ttu-id="4ce69-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ce69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ce69-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="4ce69-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce69-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="4ce69-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="4ce69-109">*типарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ce69-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ce69-110">**TAGID** начала поиска.</span><span class="sxs-lookup"><span data-stu-id="4ce69-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="4ce69-111">Этот параметр может иметь **тип TAGID \_ root** или **Tag \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="4ce69-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ce69-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ce69-112">Return value</span></span>

<span data-ttu-id="4ce69-113">**TAGID** первого дочернего элемента или **TAGID \_ null** не найден дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="4ce69-113">The **TAGID** of the first child or **TAGID\_NULL** is no child is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ce69-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4ce69-114">Requirements</span></span>



| <span data-ttu-id="4ce69-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4ce69-115">Requirement</span></span> | <span data-ttu-id="4ce69-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4ce69-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce69-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ce69-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4ce69-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4ce69-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4ce69-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ce69-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4ce69-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ce69-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4ce69-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4ce69-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ce69-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ce69-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ce69-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ce69-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce69-124">**сдбфиндфирсттаг**</span><span class="sxs-lookup"><span data-stu-id="4ce69-124">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="4ce69-125">**сдбфинднексттаг**</span><span class="sxs-lookup"><span data-stu-id="4ce69-125">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="4ce69-126">**сдбжетнекстчилд**</span><span class="sxs-lookup"><span data-stu-id="4ce69-126">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
</dt> </dl>

 

 




