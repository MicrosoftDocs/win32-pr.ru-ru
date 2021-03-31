---
description: Применяет к строке шаблон стиппле.
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'Метод ID3DXLine:: Сетпаттерн (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80a0485991bc06bdb9fcd3280017d4cc60b492ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157235"
---
# <a name="id3dxlinesetpattern-method"></a>Метод ID3DXLine:: Сетпаттерн

Применяет к строке шаблон стиппле.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двпаттерн* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Описывает шаблон стиппле: 1 является непрозрачным, 0 является прозрачным.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
