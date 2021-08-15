---
title: Иаженткоммандекс Жеселпконтекстид
description: Иаженткоммандекс Жеселпконтекстид
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80f259b10adbdd1460f319b6fda4e5097c11136a5bf7ffde00a11d40a99656a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750196"
---
# <a name="iagentcommandexgethelpcontextid"></a>Иаженткоммандекс:: Жеселпконтекстид

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

Получает [**хелпконтекстид**](helpcontextid-property-com.md) для объекта [**команды**](/windows/desktop/lwef/the-command-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*пулид*
</dt> <dd>

Адрес переменной, которая получает контекстный номер раздела справки, связанного с объектом [**Command**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

если вы создали файл справки Windows для своего приложения и установите для свойства [**HelpFile**](helpfile-property.md) символа этот файл, Microsoft Agent автоматически вызывает справку, когда [**хелпмодеон**](helpmodeon-property.md) имеет значение **True** и пользователь выбирает команду. Если в [**хелпконтекстид**](helpcontextid-property-com.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером. Текущий контекстный номер — это значение **хелпконтекстид** для команды.

> [!Note]  
> для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также

[**Иаженткоммандекс:: сеселпконтекстид**](iagentcommandex--sethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 