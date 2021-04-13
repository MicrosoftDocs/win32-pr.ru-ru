---
description: Завершение активного прохода.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'Метод ID3DXEffect:: Ендпасс (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355010"
---
# <a name="id3dxeffectendpass-method"></a>Метод ID3DXEffect:: Ендпасс

Завершение активного прохода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndPass();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Этот метод всегда возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Приложение сообщает об окончании отрисовки активного прохода, вызвав **ID3DXEffect:: ендпасс**. Каждый **ID3DXEffect:: ендпасс** должен быть частью соответствующей пары вызовов [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) и **ID3DXEffect:: ендпасс** .

Все совпадающие пары вызовов [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) и **ID3DXEffect:: ендпасс** должны находиться в соответствующей паре вызовов [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) и [**ID3DXEffect:: end**](id3dxeffect--end.md) .

Если приложение изменяет любое состояние влияния с помощью любого из методов [**Effect:: Setx**](id3dxeffect.md) внутри пары сопоставления [**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) / **ID3DXEffect:: ендпасс** , приложение должно вызвать [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) перед любым вызовом дравкспримитиве для распространения изменений состояния на устройство перед отрисовкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




