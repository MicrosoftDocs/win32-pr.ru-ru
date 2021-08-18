---
description: Получите указатель интерфейса устройства Direct3D 10,1 из указателя интерфейса Direct3D 10,0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: Функция D3DX10GetFeatureLevel1 (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: c6511e0d3963e21f8950529b32cf8c3b414cc00b0625b97b2a9d569d1523c326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753174"
---
# <a name="d3dx10getfeaturelevel1-function"></a>Функция D3DX10GetFeatureLevel1

Получите указатель интерфейса устройства Direct3D 10,1 из указателя интерфейса Direct3D 10,0.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Указатель на устройство Direct3D 10,0 (см. интерфейс [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).

</dd> <dt>

*ппдевице* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***

Указатель на устройство Direct3D 10,1 (см. интерфейс [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) ).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Эта функция возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md). Если можно получить интерфейс устройства Direct3D 10,1, эта функция завершается успешно и передает указатель на интерфейс 10,1 с помощью параметра *ппдевице* . Если интерфейс устройства Direct3D 10,1 не может быть получен, эта функция возвращает \_ ошибку E и не возвращает ничего для параметра *ппдевице* .

## <a name="remarks"></a>Remarks

Чтобы эта функция была выполнена успешно, необходимо получить предоставленный указатель [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) с помощью вызова функции [**D3DX10CreateDevice**](d3dx10createdevice.md) , функции [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) , функции [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) или функции [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) .

устройство Direct3D 10,1 можно создать только на компьютерах под управлением Windows Vista с пакетом обновления 1 (sp1) или более поздней версии, а также с установленным оборудованием, совместимым с Direct3D 10,1. Эта функция возвращает «E \_ Fail» на любом компьютере, не отвечающих этим требованиям. однако эту функцию можно вызвать для любой версии Windows с установленной библиотекой DLL D3DX10.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




