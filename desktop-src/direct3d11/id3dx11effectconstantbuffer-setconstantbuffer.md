---
title: Метод ID3DX11EffectConstantBuffer Сетконстантбуффер (D3dx11effect. h)
description: Установите константный буфер.
ms.assetid: 288e029a-e69a-4f58-be3f-8f9900c0e1dd
keywords:
- Метод Сетконстантбуффер Direct3D 11
- Метод Сетконстантбуффер Direct3D 11, интерфейс ID3DX11EffectConstantBuffer
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, метод Сетконстантбуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12249d9830ced43c3a56a2c8cf51942e66f6494e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273935"
---
# <a name="id3dx11effectconstantbuffersetconstantbuffer-method"></a><span data-ttu-id="b5d4e-106">Метод ID3DX11EffectConstantBuffer:: Сетконстантбуффер</span><span class="sxs-lookup"><span data-stu-id="b5d4e-106">ID3DX11EffectConstantBuffer::SetConstantBuffer method</span></span>

<span data-ttu-id="b5d4e-107">Установите константный буфер.</span><span class="sxs-lookup"><span data-stu-id="b5d4e-107">Set a constant-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d4e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5d4e-108">Syntax</span></span>


```C++
HRESULT SetConstantBuffer(
   ID3D11Buffer *pConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b5d4e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5d4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d4e-110">*пконстантбуффер*</span><span class="sxs-lookup"><span data-stu-id="b5d4e-110">*pConstantBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b5d4e-111">Тип: **[ **ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***</span><span class="sxs-lookup"><span data-stu-id="b5d4e-111">Type: **[**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)\***</span></span>

<span data-ttu-id="b5d4e-112">Указатель на интерфейс постоянного буфера.</span><span class="sxs-lookup"><span data-stu-id="b5d4e-112">A pointer to a constant-buffer interface.</span></span> <span data-ttu-id="b5d4e-113">См. [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span><span class="sxs-lookup"><span data-stu-id="b5d4e-113">See [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d4e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5d4e-114">Return value</span></span>

<span data-ttu-id="b5d4e-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5d4e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5d4e-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b5d4e-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5d4e-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5d4e-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5d4e-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="b5d4e-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b5d4e-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="b5d4e-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b5d4e-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b5d4e-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5d4e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b5d4e-121">Requirements</span></span>



| <span data-ttu-id="b5d4e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b5d4e-122">Requirement</span></span> | <span data-ttu-id="b5d4e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b5d4e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d4e-124">Header</span><span class="sxs-lookup"><span data-stu-id="b5d4e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b5d4e-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d4e-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b5d4e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b5d4e-126">Library</span></span><br/> | <dl> <span data-ttu-id="b5d4e-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="b5d4e-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d4e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5d4e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d4e-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="b5d4e-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





