---
description: Используется в любом шейдере нажатия для фиксации текущего попадания, а затем для поиска большего числа попаданий для луча.
ms.assetid: ''
title: Функция AcceptHitAndEndSearch
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647143"
---
# <a name="accepthitandendsearch-function"></a><span data-ttu-id="f4a4b-103">Функция AcceptHitAndEndSearch</span><span class="sxs-lookup"><span data-stu-id="f4a4b-103">AcceptHitAndEndSearch function</span></span>

<span data-ttu-id="f4a4b-104">Используется в [любом шейдере нажатия](any-hit-shader.md) для фиксации текущего попадания, а затем для поиска большего числа попаданий для луча.</span><span class="sxs-lookup"><span data-stu-id="f4a4b-104">Used in an [any hit shader](any-hit-shader.md) to commit the current hit and then stop searching for more hits for the ray.</span></span> <span data-ttu-id="f4a4b-105">Если выполняется шейдер пересечения, выполнение останавливается.</span><span class="sxs-lookup"><span data-stu-id="f4a4b-105">If there is an intersection shader running, it's execution stops.</span></span>  <span data-ttu-id="f4a4b-106">Выполнение передается в [ближайший шейдер](closest-hit-shader.md), если он включен, при достижении ближайшей записи на данный момент.</span><span class="sxs-lookup"><span data-stu-id="f4a4b-106">Execution passes to the [closest hit shader](closest-hit-shader.md), if enabled, with the closest hit recorded so far.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a4b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4a4b-107">Syntax</span></span>

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a><span data-ttu-id="f4a4b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4a4b-108">Return Value</span></span>

<span data-ttu-id="f4a4b-109">**void**</span><span class="sxs-lookup"><span data-stu-id="f4a4b-109">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="f4a4b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4a4b-110">Remarks</span></span>

<span data-ttu-id="f4a4b-111">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="f4a4b-111">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="f4a4b-112">**Вызываемый шейдер**</span><span class="sxs-lookup"><span data-stu-id="f4a4b-112">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="f4a4b-113">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="f4a4b-113">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="f4a4b-114">**Шейдер непопаданий**</span><span class="sxs-lookup"><span data-stu-id="f4a4b-114">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="f4a4b-115">**Шейдер создания лучей**</span><span class="sxs-lookup"><span data-stu-id="f4a4b-115">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="f4a4b-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4a4b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a4b-117">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f4a4b-117">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




