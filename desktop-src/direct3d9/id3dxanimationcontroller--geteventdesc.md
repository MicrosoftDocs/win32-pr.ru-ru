---
description: Возвращает описание указанного события анимации.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'Метод ID3DXAnimationController:: Жетевентдеск (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f717c032358dd921be2df1c8a84d1aa02a7a93a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713955"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a><span data-ttu-id="1bec7-103">Метод ID3DXAnimationController:: Жетевентдеск</span><span class="sxs-lookup"><span data-stu-id="1bec7-103">ID3DXAnimationController::GetEventDesc method</span></span>

<span data-ttu-id="1bec7-104">Возвращает описание указанного события анимации.</span><span class="sxs-lookup"><span data-stu-id="1bec7-104">Gets a description of a specified animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bec7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bec7-105">Syntax</span></span>


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="1bec7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bec7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bec7-107">*Хевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bec7-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bec7-108">Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="1bec7-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="1bec7-109">Обработчик события анимации для описания.</span><span class="sxs-lookup"><span data-stu-id="1bec7-109">Event handle to an animation event to describe.</span></span>

</dd> <dt>

<span data-ttu-id="1bec7-110">*пдеск* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1bec7-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bec7-111">Тип: **[ **LPD3DXEVENT \_ DESC**](d3dxevent-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="1bec7-111">Type: **[**LPD3DXEVENT\_DESC**](d3dxevent-desc.md)**</span></span>

<span data-ttu-id="1bec7-112">Указатель на структуру [**D3DXEVENT \_ DESC**](d3dxevent-desc.md) , содержащую описание события анимации.</span><span class="sxs-lookup"><span data-stu-id="1bec7-112">Pointer to a [**D3DXEVENT\_DESC**](d3dxevent-desc.md) structure that contains a description of the animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bec7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1bec7-113">Return value</span></span>

<span data-ttu-id="1bec7-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bec7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bec7-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="1bec7-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1bec7-116">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="1bec7-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bec7-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1bec7-117">Requirements</span></span>



| <span data-ttu-id="1bec7-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1bec7-118">Requirement</span></span> | <span data-ttu-id="1bec7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1bec7-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bec7-120">Header</span><span class="sxs-lookup"><span data-stu-id="1bec7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1bec7-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bec7-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1bec7-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1bec7-122">Library</span></span><br/> | <dl> <span data-ttu-id="1bec7-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bec7-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bec7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bec7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bec7-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="1bec7-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




