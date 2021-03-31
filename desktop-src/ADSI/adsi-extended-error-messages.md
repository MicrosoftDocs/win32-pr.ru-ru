---
title: Расширенные сообщения об ошибках ADSI
description: Этот раздел содержит список разделов, в которых объясняется, как работать с сообщениями об ошибках ADSI, возвращаемыми функцией IADs, Иадсконтаинер, Идиректорйобжект и IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Расширенные сообщения об ошибках ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067341"
---
# <a name="adsi-extended-error-messages"></a>Расширенные сообщения об ошибках ADSI

Помимо значений **HRESULT** , несколько поставщиков систем ADSI (в основном LDAP) возвращают дополнительные данные об ошибке для операций, выполняемых следующими интерфейсами:

-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Частью таких расширенных данных об ошибках является строка, отправленная сервером как часть результата сообщения.

Вызовите [**адсжетластеррор**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) для получения таких расширенных сообщений об ошибках. Первым параметром этой функции, *лперрор*, является значение **DWORD** . Для сервера Active Directory ADSI пытается сопоставить сообщение об ошибке LDAP с соответствующим кодом ошибки Win32 и присваивает *лперрор* значение кода ошибки Win32. Если не удается разрешить сопоставление, ADSI присваивает **ошибке \_ недопустимые \_ данные** *лперрор*, как и для любого другого сервера каталога. Во всех случаях ADSI точно передает строку описания ошибки с сервера клиенту через *лперрорбуф*, второй параметр функции **адсжетластеррор** .

 

 




