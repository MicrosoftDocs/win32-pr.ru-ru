---
description: Выполняет анимацию сетки и перемещает глобальное время анимации на заданный объем.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'Метод ID3DXAnimationController:: AdvanceTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694294"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a><span data-ttu-id="5e2b0-103">Метод ID3DXAnimationController:: AdvanceTime</span><span class="sxs-lookup"><span data-stu-id="5e2b0-103">ID3DXAnimationController::AdvanceTime method</span></span>

<span data-ttu-id="5e2b0-104">Выполняет анимацию сетки и перемещает глобальное время анимации на заданный объем.</span><span class="sxs-lookup"><span data-stu-id="5e2b0-104">Animates the mesh and advances the global animation time by a specified amount.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e2b0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e2b0-105">Syntax</span></span>


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a><span data-ttu-id="5e2b0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e2b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e2b0-107">*Тимеделта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e2b0-107">*TimeDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e2b0-108">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e2b0-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e2b0-109">Величина (в секундах), с которой следует переместить глобальное время анимации.</span><span class="sxs-lookup"><span data-stu-id="5e2b0-109">Amount, in seconds, by which to advance the global animation time.</span></span> <span data-ttu-id="5e2b0-110">Значение Тимеделта не может быть отрицательным или равным нулю.</span><span class="sxs-lookup"><span data-stu-id="5e2b0-110">TimeDelta value must be non-negative or zero.</span></span>

</dd> <dt>

<span data-ttu-id="5e2b0-111">*пкаллбаккхандлер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e2b0-111">*pCallbackHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e2b0-112">Тип: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span><span class="sxs-lookup"><span data-stu-id="5e2b0-112">Type: **[**LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span></span>

<span data-ttu-id="5e2b0-113">Указатель на пользовательский интерфейс обработчика обратного вызова анимации [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span><span class="sxs-lookup"><span data-stu-id="5e2b0-113">Pointer to a user-defined animation callback handler interface, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e2b0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e2b0-114">Return value</span></span>

<span data-ttu-id="5e2b0-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e2b0-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e2b0-116">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="5e2b0-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5e2b0-117">Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5e2b0-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2b0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5e2b0-118">Requirements</span></span>



| <span data-ttu-id="5e2b0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5e2b0-119">Requirement</span></span> | <span data-ttu-id="5e2b0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5e2b0-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2b0-121">Header</span><span class="sxs-lookup"><span data-stu-id="5e2b0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5e2b0-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e2b0-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5e2b0-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e2b0-123">Library</span></span><br/> | <dl> <span data-ttu-id="5e2b0-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e2b0-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e2b0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e2b0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2b0-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="5e2b0-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
