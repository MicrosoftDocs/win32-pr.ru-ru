---
title: Групповые функции
description: Глобальная группа содержит учетные записи пользователей из одного домена, сгруппированных с одной группой имен учетных записей.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413484"
---
# <a name="group-functions"></a>Групповые функции

*Глобальная группа* содержит учетные записи пользователей из одного домена, сгруппированных с одной группой имен учетных записей. Глобальная группа может содержать только членов (пользователей) из домена, в котором создана Глобальная группа; Он не может содержать локальные группы. Глобальная группа доступна в собственном домене и в любом доверяющем домене.

Функции группы управления сетью управляют глобальными группами. Групповые функции перечислены ниже.



| Функция                                     | Описание                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**нетграупадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Создает глобальную группу.                                                           |
| [**нетграупаддусер**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Добавляет одного пользователя в существующую глобальную группу.                                        |
| [**нетграупдел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Удаляет глобальную группу независимо от того, содержит ли группа какие-либо члены.                  |
| [**нетграупделусер**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Удаляет одно имя пользователя из глобальной группы.                                        |
| [**нетграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Список всех глобальных групп на сервере.                                              |
| [**нетграупжетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Возвращает сведения о конкретной глобальной группе.                              |
| [**нетграупжетусерс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Список всех членов определенной глобальной группы.                                   |
| [**нетграупсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Задает общие сведения о глобальной группе.                                    |
| [**нетграупсетусерс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Назначает члены новой глобальной группе; заменяет члены существующей группы. |



 

При вызове функции [**нетграупадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) для создания глобальной группы необходимо указать имя группы. Изначально новая группа не имеет членов.

Учетные записи пользователей автоматически принадлежат к особым пользователям домена глобальной группы. Членство в этой группе косвенно контролируется функциями [**нетусерадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**нетусердел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)и [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .

Сведения об учетной записи глобальной группы доступны на следующих уровнях:

-   [**\_Сведения о группе \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [**\_Сведения о группе \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [**\_Сведения о группе \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [**\_Сведения о группе \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [**\_Сведения о группе \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [**\_Сведения о группе \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

Уровни 1002 и 1005 допустимы только для функции [**нетграупсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) .

Сведения о члене глобальной группы доступны на следующем уровне информации:

-   [**\_Сведения о пользователях группы \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

Дополнительные сведения см. в разделе [функции локальной группы](local-group-functions.md)управления сетью.

При программировании для Active Directory можно вызвать определенные методы интерфейса Active Directory (ADSI) для достижения тех же функций, которые можно достичь, вызвав функции группы управления сетью. Дополнительные сведения см. в разделе [**иадсграуп**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 