---
description: Вызывает другой шейдер из шейдера.
ms.assetid: ''
title: Функция CallShader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710718"
---
# <a name="callshader-function"></a><span data-ttu-id="7b4bf-103">Функция CallShader</span><span class="sxs-lookup"><span data-stu-id="7b4bf-103">CallShader function</span></span>

<span data-ttu-id="7b4bf-104">Вызывает другой шейдер из шейдера.</span><span class="sxs-lookup"><span data-stu-id="7b4bf-104">Invokes another shader from within a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b4bf-105">Syntax</span></span>
<span data-ttu-id="7b4bf-106">Это встроенное определение функции эквивалентно следующему шаблону функции:</span><span class="sxs-lookup"><span data-stu-id="7b4bf-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a><span data-ttu-id="7b4bf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b4bf-107">Parameters</span></span>

`ShaderIndex`

<span data-ttu-id="7b4bf-108">Целое число без знака, представляющее индекс в [вызываемой таблице шейдеров](callable-shader.md) , указанной в вызове [**диспатчрайс**] (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.</span><span class="sxs-lookup"><span data-stu-id="7b4bf-108">An unsigned integer representing the index into the [callable shader](callable-shader.md) table specified in the call to [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.</span></span>

`Parameter`

<span data-ttu-id="7b4bf-109">Определяемые пользователем параметры для передачи в вызываемый шейдер.</span><span class="sxs-lookup"><span data-stu-id="7b4bf-109">The user-defined parameters to pass to the callable shader.</span></span>  <span data-ttu-id="7b4bf-110">Эта структура параметра должна соответствовать структуре параметров, используемой в вызываемом шейдере, на которую указывает в таблице шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7b4bf-110">This parameter structure must match the parameter structure used in the callable shader pointed to in the shader table.</span></span>


## <a name="return-value"></a><span data-ttu-id="7b4bf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b4bf-111">Return Value</span></span>

<span data-ttu-id="7b4bf-112">**void**</span><span class="sxs-lookup"><span data-stu-id="7b4bf-112">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="7b4bf-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b4bf-113">Remarks</span></span>

<span data-ttu-id="7b4bf-114">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="7b4bf-114">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="7b4bf-115">**Вызываемый шейдер**</span><span class="sxs-lookup"><span data-stu-id="7b4bf-115">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="7b4bf-116">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="7b4bf-116">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="7b4bf-117">**Шейдер непопаданий**</span><span class="sxs-lookup"><span data-stu-id="7b4bf-117">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="7b4bf-118">**Шейдер создания лучей**</span><span class="sxs-lookup"><span data-stu-id="7b4bf-118">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="7b4bf-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b4bf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4bf-120">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7b4bf-120">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




