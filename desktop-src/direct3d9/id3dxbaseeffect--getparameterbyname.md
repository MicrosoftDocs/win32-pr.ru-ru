---
description: Возвращает маркер параметра верхнего уровня или параметра члена структуры путем поиска его имени.
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: 'Метод ID3DXBaseEffect:: Жетпараметербинаме (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f9f7457ffa3bba867d03cceb3521664fecc9d67d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000514"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a>Метод ID3DXBaseEffect:: Жетпараметербинаме

Возвращает маркер параметра верхнего уровня или параметра члена структуры путем поиска его имени.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер параметра или **значение NULL** для параметров верхнего уровня. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Строка, содержащая имя параметра.

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

 

 
