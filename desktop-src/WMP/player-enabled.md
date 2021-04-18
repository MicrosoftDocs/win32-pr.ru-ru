---
title: Проигрыватель. включен
description: Свойство Enabled указывает или получает значение, указывающее, включен ли элемент управления проигрывателя Windows Media.
ms.assetid: 65fea4d2-3330-4cce-bdaf-fae00304271a
keywords:
- Проигрыватель Windows Media с поддержкой проигрывателя.
topic_type:
- apiref
api_name:
- Player.enabled
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d002d1f1420d17d4b1a0b7dd3028b0f2dc0f6f7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694579"
---
# <a name="playerenabled"></a>Проигрыватель. включен

Свойство **Enabled** указывает или получает значение, указывающее, включен ли элемент управления проигрывателя Windows Media.

## <a name="syntax"></a>Синтаксис

*проигрыватель* . **включено**

## <a name="possible-values"></a>Возможные значения

Это свойство является **логическим значением** для чтения и записи.



| Значение | Описание                                           |
|-------|-------------------------------------------------------|
| true  | По умолчанию. Элемент управления проигрывателя Windows Media включен. |
| false | Элемент управления проигрывателя Windows Media отключен.         |



 

## <a name="remarks"></a>Комментарии

Если параметр **включен** имеет значение false, то во время полноэкранного воспроизведения проигрыватель Windows Media скрывает пользовательские элементы управления.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





