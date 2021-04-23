---
title: Метод ID3DX11EffectShaderVariable Жетшадердеск (D3dx11effect. h)
description: Получение описания шейдера.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- Метод Жетшадердеск Direct3D 11
- Метод Жетшадердеск Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетшадердеск
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c76730d1ad5f3de35e273034d3a17beb71fb7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987104"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a><span data-ttu-id="5585c-106">Метод ID3DX11EffectShaderVariable:: Жетшадердеск</span><span class="sxs-lookup"><span data-stu-id="5585c-106">ID3DX11EffectShaderVariable::GetShaderDesc method</span></span>

<span data-ttu-id="5585c-107">Получение описания шейдера.</span><span class="sxs-lookup"><span data-stu-id="5585c-107">Get a shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5585c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5585c-108">Syntax</span></span>


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="5585c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5585c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5585c-110">*шадериндекс*</span><span class="sxs-lookup"><span data-stu-id="5585c-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="5585c-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5585c-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5585c-112">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="5585c-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="5585c-113">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="5585c-113">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="5585c-114">Тип: **[ **D3DX11 \_ Effect \_ Shader \_ DESC**](d3dx11-effect-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="5585c-114">Type: **[**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)\***</span></span>

<span data-ttu-id="5585c-115">Указатель на описание шейдера (см. [**D3DX11 \_ Effect \_ Shader \_ DESC**](d3dx11-effect-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="5585c-115">A pointer to a shader description (see [**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5585c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5585c-116">Return value</span></span>

<span data-ttu-id="5585c-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5585c-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5585c-118">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5585c-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5585c-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="5585c-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5585c-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="5585c-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5585c-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="5585c-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5585c-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5585c-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5585c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5585c-123">Requirements</span></span>



| <span data-ttu-id="5585c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5585c-124">Requirement</span></span> | <span data-ttu-id="5585c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5585c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5585c-126">Header</span><span class="sxs-lookup"><span data-stu-id="5585c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5585c-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5585c-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5585c-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5585c-128">Library</span></span><br/> | <dl> <span data-ttu-id="5585c-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="5585c-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5585c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5585c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5585c-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="5585c-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

