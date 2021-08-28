---
title: RootDSE (ADSI)
description: Каждый сервер каталога имеет уникальную запись RootDSE. Он предоставляет данные о сервере, например его возможности, поддерживаемую версию LDAP и используемые контексты именования.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59176315339e7458f332e2226f880b79afa10c5afc2c5089295866f6bf93939c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770634"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Каждый сервер каталога имеет уникальную запись **RootDSE**. Он предоставляет данные о сервере, например его возможности, поддерживаемую версию LDAP и используемые контексты именования.

например, для создания скрипта или приложения, которое может выполняться в любой среде домена Windows. При подключении к Active Directory можно указать различающееся имя, имя сервера или доменное имя. Если эти сведения отсутствуют, можно использовать объект **RootDSE** для установления соединения. В следующем примере кода показано изменение описания домена в любом домене.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



Получив атрибут **дефаултнамингконтекст** из **RootDSE**, можно выполнить привязку к текущему домену, например, Fabrikam **дефаултнамингконтекст** — DC = Fabrikam, DC = com.

Чтобы перечислить свойства **RootDSE**, используйте интерфейс [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) . [**Идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) нельзя использовать для этой задачи.

Дополнительные сведения см. в статье [бессерверная привязка и RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).

 

 