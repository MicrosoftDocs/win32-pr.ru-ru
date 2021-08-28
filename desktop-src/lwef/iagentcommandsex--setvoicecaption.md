---
title: Иаженткоммандсекс Сетвоицекаптион
description: Иаженткоммандсекс Сетвоицекаптион
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85de69b4b594f93adfb0ff554819243c94986420a79c35e8d7a64a3c2eaccb6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716144"
---
# <a name="iagentcommandsexsetvoicecaption"></a>Иаженткоммандсекс:: Сетвоицекаптион

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иаженткоммандсекс:: Жетвоицекаптион**](iagentcommandsex--getvoicecaption.md)


 

 