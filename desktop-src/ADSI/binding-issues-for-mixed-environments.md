---
title: Проблемы привязки для смешанных сред
description: Проблемы привязки для смешанных сред
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, использование, проблемы привязки для смешанных сред
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654347"
---
# <a name="binding-issues-for-mixed-environments"></a>Проблемы привязки для смешанных сред

Для сред, в которых домен, содержащий Active Directory, имеет отношение доверия с доменом Windows NT 4,0, может возникнуть проблема с использованием привязки без сервера для привязки к Active Directory объектам.

В некоторых сетевых средах между контроллерами домена, содержащими Active Directory и серверами Windows NT 4,0, были настроены доверительные отношения с целью разрешения проверки подлинности между доменами. В этих смешанных средах, если пользователь, являющийся членом Windows NT 4,0, пытается привязать бессерверную привязку к объекту Active Directory в доверенном домене, произойдет сбой привязки и будет возвращена ошибка. Это обусловлено тем, что в бессерверной привязке используется функция [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) для привязки к объекту в Active Directory, который зависит от правильной службы DNS.

В этом сценарии пользователь Windows NT должен указать имя определенного домена для привязки. Пример.

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 