---
title: Метод ID3DX11EffectShaderVariable Жетаутпутсигнатурилементдеск (D3dx11effect. h)
description: Получение описания выходной подписи.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- Метод Жетаутпутсигнатурилементдеск Direct3D 11
- Метод Жетаутпутсигнатурилементдеск Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетаутпутсигнатурилементдеск
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetOutputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29545754be560a3a7710adf23963566a324d8a3f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998663"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a><span data-ttu-id="55053-106">Метод ID3DX11EffectShaderVariable:: Жетаутпутсигнатурилементдеск</span><span class="sxs-lookup"><span data-stu-id="55053-106">ID3DX11EffectShaderVariable::GetOutputSignatureElementDesc method</span></span>

<span data-ttu-id="55053-107">Получение описания выходной подписи.</span><span class="sxs-lookup"><span data-stu-id="55053-107">Get an output-signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="55053-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55053-108">Syntax</span></span>


```C++
HRESULT GetOutputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="55053-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="55053-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55053-110">*шадериндекс*</span><span class="sxs-lookup"><span data-stu-id="55053-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="55053-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55053-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="55053-112">Индекс шейдера, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="55053-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="55053-113">*Элемент*</span><span class="sxs-lookup"><span data-stu-id="55053-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="55053-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55053-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="55053-115">Индекс элемента, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="55053-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="55053-116">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="55053-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="55053-117">Тип: **[ **\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="55053-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="55053-118">Указатель на описание параметра (см. раздел [**\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="55053-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55053-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55053-119">Return value</span></span>

<span data-ttu-id="55053-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55053-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55053-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="55053-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55053-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="55053-122">Remarks</span></span>

<span data-ttu-id="55053-123">Результат содержит один или несколько шейдеров; Каждый шейдер имеет входную и выходную сигнатуру; Каждая сигнатура содержит один или несколько элементов (или параметров).</span><span class="sxs-lookup"><span data-stu-id="55053-123">An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters).</span></span> <span data-ttu-id="55053-124">Индекс шейдера определяет шейдер, а индекс элемента определяет элемент (или параметр) в сигнатуре шейдера.</span><span class="sxs-lookup"><span data-stu-id="55053-124">The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.</span></span>

> [!Note]  
> <span data-ttu-id="55053-125">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="55053-125">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="55053-126">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="55053-126">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="55053-127">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="55053-127">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="55053-128">Требования</span><span class="sxs-lookup"><span data-stu-id="55053-128">Requirements</span></span>



| <span data-ttu-id="55053-129">Требование</span><span class="sxs-lookup"><span data-stu-id="55053-129">Requirement</span></span> | <span data-ttu-id="55053-130">Значение</span><span class="sxs-lookup"><span data-stu-id="55053-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55053-131">Header</span><span class="sxs-lookup"><span data-stu-id="55053-131">Header</span></span><br/>  | <dl> <span data-ttu-id="55053-132"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="55053-132"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="55053-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55053-133">Library</span></span><br/> | <dl> <span data-ttu-id="55053-134"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="55053-134"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55053-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55053-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55053-136">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="55053-136">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

