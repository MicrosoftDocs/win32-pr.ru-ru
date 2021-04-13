---
title: Иаженткоммандекс Жеселпконтекстид
description: Иаженткоммандекс Жеселпконтекстид
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412939"
---
# <a name="iagentcommandexgethelpcontextid"></a>Иаженткоммандекс:: Жеселпконтекстид

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

Если вы создали файл справки Windows для приложения и устанавливаете для свойства [**HelpFile**](helpfile-property.md) символа этот файл, Microsoft Agent автоматически вызывает справку, когда [**Хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает команду. Если в [**хелпконтекстид**](helpcontextid-property-com.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером. Текущий контекстный номер — это значение **хелпконтекстид** для команды.

> [!Note]  
> Для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также:

[**Иаженткоммандекс:: сеселпконтекстид**](iagentcommandex--sethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 