---
description: Протокол PNRP использует функцию Всалукупсервицеенд для следующих действий.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP и Всалукупсервицеенд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663835"
---
# <a name="pnrp-and-wsalookupserviceend"></a>PNRP и Всалукупсервицеенд

Протокол PNRP использует функцию [**всалукупсервицеенд**](winsock-nsp-reference-links.md) для следующих действий:

-   Завершение запроса, инициированного в предыдущем вызове [ **всалукупсервицебегин**](winsock-nsp-reference-links.md)
-   Разблокирование вызова [**всалукупсервиценекст**](winsock-nsp-reference-links.md) для отмены поиска

Вызов [**всалукупсервицеенд**](winsock-nsp-reference-links.md) завершает запрос и очищает контекст. Маркер, полученный из вызова **всалукупсервицебегин** , должен быть передан в качестве параметра **всалукупсервицеенд**.

Дополнительные сведения о протоколе PNRP и функции [**всалукупсервицебегин**](winsock-nsp-reference-links.md) см. в разделе [PNRP и всалукупсервицебегин](pnrp-and-wsalookupservicebegin.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[PNRP и Всалукупсервицебегин](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[Коды ошибок PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**всалукупсервиценекст**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



