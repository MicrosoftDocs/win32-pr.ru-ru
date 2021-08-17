---
description: 'Метод ID3DXEffectStateManager:: Сетпикселшадерконстанти — функция обратного вызова, которая должна быть реализована пользователем для установки массива целочисленных констант шейдера вершин.'
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: 'Метод ID3DXEffectStateManager:: Сетпикселшадерконстанти (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a817ac4e092eb9d8be2e4e2da02af051ae957dc97655b45e4e48dbe85b115ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121507"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a>Метод ID3DXEffectStateManager:: Сетпикселшадерконстанти

Функция обратного вызова, которая должна быть реализована пользователем для задания массива целочисленных констант шейдера вершин.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Стартрегистер* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс первого регистра констант.

</dd> <dt>

*пконстантдата* \[ заполняет\]
</dt> <dd>

Тип: **const [**int**](../winprog/windows-data-types.md) \***

Массив целочисленных констант.

</dd> <dt>

*Регистеркаунт* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество регистров в Пконстантдата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Метод, реализуемый пользователем, должен возвращать значение S \_ ОК. Если при задании состояния устройства происходит сбой обратного вызова, произойдет одно из следующих условий.

-   При выполнении действия [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md)произойдет сбой.
-   Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетпикселшадерконстанти**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) завершится ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
