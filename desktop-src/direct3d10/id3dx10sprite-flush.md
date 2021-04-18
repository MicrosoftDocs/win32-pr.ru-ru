---
description: 'Принудительная отправка всех пакетированных спрайтов на устройство. Состояния устройств остаются в том виде, в котором они были после последнего вызова ID3DX10Sprite:: Begin. Затем список пакетных спрайтов удаляется.'
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'Метод ID3DX10Sprite:: Flush (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714040"
---
# <a name="id3dx10spriteflush-method"></a>Метод ID3DX10Sprite:: Flush

Принудительная отправка всех пакетированных спрайтов на устройство. Состояния устройств остаются в том виде, в котором они были после последнего вызова ID3DX10Sprite:: Begin. Затем список пакетных спрайтов удаляется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




