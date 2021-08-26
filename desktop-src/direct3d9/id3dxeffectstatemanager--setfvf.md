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
ms.openlocfilehash: 828f6873ed9bf48de6a02d4195fdd1fa9d2bc39f99da1f8906fd8a2c53075cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026414"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
