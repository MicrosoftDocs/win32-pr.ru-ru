---
description: Извлекает устройство, связанное с этим действием.
ms.assetid: acef5d0a-b185-4054-8982-0580440ab76b
title: Метод ID3DXEffect::-Device (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fde2d9f3d9db362bf48fda66e9da10b91a864bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714046"
---
# <a name="id3dxeffectgetdevice-method"></a><span data-ttu-id="2ea28-103">Метод ID3DXEffect:: of Device</span><span class="sxs-lookup"><span data-stu-id="2ea28-103">ID3DXEffect::GetDevice method</span></span>

<span data-ttu-id="2ea28-104">Извлекает устройство, связанное с этим действием.</span><span class="sxs-lookup"><span data-stu-id="2ea28-104">Retrieves the device associated with the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ea28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ea28-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="2ea28-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ea28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ea28-107">*ппдевице* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ea28-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ea28-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="2ea28-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="2ea28-109">Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с этим действием.</span><span class="sxs-lookup"><span data-stu-id="2ea28-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ea28-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ea28-110">Return value</span></span>

<span data-ttu-id="2ea28-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ea28-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ea28-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="2ea28-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2ea28-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="2ea28-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ea28-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ea28-114">Remarks</span></span>

<span data-ttu-id="2ea28-115">Вызов этого метода приведет к увеличению внутреннего счетчика ссылок для интерфейса [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="2ea28-115">Calling this method will increase the internal reference count for the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="2ea28-116">Не забудьте вызвать IUnknown:: Release, когда вы завершите работу с интерфейсом **IDirect3DDevice9** , или у вас будет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="2ea28-116">Be sure to call IUnknown::Release when you are done using the **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ea28-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2ea28-117">Requirements</span></span>



| <span data-ttu-id="2ea28-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2ea28-118">Requirement</span></span> | <span data-ttu-id="2ea28-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2ea28-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ea28-120">Header</span><span class="sxs-lookup"><span data-stu-id="2ea28-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2ea28-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ea28-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2ea28-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ea28-122">Library</span></span><br/> | <dl> <span data-ttu-id="2ea28-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ea28-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2ea28-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ea28-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ea28-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="2ea28-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
