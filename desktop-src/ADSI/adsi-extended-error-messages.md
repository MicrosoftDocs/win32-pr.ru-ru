---
title: Расширенные сообщения об ошибках ADSI
description: Этот раздел содержит список разделов, в которых объясняется, как работать с сообщениями об ошибках ADSI, возвращаемыми функцией IADs, Иадсконтаинер, Идиректорйобжект и IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Расширенные сообщения об ошибках ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2bf4c7faef20feeb868fdcbb0e36d7f1ad5d0b9c68cc8879d5019e81e186a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180878"
---
# <a name="adsi-extended-error-messages"></a>Расширенные сообщения об ошибках ADSI

Помимо значений **HRESULT** , несколько поставщиков систем ADSI (в основном LDAP) возвращают дополнительные данные об ошибке для операций, выполняемых следующими интерфейсами:

-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Частью таких расширенных данных об ошибках является строка, отправленная сервером как часть результата сообщения.

Вызовите [**адсжетластеррор**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) для получения таких расширенных сообщений об ошибках. Первым параметром этой функции, *лперрор*, является значение **DWORD** . Для сервера Active Directory ADSI пытается сопоставить сообщение об ошибке LDAP с соответствующим кодом ошибки Win32 и присваивает *лперрор* значение кода ошибки Win32. Если не удается разрешить сопоставление, ADSI присваивает **ошибке \_ недопустимые \_ данные** *лперрор*, как и для любого другого сервера каталога. Во всех случаях ADSI точно передает строку описания ошибки с сервера клиенту через *лперрорбуф*, второй параметр функции **адсжетластеррор** .

 

 




