---
title: Списки управления доступом для COM
description: Списки управления доступом для COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50e1641691b1a2812e861a95c5bc0f7eac8f0f8af67d41b18287c07253b8d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551358"
---
# <a name="access-control-lists-for-com"></a>Списки управления доступом для COM

Windows в server XP с пакетом обновления 2 (sp2) и Windows server 2003 с пакетом обновления 1 (sp 1) представлены улучшения безопасности для модели dcom. Одно из этих улучшений — более конкретные права доступа для использования в списках управления доступом (ACL). Права доступа:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

для обеспечения обратной совместимости может существовать список ACL в формате, который использовался до Windows XP sp 2 и Windows Server 2003 sp 1, который использует только права доступа com справа \_ \_ , или он может существовать в новом формате, используемом в Windows XP SP 2 и Windows Server 2003 sp 1, который использует права com, выполняются \_ вместе с сочетанием прав com-доступа \_ \_ \_ \_ local, \_ права com \_ execute \_ remote, com \_ rights \_ активировать \_ локальные, а права com — \_ \_ активировать \_ удаленно.

> [!Note]  
> \_ \_ Всегда должна присутствовать возможность выполнения прав com; отсутствие этого права создает недопустимый дескриптор безопасности.

 

Не следует смешивать старый формат и новый формат в одном списке ACL; либо все записи контроля доступа (ACE) должны предоставлять только право на \_ \_ выполнение прав доступа COM, либо все они должны ПРЕДОСТАВЛЯТЬ \_ права com \_ в сочетании с правами com, выполнять удаленное выполнение, права com на удаленный доступ, \_ \_ \_ \_ \_ \_ \_ \_ \_ а также \_ активировать права com \_ \_ .

Ниже приведен пример неверно отформатированного списка ACL:

``` syntax
Revision 1
Sbz1 0
Control 0x8004
    SE_DACL_PRESENT
    SE_SELF_RELATIVE
Owner: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
Group: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
DACL:
    AclRevision 2
    Sbz1 0
    AclSize 128
    AceCount 4
    Sbz2 0
    Ace[0]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 36
        AccessMask 0x1
        S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
    Ace[1]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0xb
        S-1-5-18 (Well Known Group: NT AUTHORITY\SYSTEM)
    Ace[2]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0x9
        S-1-5-11 (Well Known Group: NT AUTHORITY\Authenticated Users)
SACL:
    (null)
```

Обратите внимание, что первая запись управления доступом (ACE) \_ предоставляет \_ только выполнение прав com (0x1), а вторая запись ACE предоставляет права com на выполнение, \_ локальные права com и COM- \_ \_ \_ \_ \_ права активировать локальные \_ \_ (0XB), а третья — право на \_ выполнение прав com \_ и \_ \_ активировать \_ локальную службу (0x9).

Чтобы исправить это, необходимо изменить первую запись ACE, чтобы предоставить \_ права com \_ в сочетании с одним из четырех прав доступа, или же второй и третий элементы ACE следует изменить, чтобы предоставить только \_ выполнение прав com \_ .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[улучшения безопасности DCOM в Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1 (sp1)](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Безопасность в COM](security-in-com.md)
</dt> </dl>

 

 




