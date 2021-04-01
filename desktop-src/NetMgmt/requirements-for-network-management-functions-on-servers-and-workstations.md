---
title: Требования к функциям управления сетью на серверах и рабочих станциях
description: При вызове одной из функций управления сетью, перечисленных в этом разделе на сервере или рабочей станции, разные требования к доступу применяются к информационным запросам и обновлениям информации.
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890992"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a>Требования к функциям управления сетью на серверах и рабочих станциях

При вызове одной из функций управления сетью, перечисленных в этом разделе на сервере или рабочей станции, разные требования к доступу применяются к информационным запросам и обновлениям информации.

## <a name="queries"></a>Запросы

При вызове одной из следующих функций для выполнения запроса на сервере или рабочей станции по умолчанию все прошедшие проверку пользователи могут считывать и перечислять данные.

-   [**Нетграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**нетграупжетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**нетграупжетусерс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**Нетлокалграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**нетлокалграупжетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**нетлокалграупжетмемберс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**неткуеридисплайинформатион**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**Нетсессионжетинфо**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (только уровни 1 и 2)
-   [**Нетшаринум**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (только уровни 2 и 502)
-   [**Нетусеренум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**нетусержетграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**нетусержетлокалграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**нетусермодалсжет**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**Нетвкстажетинфо**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **нетвкстаусеренум**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

Ниже приведены дополнительные сведения об анонимном доступе при чтении и перечислении информации.

**Windows Server 2003 и Windows XP:** Анонимный доступ к информации возможен, если параметр политики Еверйонеинклудесанонимаус разрешает анонимный доступ.

**Windows 2000:** Анонимный доступ к защищаемым объектам возможен, если параметр политики RestrictAnonymous разрешает анонимный доступ. Можно ограничить анонимный доступ, задав для следующего раздела реестра значение 1.

**HKey \_ Локальный \_ компьютер \\ система \\ CurrentControlSet \\ Управление \\ LSA** \\ **RestrictAnonymous** = 1

Дополнительные сведения см. в следующей статье базы знаний Майкрософт:

Идентификатор статьи: [Q246261](https://support.microsoft.com/kb/246261)

TITLE: использование значения реестра RestrictAnonymous.

## <a name="updates"></a>Обновления

По умолчанию данные могут записывать только администраторы и опытные пользователи.

Дополнительные сведения об управлении доступом к защищаемым объектам см. в разделе [Управление доступом](/windows/desktop/SecAuthZ/access-control), [права](/windows/desktop/SecAuthZ/privileges)доступа и [защищаемые объекты](/windows/desktop/SecAuthZ/securable-objects). Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).

 

 