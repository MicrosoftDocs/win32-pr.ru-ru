---
description: Вспомогательная служба IP предоставляет возможности извлечения данных, которые полезны для сетевого администрирования локального компьютера.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Получение сведений о протоколе Интернета и протоколе управляющих сообщений Интернета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990868"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a>Получение сведений о протоколе Интернета и протоколе управляющих сообщений Интернета

Вспомогательная служба IP предоставляет возможности извлечения данных, которые полезны для сетевого администрирования локального компьютера. Следующие функции извлекают статистику по протоколу IP и ICMP. Эти функции также можно использовать для задания определенных параметров конфигурации для IP.

Функция [**жетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) извлекает текущую статистику IP-адресов для локального компьютера. Примеры кода, включающие **жетипстатистикс** , см. [в разделе Получение сведений с помощью жетипстатистикс](retrieving-information-using-getipstatistics.md).

Функция [**жетикмпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) извлекает текущую статистику ICMP.

Используйте функцию [**сетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) для включения или отключения IP-пересылки. Эта функция также дает возможность задать срок жизни (TTL) по умолчанию для IP-датаграмм. Кроме того, можно задать TTL с помощью функции [**сетипттл**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .

 

 



