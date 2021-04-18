---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки состояния отрисовки.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'Метод ID3DXEffectStateManager:: Сетрендерстате (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713782"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a>Метод ID3DXEffectStateManager:: Сетрендерстате

Функция обратного вызова, которая должна быть реализована пользователем для установки состояния отрисовки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Состояние* \[ окне\]
</dt> <dd>

Тип: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**

Заданное состояние отрисовки. [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

</dd> <dt>

*Значение* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Значение состояния отрисовки. См. раздел [состояния эффектов (Direct3D 9)](effect-states.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Метод, реализуемый пользователем, должен возвращать значение S \_ ОК. Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.

-   При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.
-   Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) завершится ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
