---
title: Иажентчарактер ожидания
description: Иажентчарактер ожидания
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fba3f292b9dc7a0651cf3a1a27adcfe0ea808127d8ce00ae62cb1e84cc126a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014224"
---
# <a name="iagentcharacterwait"></a>Иажентчарактер:: wait

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Содержит очередь анимации символа в указанной анимации (запрос) до завершения другого запроса другого символа.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*дврекид*
</dt> <dd>

Идентификатор запроса для ожидания.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*пдврекид*
</dt> <dd>

Адрес переменной, которая получает идентификатор запроса на **Ожидание** .

</dd> </dl>

Этот метод следует использовать только в том случае, если поддерживается несколько (одновременных) символов и требуется последовательное взаимодействие. (Для одного символа каждый запрос анимации воспроизводится последовательно — по завершении предыдущего запроса.) Если у вас есть два символа и требуется, чтобы запрос анимации одного символа дождался до завершения анимации другого символа, присвойте методу **Wait** идентификатор запроса анимации другого символа.

 

 




