---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки освещения.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'Метод ID3DXEffectStateManager:: Сетлигхт (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1306283b098922706f39abc7ffe2514d2fba0e5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694209"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a>Метод ID3DXEffectStateManager:: Сетлигхт

Функция обратного вызова, которая должна быть реализована пользователем для установки освещения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс источника освещения. Это тот же индекс в [**IDirect3DDevice9:: сетлигхт**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).

</dd> <dt>

*плигхт* \[ окне\]
</dt> <dd>

Тип: **const [**D3DLight9**](d3dlight9.md) \***

Объект light. См. [**D3DLIGHT9**](d3dlight9.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Метод, реализуемый пользователем, должен возвращать значение S \_ ОК. Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.

-   При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.
-   Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетлигхт**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) завершится ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
