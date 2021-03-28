---
title: Метод ID3DX11EffectShaderVariable Жетпатчконстантсигнатурилементдеск (D3dx11effect. h)
description: Получить описание подписи константы исправлений.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- Метод Жетпатчконстантсигнатурилементдеск Direct3D 11
- Метод Жетпатчконстантсигнатурилементдеск Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетпатчконстантсигнатурилементдеск
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fcbc8f7c1bc34b0da42dd08c255a04a6d2fc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998660"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a><span data-ttu-id="fe6cc-106">Метод ID3DX11EffectShaderVariable:: Жетпатчконстантсигнатурилементдеск</span><span class="sxs-lookup"><span data-stu-id="fe6cc-106">ID3DX11EffectShaderVariable::GetPatchConstantSignatureElementDesc method</span></span>

<span data-ttu-id="fe6cc-107">Получить описание подписи константы исправлений.</span><span class="sxs-lookup"><span data-stu-id="fe6cc-107">Get a patch constant signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe6cc-108">Syntax</span></span>


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="fe6cc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe6cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6cc-110">*шадериндекс*</span><span class="sxs-lookup"><span data-stu-id="fe6cc-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6cc-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe6cc-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe6cc-112">Индекс шейдера, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="fe6cc-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="fe6cc-113">*Элемент*</span><span class="sxs-lookup"><span data-stu-id="fe6cc-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6cc-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fe6cc-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fe6cc-115">Индекс элемента, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="fe6cc-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="fe6cc-116">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="fe6cc-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="fe6cc-117">Тип: **[ **\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="fe6cc-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="fe6cc-118">Указатель на описание параметра (см. раздел [**\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="fe6cc-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6cc-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe6cc-119">Return value</span></span>

<span data-ttu-id="fe6cc-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe6cc-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe6cc-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fe6cc-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6cc-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe6cc-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe6cc-123">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="fe6cc-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fe6cc-124">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="fe6cc-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fe6cc-125">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fe6cc-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe6cc-126">Требования</span><span class="sxs-lookup"><span data-stu-id="fe6cc-126">Requirements</span></span>



| <span data-ttu-id="fe6cc-127">Требование</span><span class="sxs-lookup"><span data-stu-id="fe6cc-127">Requirement</span></span> | <span data-ttu-id="fe6cc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="fe6cc-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6cc-129">Header</span><span class="sxs-lookup"><span data-stu-id="fe6cc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fe6cc-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe6cc-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fe6cc-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe6cc-131">Library</span></span><br/> | <dl> <span data-ttu-id="fe6cc-132"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="fe6cc-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe6cc-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe6cc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6cc-134">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="fe6cc-134">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

