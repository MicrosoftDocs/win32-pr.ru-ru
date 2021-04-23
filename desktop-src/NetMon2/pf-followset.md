---
description: '\_Структура следов PF определяет протоколы, которые могут предшествовать протоколу или следовать за ним.'
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: Структура PF_FOLLOWSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673969"
---
# <a name="pf_followset-structure"></a><span data-ttu-id="3b19f-103">Общая папка PF, \_ Структура</span><span class="sxs-lookup"><span data-stu-id="3b19f-103">PF\_FOLLOWSET structure</span></span>

<span data-ttu-id="3b19f-104">Структура **\_ следов PF** определяет протоколы, которые могут предшествовать протоколу или следовать за ним.</span><span class="sxs-lookup"><span data-stu-id="3b19f-104">The **PF\_FOLLOWSET** structure defines the protocols that may precede or follow a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b19f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b19f-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a><span data-ttu-id="3b19f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3b19f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b19f-107">**нентриес**</span><span class="sxs-lookup"><span data-stu-id="3b19f-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="3b19f-108">Число протоколов в списке.</span><span class="sxs-lookup"><span data-stu-id="3b19f-108">Number of protocols in the list.</span></span>

</dd> <dt>

<span data-ttu-id="3b19f-109">**Ввод**</span><span class="sxs-lookup"><span data-stu-id="3b19f-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="3b19f-110">Массив структур [PF \_ фолловентри](pf-followentry.md) , описывающих каждый протокол.</span><span class="sxs-lookup"><span data-stu-id="3b19f-110">Array of [PF\_FOLLOWENTRY](pf-followentry.md) structures that describe each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b19f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b19f-111">Remarks</span></span>

<span data-ttu-id="3b19f-112">Структура " [PF \_ парсеринфо](pf-parserinfo.md) " использует **структуру \_ следов PF** для перечисления протоколов, которые могут предшествовать или отслеживать протокол, обнаруженный анализатором.</span><span class="sxs-lookup"><span data-stu-id="3b19f-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_FOLLOWSET** structure to list the protocols that may precede or follow the protocol that the parser detects.</span></span>

<span data-ttu-id="3b19f-113">Сетевой монитор использует сведения в структуре " **Общая \_ Папка** " для обновления следующих наборов конкретных анализаторов.</span><span class="sxs-lookup"><span data-stu-id="3b19f-113">Network Monitor uses the information in the **PF\_FOLLOWSET** structure to update the follow sets of specific parsers.</span></span> <span data-ttu-id="3b19f-114">Структура **\_ следов PF** должна быть выделена с помощью **хеапаллок**.</span><span class="sxs-lookup"><span data-stu-id="3b19f-114">The **PF\_FOLLOWSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b19f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3b19f-115">Requirements</span></span>



| <span data-ttu-id="3b19f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3b19f-116">Requirement</span></span> | <span data-ttu-id="3b19f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3b19f-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b19f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b19f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3b19f-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b19f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b19f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b19f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3b19f-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3b19f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b19f-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3b19f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b19f-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b19f-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b19f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b19f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b19f-125">PF \_ фолловентри</span><span class="sxs-lookup"><span data-stu-id="3b19f-125">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)
</dt> <dt>

[<span data-ttu-id="3b19f-126">PF \_ парсеринфо</span><span class="sxs-lookup"><span data-stu-id="3b19f-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> </dl>

 

 




