---
description: Создайте наилучшее устройство Direct3D 10, представляющее видеоадаптер. Если можно создать совместимое с Direct3D 10,1 устройство, вы сможете получить указатель интерфейса ID3D10Device1 из возвращенного указателя интерфейса устройства.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: Функция D3DX10CreateDevice (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 9300eb74027d25562dabb9a596face10105110d1750b359bcaae9ab6b2b83084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634704"
---
# <a name="d3dx10createdevice-function"></a>Функция D3DX10CreateDevice

Создайте наилучшее устройство Direct3D 10, представляющее видеоадаптер. Если можно создать совместимое с Direct3D 10,1 устройство, вы сможете получить указатель [**интерфейса ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) из возвращенного указателя интерфейса устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*падаптер* \[ окне\]
</dt> <dd>

Тип: **[ **идксгиадаптер**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Указатель на адаптер дисплея (см. интерфейс [**идксгиадаптер**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ) при создании аппаратного устройства; в противном случае присвойте этому параметру **значение NULL**. Если при создании аппаратного устройства указано **значение NULL** , Direct3D будет использовать первый адаптер, перечисленный интерфейсом [**идксгифактори**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) .

</dd> <dt>

*Дривертипе* \[ окне\]
</dt> <dd>

Тип: **[ **D3D10 \_ \_ Тип драйвера**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Тип драйвера устройства (см. раздел перечисление [**\_ \_ типов драйверов D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) ). Тип драйвера определяется типом создаваемого устройства.

</dd> <dt>

*Программное обеспечение* \[ окне\]
</dt> <dd>

Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**

Маркер загруженного модуля, который реализует драйвер программного обеспечения (например, D3D10Ref.dll). Чтобы получить маркер, вызовите функцию [Ошибка GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Флаги создания устройства (см. раздел перечисление [**D3D10 \_ Создание \_ \_ флага устройства**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) ), включающее [уровни API](d3d10-graphics-programming-guide-api-features-layers.md). Эти флаги могут быть побитовыми или объединенными.

</dd> <dt>

*ппдевице* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Адрес указателя на созданное устройство (см. интерфейс [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Эта функция возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Эта функция пытается создать наилучшее устройство для оборудования. Во-первых, функция пытается создать устройство 10,1. Если не удается создать устройство 10,1, функция пытается создать устройство 10,0. Если ни одно из устройств не было успешно создано, функция возвращает \_ ошибку E.

Если приложению нужно создать только устройство 10,1 или только устройство 10,0, используйте следующие функции:

-   Используйте функцию [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) , чтобы создать только устройство Direct3D 10,0.
-   Используйте функцию [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) , чтобы создать только устройство Direct3D 10,1.
-   Используйте функцию [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) для получения указателя интерфейса [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) из указателя интерфейса [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .

устройство Direct3D 10,1 можно создать только на компьютерах под управлением Windows Vista с пакетом обновления 1 (sp1) или более поздней версии, а также с установленным оборудованием, совместимым с Direct3D 10,1. однако допускается вызов этой функции на компьютерах, работающих под управлением любой версии Windows с установленной библиотекой DLL D3DX10.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
