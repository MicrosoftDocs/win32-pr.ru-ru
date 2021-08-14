---
title: Иажентчарактерекс Жеселпконтекстид
description: Иажентчарактерекс Жеселпконтекстид
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3a64de0f4373bcaa890156ec88595d066aae9ae84b5b242fe62ffae10479d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750799"
---
# <a name="iagentcharacterexgethelpcontextid"></a>Иажентчарактерекс:: Жеселпконтекстид

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

Возвращает [**хелпконтекстид**](helpcontextid-property.md) для символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*пулхелпид*
</dt> <dd>

Адрес переменной, которая получает контекстный номер раздела справки для символа.

</dd> </dl>

если для приложения был создан файл справки Windows и задано свойство [**HelpFile**](helpfile-property.md) символа, то Microsoft Agent автоматически вызывает справку, когда [**хелпмодеон**](helpmodeon-property.md) имеет значение **True** и пользователь выбирает символ. Если в [**хелпконтекстид**](helpcontextid-property.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером. Текущий контекстный номер — это значение **хелпконтекстид** для символа.

**Иажентчарактерекс:: жеселпконтекстид** возвращает [**хелпконтекстид**](helpcontextid-property.md) , заданное для символа. Он не возвращает **хелпконтекстид** , заданный другими клиентами.

> [!Note]  
> для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также

[**Иажентчарактерекс:: сеселпконтекстид**](iagentcharacterex--sethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




