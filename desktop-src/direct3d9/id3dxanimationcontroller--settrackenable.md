---
description: Включает или отключает запись в контроллере анимации.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'Метод ID3DXAnimationController:: Сеттраккенабле (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081916"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a><span data-ttu-id="b326b-103">Метод ID3DXAnimationController:: Сеттраккенабле</span><span class="sxs-lookup"><span data-stu-id="b326b-103">ID3DXAnimationController::SetTrackEnable method</span></span>

<span data-ttu-id="b326b-104">Включает или отключает запись в контроллере анимации.</span><span class="sxs-lookup"><span data-stu-id="b326b-104">Enables or disables a track in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="b326b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b326b-105">Syntax</span></span>


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="b326b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b326b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b326b-107">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b326b-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b326b-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b326b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b326b-109">Идентификатор смешанной записи.</span><span class="sxs-lookup"><span data-stu-id="b326b-109">Identifier of the track to be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="b326b-110">*Включить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b326b-110">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b326b-111">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b326b-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b326b-112">Включить значение.</span><span class="sxs-lookup"><span data-stu-id="b326b-112">Enable value.</span></span> <span data-ttu-id="b326b-113">Задайте значение **true** , чтобы включить эту запись в контроллере, или **значение false** , чтобы предотвратить смешанный режим.</span><span class="sxs-lookup"><span data-stu-id="b326b-113">Set to **TRUE** to enable this track in the controller, or to **FALSE** to prevent it from being mixed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b326b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b326b-114">Return value</span></span>

<span data-ttu-id="b326b-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b326b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b326b-116">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="b326b-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b326b-117">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b326b-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b326b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b326b-118">Remarks</span></span>

<span data-ttu-id="b326b-119">Для смешивания дорожек с другими дорожками флаг enable должен иметь значение **true**.</span><span class="sxs-lookup"><span data-stu-id="b326b-119">To mix a track with other tracks, the Enable flag must be set to **TRUE**.</span></span> <span data-ttu-id="b326b-120">И наоборот, установка флага в **значение false** предотвратит смешение дорожки с другими дорожками.</span><span class="sxs-lookup"><span data-stu-id="b326b-120">Conversely, setting the flag to **FALSE** will prevent the track from being mixed with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="b326b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b326b-121">Requirements</span></span>



| <span data-ttu-id="b326b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b326b-122">Requirement</span></span> | <span data-ttu-id="b326b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b326b-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b326b-124">Header</span><span class="sxs-lookup"><span data-stu-id="b326b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b326b-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b326b-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b326b-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b326b-126">Library</span></span><br/> | <dl> <span data-ttu-id="b326b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b326b-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b326b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b326b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b326b-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="b326b-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
