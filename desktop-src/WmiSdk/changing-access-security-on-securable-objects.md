---
description: начиная с Windows Vista, многие защищаемые объекты имеют методы для получения или установки дескриптора безопасности. С соответствующими разрешениями можно считывать или изменять дескрипторы безопасности защищаемых объектов.
ms.assetid: da660e7e-f32d-4b7d-b979-f7b482a73fa2
ms.tgt_platform: multiple
title: Изменение параметров безопасности доступа для защищаемых объектов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4cdaa948e6f0e695b3e77576b0a0726f0b38f3b649f005b42aa8e205c894db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050992"
---
# <a name="changing-access-security-on-securable-objects"></a>Изменение параметров безопасности доступа для защищаемых объектов

Принтеры, службы, разделы реестра, приложения DCOM и пространства имен WMI являются защищаемыми объектами. Доступ к защищаемым объектам защищается [*дескрипторами безопасности*](/windows/desktop/SecGloss/s-gly), которые указывают пользователей, имеющих доступ. начиная с Windows Vista, многие защищаемые объекты имеют методы для получения или установки дескриптора безопасности. С соответствующими разрешениями можно считывать или изменять дескрипторы безопасности защищаемых объектов. С помощью этих методов можно управлять тем, какие учетные записи пользователей или группы имеют доступ к принтеру, службе, пространству имен WMI или другому объекту. Дополнительные сведения о дескрипторах безопасности и их использовании в WMI см. в разделе [доступ к защищаемым ОБЪЕКТАМ WMI](access-to-wmi-securable-objects.md).

В этом разделе обсуждаются следующие разделы:

-   [Объекты и методы дескрипторов безопасности](#objects-and-security-descriptor-methods)
-   [Преобразование форматов дескрипторов безопасности](#converting-between-security-descriptor-formats)
-   [Проблемы безопасности](#security-issues)
-   [Связанные темы](#related-topics)

## <a name="objects-and-security-descriptor-methods"></a>Объекты и методы дескрипторов безопасности

В следующем списке содержатся методы, которые защищаемые объекты должны использовать для чтения или изменения дескриптора безопасности:

-   Пространства имен WMI

    Поставщик может устанавливать безопасность, позволяя только определенным группам иметь доступ к данным в пространстве имен WMI. Безопасность пространства имен управляется методами класса [**\_ \_ системсекурити**](--systemsecurity.md) . начиная с Windows Vista методы [**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class---systemsecurity-.md) и [**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class---systemsecurity.md) возвращают и записывают объекты [**\_ \_ SecurityDescriptor**](--securitydescriptor.md) . Дополнительные сведения см. в разделе [Задание дескрипторов безопасности пространства имен](setting-namespace-security-descriptors.md).

-   Разделы реестра

    начиная с Windows Vista можно защитить разделы реестра, чтобы они не могли быть изменены неавторизованными пользователями. Класс [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) содержит методы [**жетсекуритидескриптор**](/previous-versions/windows/desktop/regprov/getsecuritydescriptor-method-in-class-stdregprov) и [**сетсекуритидескриптор**](/previous-versions/windows/desktop/regprov/setsecuritydescriptor-method-in-class-stdregprov) . Эти методы возвращают и записывают объекты [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   принтеры;

    начиная с Windows Vista можно защитить доступ к экземплярам класса [**\_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) с помощью методов [**жетсекуритидескриптор**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) и [**сетсекуритидескриптор**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) . Эти методы возвращают и записывают объекты [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Службы

    начиная с Windows Vista можно защитить доступ к экземплярам класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) с помощью методов [**жетсекуритидескриптор**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) и [**сетсекуритидескриптор**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) . Эти методы возвращают и записывают объекты [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

-   Приложения DCOM

    Экземпляры приложений DCOM имеют несколько дескрипторов безопасности. начиная с Windows Vista используйте методы класса [**Win32 \_ дкомаппликатионсеттинг**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting) для получения или изменения различных дескрипторов безопасности. Дескрипторы безопасности возвращаются в виде экземпляров класса [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

    Чтобы получить или изменить разрешения конфигурации, вызовите методы [**жетконфигуратионсекуритидескриптор**](/windows/desktop/CIMWin32Prov/getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) или [**сетконфигуратионсекуритидескриптор**](/windows/desktop/CIMWin32Prov/setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) .

    Чтобы получить или изменить разрешения доступа, вызовите методы [**жетакцесссекуритидескриптор**](/windows/desktop/CIMWin32Prov/getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) или [**сетакцесссекуритидескриптор**](/windows/desktop/CIMWin32Prov/setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) .

    Чтобы получить или изменить разрешения на запуск и активацию, вызовите методы [**жетлаунчсекуритидескриптор**](/windows/desktop/CIMWin32Prov/getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting) или [**сетлаунчсекуритидескриптор**](/windows/desktop/CIMWin32Prov/setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) ,

-   Файлы

    Методы [**жетсекуритидескриптор**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) и [**сетсекуритидескриптор**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) находятся в классе [**Win32 \_ Логикалфилесекуритисеттинг**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) , а не в классе [**\_ файлов CIM**](/windows/desktop/CIMWin32Prov/cim-datafile) .

-   Shares (Общие папки)

    Методы [**жетсекуритидескриптор**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) и [**сетсекуритидескриптор**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) находятся в классе [**Win32 \_ логикалшаресекуритисеттинг**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) , а не в [**общем классе \_ ресурса Win32**](/windows/desktop/CIMWin32Prov/win32-share) .

> [!Note]  
> Если в вызове метода **сетсекуритидескриптор** не указан новый [*список управления доступом для системы безопасности (SACL)*](/windows/desktop/SecGloss/s-gly) , то в списке SACL дескриптора безопасности на целевом защищаемом объекте устанавливается **значение NULL** , чтобы предыдущий параметр SACL не сохранялся.

 

## <a name="converting-between-security-descriptor-formats"></a>Преобразование форматов дескрипторов безопасности

Дескрипторы безопасности — это сложные двоичные байтовые массивы, которые обычно должны создаваться и изменяться в C++. После того как вы использовали один из методов Get для получения дескриптора безопасности, класс [**Win32 \_ секуритидескрипторхелпер**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) предоставляет методы, которые преобразуют дескрипторы безопасности в [язык определения дескрипторов безопасности (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) или в экземпляры [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

Вы можете управлять списками управления доступом (ACL) проще в экземплярах [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) или в SDDL. Дополнительные сведения о структуре и использовании дескрипторов безопасности в WMI см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md).

В C++ или C# используйте функции преобразования для преобразования двоичных дескрипторов безопасности в [язык определения дескрипторов безопасности (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Чтобы изменить значения дескрипторов безопасности в приложениях C++, используйте [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) и [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="security-issues"></a>Проблемы с безопасностью

Рекомендуется, чтобы изменения в дескрипторах безопасности были очень осторожными, чтобы безопасность объекта не была скомпрометирована. Имейте в виду, что порядок записей контроля доступа (ACE) в избирательном списке управления доступом (DACL) может повлиять на безопасность доступа. Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Вспомогательный класс дескриптора безопасности](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Рекомендации по обеспечению безопасности](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> <dt>

[Управление доступом](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Доступ к пространствам имен WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
