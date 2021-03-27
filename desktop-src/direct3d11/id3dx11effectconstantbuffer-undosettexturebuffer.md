---
title: Метод ID3DX11EffectConstantBuffer Ундосеттекстуребуффер (D3dx11effect. h)
description: Восстанавливает ранее установленный буфер текстуры.
ms.assetid: 982e7899-9569-4611-9fe0-b78624acba2c
keywords:
- Метод Ундосеттекстуребуффер Direct3D 11
- Метод Ундосеттекстуребуффер Direct3D 11, интерфейс ID3DX11EffectConstantBuffer
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, метод Ундосеттекстуребуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5e1e1b2be167466da5a4d92999646bb7c8f225
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355260"
---
# <a name="id3dx11effectconstantbufferundosettexturebuffer-method"></a><span data-ttu-id="a41ed-106">Метод ID3DX11EffectConstantBuffer:: Ундосеттекстуребуффер</span><span class="sxs-lookup"><span data-stu-id="a41ed-106">ID3DX11EffectConstantBuffer::UndoSetTextureBuffer method</span></span>

<span data-ttu-id="a41ed-107">Восстанавливает ранее установленный буфер текстуры.</span><span class="sxs-lookup"><span data-stu-id="a41ed-107">Reverts a previously set texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a41ed-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a41ed-108">Syntax</span></span>


```C++
HRESULT UndoSetTextureBuffer();
```



## <a name="parameters"></a><span data-ttu-id="a41ed-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a41ed-109">Parameters</span></span>

<span data-ttu-id="a41ed-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a41ed-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a41ed-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a41ed-111">Return value</span></span>

<span data-ttu-id="a41ed-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a41ed-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a41ed-113">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a41ed-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a41ed-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a41ed-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a41ed-115">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="a41ed-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a41ed-116">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="a41ed-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a41ed-117">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a41ed-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a41ed-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a41ed-118">Requirements</span></span>



| <span data-ttu-id="a41ed-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a41ed-119">Requirement</span></span> | <span data-ttu-id="a41ed-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a41ed-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a41ed-121">Header</span><span class="sxs-lookup"><span data-stu-id="a41ed-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a41ed-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a41ed-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a41ed-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a41ed-123">Library</span></span><br/> | <dl> <span data-ttu-id="a41ed-124"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="a41ed-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a41ed-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a41ed-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41ed-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="a41ed-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





