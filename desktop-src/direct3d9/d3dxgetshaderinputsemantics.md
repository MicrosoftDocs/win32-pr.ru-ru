---
description: Возвращает семантику для входных данных шейдера. Используйте этот метод, чтобы определить формат входной вершины.
ms.assetid: e94b2b14-3830-4a13-8c23-7841a56d6730
title: Функция D3DXGetShaderInputSemantics (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderInputSemantics
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2032f241d6ca5c22506c0875a21f9d5b431920df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713665"
---
# <a name="d3dxgetshaderinputsemantics-function"></a>Функция D3DXGetShaderInputSemantics

Возвращает семантику для входных данных шейдера. Используйте этот метод, чтобы определить формат входной вершины.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXGetShaderInputSemantics(
  _In_  const DWORD        *pFunction,
  _In_        D3DXSEMANTIC *pSemantics,
  _Out_       UINT         *pCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфунктион* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на поток функции шейдера DWORD.

</dd> <dt>

*псемантикс* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXSEMANTIC**](d3dxsemantic.md)\***

Указатель на массив структур [**D3DXSEMANTIC**](d3dxsemantic.md) . Функция будет заполнять этот массив семантикой для каждого входного элемента, на который ссылается шейдер. Предполагается, что этот массив содержит по крайней мере элементы MAXD3DDECLLENGTH. Однако вызов **D3DXGetShaderInputSemantics** с Псемантикс = **null** возвратит количество элементов, необходимых для pCount.

</dd> <dt>

*pCount* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Возвращает количество элементов в Псемантикс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Используйте **D3DXGetShaderInputSemantics** для возврата списка семантики ввода, необходимой шейдеру. Это способ узнать, какой формат входной вершины предназначен для шейдера высокого уровня (HLSL). Если у шейдера есть дополнительные входы, которые отсутствуют в объявлении вершины, можно создать дополнительный поток вершин с шагом 0, в котором отсутствуют компоненты со значениями по умолчанию. Например, этот метод можно использовать для предоставления цвета вершин по умолчанию для моделей, которые не задают его.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
