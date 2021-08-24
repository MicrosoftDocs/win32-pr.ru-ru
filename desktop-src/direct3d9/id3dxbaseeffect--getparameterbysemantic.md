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
ms.openlocfilehash: fa00ef4585462f068e95fcefca8332acd46930efaf1bb1c108a471511ab63eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791014"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
