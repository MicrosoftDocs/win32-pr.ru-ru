---
title: Иаженткоммандекс Сеселпконтекстид
description: Иаженткоммандекс Сеселпконтекстид
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b876276d42ff07081b60194e90beff3ad9ef19fec383c50d70a551e1c9a5e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750198"
---
# <a name="iagentcommandexsethelpcontextid"></a>Иаженткоммандекс:: Сеселпконтекстид

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

Задает [**хелпконтекстид**](helpcontextid-property-com.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*улид*
</dt> <dd>

Контекстный номер раздела справки, связанного с объектом [**Command**](/windows/desktop/lwef/the-command-object) ; используется для предоставления контекстной справки для команды.

</dd> </dl>

если вы создали файл справки Windows для своего приложения и установили его в свойстве [**HelpFile**](helpfile-property.md) символа. Microsoft Agent автоматически вызывает справку, когда [**хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает команду. Если в [**хелпконтекстид**](helpcontextid-property-com.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером. Текущий контекстный номер — это значение **хелпконтекстид** для команды.

> [!Note]  
> для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также

[**Иаженткоммандекс:: жеселпконтекстид**](iagentcommandex--gethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 