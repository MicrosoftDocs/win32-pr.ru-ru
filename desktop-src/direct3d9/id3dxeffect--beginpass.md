---
description: Начинает проход в активном методе.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'Метод ID3DXEffect:: Бегинпасс (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9013a67c2d4e0e9760167bc979ac05edd4879c5414ce5c9b9c55528baf3f6a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987553"
---
# <a name="id3dxeffectbeginpass-method"></a>Метод ID3DXEffect:: Бегинпасс

Начинает проход в активном методе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Передать* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля целочисленный индекс в методе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Приложение устанавливает один активный проход (в рамках одной активной методики) в системе эффектов, вызывая **ID3DXEffect:: бегинпасс**. Приложение сигнализирует об окончании активного прохода, вызвав [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md). **ID3DXEffect:: бегинпасс** и **ID3DXEffect:: ендпасс** должны находиться в соответствующей паре в совпадающей паре [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) и [**ID3DXEffect:: end**](id3dxeffect--end.md) Calls.

Если приложение изменяет любое состояние влияния с помощью любого из методов [**Effect:: Setx**](id3dxeffect.md) внутри пары сопоставления **ID3DXEffect:: бегинпасс** / [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md) , приложение должно вызвать [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) , чтобы установить обновление устройства с изменением состояния. Если изменения состояния не происходят в паре **ID3DXEffect:: бегинпасс** и **ID3DXEffect:: Ендпасс** , вызов **ID3DXEffect:: CommitChanges** не требуется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
