---
title: Параметры. дефаултфраме
description: Свойство Дефаултфраме указывает или получает имя кадра, используемого для вывода URL-адреса, полученного в событии команду скрипта.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Параметры. дефаултфраме проигрыватель Windows Media
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
ms.openlocfilehash: 0240864cd19c1a4d84c30abfc6e6b8ecb08457d26c3c660d19fc18d228b19615
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571814"
---
# <a name="settingsdefaultframe"></a>Параметры. дефаултфраме

Свойство **дефаултфраме** указывает или получает имя кадра, используемого для вывода URL-адреса, полученного в событии **команду скрипта** .

## <a name="syntax"></a>Синтаксис

Player. Settings. Дефаултфраме

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи, соответствующей значению атрибута **Name** целевого элемента Frame.

## <a name="remarks"></a>Remarks

Если целевой кадр указан в событии **команду скрипта** , это свойство игнорируется.

Это свойство игнорируется при использовании приложения Netscape Navigator Java. в навигаторе каждая полученная команда сценария URL-адреса отображает URL-адрес в новом окне браузера, независимо от значения *Параметры*. **дефаултфраме**.

**проигрыватель Windows Media 10 Mobile**: это свойство доступно только для чтения и всегда возвращает пустую строку.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Событие Player. команду скрипта**](player-player-scriptcommand.md)
</dt> <dt>

[**Параметры Объектами**](settings-object.md)
</dt> <dt>

[**Использование проигрывателя Windows Media с Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





