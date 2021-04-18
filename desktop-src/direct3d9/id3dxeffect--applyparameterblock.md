---
description: Применить значения в блоке состояния к текущему состоянию системы.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'Метод ID3DXEffect:: Апплипараметерблокк (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713724"
---
# <a name="id3dxeffectapplyparameterblock-method"></a>Метод ID3DXEffect:: Апплипараметерблокк

Применить значения в блоке состояния к текущему состоянию системы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ApplyParameterBlock(
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

## <a name="remarks"></a>Комментарии

Изменения состояния параметров эффектов захвата в блоке параметров путем вызова Бегинпараметерблокк; останавливает запись изменений состояния путем вызова Ендпараметерблокк. Эти изменения состояния включают любые изменения параметров эффектов, происходящие внутри метода (в том числе за пределами прохода). Когда вы завершите работу с блоком параметров, вызовите Делетепараметерблокк для восстановления памяти.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: Бегинпараметерблокк**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect:: Ендпараметерблокк**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D Елетепараметерблокк**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




