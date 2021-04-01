---
title: Иаженткоммандсекс Сетглобалвоицекоммандсенаблед
description: Иаженткоммандсекс Сетглобалвоицекоммандсенаблед
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133795"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a>Иаженткоммандсекс:: Сетглобалвоицекоммандсенаблед

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

Задает свойство [**Enabled**](enabled-property.md) для грамматики голоса для глобальных команд агента Microsoft Agent.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*бенабле*
</dt> <dd>

Логическое значение, которое указывает, включена ли грамматика голоса для глобальных команд агента. **Значение true** включает грамматику голоса; **Значение false** отключает его.

</dd> </dl>

Microsoft Agent автоматически добавляет параметры голоса (грамматики) для открытия и закрытия окна "Voice Commands", а также для отображения и скрытия символа. Если задано **значение false**, то агент отключает любые параметры голоса для этих команд, а также параметры голоса для [**заголовка**](caption-property.md) объектов [**команд**](/windows/desktop/lwef/the-command-object) другого клиента. Это позволяет исключить их из текущей активной грамматики клиента. Однако, так как это потенциально блокирует голосовой доступ к другим клиентам, сбросьте это свойство в **значение true** после обработки речевого ввода пользователя.

Отключение свойства не влияет на всплывающее меню символа. Глобальные команды, добавленные сервером, по-прежнему будут отображаться. Их нельзя удалить из всплывающего меню.

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: Жетглобалвоицекоммандсенаблед**](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 