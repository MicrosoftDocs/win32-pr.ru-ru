---
description: Список экспортируемых библиотек DLL, которые должны быть реализованы для создания диспетчера учетных данных.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Реализация диспетчера учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912480"
---
# <a name="implementing-a-credential-manager"></a>Реализация диспетчера учетных данных

Чтобы создать диспетчер учетных данных, необходимо создать библиотеку DLL, которая экспортирует следующие функции:

-   [**нплогоннотифи**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**нппассвордчанженотифи**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

Чтобы восстановить уведомления в функциях [**нплогоннотифи**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) и [**нппассвордчанженотифи**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) для входа со смарт-картой, создайте запись реестра с именем **смарткардлогоннотифи** в виде **DWORD** и задайте для нее значение 1:

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

**Windows Server 2003 и Windows XP:** Запись реестра **смарткардлогоннотифи** не требуется.

Кроме того, диспетчеры учетных данных также должны поддерживать функцию [**нпжеткапс**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) для \_ запуска вннк (поддержка других индексов для диспетчеров учетных данных не требуется). Это говорит о том, что будет запущен диспетчер учетных данных. При вызове **нпжеткапс** с параметром *ниндекс* , для которого задано значение вннк \_ Start, многопротокольный маршрутизатор получает время ожидания перед вызовом функций точки входа управления учетными данными поставщика. И если многопротокольный маршрутизатор имеет эти сведения, он может переслать его диспетчеру учетных данных, установив время ожидания.

 

 



