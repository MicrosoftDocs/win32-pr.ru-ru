---
description: Извлекает устройство Direct3D, связанное с объектом Line.
ms.assetid: 42459668-aa18-478d-82d9-b8b25dc4a898
title: Метод ID3DXLine::-Device (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a97edf37d14edce4982d62d76f9429091ad491ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694351"
---
# <a name="id3dxlinegetdevice-method"></a><span data-ttu-id="6142d-103">Метод ID3DXLine:: of Device</span><span class="sxs-lookup"><span data-stu-id="6142d-103">ID3DXLine::GetDevice method</span></span>

<span data-ttu-id="6142d-104">Извлекает устройство Direct3D, связанное с объектом Line.</span><span class="sxs-lookup"><span data-stu-id="6142d-104">Retrieves the Direct3D device associated with the line object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6142d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6142d-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="6142d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6142d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6142d-107">*ппдевице* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6142d-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6142d-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="6142d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="6142d-109">Адрес указателя на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства Direct3D, связанный с объектом Line.</span><span class="sxs-lookup"><span data-stu-id="6142d-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the line object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6142d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6142d-110">Return value</span></span>

<span data-ttu-id="6142d-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6142d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6142d-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6142d-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6142d-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="6142d-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="6142d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6142d-114">Requirements</span></span>



| <span data-ttu-id="6142d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6142d-115">Requirement</span></span> | <span data-ttu-id="6142d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6142d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6142d-117">Header</span><span class="sxs-lookup"><span data-stu-id="6142d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6142d-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6142d-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="6142d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6142d-119">Library</span></span><br/> | <dl> <span data-ttu-id="6142d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6142d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6142d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6142d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6142d-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="6142d-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
