---
description: Представляет описание среза текстуры.
MS-HAID: vspixengine.PixEngineTextureSliceDescriptor
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Пиксенгинетекстуреслицедескриптор
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1A183AFB-0BEF-4474-A60C-DBCFA4B34604
api_name:
- PixEngineTextureSliceDescriptor
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b80a23a5ec3340b775c314f66651926743249ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139639"
---
# <a name="span-idvspixenginepixenginetextureslicedescriptorspanpixenginetextureslicedescriptor-structure"></a><span data-ttu-id="d49bc-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>Структура Пиксенгинетекстуреслицедескриптор</span><span class="sxs-lookup"><span data-stu-id="d49bc-103"><span id="vspixengine.pixenginetextureslicedescriptor"></span>PixEngineTextureSliceDescriptor structure</span></span>

<span data-ttu-id="d49bc-104">Представляет описание среза текстуры.</span><span class="sxs-lookup"><span data-stu-id="d49bc-104">Represents a description of a texture slice.</span></span>

## <a name="syntax"></a><span data-ttu-id="d49bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d49bc-105">Syntax</span></span>


```C++
} PixEngineTextureSliceDescriptor;
```

## <a name="members"></a><span data-ttu-id="d49bc-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d49bc-106">Members</span></span>

<span data-ttu-id="d49bc-107">**width**</span><span class="sxs-lookup"><span data-stu-id="d49bc-107">**width**</span></span>  
<span data-ttu-id="d49bc-108">Ширина (число выборок на оси X) среза.</span><span class="sxs-lookup"><span data-stu-id="d49bc-108">The width (number of samples in the X axis) of the slice.</span></span>

<span data-ttu-id="d49bc-109">**height**</span><span class="sxs-lookup"><span data-stu-id="d49bc-109">**height**</span></span>  
<span data-ttu-id="d49bc-110">Высота (число выборок на оси Y) среза.</span><span class="sxs-lookup"><span data-stu-id="d49bc-110">The height (number of samples in the Y axis) of the slice.</span></span>

<span data-ttu-id="d49bc-111">**блоккровбитес**</span><span class="sxs-lookup"><span data-stu-id="d49bc-111">**blockRowBytes**</span></span>  
<span data-ttu-id="d49bc-112">Число байтов в каждой строке в каждом блоке.</span><span class="sxs-lookup"><span data-stu-id="d49bc-112">The number of bytes per row in each block.</span></span>

<span data-ttu-id="d49bc-113">**offset**</span><span class="sxs-lookup"><span data-stu-id="d49bc-113">**offset**</span></span>  
<span data-ttu-id="d49bc-114">Смещение среза в пределах всей текстуры.</span><span class="sxs-lookup"><span data-stu-id="d49bc-114">The offset of the slice within the whole texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d49bc-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d49bc-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d49bc-116">Header</span><span class="sxs-lookup"><span data-stu-id="d49bc-116">Header</span></span></p></td><td><span data-ttu-id="d49bc-117">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="d49bc-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



