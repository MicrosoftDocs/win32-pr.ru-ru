---
description: Функция обратного вызова, которая должна быть реализована пользователем для установки кода ФВФ.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'Метод ID3DXEffectStateManager:: Сетфвф (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694210"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a>Метод ID3DXEffectStateManager:: Сетфвф

Функция обратного вызова, которая должна быть реализована пользователем для установки кода ФВФ.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Фвф* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Константа ФВФ, определяющая способ интерпретации данных вершин. См. [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Метод, реализуемый пользователем, должен возвращать значение S \_ ОК. Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.

-   При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.
-   Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетфвф**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) завершится ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
