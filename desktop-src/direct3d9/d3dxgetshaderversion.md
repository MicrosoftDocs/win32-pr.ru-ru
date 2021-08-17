---
description: Возвращает версию шейдера скомпилированного шейдера.
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: Функция D3DXGetShaderVersion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cc76ebcb9a3b62b0097db5f1575e50416a89b9bfffdc9a17820388da4362aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123180"
---
# <a name="d3dxgetshaderversion-function"></a>Функция D3DXGetShaderVersion

Возвращает версию шейдера скомпилированного шейдера.

## <a name="syntax"></a>Синтаксис


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфунктион* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на поток функции DWORD.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Возвращает версию шейдера данного шейдера или нуль, если функция шейдера имеет **значение NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
