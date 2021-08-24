---
description: Возвращает имя кости из индекса костей.
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'Метод ID3DXSkinInfo:: Жетбоненаме (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa56b175d9047935b9f92829823ba2608536ddabb90cb0ad674b86b73cc17475
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674734"
---
# <a name="id3dxskininfogetbonename-method"></a>Метод ID3DXSkinInfo:: Жетбоненаме

Возвращает имя кости из индекса костей.

## <a name="syntax"></a>Синтаксис


```C++
LPCSTR GetBoneName(
  [in] DWORD Bone
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Кость* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Номер кости.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Возвращает имя кости. Не освобождайте эту строку.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: Сетбоненаме**](id3dxskininfo--setbonename.md)
</dt> <dt>

[**ID3DXSkinInfo:: Жетнумбонес**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
