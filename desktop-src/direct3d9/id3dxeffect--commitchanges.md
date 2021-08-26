---
description: Распространите изменения состояния, происходящие внутри активного прохода на устройстве перед отрисовкой.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'Метод ID3DXEffect:: CommitChanges (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5b81cd2674e08473358e031b827528121537264df11dba54c6a1f610ac054ee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951764"
---
# <a name="id3dxeffectcommitchanges-method"></a>Метод ID3DXEffect:: CommitChanges

Распространите изменения состояния, происходящие внутри активного прохода на устройстве перед отрисовкой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Remarks

Если приложение изменяет любое состояние влияния с помощью любого из методов [**ID3DXEffect:: Setx**](id3dxeffect.md) в паре сопоставления [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) / [**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md) , приложение должно вызвать **ID3DXEffect:: CommitChanges** перед любым вызовом дравкспримитиве для распространения изменений состояния на устройство перед отрисовкой. Если изменения состояния не происходят в паре **ID3DXEffect:: бегинпасс** и **ID3DXEffect:: Ендпасс** , вызов **ID3DXEffect:: CommitChanges** не требуется.

Это несколько отличается для всех общих параметров в клонированном результате. Если прием активен в клонированном результате (то есть при вызове [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) , но и при вызове [**ID3DXEffect:: end**](id3dxeffect--end.md) не был вызван), **ID3DXEffect:: CommitChanges** обновляет параметры, которые не являются общими, как ожидалось. Чтобы обновить общий параметр (только для клонированного действия, для которого активен метод), вызовите **ID3DXEffect:: end** , чтобы деактивировать методику, и **ID3DXEffect:: Begin** для повторной активации метода перед вызовом **ID3DXEffect:: CommitChanges**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




