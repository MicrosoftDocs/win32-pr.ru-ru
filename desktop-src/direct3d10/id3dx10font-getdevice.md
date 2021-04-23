---
description: Получите устройство Direct3D, связанное с объектом Font.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: Метод ID3DX10Font::-Device (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703803"
---
# <a name="id3dx10fontgetdevice-method"></a><span data-ttu-id="32433-103">Метод ID3DX10Font:: of Device</span><span class="sxs-lookup"><span data-stu-id="32433-103">ID3DX10Font::GetDevice method</span></span>

<span data-ttu-id="32433-104">Получите устройство Direct3D, связанное с объектом Font.</span><span class="sxs-lookup"><span data-stu-id="32433-104">Retrieve the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="32433-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32433-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="32433-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32433-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32433-107">*ппдевице* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="32433-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32433-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="32433-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="32433-109">Адрес указателя на интерфейс ID3D10Device, представляющий объект устройства Direct3D, связанный с объектом Font.</span><span class="sxs-lookup"><span data-stu-id="32433-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32433-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32433-110">Return value</span></span>

<span data-ttu-id="32433-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="32433-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="32433-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="32433-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="32433-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="32433-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="32433-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32433-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="32433-115">Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="32433-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span> <span data-ttu-id="32433-116">Не забудьте вызвать IUnknown, когда вы завершите работу с этим интерфейсом ID3D10Device, или у вас будет утечка памяти.</span><span class="sxs-lookup"><span data-stu-id="32433-116">Be sure to call IUnknown when you are done using this ID3D10Device interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="32433-117">Требования</span><span class="sxs-lookup"><span data-stu-id="32433-117">Requirements</span></span>



| <span data-ttu-id="32433-118">Требование</span><span class="sxs-lookup"><span data-stu-id="32433-118">Requirement</span></span> | <span data-ttu-id="32433-119">Значение</span><span class="sxs-lookup"><span data-stu-id="32433-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32433-120">Header</span><span class="sxs-lookup"><span data-stu-id="32433-120">Header</span></span><br/>  | <dl> <span data-ttu-id="32433-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="32433-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="32433-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="32433-122">Library</span></span><br/> | <dl> <span data-ttu-id="32433-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32433-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32433-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32433-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32433-125">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="32433-125">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="32433-126">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="32433-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




