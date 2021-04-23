---
title: Метод ID3DX11EffectPass Жетвертексшадердеск (D3dx11effect. h)
description: Получите описание вершинного шейдера.
ms.assetid: 7e02a438-2ff4-4e32-bc16-d112aafa57cb
keywords:
- Метод Жетвертексшадердеск Direct3D 11
- Метод Жетвертексшадердеск Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Жетвертексшадердеск
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetVertexShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8c69bab360fa3d12ccfc1a701926183dad7bbe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000472"
---
# <a name="id3dx11effectpassgetvertexshaderdesc-method"></a><span data-ttu-id="bd914-106">Метод ID3DX11EffectPass:: Жетвертексшадердеск</span><span class="sxs-lookup"><span data-stu-id="bd914-106">ID3DX11EffectPass::GetVertexShaderDesc method</span></span>

<span data-ttu-id="bd914-107">Получите описание вершинного шейдера.</span><span class="sxs-lookup"><span data-stu-id="bd914-107">Get a vertex-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd914-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd914-108">Syntax</span></span>


```C++
HRESULT GetVertexShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="bd914-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd914-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd914-110">*пдеск*</span><span class="sxs-lookup"><span data-stu-id="bd914-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="bd914-111">Тип: **[ **D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd914-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="bd914-112">Указатель на описание вершинного шейдера (см. раздел [**D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="bd914-112">A pointer to a vertex-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd914-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd914-113">Return value</span></span>

<span data-ttu-id="bd914-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd914-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd914-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bd914-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd914-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="bd914-116">Remarks</span></span>

<span data-ttu-id="bd914-117">Передача результата может содержать назначения состояния визуализации и назначения объектов шейдера.</span><span class="sxs-lookup"><span data-stu-id="bd914-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="bd914-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="bd914-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bd914-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="bd914-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bd914-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bd914-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd914-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bd914-121">Requirements</span></span>



| <span data-ttu-id="bd914-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bd914-122">Requirement</span></span> | <span data-ttu-id="bd914-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bd914-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd914-124">Header</span><span class="sxs-lookup"><span data-stu-id="bd914-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bd914-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd914-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bd914-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bd914-126">Library</span></span><br/> | <dl> <span data-ttu-id="bd914-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="bd914-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd914-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd914-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd914-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="bd914-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





