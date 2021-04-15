---
description: Вспомогательный модуль IP может помочь в управлении IP-адресами, связанными с интерфейсами на локальном компьютере. Используйте функции, описанные в следующих параграфах, для управления IP-адресами.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Управление IP-адресами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682616"
---
# <a name="managing-ip-addresses"></a>Управление IP-адресами

Вспомогательный модуль IP может помочь в управлении IP-адресами, связанными с интерфейсами на локальном компьютере. Используйте функции, описанные в следующих параграфах, для управления IP-адресами.

Функция [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) извлекает таблицу, содержащую сопоставление IP-адресов с интерфейсами. С одним интерфейсом может быть связано более одного IP-адреса.

Используйте функцию [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) для добавления IP-адреса к определенному интерфейсу. Чтобы удалить IP-адреса, которые были ранее добавлены с помощью **аддипаддресс**, используйте функцию [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .

Для функций [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) требуется, чтобы локальный компьютер использовал протокол DHCP. Функция **ипрелеасеаддресс** освобождает IP-адрес, который ранее был ПОЛУЧЕН от DHCP. Функция **ипреневаддресс** ОБНОВЛЯЕТ аренду DHCP по ОПРЕДЕЛЕННОМУ IP-адресу. Аренда DHCP позволяет компьютеру использовать IP-адрес в течение указанного периода времени.

-   Примеры кода, включающие [**жетипаддртабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , см. [в разделе Управление IP-адресами с помощью жетипаддртабле](managing-ip-addresses-using-getipaddrtable.md).

-   Примеры кода, включающие [**аддипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) и [**делетеипаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), см. в разделе [Управление IP-адресами с помощью аддипаддресс и делетеипаддресс](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).

-   Примеры кода, включающие [**ипрелеасеаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) и [**ипреневаддресс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , см. [в разделе Управление арендой DHCP с помощью ипрелеасеаддресс и ипреневаддресс](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 



