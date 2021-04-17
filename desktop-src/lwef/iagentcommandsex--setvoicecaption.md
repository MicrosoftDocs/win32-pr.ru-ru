---
title: Иаженткоммандсекс Сетвоицекаптион
description: Иаженткоммандсекс Сетвоицекаптион
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710276"
---
# <a name="iagentcommandsexsetvoicecaption"></a>Иаженткоммандсекс:: Сетвоицекаптион

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Задает текст [**воицекаптион**](voicecaption-property.md) , отображаемый для [**командного**](/windows/desktop/lwef/the-command-object) объекта.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*бсзвоицекаптион*
</dt> <dd>

Значение типа BSTR, указывающее текст для свойства [**воицекаптион**](voicecaption-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Если вы определяете объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) и устанавливаете его свойство [**Voice**](voice-property.md) , обычно также устанавливается свойство [**воицекаптион**](voicecaption-property.md) . Этот текст будет отображаться в окне "Voice Commands", если ваше клиентское приложение является активным, а сам символ является видимым. Если это свойство не задано, параметр для свойства [**Caption**](caption-property.md) определяет отображаемый текст. Если ни одно свойство **воицекаптион** или **Caption** не задано, команда не отображается в окне "Voice Commands".

## <a name="see-also"></a>См. также:

[**Иаженткоммандсекс:: Жетвоицекаптион**](iagentcommandsex--getvoicecaption.md)


 

 