---
description: Удаляет все события из указанной записи анимации.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'Метод ID3DXAnimationController:: Ункэйаллтраккевентс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5904e9e09c8a821cdc532f9046217ae64bbf3de5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714010"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a><span data-ttu-id="c4097-103">Метод ID3DXAnimationController:: Ункэйаллтраккевентс</span><span class="sxs-lookup"><span data-stu-id="c4097-103">ID3DXAnimationController::UnkeyAllTrackEvents method</span></span>

<span data-ttu-id="c4097-104">Удаляет все события из указанной записи анимации.</span><span class="sxs-lookup"><span data-stu-id="c4097-104">Removes all events from a specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4097-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4097-105">Syntax</span></span>


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a><span data-ttu-id="c4097-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4097-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4097-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4097-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4097-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4097-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4097-109">Идентификатор записи, по которой должны быть удалены все события.</span><span class="sxs-lookup"><span data-stu-id="c4097-109">Identifier of the track on which all events should be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4097-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4097-110">Return value</span></span>

<span data-ttu-id="c4097-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4097-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4097-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="c4097-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c4097-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="c4097-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4097-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4097-114">Remarks</span></span>

<span data-ttu-id="c4097-115">Этот метод предотвращает выполнение всех событий, ранее запланированных на дорожке, и отклоняет все данные, связанные с этими событиями.</span><span class="sxs-lookup"><span data-stu-id="c4097-115">This method prevents the execution of all events previously scheduled on the track, and discards all data associated with those events.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4097-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c4097-116">Requirements</span></span>



| <span data-ttu-id="c4097-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c4097-117">Requirement</span></span> | <span data-ttu-id="c4097-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c4097-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4097-119">Header</span><span class="sxs-lookup"><span data-stu-id="c4097-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c4097-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4097-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c4097-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c4097-121">Library</span></span><br/> | <dl> <span data-ttu-id="c4097-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4097-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4097-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4097-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4097-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="c4097-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
