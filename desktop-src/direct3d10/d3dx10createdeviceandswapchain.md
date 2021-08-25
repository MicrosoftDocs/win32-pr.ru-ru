---
description: Создайте наилучшее устройство Direct3D и цепочку буферов.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: Функция D3DX10CreateDeviceAndSwapChain (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: aa92b0fd7efb9c6f457fd035fad28992d965a4cf2f6fdad39936292f7a70a996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852374"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>Функция D3DX10CreateDeviceAndSwapChain

Создайте наилучшее устройство Direct3D и цепочку буферов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*падаптер* \[ окне\]
</dt> <dd>

Тип: **[ **идксгиадаптер**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Указатель на [**идксгиадаптер**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).

</dd> <dt>

*Дривертипе* \[ окне\]
</dt> <dd>

Тип: **[ **D3D10 \_ \_ Тип драйвера**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Тип драйвера для устройства. См. раздел [**\_ \_ Тип драйвера D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

</dd> <dt>

*Программное обеспечение* \[ окне\]
</dt> <dd>

Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**

Обработчик для библиотеки DLL, реализующей программное средство прорисовки. Должен иметь **значение NULL** , если дривертипе не является программным. ХМОДУЛЕ библиотеки DLL можно получить с помощью [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)или [Ошибка GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Необязательный элемент. Флаги создания устройств (см. раздел [**D3D10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)), который включает [уровни API](d3d10-graphics-programming-guide-api-features-layers.md). Эти флаги могут быть побитовыми или объединенными.

</dd> <dt>

*псвапчаиндеск* \[ окне\]
</dt> <dd>

Тип: **[ **\_ \_ цепочка \_ перекачки DXGI**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

Описание цепочки буферов обмена. См. раздел " [**\_ \_ цепочка \_ подкачки DXGI**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)".

</dd> <dt>

*ппсвапчаин* \[ заполняет\]
</dt> <dd>

Тип: **[ **идксгисвапчаин**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

Адрес указателя на [**идксгисвапчаин**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).

</dd> <dt>

*ппдевице* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Адрес указателя на [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) , который будет принимать созданное устройство.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Этот метод возвращает один из следующих [кодов возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

Для создания наилучшего устройства этот метод реализует несколько вариантов создания устройства. Во-первых, метод пытается создать устройство 10,1 (и цепь подкачки). Если это не удается, метод пытается создать устройство 10,0. Если это не удается, метод завершится ошибкой. Если приложению нужно создать только устройство 10,1 или только устройство 10,0, используйте эти API-интерфейсы.

-   Используйте [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) , чтобы создать устройство и цепочку подкачки Direct3D 10,0.
-   Используйте [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) , чтобы создать устройство и цепочку подкачки Direct3D 10,1.

для этого метода требуется Windows Vista с пакетом обновления 1 (sp1).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
