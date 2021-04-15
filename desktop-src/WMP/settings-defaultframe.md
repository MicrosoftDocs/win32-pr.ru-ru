---
title: Settings. Дефаултфраме
description: Свойство Дефаултфраме указывает или получает имя кадра, используемого для вывода URL-адреса, полученного в событии команду скрипта.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Проигрыватель Windows Media Settings. Дефаултфраме
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648725"
---
# <a name="settingsdefaultframe"></a>Settings. Дефаултфраме

Свойство **дефаултфраме** указывает или получает имя кадра, используемого для вывода URL-адреса, полученного в событии **команду скрипта** .

## <a name="syntax"></a>Синтаксис

Player. Settings. Дефаултфраме

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи, соответствующей значению атрибута **Name** целевого элемента Frame.

## <a name="remarks"></a>Комментарии

Если целевой кадр указан в событии **команду скрипта** , это свойство игнорируется.

Это свойство игнорируется при использовании приложения Netscape Navigator Java. В навигаторе каждая полученная команда сценария URL-адреса отображает URL-адрес в новом окне браузера, независимо от значения *параметров*. **дефаултфраме**.

**Проигрыватель Windows Media 10 Mobile**: это свойство доступно только для чтения и всегда возвращает пустую строку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Событие Player. команду скрипта**](player-player-scriptcommand.md)
</dt> <dt>

[**Объект параметров**](settings-object.md)
</dt> <dt>

[**Использование проигрывателя Windows Media с Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





