---
description: Выполняет поиск определенного комментария в шейдере. Комментарий определяется с помощью кода с четырьмя символами (FOURCC) в первом DWORD комментария.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Функция D3DXFindShaderComment (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703791"
---
# <a name="d3dxfindshadercomment-function"></a>Функция D3DXFindShaderComment

Выполняет поиск определенного комментария в шейдере. Комментарий определяется с помощью кода с четырьмя символами (FOURCC) в первом DWORD комментария.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфунктион* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на поток функции шейдера DWORD.

</dd> <dt>

*FourCC* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Код FOURCC, определяющий блок комментариев. См. раздел [форматы FourCC](d3dformat.md).

</dd> <dt>

*ппдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)\***

Возвращает указатель на данные комментария (не включая маркер комментария и код FOURCC). Это значение может быть **равно NULL**.

</dd> <dt>

*псизеинбитес* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Возвращает размер данных комментария в байтах. Это значение может быть **равно NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если комментарий не найден и другие ошибки не произошли, \_ возвращается значение false.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции шейдера](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
