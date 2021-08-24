---
description: Возвращает маркер заметки.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: Метод ID3DXBaseEffect::-annotation (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c35deeb04e7cf21be429976c102fdf7c3126b1691b3f63725fc994ef79f7ad42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279014"
---
# <a name="id3dxbaseeffectgetannotation-method"></a>Метод ID3DXBaseEffect:: annotation

Возвращает маркер заметки.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хобжект* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер метода, этапа или параметра верхнего уровня. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс заметки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает маркер указанной заметки или **значение NULL** , если индекс является недопустимым. См. раздел [Handles (Direct3D 9)](handles.md).

## <a name="remarks"></a>Remarks

Заметки представляют собой определяемые пользователем данные, которые могут быть присоединены к любому методу, параметру Pass или. См. раздел [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
