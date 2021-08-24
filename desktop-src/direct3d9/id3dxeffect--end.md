---
description: Завершает активный метод.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'Метод ID3DXEffect:: end (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6c93dc98febe2f5e539d3be678322860fe14069c2f8bf6b75cc42864b922e1f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748664"
---
# <a name="id3dxeffectend-method"></a>Метод ID3DXEffect:: end

Завершает активный метод.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT End();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Этот метод всегда возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Все отрисовки в результате выполняются в соответствующей паре вызовов [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) и **ID3DXEffect:: end** . После отрисовки всех проходов необходимо вызвать **ID3DXEffect:: end** , чтобы завершить активный метод. Система эффектов отвечает с помощью блока State, созданного при вызове **ID3DXEffect:: Begin** , для автоматического восстановления состояния конвейера перед **ID3DXEffect:: Begin**.

По умолчанию система эффектов осуществляет сохранение состояния перед приемом и восстановление состояния после приемки. Если вы решили отключить эту функцию сохранения и восстановления, см. раздел [D3DXFX \_ донотсавесамплерстате](d3dxfx.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




