---
title: Команда Иажентнотифисинк
description: Команда Иажентнотифисинк
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987446"
---
# <a name="iagentnotifysinkcommand"></a>Иажентнотифисинк:: Command

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

Уведомляет клиентское приложение о том, что [**команда**](/windows/desktop/lwef/the-command-object) была выбрана пользователем.

-   Нет возвращаемого значения.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*двкоммандид*
</dt> <dd>

Идентификатор альтернативы для команды наилучшего соответствия.

</dd> <dt>

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*пункусеринпут*
</dt> <dd>

Адрес интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) для объекта [**иажентусеринпут**](iagentuserinput.md) .

</dd> </dl>

Используйте [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения интерфейса [**иажентусеринпут**](iagentuserinput.md) .

Сервер оповещает входной-активный клиент, когда пользователь выбирает команду с помощью голоса или выбирая команду во всплывающем меню символа. Это событие возникает, даже если пользователь выбирает одну из команд сервера. В этом случае сервер возвращает идентификатор команды null, оценку достоверности и голосовой текст, возвращенный модулем распознавания речи для этой записи.

## <a name="see-also"></a>См. также:

[**иажентусеринпут**](iagentuserinput.md)


 

 