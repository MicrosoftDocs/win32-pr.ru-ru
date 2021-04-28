---
description: 'Метод ID3DXEffectStateManager:: Сетвертексшадерконстантб — функция обратного вызова, которая должна быть реализована пользователем для установки массива логических констант шейдера вершин.'
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: 'Метод ID3DXEffectStateManager:: Сетвертексшадерконстантб (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79d4972c301d7333869d68d36267186a67b37eb1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090412"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a>Метод ID3DXEffectStateManager:: Сетвертексшадерконстантб

Функция обратного вызова, которая должна быть реализована пользователем для задания массива логических констант шейдера вершин.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
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

Тип: **const [**bool**](../winprog/windows-data-types.md) \***

Массив логических констант.

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
-   Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетвертексшадерконстантб**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) завершится ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
