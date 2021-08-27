---
title: Иаженткоммандс субтитры
description: Иаженткоммандс субтитры
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6eb40b0be58695e79a02ab0ad67ad0d26a47bd13a1637dc1d1f5a4380a7429
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749890"
---
# <a name="iagentcommandsgetcaption"></a>Иаженткоммандс:: oncaption

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иаженткоммандс:: сеткаптион**](iagentcommands--setcaption.md), [**иаженткоммандс::**](iagentcommands--getvisible.md), [**иаженткоммандс:: Voice**](iagentcommands--getvoice.md)


 

 