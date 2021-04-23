---
title: Структура полезной нагрузки лучей
description: Определяемая пользователем структура, предоставляемая как аргумент Inout в вызове Трацерай, и как параметр Inout в типах шейдеров, которые могут обращаться к полезной нагрузке лучей.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 9887bbadc2fd94b2e766c568a30fd6669f51e048
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "105703422"
---
# <a name="ray-payload-structure"></a><span data-ttu-id="c9a18-103">Структура полезной нагрузки лучей</span><span class="sxs-lookup"><span data-stu-id="c9a18-103">Ray payload structure</span></span> 

<span data-ttu-id="c9a18-104">Определяемая пользователем структура, предоставляемая как аргумент Inout в вызове [**трацерай**](traceray-function.md) , и в качестве параметра Inout в типах шейдеров, которые могут обращаться к полезной нагрузке луча, в том числе к [любым нажатиям](any-hit-shader.md), [ближайшему попаданию](closest-hit-shader.md)и шейдеру [промахов](miss-shader.md) .</span><span class="sxs-lookup"><span data-stu-id="c9a18-104">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload, which include [any hit](any-hit-shader.md), [closest hit](closest-hit-shader.md), and [miss](miss-shader.md) shaders.</span></span> <span data-ttu-id="c9a18-105">Любые шейдеры, обращающиеся к полезной нагрузке Ray, должны использовать ту же структуру, что и в исходном вызове **трацерай** .</span><span class="sxs-lookup"><span data-stu-id="c9a18-105">Any shaders that access the ray payload must use the same structure as the one provided at the originating **TraceRay** call.</span></span>  <span data-ttu-id="c9a18-106">Даже если один из этих шейдеров не ссылается на полезные данные лучей, он по-прежнему должен указывать соответствующие полезные данные в качестве исходного вызова **трацерай** .</span><span class="sxs-lookup"><span data-stu-id="c9a18-106">Even if one of these shaders doesn’t reference the ray payload at all, it still must specify the matching payload as the originating **TraceRay** call.</span></span>

