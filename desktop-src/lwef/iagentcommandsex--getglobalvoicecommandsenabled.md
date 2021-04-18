---
title: Иаженткоммандсекс Жетглобалвоицекоммандсенаблед
description: Иаженткоммандсекс Жетглобалвоицекоммандсенаблед
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412883"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a>Иаженткоммандсекс:: Жетглобалвоицекоммандсенаблед

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

Возвращает значение, указывающее, включена ли грамматика голоса для глобальных команд агента.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*пбенаблед*
</dt> <dd>

Адрес, который получает **значение true** , если включена грамматика голоса для глобальных команд агента, **значение false** , если отключено.

</dd> </dl>

Microsoft Agent автоматически добавляет параметры голоса (грамматики) для открытия и закрытия окна "Voice Commands", а также для отображения и скрытия символа. Когда этот метод возвращает **значение false**, все параметры голоса для этих команд, а также параметры голоса для [**заголовка**](caption-property.md) объектов [**команд**](/windows/desktop/lwef/the-command-object) других клиентов не включаются в грамматику. Это позволяет исключить их из текущей активной грамматики клиента. Однако этот параметр не отражает включение этих команд во всплывающем меню символа.

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: Сетглобалвоицекоммандсенаблед**](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 