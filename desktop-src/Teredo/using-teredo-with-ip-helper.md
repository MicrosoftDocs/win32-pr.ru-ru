---
title: Использование Teredo с вспомогательным модулем IP
description: API вспомогательного приложения протокола Интернета (IP-адрес) используется приложением для сбора и предоставления важной информации о конфигурации сети локального компьютера.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e977dd585f9759a4eef93daca55e0ff95abdc98085393577afabb4ae6e5908ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990804"
---
# <a name="using-teredo-with-ip-helper"></a>Использование Teredo с вспомогательным модулем IP

API [вспомогательного приложения протокола Интернета](/windows/desktop/IpHlp/about-ip-helper) (IP-адрес) используется приложением для сбора и предоставления важной информации о конфигурации сети локального компьютера. при работе на платформе Windows Vista эти сведения включают в себя динамический UDP-порт, назначенный интерфейсу Teredo, и изменения, которые могут происходить с назначенным портом.

Для упрощения использования интерфейса Teredo используются следующие функции API вспомогательного приложения IP:

-   [**жеттередопорт**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**нотифитередопортчанже**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**нотифистаблеуникастипаддресстабле**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 