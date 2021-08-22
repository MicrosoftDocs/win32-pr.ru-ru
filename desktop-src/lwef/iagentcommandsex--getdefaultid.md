---
title: Иаженткоммандсекс Жетдефаултид
description: Иаженткоммандсекс Жетдефаултид
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4dabfb1c957031b353303775921a352bf40d984ac5de1ee9c933f79a5e02cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105230"
---
# <a name="iagentcommandsexgetdefaultid"></a>Иаженткоммандсекс:: Жетдефаултид

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

Возвращает идентификатор команды по умолчанию в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*пдвид*
</dt> <dd>

Адрес переменной, которая получает идентификатор набора [**команд**](/windows/desktop/lwef/the-command-object) по умолчанию.

</dd> </dl>

Это свойство возвращает текущий объект [**команды**](/windows/desktop/lwef/the-command-object) по умолчанию в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) . Команда по умолчанию выделяется полужирным шрифтом во всплывающем меню символа. Однако при установке команды по умолчанию обработка команд или события двойного щелчка не меняются.

Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.

## <a name="see-also"></a>См. также

[**Иаженткоммандсекс:: Сетдефаултид**](iagentcommandsex--setdefaultid.md)


 

 