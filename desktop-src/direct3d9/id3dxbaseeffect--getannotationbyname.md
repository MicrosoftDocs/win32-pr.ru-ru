---
description: Возвращает маркер заметки путем поиска ее имени.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'Метод ID3DXBaseEffect:: Жетаннотатионбинаме (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694322"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a>Метод ID3DXBaseEffect:: Жетаннотатионбинаме

Возвращает маркер заметки путем поиска ее имени.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хобжект* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер метода, этапа или параметра верхнего уровня. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Строка, содержащая имя заметки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает маркер указанной заметки или **значение NULL** , если имя не найдено. См. раздел [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
