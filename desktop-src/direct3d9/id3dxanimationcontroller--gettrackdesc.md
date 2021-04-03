---
description: Возвращает описание записи.
ms.assetid: 7663a26f-5ad3-4a17-a502-c0dcfa730db2
title: 'Метод ID3DXAnimationController:: Жеттраккдеск (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 940b43ede480766155d09ebe51dfb55eba114c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821229"
---
# <a name="id3dxanimationcontrollergettrackdesc-method"></a><span data-ttu-id="ca27a-103">Метод ID3DXAnimationController:: Жеттраккдеск</span><span class="sxs-lookup"><span data-stu-id="ca27a-103">ID3DXAnimationController::GetTrackDesc method</span></span>

<span data-ttu-id="ca27a-104">Возвращает описание записи.</span><span class="sxs-lookup"><span data-stu-id="ca27a-104">Gets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca27a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca27a-105">Syntax</span></span>


```C++
HRESULT GetTrackDesc(
  [in]  UINT             Track,
  [out] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ca27a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca27a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca27a-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca27a-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca27a-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca27a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca27a-109">Идентификатор трассировки.</span><span class="sxs-lookup"><span data-stu-id="ca27a-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ca27a-110">*пдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ca27a-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca27a-111">Тип: **[ **LPD3DXTRACK \_ DESC**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="ca27a-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="ca27a-112">Указатель на описание записи.</span><span class="sxs-lookup"><span data-stu-id="ca27a-112">Pointer to the track description.</span></span> <span data-ttu-id="ca27a-113">См. [**D3DXTRACK \_ DESC**](d3dxtrack-desc.md).</span><span class="sxs-lookup"><span data-stu-id="ca27a-113">See [**D3DXTRACK\_DESC**](d3dxtrack-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca27a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca27a-114">Return value</span></span>

<span data-ttu-id="ca27a-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca27a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca27a-116">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ca27a-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ca27a-117">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ca27a-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca27a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ca27a-118">Requirements</span></span>



| <span data-ttu-id="ca27a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ca27a-119">Requirement</span></span> | <span data-ttu-id="ca27a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ca27a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca27a-121">Header</span><span class="sxs-lookup"><span data-stu-id="ca27a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ca27a-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca27a-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ca27a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ca27a-123">Library</span></span><br/> | <dl> <span data-ttu-id="ca27a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca27a-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ca27a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca27a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca27a-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ca27a-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
