---
description: 'Приложение реализует этот метод. Этот метод вызывается при возникновении обратного вызова для набора анимации в одной из дорожек во время вызова ID3DXAnimationController:: AdvanceTime.'
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'Метод ID3DXAnimationCallbackHandler:: Хандлекаллбакк (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694296"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a><span data-ttu-id="dc1c9-104">Метод ID3DXAnimationCallbackHandler:: Хандлекаллбакк</span><span class="sxs-lookup"><span data-stu-id="dc1c9-104">ID3DXAnimationCallbackHandler::HandleCallback method</span></span>

<span data-ttu-id="dc1c9-105">Приложение реализует этот метод.</span><span class="sxs-lookup"><span data-stu-id="dc1c9-105">The application implements this method.</span></span> <span data-ttu-id="dc1c9-106">Этот метод вызывается при возникновении обратного вызова для набора анимации в одной из дорожек во время вызова [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="dc1c9-106">This method is called when a callback occurs for an animation set in one of the tracks during a call to [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1c9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc1c9-107">Syntax</span></span>


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="dc1c9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc1c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc1c9-109">*Track* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc1c9-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1c9-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc1c9-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc1c9-111">Идентификатор записи, в которой происходит обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="dc1c9-111">Identifier of the track on which the callback occurs.</span></span>

</dd> <dt>

<span data-ttu-id="dc1c9-112">*пкаллбаккдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc1c9-112">*pCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1c9-113">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc1c9-113">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc1c9-114">Указатель на данные обратного вызова, принадлежащие пользователю.</span><span class="sxs-lookup"><span data-stu-id="dc1c9-114">Pointer to user-owned callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc1c9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc1c9-115">Return value</span></span>

<span data-ttu-id="dc1c9-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc1c9-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc1c9-117">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="dc1c9-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="dc1c9-118">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="dc1c9-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="dc1c9-119">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке из [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="dc1c9-119">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc1c9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dc1c9-120">Requirements</span></span>



| <span data-ttu-id="dc1c9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="dc1c9-121">Requirement</span></span> | <span data-ttu-id="dc1c9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dc1c9-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc1c9-123">Header</span><span class="sxs-lookup"><span data-stu-id="dc1c9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="dc1c9-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c9-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="dc1c9-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc1c9-125">Library</span></span><br/> | <dl> <span data-ttu-id="dc1c9-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c9-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc1c9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc1c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc1c9-128">ID3DXAnimationCallbackHandler</span><span class="sxs-lookup"><span data-stu-id="dc1c9-128">ID3DXAnimationCallbackHandler</span></span>](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
