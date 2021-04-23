---
description: Извлекает устройство, связанное с сеткой.
ms.assetid: 16ff5267-0c64-4c3d-925d-6fc10f54c9c4
title: Метод ID3DXBaseMesh::-Device (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b866c86bf759305a4626f0ff5ecaa8e35bfd75d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081888"
---
# <a name="id3dxbasemeshgetdevice-method"></a><span data-ttu-id="0879c-103">Метод ID3DXBaseMesh:: of Device</span><span class="sxs-lookup"><span data-stu-id="0879c-103">ID3DXBaseMesh::GetDevice method</span></span>

<span data-ttu-id="0879c-104">Извлекает устройство, связанное с сеткой.</span><span class="sxs-lookup"><span data-stu-id="0879c-104">Retrieves the device associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0879c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0879c-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="0879c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0879c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0879c-107">*ппдевице* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0879c-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0879c-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="0879c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="0879c-109">Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства Direct3D, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="0879c-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0879c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0879c-110">Return value</span></span>

<span data-ttu-id="0879c-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0879c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0879c-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0879c-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0879c-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="0879c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0879c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0879c-114">Remarks</span></span>

<span data-ttu-id="0879c-115">Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="0879c-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="0879c-116">Не забудьте вызвать [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , когда вы завершите работу с этим интерфейсом **IDirect3DDevice9** , или у вас будет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="0879c-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="0879c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0879c-117">Requirements</span></span>



| <span data-ttu-id="0879c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0879c-118">Requirement</span></span> | <span data-ttu-id="0879c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0879c-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0879c-120">Header</span><span class="sxs-lookup"><span data-stu-id="0879c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0879c-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0879c-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0879c-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0879c-122">Library</span></span><br/> | <dl> <span data-ttu-id="0879c-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0879c-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0879c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0879c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0879c-125">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="0879c-125">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
