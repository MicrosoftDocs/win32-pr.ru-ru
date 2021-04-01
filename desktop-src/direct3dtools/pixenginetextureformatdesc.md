---
description: Представляет описание формата текстуры.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Пиксенгинетекстуреформатдеск
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990152"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span data-ttu-id="7e6be-103"><span id="vspixengine.pixenginetextureformatdesc"></span>Структура Пиксенгинетекстуреформатдеск</span><span class="sxs-lookup"><span data-stu-id="7e6be-103"><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc structure</span></span>

<span data-ttu-id="7e6be-104">Представляет описание формата текстуры.</span><span class="sxs-lookup"><span data-stu-id="7e6be-104">Represents a description of a texture format.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e6be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e6be-105">Syntax</span></span>


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a><span data-ttu-id="7e6be-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7e6be-106">Members</span></span>

<span data-ttu-id="7e6be-107">**дксгиформат**</span><span class="sxs-lookup"><span data-stu-id="7e6be-107">**dxgiFormat**</span></span>  
<span data-ttu-id="7e6be-108">Формат DXGI текстуры.</span><span class="sxs-lookup"><span data-stu-id="7e6be-108">The DXGI format of the texture.</span></span>

<span data-ttu-id="7e6be-109">**Формат.**</span><span class="sxs-lookup"><span data-stu-id="7e6be-109">**dataFormat**</span></span>  
<span data-ttu-id="7e6be-110">Формат данных текстуры.</span><span class="sxs-lookup"><span data-stu-id="7e6be-110">The data format of the texture.</span></span>

<span data-ttu-id="7e6be-111">**блоккбитес**</span><span class="sxs-lookup"><span data-stu-id="7e6be-111">**blockBytes**</span></span>  
<span data-ttu-id="7e6be-112">Число байтов в блоке данных.</span><span class="sxs-lookup"><span data-stu-id="7e6be-112">The number of bytes in a data block.</span></span>

<span data-ttu-id="7e6be-113">**блоккхеигхт**</span><span class="sxs-lookup"><span data-stu-id="7e6be-113">**blockHeight**</span></span>  
<span data-ttu-id="7e6be-114">Высота (числовые примеры на оси Y) блока.</span><span class="sxs-lookup"><span data-stu-id="7e6be-114">The height (number samples in the Y axis) of the block.</span></span>

<span data-ttu-id="7e6be-115">**блокквидс**</span><span class="sxs-lookup"><span data-stu-id="7e6be-115">**blockWidth**</span></span>  
<span data-ttu-id="7e6be-116">Ширина (число выборок на оси X) блока.</span><span class="sxs-lookup"><span data-stu-id="7e6be-116">The width (number of samples in the X axis) of the block.</span></span>

<span data-ttu-id="7e6be-117">**чаннелкс**</span><span class="sxs-lookup"><span data-stu-id="7e6be-117">**channelX**</span></span>  
<span data-ttu-id="7e6be-118">Описывает свойства канала X.</span><span class="sxs-lookup"><span data-stu-id="7e6be-118">Describes properties of the X channel.</span></span> <span data-ttu-id="7e6be-119">Дополнительные сведения см. в разделе Структура Пиксенгинечаннелдескриптион.</span><span class="sxs-lookup"><span data-stu-id="7e6be-119">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="7e6be-120">**канал**</span><span class="sxs-lookup"><span data-stu-id="7e6be-120">**channelY**</span></span>  
<span data-ttu-id="7e6be-121">Описывает свойства канала Y.</span><span class="sxs-lookup"><span data-stu-id="7e6be-121">Describes properties of the Y channel.</span></span> <span data-ttu-id="7e6be-122">Дополнительные сведения см. в разделе Структура Пиксенгинечаннелдескриптион.</span><span class="sxs-lookup"><span data-stu-id="7e6be-122">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="7e6be-123">**чаннелз**</span><span class="sxs-lookup"><span data-stu-id="7e6be-123">**channelZ**</span></span>  
<span data-ttu-id="7e6be-124">Описывает свойства канала Z.</span><span class="sxs-lookup"><span data-stu-id="7e6be-124">Describes properties of the Z channel.</span></span> <span data-ttu-id="7e6be-125">Дополнительные сведения см. в разделе Структура Пиксенгинечаннелдескриптион.</span><span class="sxs-lookup"><span data-stu-id="7e6be-125">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="7e6be-126">**чаннелв**</span><span class="sxs-lookup"><span data-stu-id="7e6be-126">**channelW**</span></span>  
<span data-ttu-id="7e6be-127">Описание свойств канала W.</span><span class="sxs-lookup"><span data-stu-id="7e6be-127">Describes properties of the W channel.</span></span> <span data-ttu-id="7e6be-128">Дополнительные сведения см. в разделе Структура Пиксенгинечаннелдескриптион.</span><span class="sxs-lookup"><span data-stu-id="7e6be-128">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="7e6be-129">**свиззле**</span><span class="sxs-lookup"><span data-stu-id="7e6be-129">**swizzle**</span></span>  
<span data-ttu-id="7e6be-130">Описывает свиззле (обмен каналами), примененный к примеру.</span><span class="sxs-lookup"><span data-stu-id="7e6be-130">Describes the swizzle (channel-swapping) applied to the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e6be-131">Требования</span><span class="sxs-lookup"><span data-stu-id="7e6be-131">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7e6be-132">Header</span><span class="sxs-lookup"><span data-stu-id="7e6be-132">Header</span></span></p></td><td><span data-ttu-id="7e6be-133">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="7e6be-133">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



