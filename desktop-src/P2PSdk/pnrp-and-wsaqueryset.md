---
description: PNRP использует структуру ВСАКУЕРИСЕТ в сочетании с различными функциями для упрощения разрешения имен и перечисления имен и облаков.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP и ВСАКУЕРИСЕТ (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbc635b0c1ca19cfaeeeb7f8b013aefad1e49e2141dd9715a36c0238e7be6f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061361"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP и ВСАКУЕРИСЕТ

PNRP использует структуру [**всакуерисет**](winsock-nsp-reference-links.md) в сочетании с различными функциями для упрощения разрешения имен и перечисления имен и облаков.

полные определения функций [**всакуерисет**](winsock-nsp-reference-links.md) или сокетов Windows см. в соответствующих определениях в документации по API Windows sockets 2 в пакете Platform SDK.

## <a name="wsaqueryset-and-wsasetservice"></a>ВСАКУЕРИСЕТ и Всасетсервице

Функция [**всасетсервице**](winsock-nsp-reference-links.md) использует структуру **всакуерисет** для регистрации или удаления одноранговых имен. На странице [PNRP и всасетсервице](pnrp-and-wsasetservice.md) показано, как использовать структуру **всакуерисет** с этой функцией.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>ВСАКУЕРИСЕТ и Всалукупсервицебегин

Структура [**всакуерисет**](winsock-nsp-reference-links.md) широко используется с функциями **всалукупсервицебегин**, **всалукупсервиценекст** и **всалукупсервицеенд** . Сведения о том, как эти функции используют структуру **всакуерисет** , подробно описаны на следующих справочных страницах:

-   [PNRP и Всалукупсервицебегин](pnrp-and-wsalookupservicebegin.md)
-   [PNRP и Всалукупсервиценекст](pnrp-and-wsalookupservicenext.md)
-   [PNRP и Всалукупсервицеенд](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                             |
| Версия<br/>                  | Windows xp с пакетом обновления 1 (SP1) и расширенным сетевым пакетом для Windows XP<br/>  |
| Заголовок<br/>                   | <dl> <dt>P2P. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[PNRP и BLOB-объект](pnrp-and-blob.md)
</dt> <dt>

[PNRP и Всасетсервице](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




