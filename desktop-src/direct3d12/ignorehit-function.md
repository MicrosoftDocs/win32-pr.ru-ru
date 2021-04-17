---
description: Вызывается из любого шейдера нажатия, чтобы отклонить попадание и завершить шейдер.
ms.assetid: ''
title: Функция IgnoreHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692032"
---
# <a name="ignorehit-function"></a><span data-ttu-id="a28dc-103">Функция IgnoreHit</span><span class="sxs-lookup"><span data-stu-id="a28dc-103">IgnoreHit function</span></span>

<span data-ttu-id="a28dc-104">Вызывается из [любого шейдера нажатия](any-hit-shader.md) , чтобы отклонить попадание и завершить шейдер.</span><span class="sxs-lookup"><span data-stu-id="a28dc-104">Called from an [any hit shader](any-hit-shader.md) to reject the hit and end the shader.</span></span> <span data-ttu-id="a28dc-105">Поиск курсоров продолжится без фиксации расстояния и атрибутов для текущего попадания.</span><span class="sxs-lookup"><span data-stu-id="a28dc-105">The hit search continues on without committing the distance and attributes for the current hit.</span></span>  <span data-ttu-id="a28dc-106">Вызов [**репорсит**](reporthit-function.md) в [шейдере пересечения](intersection-shader.md), если таковой имеется, возвратит значение false.</span><span class="sxs-lookup"><span data-stu-id="a28dc-106">The [**ReportHit**](reporthit-function.md) call in the [intersection shader](intersection-shader.md), if there is one, will return false.</span></span>  <span data-ttu-id="a28dc-107">Все изменения, внесенные в полезные данные лучей вплоть до этой точки в шейдере, сохраняются.</span><span class="sxs-lookup"><span data-stu-id="a28dc-107">Any modifications made to the ray payload up to this point in the any hit shader are preserved.</span></span>

## <a name="syntax"></a><span data-ttu-id="a28dc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a28dc-108">Syntax</span></span>

```
void IgnoreHit();

```


## <a name="return-value"></a><span data-ttu-id="a28dc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a28dc-109">Return Value</span></span>

<span data-ttu-id="a28dc-110">**void**</span><span class="sxs-lookup"><span data-stu-id="a28dc-110">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="a28dc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a28dc-111">Remarks</span></span>

<span data-ttu-id="a28dc-112">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="a28dc-112">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="a28dc-113">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="a28dc-113">**Any Hit Shader**</span></span>](any-hit-shader.md)




## <a name="see-also"></a><span data-ttu-id="a28dc-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a28dc-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28dc-115">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a28dc-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




