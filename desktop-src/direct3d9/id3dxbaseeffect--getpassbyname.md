---
description: Возвращает маркер прохода путем поиска его имени.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'Метод ID3DXBaseEffect:: Жетпассбинаме (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5837d2b69c793f788c4c89f648402e7924bc2f3af9a92bbbe596c133efe10d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987764"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a>Метод ID3DXBaseEffect:: Жетпассбинаме

Возвращает маркер прохода путем поиска его имени.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хтечникуе* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер родительского метода. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Строка, содержащая имя этапа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает маркер первого прохода в указанном методе с указанным именем или **значение NULL** , если имя не найдено. См. раздел [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
