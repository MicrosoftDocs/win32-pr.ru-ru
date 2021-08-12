---
description: 'Вызовите его после ID3DX10Sprite:: Flush. Если \_ \_ \_ при вызове ID3DX10Sprite:: Begin было указано состояние Save D3DX10, то этот API восстановит состояние устройства до вызова ID3DX10Sprite:: Begin.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'Метод ID3DX10Sprite:: end (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02cfa1e92275230bd3a853aa9079187181089c46b4e4f193404b9dc0c709c9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302293"
---
# <a name="id3dx10spriteend-method"></a>Метод ID3DX10Sprite:: end

Вызовите его после ID3DX10Sprite:: Flush. Если \_ \_ \_ при вызове ID3DX10Sprite:: Begin было указано состояние Save D3DX10, то этот API восстановит состояние устройства до вызова ID3DX10Sprite:: Begin.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT End();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




