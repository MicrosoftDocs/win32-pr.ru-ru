---
title: Метод ID3DX11EffectShaderVariable Жетжеометришадер (D3dx11effect. h)
description: Получение шейдера Geometry.
ms.assetid: 395d5c92-a941-4fbf-9bb9-b43634c1810b
keywords:
- Метод Жетжеометришадер Direct3D 11
- Метод Жетжеометришадер Direct3D 11, интерфейс ID3DX11EffectShaderVariable
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, метод Жетжеометришадер
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetGeometryShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe30478d84e0048ff7a56e5bd8faee8d50548417
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355733"
---
# <a name="id3dx11effectshadervariablegetgeometryshader-method"></a><span data-ttu-id="04f6f-106">Метод ID3DX11EffectShaderVariable:: Жетжеометришадер</span><span class="sxs-lookup"><span data-stu-id="04f6f-106">ID3DX11EffectShaderVariable::GetGeometryShader method</span></span>

<span data-ttu-id="04f6f-107">Получение шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="04f6f-107">Get a geometry shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="04f6f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04f6f-108">Syntax</span></span>


```C++
HRESULT GetGeometryShader(
   UINT                 ShaderIndex,
   ID3D11GeometryShader **ppGS
);
```



## <a name="parameters"></a><span data-ttu-id="04f6f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="04f6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f6f-110">*шадериндекс*</span><span class="sxs-lookup"><span data-stu-id="04f6f-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="04f6f-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="04f6f-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="04f6f-112">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="04f6f-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="04f6f-113">*ппгс*</span><span class="sxs-lookup"><span data-stu-id="04f6f-113">*ppGS*</span></span> 
</dt> <dd>

<span data-ttu-id="04f6f-114">Тип: **[ **ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="04f6f-114">Type: **[**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***</span></span>

<span data-ttu-id="04f6f-115">Указатель на указатель [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) , для которого будет задан шейдер Geometry при возврате.</span><span class="sxs-lookup"><span data-stu-id="04f6f-115">A pointer to an [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) pointer that will be set to the geometry shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f6f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04f6f-116">Return value</span></span>

<span data-ttu-id="04f6f-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04f6f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04f6f-118">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="04f6f-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04f6f-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="04f6f-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="04f6f-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="04f6f-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="04f6f-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="04f6f-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="04f6f-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="04f6f-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04f6f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="04f6f-123">Requirements</span></span>



| <span data-ttu-id="04f6f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="04f6f-124">Requirement</span></span> | <span data-ttu-id="04f6f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="04f6f-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f6f-126">Header</span><span class="sxs-lookup"><span data-stu-id="04f6f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="04f6f-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="04f6f-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="04f6f-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="04f6f-128">Library</span></span><br/> | <dl> <span data-ttu-id="04f6f-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="04f6f-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f6f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04f6f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f6f-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="04f6f-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

