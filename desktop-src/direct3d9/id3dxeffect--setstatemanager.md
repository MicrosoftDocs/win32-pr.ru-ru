---
description: Задайте диспетчер состояний эффектов.
ms.assetid: 87409687-03f1-4593-ae58-3a8ba08e592b
title: 'Метод ID3DXEffect:: Сетстатеманажер (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bb32e3f668884a6f51bd5c5058a4f27e141f0aa3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424342"
---
# <a name="id3dxeffectsetstatemanager-method"></a><span data-ttu-id="a3565-103">Метод ID3DXEffect:: Сетстатеманажер</span><span class="sxs-lookup"><span data-stu-id="a3565-103">ID3DXEffect::SetStateManager method</span></span>

<span data-ttu-id="a3565-104">Задайте диспетчер состояний эффектов.</span><span class="sxs-lookup"><span data-stu-id="a3565-104">Set the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3565-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3565-105">Syntax</span></span>


```C++
HRESULT SetStateManager(
  [in] LPD3DXEFFECTSTATEMANAGER pManager
);
```



## <a name="parameters"></a><span data-ttu-id="a3565-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3565-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3565-107">*пманажер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a3565-107">*pManager* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3565-108">Тип: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**</span><span class="sxs-lookup"><span data-stu-id="a3565-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**</span></span>

<span data-ttu-id="a3565-109">Указатель на диспетчер состояний.</span><span class="sxs-lookup"><span data-stu-id="a3565-109">A pointer to the state manager.</span></span> <span data-ttu-id="a3565-110">См. [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="a3565-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3565-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3565-111">Return value</span></span>

<span data-ttu-id="a3565-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3565-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3565-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a3565-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3565-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a3565-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3565-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a3565-115">Remarks</span></span>

<span data-ttu-id="a3565-116">[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) — это реализованный пользователем интерфейс, который обеспечивает обратные вызовы в приложение для установки состояния устройства с самого влияния.</span><span class="sxs-lookup"><span data-stu-id="a3565-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3565-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a3565-117">Requirements</span></span>



| <span data-ttu-id="a3565-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a3565-118">Requirement</span></span> | <span data-ttu-id="a3565-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a3565-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3565-120">Header</span><span class="sxs-lookup"><span data-stu-id="a3565-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a3565-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3565-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a3565-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a3565-122">Library</span></span><br/> | <dl> <span data-ttu-id="a3565-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3565-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a3565-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3565-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3565-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="a3565-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="a3565-126">**ID3DXEffect:: Жетстатеманажер**</span><span class="sxs-lookup"><span data-stu-id="a3565-126">**ID3DXEffect::GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)
</dt> </dl>

 

 




