---
description: Перечисление, содержащее флаги, используемые для описания результата журнала пикселей. См. Пикселхисторйоператион.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление ПИКСЕЛХИСТОРИФЛАГС
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139758"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span data-ttu-id="861a1-104"><span id="vspixengine.pixelhistoryflags"></span>Перечисление ПИКСЕЛХИСТОРИФЛАГС</span><span class="sxs-lookup"><span data-stu-id="861a1-104"><span id="vspixengine.pixelhistoryflags"></span>PIXELHISTORYFLAGS enumeration</span></span>

<span data-ttu-id="861a1-105">Перечисление, содержащее флаги, используемые для описания результата журнала пикселей.</span><span class="sxs-lookup"><span data-stu-id="861a1-105">An enum containing flags used to describe a pixel history result.</span></span> <span data-ttu-id="861a1-106">См. Пикселхисторйоператион.</span><span class="sxs-lookup"><span data-stu-id="861a1-106">See PixelHistoryOperation.</span></span>

## <a name="syntax"></a><span data-ttu-id="861a1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="861a1-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="861a1-108">Константы</span><span class="sxs-lookup"><span data-stu-id="861a1-108">Constants</span></span>

<span data-ttu-id="861a1-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**ФФ \_ инитиалвалуе**</span><span class="sxs-lookup"><span data-stu-id="861a1-109"><span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF\_INITIALVALUE**</span></span>  
<span data-ttu-id="861a1-110">Флаг, соответствующий начальному значению цвета (до кадра).</span><span class="sxs-lookup"><span data-stu-id="861a1-110">A flag that corresponds to the initial color value (prior to frame).</span></span>

<span data-ttu-id="861a1-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**ФФ \_ очистить**</span><span class="sxs-lookup"><span data-stu-id="861a1-111"><span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF\_CLEAR**</span></span>  
<span data-ttu-id="861a1-112">Флаг, соответствующий результату очистки цвета.</span><span class="sxs-lookup"><span data-stu-id="861a1-112">A flag that corresponds to the clear color result.</span></span>

<span data-ttu-id="861a1-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**ФФ \_ Draw**</span><span class="sxs-lookup"><span data-stu-id="861a1-113"><span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF\_DRAW**</span></span>  
<span data-ttu-id="861a1-114">Флаг, соответствующий цвету результат рисования.</span><span class="sxs-lookup"><span data-stu-id="861a1-114">A flag that corresponds to the draw color result.</span></span>

<span data-ttu-id="861a1-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**ФФ \_ финалвалуе**</span><span class="sxs-lookup"><span data-stu-id="861a1-115"><span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF\_FINALVALUE**</span></span>  
<span data-ttu-id="861a1-116">Флаг, соответствующий последнему результату цвета.</span><span class="sxs-lookup"><span data-stu-id="861a1-116">A flag that corresponds to the final color result.</span></span>

<span data-ttu-id="861a1-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**ФФ \_ хасколор**</span><span class="sxs-lookup"><span data-stu-id="861a1-117"><span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF\_HASCOLOR**</span></span>  
<span data-ttu-id="861a1-118">Флаг, который соответствует тому, имеется ли в структуре Пикселхисторйоператион цветовой результат.</span><span class="sxs-lookup"><span data-stu-id="861a1-118">A flag that corresponds to whether the color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="861a1-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**ФФ \_ хасфбколор**</span><span class="sxs-lookup"><span data-stu-id="861a1-119"><span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF\_HASFBCOLOR**</span></span>  
<span data-ttu-id="861a1-120">Флаг, который соответствует, имеется ли конечный результат цвета буфера в структуре Пикселхисторйоператион.</span><span class="sxs-lookup"><span data-stu-id="861a1-120">A flag that corresponds to whether the final buffer color result is present in the PixelHistoryOperation struct.</span></span>

<span data-ttu-id="861a1-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**ФФ, \_ Ошибка**</span><span class="sxs-lookup"><span data-stu-id="861a1-121"><span id="PHF_ERROR"></span><span id="phf_error"></span>**PHF\_ERROR**</span></span>  

<span data-ttu-id="861a1-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**ФФ \_ вертекспроцессингскиппед**</span><span class="sxs-lookup"><span data-stu-id="861a1-122"><span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF\_VERTEXPROCESSINGSKIPPED**</span></span>  
<span data-ttu-id="861a1-123">Не используется.</span><span class="sxs-lookup"><span data-stu-id="861a1-123">Not used.</span></span>

<span data-ttu-id="861a1-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**ФФ \_ модифиресаурце**</span><span class="sxs-lookup"><span data-stu-id="861a1-124"><span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF\_MODIFYRESOURCE**</span></span>  

<span data-ttu-id="861a1-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**ФФ \_ каннотрунфуллдепсстенЦилтест**</span><span class="sxs-lookup"><span data-stu-id="861a1-125"><span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF\_CANNOTRUNFULLDEPTHSTENCILTEST**</span></span>  
<span data-ttu-id="861a1-126">Флаг, который соответствует невозможности выполнения теста глубины или трафарета.</span><span class="sxs-lookup"><span data-stu-id="861a1-126">A flag that corresponds to not being able to run the depth or stencil test.</span></span>

## <a name="requirements"></a><span data-ttu-id="861a1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="861a1-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="861a1-128">Header</span><span class="sxs-lookup"><span data-stu-id="861a1-128">Header</span></span></p></td><td><span data-ttu-id="861a1-129">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="861a1-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



