---
description: Вспомогательный модуль IP-адресов можно использовать для выполнения операций ARP для локального компьютера. Используйте следующие функции для получения и изменения таблицы ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Использование протокола разрешения адресов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ca1ef7e5d657476ff85a8893d71e197a034c70234e44f32317b7b05f58c9b94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290014"
---
# <a name="using-the-address-resolution-protocol"></a>Использование протокола разрешения адресов

Вспомогательный модуль IP-адресов можно использовать для выполнения операций ARP для локального компьютера. Используйте следующие функции для получения и изменения таблицы ARP.

[**Жетипнеттабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) ИЗВЛЕКАЕТ таблицу ARP. Таблица ARP содержит сопоставление IP-адресов с физическими адресами. Физические адреса иногда называются MAC-адресами.

Используйте функции [**креатеипнетентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) и [**делетеипнетентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) для добавления или удаления определенных записей ARP в таблице или из нее. Функция [**флушипнеттабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) удаляет все записи из таблицы.

Чтобы создать или удалить записи прокси-сервера ARP, используйте функции [**креатепроксярпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) и [**делетепроксярпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .

Функция [**сендарп**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) ОТПРАВЛЯЕТ запрос ARP в локальную сеть.

 

 



