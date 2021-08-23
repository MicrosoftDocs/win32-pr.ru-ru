---
description: 'Метод ID3DXEffectStateManager:: Сетвертексшадерконстантф — функция обратного вызова, которая должна быть реализована пользователем для установки массива констант с плавающей запятой вершин.'
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'Метод ID3DXEffectStateManager:: Сетвертексшадерконстантф (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aecc510a01bbb461f9f8742f2125b39913335c2ff9b135083f0f59f3f6544b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748564"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a>Метод ID3DXEffectStateManager:: Сетвертексшадерконстантф

Функция обратного вызова, которая должна быть реализована пользователем для установки массива констант с плавающей точкой шейдера вершин.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
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

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Массив констант с плавающей запятой.

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
-   Вызов состояния динамического влияния (например, [**IDirect3DDevice9:: сетвертексшадерконстантф**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) завершится ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
