---
description: Возвращает указатель на массив константных описаний в таблице констант.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'Метод ID3DXConstantTable:: Жетконстантдеск (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8462ccfbbf306da08c67d460584a470d82301a5bda5f95a1ad09b2062702ee62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607214"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a>Метод ID3DXConstantTable:: Жетконстантдеск

Возвращает указатель на массив константных описаний в таблице констант.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хконстант* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор константы. См. [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*пдеск* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Возвращает указатель на массив описаний. См. [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указанный вход должен быть максимальным размером массива. Выходные данные — это количество элементов, заполняемых в массиве при возврате функции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

**ID3DXConstantTable:: жетконстантдеск** иногда возвращает [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md) с числом регистров \_ 0. Это произойдет, когда константа появится в более чем одном \_ наборе регистров, но не содержит место в выделенном наборе регистров.

Так как образец может отображаться в таблице констант более одного раза, этот метод может возвращать массив описаний, каждый из которых имеет другой индекс Register.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable:: DESC**](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
