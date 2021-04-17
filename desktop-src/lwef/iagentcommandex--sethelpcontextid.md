---
title: Иаженткоммандекс Сеселпконтекстид
description: Иаженткоммандекс Сеселпконтекстид
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691508"
---
# <a name="iagentcommandexsethelpcontextid"></a>Иаженткоммандекс:: Сеселпконтекстид

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

Если вы создали файл справки Windows для своего приложения и установили его в свойстве [**HelpFile**](helpfile-property.md) символа. Microsoft Agent автоматически вызывает справку, когда [**хелпмодеон**](helpmodeon-property.md) имеет значение **true** и пользователь выбирает команду. Если в [**хелпконтекстид**](helpcontextid-property-com.md)имеется контекстный номер, агент вызывает справку и ищет раздел, определяемый текущим контекстным номером. Текущий контекстный номер — это значение **хелпконтекстид** для команды.

> [!Note]  
> Для создания файла справки требуется компилятор справки Microsoft Windows.

 

## <a name="see-also"></a>См. также:

[**Иаженткоммандекс:: жеселпконтекстид**](iagentcommandex--gethelpcontextid.md), [**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**иажентчарактерекс:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 