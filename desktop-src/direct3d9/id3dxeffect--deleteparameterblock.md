---
description: Удаляет блок параметров.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: 'ID3DXEffect: метод:D Елетепараметерблокк (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a53d97bc077f830bdf73f5a184e253a8537626cbba575b2a5b9e74247ea48702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494244"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a>ID3DXEffect: метод:D Елетепараметерблокк

Удаляет блок параметров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

 *хпараметерблокк* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Маркер блока параметров. Это маркер, возвращаемый [**ID3DXEffect:: ендпараметерблокк**](id3dxeffect--endparameterblock.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Блоки параметров — это блоки состояний эффектов. Используйте блок параметров для записи изменений состояния, чтобы их можно было применить позже с помощью одного вызова API. Если больше не требуется, удалите блок параметров, чтобы сократить использование памяти.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: Бегинпараметерблокк**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect:: Ендпараметерблокк**](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




