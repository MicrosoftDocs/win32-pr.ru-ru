---
title: Метод ID3DX11EffectConstantBuffer Ундосетконстантбуффер (D3dx11effect. h)
description: Восстанавливает ранее установленный буфер констант.
ms.assetid: 6c5e1256-3a92-4bfe-8614-f09d627bc3db
keywords:
- Метод Ундосетконстантбуффер Direct3D 11
- Метод Ундосетконстантбуффер Direct3D 11, интерфейс ID3DX11EffectConstantBuffer
- Интерфейс ID3DX11EffectConstantBuffer Direct3D 11, метод Ундосетконстантбуффер
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.UndoSetConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c95a26f1ea92d5bfe1975e3fe4dc1961046e5535
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424490"
---
# <a name="id3dx11effectconstantbufferundosetconstantbuffer-method"></a><span data-ttu-id="03cd5-106">Метод ID3DX11EffectConstantBuffer:: Ундосетконстантбуффер</span><span class="sxs-lookup"><span data-stu-id="03cd5-106">ID3DX11EffectConstantBuffer::UndoSetConstantBuffer method</span></span>

<span data-ttu-id="03cd5-107">Восстанавливает ранее установленный буфер констант.</span><span class="sxs-lookup"><span data-stu-id="03cd5-107">Reverts a previously set constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="03cd5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03cd5-108">Syntax</span></span>


```C++
HRESULT UndoSetConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="03cd5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="03cd5-109">Parameters</span></span>

<span data-ttu-id="03cd5-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="03cd5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03cd5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03cd5-111">Return value</span></span>

<span data-ttu-id="03cd5-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="03cd5-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="03cd5-113">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="03cd5-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03cd5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="03cd5-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="03cd5-115">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="03cd5-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="03cd5-116">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="03cd5-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="03cd5-117">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="03cd5-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03cd5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="03cd5-118">Requirements</span></span>



| <span data-ttu-id="03cd5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="03cd5-119">Requirement</span></span> | <span data-ttu-id="03cd5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="03cd5-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03cd5-121">Header</span><span class="sxs-lookup"><span data-stu-id="03cd5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="03cd5-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="03cd5-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="03cd5-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03cd5-123">Library</span></span><br/> | <dl> <span data-ttu-id="03cd5-124"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="03cd5-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03cd5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03cd5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03cd5-126">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="03cd5-126">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





