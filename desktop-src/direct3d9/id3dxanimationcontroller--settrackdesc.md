---
description: Задает описание записи.
ms.assetid: bc3324b3-ca23-4035-958d-9763a70071f2
title: 'Метод ID3DXAnimationController:: Сеттраккдеск (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1aca9385f1e9bc9439b9fe4b3dc1acddda94e395
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713888"
---
# <a name="id3dxanimationcontrollersettrackdesc-method"></a><span data-ttu-id="76ccd-103">Метод ID3DXAnimationController:: Сеттраккдеск</span><span class="sxs-lookup"><span data-stu-id="76ccd-103">ID3DXAnimationController::SetTrackDesc method</span></span>

<span data-ttu-id="76ccd-104">Задает описание записи.</span><span class="sxs-lookup"><span data-stu-id="76ccd-104">Sets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ccd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76ccd-105">Syntax</span></span>


```C++
HRESULT SetTrackDesc(
  [in] UINT             Track,
  [in] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="76ccd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76ccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76ccd-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76ccd-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ccd-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76ccd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76ccd-109">Идентификатор изменяемой записи.</span><span class="sxs-lookup"><span data-stu-id="76ccd-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="76ccd-110">*пдеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76ccd-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ccd-111">Тип: **[ **LPD3DXTRACK \_ DESC**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="76ccd-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="76ccd-112">Описание курса.</span><span class="sxs-lookup"><span data-stu-id="76ccd-112">Description of the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76ccd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76ccd-113">Return value</span></span>

<span data-ttu-id="76ccd-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="76ccd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="76ccd-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="76ccd-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="76ccd-116">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="76ccd-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="76ccd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="76ccd-117">Requirements</span></span>



| <span data-ttu-id="76ccd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="76ccd-118">Requirement</span></span> | <span data-ttu-id="76ccd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="76ccd-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76ccd-120">Header</span><span class="sxs-lookup"><span data-stu-id="76ccd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="76ccd-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="76ccd-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="76ccd-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="76ccd-122">Library</span></span><br/> | <dl> <span data-ttu-id="76ccd-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76ccd-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76ccd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76ccd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ccd-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="76ccd-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
