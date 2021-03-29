---
title: Использование Teredo с вспомогательным модулем IP
description: API вспомогательного приложения протокола Интернета (IP-адрес) используется приложением для сбора и предоставления важной информации о конфигурации сети локального компьютера.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792510"
---
# <a name="using-teredo-with-ip-helper"></a>Использование Teredo с вспомогательным модулем IP

API [вспомогательного приложения протокола Интернета](/windows/desktop/IpHlp/about-ip-helper) (IP-адрес) используется приложением для сбора и предоставления важной информации о конфигурации сети локального компьютера. При работе на платформе Windows Vista эта информация включает в себя динамический UDP-порт, назначенный интерфейсу Teredo, и изменения, которые могут возникать в назначенный порт.

Для упрощения использования интерфейса Teredo используются следующие функции API вспомогательного приложения IP:

-   [**жеттередопорт**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**нотифитередопортчанже**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**нотифистаблеуникастипаддресстабле**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 