---
description: Подготовка устройства для рисования спрайтов.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'Метод ID3DX10Sprite:: Begin (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273870"
---
# <a name="id3dx10spritebegin-method"></a><span data-ttu-id="925dd-103">Метод ID3DX10Sprite:: Begin</span><span class="sxs-lookup"><span data-stu-id="925dd-103">ID3DX10Sprite::Begin method</span></span>

<span data-ttu-id="925dd-104">Подготовка устройства для рисования спрайтов.</span><span class="sxs-lookup"><span data-stu-id="925dd-104">Prepare a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="925dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="925dd-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a><span data-ttu-id="925dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="925dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="925dd-107">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="925dd-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="925dd-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="925dd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="925dd-109">Флаги, определяющие, как будут рисоваться спрайты.</span><span class="sxs-lookup"><span data-stu-id="925dd-109">Flags that control how the sprites will be drawn.</span></span> <span data-ttu-id="925dd-110">См. раздел [**D3DX10 \_ Sprite \_ Flag**](d3dx10-sprite-flag.md).</span><span class="sxs-lookup"><span data-stu-id="925dd-110">See [**D3DX10\_SPRITE\_FLAG**](d3dx10-sprite-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="925dd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="925dd-111">Return value</span></span>

<span data-ttu-id="925dd-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="925dd-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="925dd-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="925dd-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="925dd-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ АУТОФВИДЕОМЕМОРИ, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="925dd-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="925dd-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="925dd-115">Remarks</span></span>

<span data-ttu-id="925dd-116">Каждый вызов Begin должен быть сопоставлен с вызовом [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).</span><span class="sxs-lookup"><span data-stu-id="925dd-116">Every call to Begin must be matched with a call to [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="925dd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="925dd-117">Requirements</span></span>



| <span data-ttu-id="925dd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="925dd-118">Requirement</span></span> | <span data-ttu-id="925dd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="925dd-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="925dd-120">Header</span><span class="sxs-lookup"><span data-stu-id="925dd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="925dd-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="925dd-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="925dd-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="925dd-122">Library</span></span><br/> | <dl> <span data-ttu-id="925dd-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="925dd-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="925dd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="925dd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="925dd-125">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="925dd-125">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="925dd-126">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="925dd-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
