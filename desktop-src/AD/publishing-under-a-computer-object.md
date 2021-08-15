---
title: Публикация в объекте компьютера
description: Как правило, службы на основе узла создают запрашивая в объекте Computer для главного компьютера. Службы на основе узлов тесно связаны с одним ведущим компьютером.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac659ab2bf482ee6d6c57dd1481e487d6e2af95dfd85a092f48f4928499b102
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025362"
---
# <a name="publishing-under-a-computer-object"></a>Публикация в объекте компьютера

Как правило, службы на основе узла создают запрашивая в объекте Computer для главного компьютера. Службы на основе узлов тесно связаны с одним ведущим компьютером.

**Создание запрашивая в объекте Computer**

1.  Вызовите функцию [**жеткомпутеробжектнаме**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) , чтобы получить различающееся имя (DN) в каталоге объекта компьютера для локального компьютера.
2.  Используйте это различающееся имя для привязки к объекту Computer и создания точки подключения службы.

Дополнительные сведения и пример кода см. в разделе [как клиенты находят и используют точку подключения службы](how-clients-find-and-use-a-service-connection-point.md).

Имейте в виду, что только компьютеры, являющиеся членами домена, имеют допустимые объекты компьютеров в каталоге.

Чтобы получить имя DNS или NetBIOS локального компьютера, вызовите функцию [**предполагался сбой getcomputernameex**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .

 

 