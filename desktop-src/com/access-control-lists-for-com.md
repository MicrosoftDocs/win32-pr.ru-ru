---
title: Списки управления доступом для COM
description: Списки управления доступом для COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811b6cdbca36ef75bb5ee3f185b0261967d736d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774798"
---
# <a name="access-control-lists-for-com"></a>Списки управления доступом для COM

Windows Server XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP 1) предоставляют усовершенствования системы безопасности для модели DCOM. Одно из этих улучшений — более конкретные права доступа для использования в списках управления доступом (ACL). Права доступа:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Для обеспечения обратной совместимости может существовать список ACL в формате, который используется до выхода Windows XP SP 2 и Windows Server 2003 SP 1. в результате чего выполняется только право доступа COM \_ \_ , или оно может существовать в новом формате, используемом в Windows XP SP 2 и windows Server 2003 SP 1, который использует права com в \_ \_ сочетании с \_ локальными правами com-доступа, а также с \_ \_ правами COM, \_ \_ выполнять \_ Удаленный доступ, \_ права com \_ активировать \_ локальные, а права com — \_ \_ активировать \_ удаленно.

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Улучшения безопасности DCOM в Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1 (SP1)](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Безопасность в COM](security-in-com.md)
</dt> </dl>

 

 




