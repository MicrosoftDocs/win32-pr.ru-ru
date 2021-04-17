---
title: Player. status
description: Свойство Status извлекает значение, указывающее состояние проигрывателя Windows Media.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Проигрыватель проигрывателя Windows Media. status
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704151"
---
# <a name="playerstatus"></a>Player. status

Свойство **Status** извлекает значение, указывающее состояние проигрывателя Windows Media.

## <a name="syntax"></a>Синтаксис

*проигрыватель* . **состояние**

## <a name="possible-values"></a>Возможные значения

Это свойство является строкой, доступная только для чтения.

## <a name="remarks"></a>Комментарии

Значения, содержащиеся в этом свойстве, могут быть изменены в любое время, и их следует использовать только в целях вывода.

Событие **StatusChange** срабатывает при каждом изменении значения свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 7,0 или более поздней версии.<br/>                                      |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Событие Player. StatusChange**](player-player-statuschange.md)
</dt> </dl>

 

 





