---
title: MachineLaunchRestriction
description: Задает политику ограничения на уровне компьютера для запуска и активации компонента.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- COM-значение реестра Мачинелаунчрестриктион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5cd235e2dd81e596448f25adfd72ad0b16c13d2da3860eb56fb95f93ef53cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048062"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

Задает политику ограничения на уровне компьютера для запуска и активации компонента.

> [!Caution]  
> Изменение этого значения повлияет на все серверные приложения COM и может препятствовать их правильной работе. Если существуют приложения COM-сервера с ограничениями, которые менее строгими по сравнению с ограничениями на уровне компьютера, уменьшение ограничений на уровне компьютера может предоставить этим приложениям нежелательный доступ. И наоборот, при увеличении ограничений на уровне компьютера некоторые серверные приложения COM могут быть недоступны при вызове приложений.

 

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Remarks

Это **\_ двоичное значение reg** .

Участники, не имеющие разрешений здесь, не могут получить их, даже если разрешения предоставлены значением реестра [дефаултакцесспермиссион](defaultaccesspermission.md) или функцией [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .

По умолчанию администраторы могут получать разрешения локального и удаленного запуска и активации, а члены группы «все» могут получить разрешения локальной активации и запуска.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка безопасности для приложений COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




