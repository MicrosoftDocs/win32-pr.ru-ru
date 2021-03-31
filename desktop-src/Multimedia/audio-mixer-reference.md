---
title: Справочник по звуковым микшерам
description: Справочник по звуковым микшерам
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- мультимедиа аудио, аудио миксерс
- аудио, аудио миксерс
- мультимедиа аудио, Справочник по микшерам
- аудио, Справочник по микшерам
- аудио миксерс, Справочник
- миксерс, Справочник
- Справочник по Audio миксерс, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260842"
---
# <a name="audio-mixer-reference"></a>Справочник по звуковым микшерам

В этом разделе описываются функции, структуры и сообщения, связанные с Audio миксерс. Эти элементы группируются следующим образом.

## <a name="querying-devices"></a>Запросы устройств

-   [**миксеркапс**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**миксержетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**миксержетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>Открытие и закрытие

-   [**миксерклосе**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**миксеропен**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>Получение идентификаторов микшера

-   [**миксержетид**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>Получение элементов управления "линия"

-   [**миксерконтрол**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**миксержетлинеконтролс**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**миксерлинеконтролс**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>Изменение атрибутов элемента управления

-   [**миксерконтролдетаилс**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**МИКСЕРКОНТРОЛДЕТАИЛС \_ Boolean**](/previous-versions//dd757295(v=vs.85))
-   [**МИКСЕРКОНТРОЛДЕТАИЛС \_ листтекст**](/previous-versions//dd757296(v=vs.85))
-   [**МИКСЕРКОНТРОЛДЕТАИЛС \_ подписанный**](/previous-versions//dd757297(v=vs.85))
-   [**МИКСЕРКОНТРОЛДЕТАИЛС \_ без знака**](/previous-versions//dd757298(v=vs.85))
-   [**миксержетконтролдетаилс**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**миксерсетконтролдетаилс**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>Получение сведений о строке

-   [**миксержетлинеинфо**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**миксерлине**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**\_ \_ изменение элемента управления mm миксм \_**](mm-mixm-control-change.md)
-   [**\_изменение миксм в \_ линии \_ mm**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>Отправка сообщений User-Defined

-   [**миксермессаже**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по звуковым микшерам](audio-mixer-reference.md)
</dt> </dl>

 

 