---
description: Содержит группу массивов АНДЕКСП, оцененных как одноранговые.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Структура выражения (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662199"
---
# <a name="expression-structure"></a><span data-ttu-id="df8fe-103">Структура выражения</span><span class="sxs-lookup"><span data-stu-id="df8fe-103">EXPRESSION structure</span></span>

<span data-ttu-id="df8fe-104">Структура **выражения** содержит группу массивов **андексп** , вычисленную как одноранговые в логических выражениях и, имеющих формат</span><span class="sxs-lookup"><span data-stu-id="df8fe-104">The **EXPRESSION** structure contains a group of **ANDEXP** arrays evaluated as peers in logical AND expressions, which have the format</span></span>

<span data-ttu-id="df8fe-105">(АНДЕКСП 1 && АНДЕКСП 2 && АНДЕКСП 3).</span><span class="sxs-lookup"><span data-stu-id="df8fe-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span></span>

## <a name="syntax"></a><span data-ttu-id="df8fe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df8fe-106">Syntax</span></span>


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a><span data-ttu-id="df8fe-107">Члены</span><span class="sxs-lookup"><span data-stu-id="df8fe-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="df8fe-108">**нандекспс**</span><span class="sxs-lookup"><span data-stu-id="df8fe-108">**nAndExps**</span></span>
</dt> <dd>

<span data-ttu-id="df8fe-109">Количество шаблонов **андексп** .</span><span class="sxs-lookup"><span data-stu-id="df8fe-109">Number of **ANDEXP** patterns.</span></span>

</dd> <dt>

<span data-ttu-id="df8fe-110">**андексп**</span><span class="sxs-lookup"><span data-stu-id="df8fe-110">**AndExp**</span></span>
</dt> <dd>

<span data-ttu-id="df8fe-111">Массив шаблонов **андексп** .</span><span class="sxs-lookup"><span data-stu-id="df8fe-111">Array of **ANDEXP** patterns.</span></span> <span data-ttu-id="df8fe-112">Фильтр записи упорядочивает все строки этого массива как логические операторы и.</span><span class="sxs-lookup"><span data-stu-id="df8fe-112">The capture filter arranges all rows of this array as logical AND statements.</span></span> <span data-ttu-id="df8fe-113">Имейте в виду, что каждая структура выражения может содержать не более четырех шаблонов **андексп** .</span><span class="sxs-lookup"><span data-stu-id="df8fe-113">Be aware that each EXPRESSION structure can contain a maximum of four **ANDEXP** patterns.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df8fe-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df8fe-114">Remarks</span></span>

<span data-ttu-id="df8fe-115">Дополнительные сведения о реализации этой структуры в составе фильтра записи см. в разделе [фильтры записи](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="df8fe-115">For more information about implementing this structure as part of a capture filter, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df8fe-116">Требования</span><span class="sxs-lookup"><span data-stu-id="df8fe-116">Requirements</span></span>



| <span data-ttu-id="df8fe-117">Требование</span><span class="sxs-lookup"><span data-stu-id="df8fe-117">Requirement</span></span> | <span data-ttu-id="df8fe-118">Значение</span><span class="sxs-lookup"><span data-stu-id="df8fe-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="df8fe-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df8fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="df8fe-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df8fe-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="df8fe-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df8fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="df8fe-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df8fe-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="df8fe-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="df8fe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="df8fe-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="df8fe-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df8fe-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df8fe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8fe-126">андексп</span><span class="sxs-lookup"><span data-stu-id="df8fe-126">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="df8fe-127">каптурефилтер</span><span class="sxs-lookup"><span data-stu-id="df8fe-127">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




