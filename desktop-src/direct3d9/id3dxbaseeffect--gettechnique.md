---
description: Возвращает маркер метода.
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: 'Метод ID3DXBaseEffect:: Method (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6d193e08bf40ac67ba46218e9ce3e11b510d7014239a09b1c1b0000be5ec9420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987744"
---
# <a name="id3dxbaseeffectgettechnique-method"></a>Метод ID3DXBaseEffect:: Method

Возвращает маркер метода.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс методики.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает маркер указанного метода или **значение NULL** , если индекс является недопустимым. См. раздел [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
