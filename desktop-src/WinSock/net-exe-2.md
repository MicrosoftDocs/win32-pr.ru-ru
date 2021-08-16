---
description: Net.exe можно использовать для завершения и запуска протокола IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ab08a69590d6cf53a42096bf12d2e8657c571fd27b637feca4c51c61354225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741081"
---
# <a name="netexe"></a>Net.exe

Net.exe можно использовать для завершения и запуска протокола IPv6. Перезапуск IPv6 повторно инициализирует протокол, как если бы компьютер перезапускался, что может изменить номера интерфейсов. Net.exe имеет много подкоманд. Следующие команды относятся к протоколу IPv6:

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**NET tcpip6**
</dt> <dd>

Останавливает протокол IPv6 и выгружает его из памяти. Эта команда завершается ошибкой, если открыты какие-либо сокеты IPv6.

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**NET start tcpip6**
</dt> <dd>

Запускает протокол IPv6, если он был остановлен. Если в каталоге% SystemRoot% System32 имеется новый файл драйвера Tcpip6.sys \\ , он \\ загружается.

</dd> </dl>

 

 



