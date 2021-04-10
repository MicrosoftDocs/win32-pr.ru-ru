---
title: аусентикатионлевел
description: Задает уровень проверки подлинности для приложений, которые не вызывают CoInitializeSecurity, или для приложений, которые вызывают CoInitializeSecurity, и укажите AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- COM-значение реестра Аусентикатионлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332635"
---
# <a name="authenticationlevel"></a>аусентикатионлевел

Задает уровень проверки подлинности для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) , или для приложений, которые вызывают **CoInitializeSecurity** , и укажите AppID.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ DWORD** , эквивалентное \_ \_ \_ константам уровня RPC C AUTHN.



| Значение | Константа                             |
|-------|--------------------------------------|
| 1     | \_уровень RPC \_ C \_ AUTHN \_ None           |
| 2     | \_подключение на уровне RPC C \_ AUTHN \_ \_        |
| 3     | \_ \_ \_ вызов уровня RPC C \_ AUTHN           |
| 4     | \_PKT на уровне RPC C \_ AUTHN \_ \_            |
| 5     | \_ \_ \_ \_ целостность PKT RPC C AUTHN Level \_ |
| 6     | \_Конфиденциальность RPC C \_ AUTHN \_ Level \_ PKT \_   |



 

Значение **аусентикатионлевел** аналогично значению [**легациаусентикатионлевел**](legacyauthenticationlevel.md) . Если указано значение **аусентикатионлевел** , оно используется вместо значения **Легациаусентикатионлевел** для этого AppID.

Если значение **аусентикатионлевел** имеет неправильный тип или выходит за пределы допустимого диапазона, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) завершается ошибкой, что приводит к сбою упаковки интерфейса. Это не позволяет приложению выполнять любые вызовы (между апартаментами, перекрестными потоками, межпроцессными и перекрестными компьютерами).

Значения **аусентикатионлевел** и [**акцесспермиссион**](accesspermission.md) независимы. Если такой объект отсутствует, используется значение по умолчанию. В следующих правилах перечисляются взаимодействия между значением **аусентикатионлевел** и значением **акцесспермиссион** :

-   Если **аусентикатионлевел** имеет значение None, значения [**акцесспермиссион**](accesspermission.md) и [**дефаултакцесспермиссион**](defaultaccesspermission.md) игнорируются (для этого приложения).
-   Если **аусентикатионлевел** отсутствует и [**ЛЕГАЦИАУСЕНТИКАТИОНЛЕВЕЛ**](legacyauthenticationlevel.md) имеет значение None, значения [**акцесспермиссион**](accesspermission.md) и [**дефаултакцесспермиссион**](defaultaccesspermission.md) игнорируются (для этого приложения).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Константы уровня проверки подлинности](com-authentication-level-constants.md)
</dt> <dt>

[**легациаусентикатионлевел**](legacyauthenticationlevel.md)
</dt> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> <dt>

[Безопасность в COM](security-in-com.md)
</dt> </dl>

 

 




