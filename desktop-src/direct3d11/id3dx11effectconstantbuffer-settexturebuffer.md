---
title: Метод ID3DX11EffectConstantBuffer Сеттекстуребуффер (D3dx11effect. h)
description: Задайте буфер текстуры.
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- Метод Сеттекстуребуффер Direct3D 11
- Метод Сеттекстуребуффер Direct3D 11, интерфейс ID3DX11EffectConstantBuffer
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, метод Сеттекстуребуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736ec4c5f0125dfc37925d67875cf97c5441117c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986834"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a><span data-ttu-id="c04df-106">Метод ID3DX11EffectConstantBuffer:: Сеттекстуребуффер</span><span class="sxs-lookup"><span data-stu-id="c04df-106">ID3DX11EffectConstantBuffer::SetTextureBuffer method</span></span>

<span data-ttu-id="c04df-107">Задайте буфер текстуры.</span><span class="sxs-lookup"><span data-stu-id="c04df-107">Set a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c04df-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c04df-108">Syntax</span></span>


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="c04df-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c04df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c04df-110">*птекстуребуффер*</span><span class="sxs-lookup"><span data-stu-id="c04df-110">*pTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c04df-111">Тип: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="c04df-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="c04df-112">Указатель на интерфейс представления шейдера-ресурса для доступа к буферу текстуры.</span><span class="sxs-lookup"><span data-stu-id="c04df-112">A pointer to a shader-resource-view interface for accessing a texture buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c04df-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c04df-113">Return value</span></span>

<span data-ttu-id="c04df-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c04df-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c04df-115">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c04df-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c04df-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c04df-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c04df-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="c04df-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c04df-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="c04df-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c04df-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c04df-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c04df-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c04df-120">Requirements</span></span>



| <span data-ttu-id="c04df-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c04df-121">Requirement</span></span> | <span data-ttu-id="c04df-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c04df-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c04df-123">Header</span><span class="sxs-lookup"><span data-stu-id="c04df-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c04df-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c04df-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c04df-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c04df-125">Library</span></span><br/> | <dl> <span data-ttu-id="c04df-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="c04df-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c04df-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c04df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04df-128">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="c04df-128">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





