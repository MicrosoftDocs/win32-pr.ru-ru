---
description: Доступом к пространствам имен WMI и их данным управляют дескрипторы безопасности.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Защита пространств имен WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3cdf2b6e5c5cf035fed70e3e0dd949a812505f1f1ded8f1599043cdd75ba4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992374"
---
# <a name="securing-wmi-namespaces"></a>Защита пространств имен WMI

Доступом к пространствам имен WMI и их данным управляют [*дескрипторы безопасности*](gloss-s.md). Вы можете защитить данные в [*пространствах имен*](gloss-n.md) , настроив дескриптор безопасности пространства имен, чтобы управлять доступом к данным и методам. Дополнительные сведения см. [в разделе доступ к защищаемым ОБЪЕКТАМ WMI](access-to-wmi-securable-objects.md).


В следующих разделах описывается безопасность пространства имен WMI и управление доступом к пространствам имен.

<dl> <dt>

<span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Доступ к пространствам имен WMI](access-to-wmi-namespaces.md)
</dt> <dd>

безопасность пространства имен WMI зависит от стандартных [*идентификаторов безопасности*](/windows/desktop/SecGloss/s-gly) Windows (sid) и списков управления доступом. Администраторы и пользователи имеют разные разрешения по умолчанию.

</dd> <dt>

<span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Задание дескрипторов безопасности пространства имен](setting-namespace-security-descriptors.md)
</dt> <dd>

После существования пространства имен в репозитории WMI можно изменить безопасность пространства имен с помощью элемента управления WMI или путем вызова методов [**\_ \_ системсекурити**](--systemsecurity.md).

</dd> <dt>

<span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Требуется зашифрованное соединение с пространством имен](requiring-an-encrypted-connection-to-a-namespace.md)
</dt> <dd>

Квалификатор **рекуиресенкриптион** в пространстве имен требует, чтобы клиентское приложение WMI или сценарий использовали уровень проверки подлинности, который шифрует удаленные вызовы процедур. Как входящие запросы данных, так и асинхронные обратные вызовы должны быть зашифрованы.

</dd> <dt>

<span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Установка наследования безопасности пространства имен](establishing-inheritance-of-namespace-security.md)
</dt> <dd>

Можно контролировать, наследует ли Дочернее пространство имен дескриптор безопасности родительского пространства имен.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> <dt>

[Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Создание пространства имен с помощью API инструментария WMI](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[Объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
