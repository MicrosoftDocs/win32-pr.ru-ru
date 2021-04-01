---
title: Требования к функциям управления сетью на контроллерах домен Active Directory
description: При вызове одной из функций управления сетью, перечисленных в этом разделе, на контроллере домена, работающем Active Directory, доступ к защищаемому объекту разрешен или запрещен на основе списка управления доступом (ACL) для объекта.
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6b646290ef6352a529a37243a6ea30c8b0d39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890757"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Требования к функциям управления сетью на контроллерах домен Active Directory

При вызове одной из функций управления сетью, перечисленных в этом разделе, на контроллере домена, работающем Active Directory, доступ к [защищаемому объекту](/windows/desktop/SecAuthZ/securable-objects) разрешен или запрещен на основе [списка управления доступом](/windows/desktop/SecAuthZ/access-control-lists) (ACL) для объекта. (Списки управления доступом указываются в каталоге.)

Различные требования к доступу относятся к информационным запросам и обновлениям информации.

## <a name="queries"></a>Запросы

Для запросов ACL по умолчанию разрешает всем прошедшим проверку подлинности пользователям и членам группы "[пред-Windows 2000 доступ](/windows/desktop/SecAuthZ/allowing-anonymous-access)" чтение и перечисление информации. Затрагиваются перечисленные ниже функции.

-   [**Нетграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**нетграупжетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**нетграупжетусерс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**Нетлокалграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**нетлокалграупжетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**нетлокалграупжетмемберс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**неткуеридисплайинформатион**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**Нетсессионжетинфо**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (только уровни 1 и 2)
-   [**Нетшаринум**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (только уровни 2 и 502)
-   [**Нетусеренум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**нетусержетграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**нетусержетлокалграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**нетусермодалсжет**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**Нетвкстажетинфо**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **нетвкстаусеренум**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

Анонимный доступ к сведениям о группе требует явного добавления пользователя в группу "пред-Windows 2000 доступ". Это связано с тем, что анонимные маркеры не включают идентификатор безопасности группы «все».

**Windows 2000:** По умолчанию группа "пред-Windows 2000 доступ к данным" включает в себя всех членов группы. Это обеспечивает анонимный доступ (анонимный вход) к информации, если система разрешает анонимный доступ. Администраторы могут в любое время удалить всех пользователей из группы "пред-Windows 2000 доступ". Удаление всех пользователей из группы запрещает доступ к данным только прошедшим проверку пользователям. Дополнительные сведения об анонимном доступе см. в разделе [идентификаторы безопасности](/windows/desktop/SecAuthZ/security-identifiers) и [хорошо известные](/windows/desktop/SecAuthZ/well-known-sids)идентификаторы SID.

Вы можете переопределить значение по умолчанию системы, задав в реестре следующий раздел в значении 1:

**HKey \_ Локальный \_ компьютер \\ система \\ CurrentControlSet \\ Управление \\ локальным компьютером LSA** \\ **еверйонеинклудесанонимаус** = 1

Дополнительные сведения о анонимном доступе к сведениям о группе при вызове этих двух функций см. в разделе [**нетвкстажетинфо**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) и [**нетвкстаусеренум**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum) .

## <a name="updates"></a>Обновления

Для обновлений ACL по умолчанию допускает запись сведений только администраторам домена и операторам учетных записей. Единственное исключение заключается в том, что пользователи могут изменить свой пароль и задать \* \_ \_ поле комментария usr Усри. Еще одно исключение заключается в том, что операторы учета не могут изменять учетные записи администрирования. Затрагиваются перечисленные ниже функции.

-   [**Нетграупадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**нетграупаддусер**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**нетграупдел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**нетграупделусер**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**нетграупсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**нетграупсетусерс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**Нетлокалграупадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd), [**нетлокалграупаддмемберс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers), [**нетлокалграупдел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel), [**нетлокалграупделмемберс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers), [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo), [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**нетмессажебуфферсенд**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   [**Нетусерадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**нетусерчанжепассворд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword), [**нетусердел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), [**нетусермодалссет**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**нетусерсетграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups), [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

Как правило, вызывающие объекты должны иметь доступ на запись ко всему объекту для достижения вызовов [**нетусермодалссет**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo), [**нетграупсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) и [**нетлокалграупсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) . Для более точного контроля доступа рекомендуется использовать интерфейсы ADSI. Дополнительные сведения о ADSI см. в разделе [интерфейсы служб Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).

Дополнительные сведения об управлении доступом к защищаемым объектам см. в разделе [Управление доступом](/windows/desktop/SecAuthZ/access-control), [права](/windows/desktop/SecAuthZ/privileges)доступа и [защищаемые объекты](/windows/desktop/SecAuthZ/securable-objects). Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).

 

 