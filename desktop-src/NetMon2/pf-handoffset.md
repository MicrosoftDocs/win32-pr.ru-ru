---
description: Структура PF \_ хандоффсет определяет протоколы, которые передаются средству синтаксического анализа, или протоколы, к которым он передает.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: Структура PF_HANDOFFSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663841"
---
# <a name="pf_handoffset-structure"></a><span data-ttu-id="5969a-103">\_Структура PF хандоффсет</span><span class="sxs-lookup"><span data-stu-id="5969a-103">PF\_HANDOFFSET structure</span></span>

<span data-ttu-id="5969a-104">Структура **PF \_ хандоффсет** определяет протоколы, которые передаются средству синтаксического анализа, или протоколы, к которым он передает.</span><span class="sxs-lookup"><span data-stu-id="5969a-104">The **PF\_HANDOFFSET** structure defines the protocols that hand off to the parser, or the protocols that the parser hands off to.</span></span>

## <a name="syntax"></a><span data-ttu-id="5969a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5969a-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a><span data-ttu-id="5969a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5969a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5969a-107">**нентриес**</span><span class="sxs-lookup"><span data-stu-id="5969a-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="5969a-108">Число протоколов.</span><span class="sxs-lookup"><span data-stu-id="5969a-108">Number of protocols.</span></span>

</dd> <dt>

<span data-ttu-id="5969a-109">**Ввод**</span><span class="sxs-lookup"><span data-stu-id="5969a-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="5969a-110">Массив структур [PF \_ хандоффентри](pf-handoffentry.md) , определяющий каждый протокол.</span><span class="sxs-lookup"><span data-stu-id="5969a-110">An array of [PF\_HANDOFFENTRY](pf-handoffentry.md) structures that define each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5969a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5969a-111">Remarks</span></span>

<span data-ttu-id="5969a-112">Структура [PF \_ парсеринфо](pf-parserinfo.md) использует структуру **PF \_ хандоффсет** для перечисления следующих целей:</span><span class="sxs-lookup"><span data-stu-id="5969a-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_HANDOFFSET** structure to list the following:</span></span>

-   <span data-ttu-id="5969a-113">Какие протоколы передаются средству синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="5969a-113">Which protocols hand off to the parser.</span></span>
-   <span data-ttu-id="5969a-114">Протоколы, к которым средство синтаксического анализа передает.</span><span class="sxs-lookup"><span data-stu-id="5969a-114">Which protocols the parser hands off to.</span></span>

<span data-ttu-id="5969a-115">Структура **PF \_ хандоффсет** должна быть выделена с помощью **хеапаллок**.</span><span class="sxs-lookup"><span data-stu-id="5969a-115">The **PF\_HANDOFFSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5969a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="5969a-116">Requirements</span></span>



| <span data-ttu-id="5969a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="5969a-117">Requirement</span></span> | <span data-ttu-id="5969a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="5969a-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5969a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5969a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5969a-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5969a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5969a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5969a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5969a-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5969a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5969a-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5969a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5969a-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5969a-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5969a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5969a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5969a-126">PF \_ парсеринфо</span><span class="sxs-lookup"><span data-stu-id="5969a-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="5969a-127">PF \_ хандоффентри</span><span class="sxs-lookup"><span data-stu-id="5969a-127">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)
</dt> </dl>

 

 




