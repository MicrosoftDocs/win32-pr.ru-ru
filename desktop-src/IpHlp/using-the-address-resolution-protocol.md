---
description: Вспомогательный модуль IP-адресов можно использовать для выполнения операций ARP для локального компьютера. Используйте следующие функции для получения и изменения таблицы ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Использование протокола разрешения адресов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674313"
---
# <a name="using-the-address-resolution-protocol"></a>Использование протокола разрешения адресов

Вспомогательный модуль IP-адресов можно использовать для выполнения операций ARP для локального компьютера. Используйте следующие функции для получения и изменения таблицы ARP.

[**Жетипнеттабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) ИЗВЛЕКАЕТ таблицу ARP. Таблица ARP содержит сопоставление IP-адресов с физическими адресами. Физические адреса иногда называются MAC-адресами.

Используйте функции [**креатеипнетентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) и [**делетеипнетентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) для добавления или удаления определенных записей ARP в таблице или из нее. Функция [**флушипнеттабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) удаляет все записи из таблицы.

Чтобы создать или удалить записи прокси-сервера ARP, используйте функции [**креатепроксярпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) и [**делетепроксярпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .

Функция [**сендарп**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) ОТПРАВЛЯЕТ запрос ARP в локальную сеть.

 

 



