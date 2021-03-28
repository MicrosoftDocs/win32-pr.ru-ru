---
title: Метод ID3DX11EffectConstantBuffer Жетконстантбуффер (D3dx11effect. h)
description: Получение постоянного буфера.
ms.assetid: 857b3dc2-41ae-4a52-904a-9ca8f0afeb9e
keywords:
- Метод Жетконстантбуффер Direct3D 11
- Метод Жетконстантбуффер Direct3D 11, интерфейс ID3DX11EffectConstantBuffer
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, метод Жетконстантбуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041ca2fea028cb86d0959313bae73c320e6e5a36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081949"
---
# <a name="id3dx11effectconstantbuffergetconstantbuffer-method"></a><span data-ttu-id="49498-106">Метод ID3DX11EffectConstantBuffer:: Жетконстантбуффер</span><span class="sxs-lookup"><span data-stu-id="49498-106">ID3DX11EffectConstantBuffer::GetConstantBuffer method</span></span>

<span data-ttu-id="49498-107">Получение постоянного буфера.</span><span class="sxs-lookup"><span data-stu-id="49498-107">Get a constant-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="49498-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49498-108">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
   ID3D11Buffer **ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="49498-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="49498-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49498-110">*ппконстантбуффер*</span><span class="sxs-lookup"><span data-stu-id="49498-110">*ppConstantBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="49498-111">Тип: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="49498-111">Type: **[**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\*\***</span></span>

<span data-ttu-id="49498-112">Адрес указателя на интерфейс постоянного буфера.</span><span class="sxs-lookup"><span data-stu-id="49498-112">The address of a pointer to a constant-buffer interface.</span></span> <span data-ttu-id="49498-113">См. [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span><span class="sxs-lookup"><span data-stu-id="49498-113">See [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49498-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49498-114">Return value</span></span>

<span data-ttu-id="49498-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49498-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49498-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="49498-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="49498-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="49498-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49498-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="49498-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="49498-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="49498-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="49498-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="49498-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49498-121">Требования</span><span class="sxs-lookup"><span data-stu-id="49498-121">Requirements</span></span>



| <span data-ttu-id="49498-122">Требование</span><span class="sxs-lookup"><span data-stu-id="49498-122">Requirement</span></span> | <span data-ttu-id="49498-123">Значение</span><span class="sxs-lookup"><span data-stu-id="49498-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49498-124">Header</span><span class="sxs-lookup"><span data-stu-id="49498-124">Header</span></span><br/>  | <dl> <span data-ttu-id="49498-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="49498-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="49498-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49498-126">Library</span></span><br/> | <dl> <span data-ttu-id="49498-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="49498-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49498-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49498-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49498-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="49498-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





