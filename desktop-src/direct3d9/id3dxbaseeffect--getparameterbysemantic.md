---
description: Возвращает маркер параметра верхнего уровня или параметра-члена структуры путем поиска его семантики с поиском без учета регистра.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'Метод ID3DXBaseEffect:: Жетпараметербисемантик (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355880"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>Метод ID3DXBaseEffect:: Жетпараметербисемантик

Возвращает маркер параметра верхнего уровня или параметра-члена структуры путем поиска его семантики с поиском без учета регистра.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер параметра или **значение NULL** для параметров верхнего уровня. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*псемантик* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Строка, содержащая имя семантики.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает маркер первого параметра, который соответствует заданной семантике, или **значение NULL** , если семантика не была найдена. См. раздел [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
