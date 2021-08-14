---
description: Возвращает указатель на пул общих параметров.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: Метод ID3DXEffect::-Pool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0220b2864d6c668c2d4fbb71925da6452f6cc8661d0d931a379969418dfe7e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521230"
---
# <a name="id3dxeffectgetpool-method"></a>Метод ID3DXEffect:: pool

Возвращает указатель на пул общих параметров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пппул* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Этот метод всегда возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Пулы содержат общие параметры между различными эффектами. См. раздел [клонирование и совместное использование (Direct3D 9)](cloning-and-sharing.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




