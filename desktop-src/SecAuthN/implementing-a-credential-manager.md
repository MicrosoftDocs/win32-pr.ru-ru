---
description: Список экспортируемых библиотек DLL, которые должны быть реализованы для создания диспетчера учетных данных.
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: Реализация диспетчера учетных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a1787fcf72d88ad809f904f9f83179ac86631b83a23314f9d24ee31ce3dec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482664"
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

 

 



