---
title: Player. status
description: свойство status получает значение, указывающее состояние проигрыватель Windows Media.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- проигрыватель Windows Media Player. status
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
ms.openlocfilehash: a03ef010bfcb5ee936183724331e97fac5d6f5912d87c5281a55106519c104e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572053"
---
# <a name="playerstatus"></a>Player. status

свойство **status** получает значение, указывающее состояние проигрыватель Windows Media.

## <a name="syntax"></a>Синтаксис

*проигрыватель* . **состояние**

## <a name="possible-values"></a>Возможные значения

Это свойство является строкой, доступная только для чтения.

## <a name="remarks"></a>Remarks

Значения, содержащиеся в этом свойстве, могут быть изменены в любое время, и их следует использовать только в целях вывода.

Событие **StatusChange** срабатывает при каждом изменении значения свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 7,0 или более поздней версии.<br/>                                      |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Событие Player. StatusChange**](player-player-statuschange.md)
</dt> </dl>

 

 





