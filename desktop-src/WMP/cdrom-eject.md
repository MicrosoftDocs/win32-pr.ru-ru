---
title: Метод CDROM. EJECT
description: Метод Eject извлекает компакт-диск или DVD-диск из накопителя. | Метод CDROM. EJECT
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- метод извлечения Windows Media Player
- метод извлечения Windows Media Player, класс CDROM
- Класс CDROM проигрыватель Windows Media Player, метод reeject
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693984"
---
# <a name="cdromeject-method"></a>Метод CDROM. EJECT

Метод **Eject** извлекает компакт-диск или DVD-диск из накопителя.

## <a name="syntax"></a>Синтаксис


```JScript
Cdrom.eject()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если дверца диска открыта, этот метод закрывает дверцу.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере создается HTML-элемент Button, который использует *CDROM*. **Извлеките** , чтобы открыть дверцу диска с нулевым индексом описателя. Объект **Player** создан с идентификатором "Player".


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Версия<br/>                  | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект CDROM**](cdrom-object.md)
</dt> <dt>

[**Player. Плайстате**](player-playstate.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





