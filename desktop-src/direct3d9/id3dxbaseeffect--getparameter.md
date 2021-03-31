---
description: Возвращает маркер параметра верхнего уровня или параметра-члена структуры.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: Метод ID3DXBaseEffect::-Parameter (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081944"
---
# <a name="id3dxbaseeffectgetparameter-method"></a>Метод ID3DXBaseEffect:: Parameter

Возвращает маркер параметра верхнего уровня или параметра-члена структуры.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер параметра или **значение NULL** для параметров верхнего уровня. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс параметра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает маркер указанного параметра или **значение NULL** , если индекс является недопустимым. См. раздел [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
