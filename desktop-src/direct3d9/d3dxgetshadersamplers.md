---
description: Получение имен образцов, на которые имеются ссылки в шейдере.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Функция D3DXGetShaderSamplers (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da4c7381b0fe058e18dd2edfd86ef49f434cd1b57bff18303fce0ba939c5d299
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045002"
---
# <a name="d3dxgetshadersamplers-function"></a>Функция D3DXGetShaderSamplers

Получение имен образцов, на которые имеются ссылки в шейдере.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфунктион* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на поток функции шейдера DWORD.

</dd> <dt>

*псамплерс* \[ в, out\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Указатель на массив Лпкстрс. Функция будет заполнять этот массив указателями на имена образцов, содержащихся в *пфунктион*. Максимальный размер массива — это максимальное количество регистров образцов (16 для VS \_ 3 \_ 0 и PS \_ 3 \_ 0).

Чтобы узнать число используемых проб, проверьте *pCount* после вызова **D3DXGetShaderSamplers** с псамплерс = **null**.

</dd> <dt>

*pCount* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Возвращает число образцов, на которые ссылается шейдер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
