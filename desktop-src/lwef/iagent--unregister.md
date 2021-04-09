---
title: Отмена регистрации Иажент
description: Отмена регистрации Иажент
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890632"
---
# <a name="iagentunregister"></a>Иажент:: Отмена регистрации

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 