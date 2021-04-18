---
description: Возвращает маркер метода путем поиска его имени.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'Метод ID3DXBaseEffect:: Жеттечникуебинаме (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713989"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a>Метод ID3DXBaseEffect:: Жеттечникуебинаме

Возвращает маркер метода путем поиска его имени.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Строка, содержащая имя метода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает маркер первого метода с указанным именем или **значение NULL** , если имя не найдено. См. раздел [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
