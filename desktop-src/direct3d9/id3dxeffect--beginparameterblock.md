---
description: Начать запись изменений состояния в блоке параметров.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'Метод ID3DXEffect:: Бегинпараметерблокк (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7345a045d152d5637b656bf4e9090b9645baf33645905e5e956737a1e6ede30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494284"
---
# <a name="id3dxeffectbeginparameterblock-method"></a>Метод ID3DXEffect:: Бегинпараметерблокк

Начать запись изменений состояния в блоке параметров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Изменения состояния параметров эффектов захвата до вызова Ендпараметерблокк. Параметры эффектов включают любые изменения состояния, находящиеся за пределами прохода. Удалите блоки параметров, если они больше не нужны, вызвав Делетепараметерблокк.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: Ендпараметерблокк**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect:: Апплипараметерблокк**](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D Елетепараметерблокк**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




