---
description: 'Принудительная отправка всех пакетированных спрайтов на устройство. Состояния устройств остаются в том виде, в котором они были после последнего вызова ID3DXSprite:: Begin. Затем список пакетных спрайтов удаляется.'
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'Метод ID3DXSprite:: Flush (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713770"
---
# <a name="id3dxspriteflush-method"></a>Метод ID3DXSprite:: Flush

Принудительная отправка всех пакетированных спрайтов на устройство. Состояния устройств остаются в том виде, в котором они были после последнего вызова [**ID3DXSprite:: Begin**](id3dxsprite--begin.md). Затем список пакетных спрайтов удаляется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: end**](id3dxsprite--end.md)
</dt> </dl>

 

 




