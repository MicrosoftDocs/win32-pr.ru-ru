---
description: Приложения и скрипты C++, работающие под полной учетной записью администратора, могут изменять дескриптор безопасности пространства имен.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Задание дескрипторов безопасности пространства имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703176"
---
# <a name="setting-namespace-security-descriptors"></a>Задание дескрипторов безопасности пространства имен

Приложения и скрипты C++, работающие под полной учетной записью администратора, могут изменять дескриптор безопасности пространства имен.

## <a name="namespace-security-descriptors"></a>Дескрипторы безопасности пространства имен

Каждое пространство имен WMI имеет [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly), который позволяет каждому пространству имен иметь уникальные параметры безопасности, определяющие, кто имеет доступ к данным и методам пространства имен. Дополнительные сведения о безопасности доступа WMI см. [в разделе доступ к защищаемым ОБЪЕКТАМ WMI](access-to-wmi-securable-objects.md). [Доступ к пространствам имен WMI](access-to-wmi-namespaces.md) описывает параметры безопасности по умолчанию для пространств имен WMI и аудита безопасности в WMI.

Разрешения учетной записи для каждого пространства имен WMI в репозитории WMI (CIM) можно задать следующими способами.

-   При создании пространства имен в MOF-файле. Дополнительные сведения см. [в разделе Настройка безопасности пространства имен при создании пространства имен](setting-namespace-security-when-the-namespace-is-created.md).
-   Вручную, используя элемент управления WMI. Дополнительные сведения см. [в разделе Настройка безопасности пространства имен с помощью элемента управления WMI](setting-namespace-security-with-the-wmi-control.md).
-   Программно, путем вызова методов класса [**\_ \_ системсекурити**](--systemsecurity.md) .

Следующие методы объекта [**\_ \_ системсекурити**](--systemsecurity.md) , связанного с каждым пространством имен, позволяют считывать или изменять безопасность пространства имен.

<dl> <dt>

<span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**жеткаллеракцессригхтс**](--systemsecurity-getcalleraccessrights.md)
</dt> <dd>

Устанавливает параметр *прав* в виде точечного рисунка с каждым битом, соответствующим прав доступа.

</dd> <dt>

<span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**Получает**](--systemsecurity-getsd.md)
</dt> <dd>

Возвращает дескриптор безопасности для пространства имен, к которому подключен пользователь. Этот метод возвращает дескриптор безопасности в двоичном формате массива байтов. При написании скрипта используйте метод [**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .

</dd> <dt>

<span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**Устанавливается**](--systemsecurity-setsd.md)
</dt> <dd>

Задает дескриптор безопасности (SD) для пространства имен, к которому подключен пользователь. Этот метод требует наличия дескриптора безопасности в двоичном формате массива байтов. При написании скрипта используйте метод [**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class---systemsecurity.md) .

</dd> <dt>

<span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class---systemsecurity-.md)
</dt> <dd>

Возвращает дескриптор безопасности, управляющий доступом к пространству имен WMI, связанному с экземпляром [**\_ \_ системсекурити**](--systemsecurity.md). Дескриптор безопасности возвращается в виде экземпляра [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class---systemsecurity.md)
</dt> <dd>

Записывает обновленную версию дескриптора безопасности, которая управляет доступом к принтеру. Дескриптор безопасности представлен экземпляром [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).

</dd> <dt>

<span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)
</dt> <dd>

Получает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.

</dd> <dt>

<span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)
</dt> <dd>

Задает права удаленного доступа для списка отдельных пользователей на компьютерах, использующих устаревшие версии Windows, которые недоступны для управления доступом с помощью дескрипторов безопасности Windows.

</dd> </dl>

При написании скриптов используйте [**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class---systemsecurity-.md) и [**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class---systemsecurity.md). Для изменения дескрипторов безопасности можно использовать методы класса [**\_ Секуритидескрипторхелпер в Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) .

При программировании на C++ можно манипулировать двоичным дескриптором безопасности с помощью [языка определения дескрипторов безопасности (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)и методов преобразования [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) и [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Имейте в виду, что начиная с Windows Vista [Управление учетными записями пользователей](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) влияет на доступ к данным WMI и что может быть настроено с помощью [*элемента управления WMI*](gloss-w.md). Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Защита пространств имен WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Константы безопасности WMI](wmi-security-constants.md)
</dt> <dt>

[Доступ к пространствам имен WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
