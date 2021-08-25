---
description: Компиляция результата.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'Метод ID3DXEffectCompiler:: Компилиффект (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f3769f3f7433aadc55e766d68ecc152a4e26444cf506344f80e3f11a0bca8fcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951664"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a>Метод ID3DXEffectCompiler:: Компилиффект

Компиляция результата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Параметры компиляции, определяемые различными флагами. Компилятор Direct3D 10 HLSL теперь является значением по умолчанию. Дополнительные сведения см. в разделе [Флаги D3DXSHADER](d3dxshader-flags.md) .

</dd> <dt>

*ппеффект* \[ out, retval\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Буфер, содержащий скомпилированный результат. Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*пперрормсгс* \[ out, retval\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Буфер, содержащий по крайней мере первое сообщение об ошибке компиляции. Это относится к ошибкам компилятора и ошибкам при компиляции на высоком уровне. Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ .

Если аргументы недопустимы, метод возвратит D3DERR \_ инвалидкалл.

Если метод завершается с ошибкой, возвращается значение E \_ Failed.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> </dl>

 

 
