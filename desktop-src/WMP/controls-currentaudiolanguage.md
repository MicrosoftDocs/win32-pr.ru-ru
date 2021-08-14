---
title: Controls. Куррентаудиолангуаже
description: Свойство Куррентаудиолангуаже указывает или получает код локали (LCID) звукового языка для воспроизведения.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- controls. куррентаудиолангуаже проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63c5eb53c9f408a9d50a7f738434e5dcd30fc804970b3e1ea95c985c90d62063
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750616"
---
# <a name="controlscurrentaudiolanguage"></a>Controls. Куррентаудиолангуаже

Свойство **куррентаудиолангуаже** указывает или получает код локали (LCID) звукового языка для воспроизведения.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство имеет **номер** для чтения и записи (**Long**).

## <a name="remarks"></a>Remarks

Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.

для Windows содержимого на основе носителя свойства и методы, связанные с выбором языка, поддерживают только один выход.

При работе с содержимым DVD при указании LCID будет выбрана первая доступная звуковая дорожка с указанным ИДЕНТИФИКАТОРом языка.

**проигрыватель Windows Media 10 Mobile:** Это свойство принимает или возвращает только код, не зависящий от языка (0).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Controls. Аудиолангуажекаунт**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls. Куррентаудиолангуажеиндекс**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. Жетаудиолангуажедескриптион**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. Жетаудиолангуажеид**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. Жетлангуаженаме**](controls-getlanguagename.md)
</dt> </dl>

 

 





