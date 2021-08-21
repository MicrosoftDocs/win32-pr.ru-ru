---
title: Проблемы привязки для смешанных сред
description: Проблемы привязки для смешанных сред
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, использование, проблемы привязки для смешанных сред
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822795e050d2b69a3f7b60aac6847a150760f35cc62806c36f14d4d6c4694a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017998"
---
# <a name="binding-issues-for-mixed-environments"></a>Проблемы привязки для смешанных сред

для сред, в которых домен, содержащий Active Directory, имеет отношение доверия с доменом Windows NT 4,0, может возникнуть проблема с использованием привязки без сервера для привязки к Active Directory объектам.

в некоторых сетевых средах между контроллерами домена, содержащими серверы Active Directory и Windows NT 4,0, были настроены доверительные отношения с целью разрешения проверки подлинности между доменами. в этих смешанных средах, если пользователь, являющийся членом Windows NT 4,0, домен пытается использовать бессерверную привязку для привязки к объекту Active Directory в доверенном домене, произойдет сбой привязки и будет возвращена ошибка. Это обусловлено тем, что в бессерверной привязке используется функция [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) для привязки к объекту в Active Directory, который зависит от правильной службы DNS.

в этом сценарии Windows NT пользователь должен указать имя определенного домена для привязки. Пример.

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 