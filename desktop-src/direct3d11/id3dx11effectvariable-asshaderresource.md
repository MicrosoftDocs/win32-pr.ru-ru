---
title: Метод ID3DX11EffectVariable Асшадерресаурце (D3dx11effect. h)
description: Получение переменной-ресурса шейдера.
ms.assetid: 02db94eb-980a-4677-af89-3006aef6faca
keywords:
- Метод Асшадерресаурце Direct3D 11
- Метод Асшадерресаурце Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асшадерресаурце
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShaderResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3af6236d25e8a2c652f5a551bf7199f3a78d8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998774"
---
# <a name="id3dx11effectvariableasshaderresource-method"></a><span data-ttu-id="92331-106">Метод ID3DX11EffectVariable:: Асшадерресаурце</span><span class="sxs-lookup"><span data-stu-id="92331-106">ID3DX11EffectVariable::AsShaderResource method</span></span>

<span data-ttu-id="92331-107">Получение переменной-ресурса шейдера.</span><span class="sxs-lookup"><span data-stu-id="92331-107">Get a shader-resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="92331-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92331-108">Syntax</span></span>


```C++
ID3DX11EffectShaderResourceVariable* AsShaderResource();
```



## <a name="parameters"></a><span data-ttu-id="92331-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="92331-109">Parameters</span></span>

<span data-ttu-id="92331-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="92331-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92331-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92331-111">Return value</span></span>

<span data-ttu-id="92331-112">Тип: **[ **ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="92331-112">Type: **[**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md)\***</span></span>

<span data-ttu-id="92331-113">Указатель на переменную-ресурс шейдера.</span><span class="sxs-lookup"><span data-stu-id="92331-113">A pointer to a shader-resource variable.</span></span> <span data-ttu-id="92331-114">См. [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).</span><span class="sxs-lookup"><span data-stu-id="92331-114">See [**ID3DX11EffectShaderResourceVariable**](id3dx11effectshaderresourcevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92331-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="92331-115">Remarks</span></span>

<span data-ttu-id="92331-116">Асшадерресаурце Возвращает версию переменной Effect, которая была специализированной для переменной-ресурса шейдера.</span><span class="sxs-lookup"><span data-stu-id="92331-116">AsShaderResource returns a version of the effect variable that has been specialized to a shader-resource variable.</span></span> <span data-ttu-id="92331-117">Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит данных о ресурсах шейдера.</span><span class="sxs-lookup"><span data-stu-id="92331-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader-resource data.</span></span>

<span data-ttu-id="92331-118">Приложения могут проверить возвращаемый объект на допустимость, вызвав [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="92331-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="92331-119">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="92331-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="92331-120">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="92331-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="92331-121">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="92331-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92331-122">Требования</span><span class="sxs-lookup"><span data-stu-id="92331-122">Requirements</span></span>



| <span data-ttu-id="92331-123">Требование</span><span class="sxs-lookup"><span data-stu-id="92331-123">Requirement</span></span> | <span data-ttu-id="92331-124">Значение</span><span class="sxs-lookup"><span data-stu-id="92331-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92331-125">Header</span><span class="sxs-lookup"><span data-stu-id="92331-125">Header</span></span><br/>  | <dl> <span data-ttu-id="92331-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="92331-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="92331-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92331-127">Library</span></span><br/> | <dl> <span data-ttu-id="92331-128"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="92331-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92331-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92331-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92331-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="92331-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





