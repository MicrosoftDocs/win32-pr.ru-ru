---
title: аусентикатионлевел
description: Задает уровень проверки подлинности для приложений, которые не вызывают CoInitializeSecurity, или для приложений, которые вызывают CoInitializeSecurity, и укажите AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- COM-значение реестра Аусентикатионлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7968382ea97243c1116dd6785be34a0d1c3e6eafc6cb9ee13f16b939029a6611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120534"
---
# <a name="authenticationlevel"></a>аусентикатионлевел

Задает уровень проверки подлинности для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) , или для приложений, которые вызывают **CoInitializeSecurity** , и укажите AppID.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Remarks

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Константы уровня проверки подлинности](com-authentication-level-constants.md)
</dt> <dt>

[**легациаусентикатионлевел**](legacyauthenticationlevel.md)
</dt> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> <dt>

[Безопасность в COM](security-in-com.md)
</dt> </dl>

 

 




