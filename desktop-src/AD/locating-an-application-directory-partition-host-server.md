---
title: Поиск сервера узла раздела каталога приложений
description: В этом разделе описывается, как разместить сервер узла раздела каталога приложений.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Поиск сервера узла раздела каталога приложений AD
- Разделы каталога приложений Active Directory, поиск сервера узла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3cef9442d694b80893f67d5530b83aa188df4d172028271117492ed221bd239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186795"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Поиск сервера узла раздела каталога приложений

Служба NetLogon регистрирует следующий список записей SRV для раздела каталога приложений:

-   \_Протокол LDAP. \_ входящий.<partition name>
-   \_Протокол LDAP. \_ TCP. <site name> . \_ черн.<partition name>

Чтобы определить контроллер домена, на котором размещена реплика указанного раздела каталога приложений, вызовите функцию [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) с параметром *имя_домена* , заданным как DNS-имя раздела каталога приложений, и установленный в параметре *flags* флаг **\_ \_ LDAP \_ только DS** . Дополнительные сведения и пример кода, демонстрирующий использование функции **DsGetDcName** , как найти контроллер домена, на котором размещена реплика раздела каталога приложений, см. в разделе [пример кода для поиска сервера узла раздела каталога приложений](example-code-for-locating-an-application-directory-partition-host-server.md).

 

 




