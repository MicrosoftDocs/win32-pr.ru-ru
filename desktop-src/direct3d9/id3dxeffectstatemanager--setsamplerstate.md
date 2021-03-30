---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки образца.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: 'Метод ID3DXEffectStateManager:: Сетсамплерстате (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355180"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a>Метод ID3DXEffectStateManager:: Сетсамплерстате

Функция обратного вызова, которая должна быть реализована пользователем для установки образца.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Образец* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Номер образца для отсчета от нуля.

</dd> <dt>

*Тип* \[ окне\]
</dt> <dd>

Тип: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**

Определяет состояние образца, которое может определять фильтрацию, адресацию или цвет границы. См. [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).

</dd> <dt>

*Значение* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Значение из одного из типов состояния выборки в поле Тип.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Метод, реализуемый пользователем, должен возвращать значение S \_ ОК. Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.

-   При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.
-   Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) завершится ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
