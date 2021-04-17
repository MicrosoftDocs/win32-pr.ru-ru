---
title: VIEW. Ретурнтомедиацентер
description: Метод Ретурнтомедиацентер возвращает пользователя в полноэкранный режим проигрывателя Windows Media.
ms.assetid: eebf0679-5704-498c-8eb3-f7710e0cb1fe
keywords:
- Просмотреть. Ретурнтомедиацентер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.returnToMediaCenter
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c5f0c86bdd15140ba92261d1f5e8c510d77afc7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704531"
---
# <a name="viewreturntomediacenter"></a>VIEW. Ретурнтомедиацентер

Метод **ретурнтомедиацентер** возвращает пользователя в полноэкранный режим проигрывателя Windows Media.

``` syntax
        elementID.returnToMediaCenter()
```

## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="examples"></a>Примеры


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.returnToMediaCenter()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**VIEW, элемент**](view-element.md)
</dt> </dl>

 

 





