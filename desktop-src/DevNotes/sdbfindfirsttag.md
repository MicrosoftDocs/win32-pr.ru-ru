---
description: Выполняет поиск совпадения ТЕГА в указанном родительском элементе и возвращает TAGID первого совпадения.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: Функция Сдбфиндфирсттаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990308"
---
# <a name="sdbfindfirsttag-function"></a><span data-ttu-id="01913-103">Функция Сдбфиндфирсттаг</span><span class="sxs-lookup"><span data-stu-id="01913-103">SdbFindFirstTag function</span></span>

<span data-ttu-id="01913-104">Выполняет поиск совпадения ТЕГА в указанном родительском элементе и возвращает **TAGID** первого совпадения.</span><span class="sxs-lookup"><span data-stu-id="01913-104">Searches for a TAG match within the specified parent and returns the **TAGID** of the first match.</span></span>

## <a name="syntax"></a><span data-ttu-id="01913-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01913-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
);
```



## <a name="parameters"></a><span data-ttu-id="01913-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01913-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01913-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="01913-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01913-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="01913-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="01913-109">*типарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01913-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01913-110">**TAGID** начала поиска.</span><span class="sxs-lookup"><span data-stu-id="01913-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="01913-111">Этот параметр может иметь **тип TAGID \_ root** или **Tag \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="01913-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="01913-112">*ттаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01913-112">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01913-113">ТЕГ для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="01913-113">The TAG to be matched.</span></span> <span data-ttu-id="01913-114">Список возможных значений см. в разделе [тег](tag.md) .</span><span class="sxs-lookup"><span data-stu-id="01913-114">See [TAG](tag.md) for a list of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01913-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01913-115">Return value</span></span>

<span data-ttu-id="01913-116">**TAGID** первого совпадения.</span><span class="sxs-lookup"><span data-stu-id="01913-116">The **TAGID** of the first match.</span></span>

## <a name="requirements"></a><span data-ttu-id="01913-117">Требования</span><span class="sxs-lookup"><span data-stu-id="01913-117">Requirements</span></span>



| <span data-ttu-id="01913-118">Требование</span><span class="sxs-lookup"><span data-stu-id="01913-118">Requirement</span></span> | <span data-ttu-id="01913-119">Значение</span><span class="sxs-lookup"><span data-stu-id="01913-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01913-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01913-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01913-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01913-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="01913-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01913-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01913-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01913-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="01913-124">DLL</span><span class="sxs-lookup"><span data-stu-id="01913-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01913-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01913-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01913-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01913-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01913-127">**сдбфинднексттаг**</span><span class="sxs-lookup"><span data-stu-id="01913-127">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="01913-128">**сдбтагрефтотагид**</span><span class="sxs-lookup"><span data-stu-id="01913-128">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




