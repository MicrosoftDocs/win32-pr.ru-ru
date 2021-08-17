---
description: 'Метод ID3DXTextureShader:: Жетконстантбинаме — возвращает константу путем поиска ее имени.'
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: 'Метод ID3DXTextureShader:: Жетконстантбинаме (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55b3de81179c01171d7ee5ff7b845295709dfb8ead1a9bc1a7cdf615bc37c44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729105"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a>Метод ID3DXTextureShader:: Жетконстантбинаме

Возвращает константу путем поиска ее имени.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хконстант* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

[Маркер](handles.md) родительской структуры данных. Если константа является параметром верхнего уровня (отсутствует родительская структура данных), используйте **значение NULL**.

</dd> <dt>

*pName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Строка, содержащая имя константы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает уникальный идентификатор для константы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
