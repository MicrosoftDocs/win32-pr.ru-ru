---
description: Возвращает описание результата.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'Метод ID3DXBaseEffect:: desc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694321"
---
# <a name="id3dxbaseeffectgetdesc-method"></a><span data-ttu-id="50681-103">Метод ID3DXBaseEffect:: DESC</span><span class="sxs-lookup"><span data-stu-id="50681-103">ID3DXBaseEffect::GetDesc method</span></span>

<span data-ttu-id="50681-104">Возвращает описание результата.</span><span class="sxs-lookup"><span data-stu-id="50681-104">Gets the effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="50681-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50681-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="50681-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50681-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50681-107">*пдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="50681-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50681-108">Тип: **[ **D3DXEFFECT \_ DESC**](d3dxeffect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="50681-108">Type: **[**D3DXEFFECT\_DESC**](d3dxeffect-desc.md)\***</span></span>

<span data-ttu-id="50681-109">Возвращает описание результата.</span><span class="sxs-lookup"><span data-stu-id="50681-109">Returns a description of the effect.</span></span> <span data-ttu-id="50681-110">См. [**D3DXEFFECT \_ DESC**](d3dxeffect-desc.md).</span><span class="sxs-lookup"><span data-stu-id="50681-110">See [**D3DXEFFECT\_DESC**](d3dxeffect-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50681-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50681-111">Return value</span></span>

<span data-ttu-id="50681-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50681-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50681-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="50681-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="50681-114">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="50681-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="50681-115">Требования</span><span class="sxs-lookup"><span data-stu-id="50681-115">Requirements</span></span>



| <span data-ttu-id="50681-116">Требование</span><span class="sxs-lookup"><span data-stu-id="50681-116">Requirement</span></span> | <span data-ttu-id="50681-117">Значение</span><span class="sxs-lookup"><span data-stu-id="50681-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50681-118">Header</span><span class="sxs-lookup"><span data-stu-id="50681-118">Header</span></span><br/>  | <dl> <span data-ttu-id="50681-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="50681-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="50681-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="50681-120">Library</span></span><br/> | <dl> <span data-ttu-id="50681-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50681-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="50681-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50681-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50681-123">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="50681-123">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




