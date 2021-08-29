---
description: Протокол PNRP использует функцию Всалукупсервицеенд для следующих действий.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP и Всалукупсервицеенд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9d91dea87b5a8c41cb5f689d89464bf7fd7e0179b1cad71943c14d107842b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553384"
---
# <a name="pnrp-and-wsalookupserviceend"></a>PNRP и Всалукупсервицеенд

Протокол PNRP использует функцию [**всалукупсервицеенд**](winsock-nsp-reference-links.md) для следующих действий:

-   Завершение запроса, инициированного в предыдущем вызове [ **всалукупсервицебегин**](winsock-nsp-reference-links.md)
-   Разблокирование вызова [**всалукупсервиценекст**](winsock-nsp-reference-links.md) для отмены поиска

Вызов [**всалукупсервицеенд**](winsock-nsp-reference-links.md) завершает запрос и очищает контекст. Маркер, полученный из вызова **всалукупсервицебегин** , должен быть передан в качестве параметра **всалукупсервицеенд**.

Дополнительные сведения о протоколе PNRP и функции [**всалукупсервицебегин**](winsock-nsp-reference-links.md) см. в разделе [PNRP и всалукупсервицебегин](pnrp-and-wsalookupservicebegin.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[PNRP и Всалукупсервицебегин](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[Коды ошибок PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**всалукупсервиценекст**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



