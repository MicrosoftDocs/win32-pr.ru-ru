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
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355013"
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

## <a name="remarks"></a>Комментарии

Все отрисовки в результате выполняются в соответствующей паре вызовов [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) и **ID3DXEffect:: end** . После отрисовки всех проходов необходимо вызвать **ID3DXEffect:: end** , чтобы завершить активный метод. Система эффектов отвечает с помощью блока State, созданного при вызове **ID3DXEffect:: Begin** , для автоматического восстановления состояния конвейера перед **ID3DXEffect:: Begin**.

По умолчанию система эффектов осуществляет сохранение состояния перед приемом и восстановление состояния после приемки. Если вы решили отключить эту функцию сохранения и восстановления, см. раздел [D3DXFX \_ донотсавесамплерстате](d3dxfx.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




