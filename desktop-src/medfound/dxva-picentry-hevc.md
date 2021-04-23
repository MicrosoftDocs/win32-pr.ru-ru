---
description: Задает ссылку на несжатую поверхность.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: Структура DXVA_PicEntry_HEVC (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647151"
---
# <a name="dxva_picentry_hevc-structure"></a><span data-ttu-id="e7414-103">\_ \_ Структура HEVC пицентри дксва</span><span class="sxs-lookup"><span data-stu-id="e7414-103">DXVA\_PicEntry\_HEVC structure</span></span>

<span data-ttu-id="e7414-104">Задает ссылку на несжатую поверхность.</span><span class="sxs-lookup"><span data-stu-id="e7414-104">Specifies a reference to an uncompressed surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7414-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7414-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a><span data-ttu-id="e7414-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e7414-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7414-107">**Index7Bits**</span><span class="sxs-lookup"><span data-stu-id="e7414-107">**Index7Bits**</span></span>
</dt> <dd>

<span data-ttu-id="e7414-108">Индекс, определяющий несжатую поверхность.</span><span class="sxs-lookup"><span data-stu-id="e7414-108">An index that identifies an uncompressed surface .</span></span>

</dd> <dt>

<span data-ttu-id="e7414-109">**ассоЦиатедфлаг**</span><span class="sxs-lookup"><span data-stu-id="e7414-109">**AssociatedFlag**</span></span> 
</dt> <dd>

<span data-ttu-id="e7414-110">Необязательный 1-разрядный флаг, связанный с поверхностью.</span><span class="sxs-lookup"><span data-stu-id="e7414-110">Optional 1-bit flag associated with the surface.</span></span> <span data-ttu-id="e7414-111">Значение флага зависит от контекста.</span><span class="sxs-lookup"><span data-stu-id="e7414-111">The meaning of the flag depends on the context.</span></span> <span data-ttu-id="e7414-112">Например, он может указать, является ли ссылочный кадр долгосрочной ссылкой или краткосрочной ссылкой.</span><span class="sxs-lookup"><span data-stu-id="e7414-112">For example, it can specify whether the reference frame is a long-term reference or a short-term reference.</span></span>

</dd> <dt>

<span data-ttu-id="e7414-113">**бпицентри**</span><span class="sxs-lookup"><span data-stu-id="e7414-113">**bPicEntry**</span></span>
</dt> <dd>

<span data-ttu-id="e7414-114">Обращается ко всем 8 битам объединения.</span><span class="sxs-lookup"><span data-stu-id="e7414-114">Accesses the entire 8 bits of the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7414-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e7414-115">Requirements</span></span>



| <span data-ttu-id="e7414-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e7414-116">Requirement</span></span> | <span data-ttu-id="e7414-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e7414-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e7414-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7414-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e7414-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e7414-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e7414-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7414-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e7414-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7414-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e7414-122">Header</span><span class="sxs-lookup"><span data-stu-id="e7414-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7414-123"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7414-123"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7414-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7414-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7414-125">Структуры Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7414-125">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




