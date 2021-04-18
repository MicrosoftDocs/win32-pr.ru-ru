---
title: Иаженткоммандс субтитры
description: Иаженткоммандс субтитры
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691484"
---
# <a name="iagentcommandsgetcaption"></a>Иаженткоммандс:: oncaption

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

Извлекает [**заголовок**](caption-property.md) коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*пбсзкаптион*
</dt> <dd>

Адрес объекта BSTR, который получает значение параметра текста [**заголовка**](caption-property.md) , отображаемое для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткоммандс:: сеткаптион**](iagentcommands--setcaption.md), [**иаженткоммандс::**](iagentcommands--getvisible.md), [**иаженткоммандс:: Voice**](iagentcommands--getvoice.md)


 

 