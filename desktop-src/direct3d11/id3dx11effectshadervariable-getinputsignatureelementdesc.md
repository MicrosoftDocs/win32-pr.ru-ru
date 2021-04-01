---
title: Метод ID3DX11EffectShaderVariable Жетинпутсигнатурилементдеск (D3dx11effect. h)
description: Получить описание входной подписи.
ms.assetid: 45b1fd25-1005-48fd-8a61-561ea2c273e5
keywords:
- Метод Жетинпутсигнатурилементдеск Direct3D 11
- Метод Жетинпутсигнатурилементдеск Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетинпутсигнатурилементдеск
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetInputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf788370c26da1ba773d797de544b1a64750d90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157267"
---
# <a name="id3dx11effectshadervariablegetinputsignatureelementdesc-method"></a><span data-ttu-id="9a12b-106">Метод ID3DX11EffectShaderVariable:: Жетинпутсигнатурилементдеск</span><span class="sxs-lookup"><span data-stu-id="9a12b-106">ID3DX11EffectShaderVariable::GetInputSignatureElementDesc method</span></span>

<span data-ttu-id="9a12b-107">Получить описание входной подписи.</span><span class="sxs-lookup"><span data-stu-id="9a12b-107">Get an input-signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a12b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a12b-108">Syntax</span></span>


```C++
HRESULT GetInputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="9a12b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a12b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a12b-110">*шадериндекс*</span><span class="sxs-lookup"><span data-stu-id="9a12b-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="9a12b-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a12b-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a12b-112">Индекс шейдера, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="9a12b-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="9a12b-113">*Элемент*</span><span class="sxs-lookup"><span data-stu-id="9a12b-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="9a12b-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a12b-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a12b-115">Индекс элемента шейдера, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="9a12b-115">A zero-based shader-element index.</span></span>

</dd> <dt>

<span data-ttu-id="9a12b-116">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="9a12b-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="9a12b-117">Тип: **[ **\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="9a12b-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="9a12b-118">Указатель на описание параметра (см. раздел [**\_ параметр подписи \_ D3D11 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="9a12b-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a12b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a12b-119">Return value</span></span>

<span data-ttu-id="9a12b-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a12b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a12b-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9a12b-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a12b-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a12b-122">Remarks</span></span>

<span data-ttu-id="9a12b-123">Результат содержит один или несколько шейдеров; Каждый шейдер имеет входную и выходную сигнатуру; Каждая сигнатура содержит один или несколько элементов (или параметров).</span><span class="sxs-lookup"><span data-stu-id="9a12b-123">An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters).</span></span> <span data-ttu-id="9a12b-124">Индекс шейдера определяет шейдер, а индекс элемента определяет элемент (или параметр) в сигнатуре шейдера.</span><span class="sxs-lookup"><span data-stu-id="9a12b-124">The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.</span></span>

> [!Note]  
> <span data-ttu-id="9a12b-125">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="9a12b-125">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9a12b-126">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="9a12b-126">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9a12b-127">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9a12b-127">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a12b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9a12b-128">Requirements</span></span>



| <span data-ttu-id="9a12b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9a12b-129">Requirement</span></span> | <span data-ttu-id="9a12b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9a12b-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a12b-131">Header</span><span class="sxs-lookup"><span data-stu-id="9a12b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9a12b-132"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a12b-132"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9a12b-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a12b-133">Library</span></span><br/> | <dl> <span data-ttu-id="9a12b-134"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="9a12b-134"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a12b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a12b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a12b-136">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="9a12b-136">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

