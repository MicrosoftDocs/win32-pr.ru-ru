---
description: Структура PF \_ фолловентри определяет протокол, который сетевой монитор добавляется в следующий набор средства синтаксического анализа.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Структура PF_FOLLOWENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910880"
---
# <a name="pf_followentry-structure"></a><span data-ttu-id="427ed-103">\_Структура PF фолловентри</span><span class="sxs-lookup"><span data-stu-id="427ed-103">PF\_FOLLOWENTRY structure</span></span>

<span data-ttu-id="427ed-104">Структура **PF \_ фолловентри** определяет протокол, который сетевой монитор добавляется в следующий набор средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="427ed-104">The **PF\_FOLLOWENTRY** structure defines a protocol that Network Monitor adds to the follow set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="427ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="427ed-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a><span data-ttu-id="427ed-106">Члены</span><span class="sxs-lookup"><span data-stu-id="427ed-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="427ed-107">**сзпротокол**</span><span class="sxs-lookup"><span data-stu-id="427ed-107">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="427ed-108">Имя протокола.</span><span class="sxs-lookup"><span data-stu-id="427ed-108">The name of the protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="427ed-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="427ed-109">Remarks</span></span>

<span data-ttu-id="427ed-110">В [структуре \_ следов PF](pf-followset.md) используется массив структур **PF \_ фолловентри** .</span><span class="sxs-lookup"><span data-stu-id="427ed-110">The [PF\_FOLLOWSET](pf-followset.md) structure uses an array of **PF\_FOLLOWENTRY** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="427ed-111">Требования</span><span class="sxs-lookup"><span data-stu-id="427ed-111">Requirements</span></span>



| <span data-ttu-id="427ed-112">Требование</span><span class="sxs-lookup"><span data-stu-id="427ed-112">Requirement</span></span> | <span data-ttu-id="427ed-113">Значение</span><span class="sxs-lookup"><span data-stu-id="427ed-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="427ed-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="427ed-114">Minimum supported client</span></span><br/> | <span data-ttu-id="427ed-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="427ed-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="427ed-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="427ed-116">Minimum supported server</span></span><br/> | <span data-ttu-id="427ed-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="427ed-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="427ed-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="427ed-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="427ed-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="427ed-119"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="427ed-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="427ed-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="427ed-121">\_следующий PF</span><span class="sxs-lookup"><span data-stu-id="427ed-121">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> </dl>

 

 




