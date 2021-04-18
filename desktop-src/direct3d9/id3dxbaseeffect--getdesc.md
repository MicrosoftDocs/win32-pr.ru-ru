---
description: Возвращает описание результата.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'Метод ID3DXBaseEffect:: desc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694321"
---
# <a name="id3dxbaseeffectgetdesc-method"></a>Метод ID3DXBaseEffect:: DESC

Возвращает описание результата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдеск* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXEFFECT \_ DESC**](d3dxeffect-desc.md)\***

Возвращает описание результата. См. [**D3DXEFFECT \_ DESC**](d3dxeffect-desc.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




