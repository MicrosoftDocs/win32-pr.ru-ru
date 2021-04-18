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
ms.openlocfilehash: 0566d423d277dc3f39f36f8c1fda297ec917eb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703629"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: Сетбоненаме**](id3dxskininfo--setbonename.md)
</dt> <dt>

[**ID3DXSkinInfo:: Жетнумбонес**](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
