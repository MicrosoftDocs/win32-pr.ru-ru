---
title: Отмена регистрации Иажент
description: Отмена регистрации Иажент
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101d0473e8563e8b0899e2f5d0bd2a440c31d17b4a0c142b43f47855ddf166b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976484"
---
# <a name="iagentunregister"></a>Иажент:: Отмена регистрации

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Выгружает символьные данные для указанного символа из коллекции [**символов**](/windows/desktop/lwef/the-characters-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*двсинкид*
</dt> <dd>

ИДЕНТИФИКАТОР приемника уведомлений.

</dd> </dl>

Используйте этот метод, если вам больше не нужны службы агента Майкрософт, например при завершении работы приложения.

## <a name="see-also"></a>См. также:

[**Иажент:: Register**](iagent--register.md)


 

 