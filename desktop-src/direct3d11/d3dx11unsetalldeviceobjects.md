---
title: Функция D3DX11UnsetAllDeviceObjects (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать метод ссылку ID3D11DeviceContext Клеарстате.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- D3DX11UnsetAllDeviceObjects функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ac7e33bfef7f8470f616ac07b3aa90463f3f3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355340"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a>Функция D3DX11UnsetAllDeviceObjects

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

> [!Note]  
> Вместо использования этой функции рекомендуется использовать метод [**ссылку ID3D11DeviceContext:: клеарстате**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) .

 

Удаляет все ресурсы с устройства, присвоив их указателям **значение NULL**. Этот метод должен вызываться во время завершения работы приложения. Это гарантирует, что когда один из них освобождает все ресурсы, которые не привязаны к устройству.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекст* \[ окне\]
</dt> <dd>

Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





