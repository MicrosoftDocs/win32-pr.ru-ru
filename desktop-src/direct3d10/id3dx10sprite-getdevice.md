---
description: Получите устройство, связанное с объектом Sprite.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: Метод ID3DX10Sprite::-Device (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d4e7a3c6ebfcbcb83aaaed6273ea321b33a44ce1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356113"
---
# <a name="id3dx10spritegetdevice-method"></a><span data-ttu-id="010a7-103">Метод ID3DX10Sprite:: of Device</span><span class="sxs-lookup"><span data-stu-id="010a7-103">ID3DX10Sprite::GetDevice method</span></span>

<span data-ttu-id="010a7-104">Получите устройство, связанное с объектом Sprite.</span><span class="sxs-lookup"><span data-stu-id="010a7-104">Retrieve the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="010a7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="010a7-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="010a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="010a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010a7-107">*ппдевице* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="010a7-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="010a7-108">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="010a7-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="010a7-109">Адрес указателя на интерфейс ID3D10Device, представляющий объект устройства Direct3D, связанный с объектом Sprite.</span><span class="sxs-lookup"><span data-stu-id="010a7-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="010a7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="010a7-110">Return value</span></span>

<span data-ttu-id="010a7-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="010a7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="010a7-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="010a7-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="010a7-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="010a7-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="010a7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="010a7-114">Remarks</span></span>

<span data-ttu-id="010a7-115">Вызов этого метода приведет к увеличению внутреннего счетчика ссылок в интерфейсе ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="010a7-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="010a7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="010a7-116">Requirements</span></span>



| <span data-ttu-id="010a7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="010a7-117">Requirement</span></span> | <span data-ttu-id="010a7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="010a7-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="010a7-119">Header</span><span class="sxs-lookup"><span data-stu-id="010a7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="010a7-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="010a7-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="010a7-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="010a7-121">Library</span></span><br/> | <dl> <span data-ttu-id="010a7-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="010a7-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010a7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="010a7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010a7-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="010a7-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="010a7-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="010a7-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




