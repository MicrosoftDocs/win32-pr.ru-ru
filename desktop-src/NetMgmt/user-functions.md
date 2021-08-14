---
title: Пользовательские функции
description: Функции пользователя управления сетью управляют учетной записью пользователя в базе данных безопасности, которая является базой данных диспетчера учетных записей безопасности (SAM), или, в случае контроллеров домена, Active Directory. Пользовательские функции перечислены ниже.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c8d7b59ff121c0225f166888b42ef1a731336ed80799cd0593ba38b4fb04ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796820"
---
# <a name="user-functions"></a>Пользовательские функции

Функции пользователя управления сетью управляют учетной записью пользователя в базе данных безопасности, которая является базой данных диспетчера учетных записей безопасности (SAM), или, в случае контроллеров домена, Active Directory. Пользовательские функции перечислены ниже.



| Функция                                               | Описание                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**нетусерадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Добавляет учетную запись пользователя и назначает пароль и уровень привилегий.     |
| [**нетусерчанжепассворд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Изменяет пароль пользователя для указанного сетевого сервера или домена. |
| [**нетусердел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Удаляет учетную запись пользователя с сервера.                             |
| [**нетусеренум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Выводит список всех учетных записей пользователей на сервере.                                |
| [**нетусержетграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Возвращает список имен глобальных групп, к которым принадлежит пользователь.       |
| [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Возвращает сведения об определенной учетной записи пользователя на сервере.    |
| [**нетусержетлокалграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Возвращает список имен локальных групп, к которым принадлежит пользователь.        |
| [**нетусерсетграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Задает членство в глобальных группах для указанной учетной записи пользователя.         |
| [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Задает пароль и другие элементы учетной записи пользователя.             |



 

Каждый пользователь или приложение, обращающееся к сетевым ресурсам, должны иметь учетную запись в базе данных безопасности. Службы каталогов используют эту учетную запись для проверки наличия у пользователя или приложения разрешения на подключение к ресурсу. когда пользователь или приложение запрашивает доступ к ресурсу, система безопасности Windows проверяет наличие соответствующей учетной записи пользователя или группы, чтобы предоставить доступ.

После удаления учетной записи пользователя с помощью вызова функции [**нетусердел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) пользователь больше не сможет получить доступ к серверу, за исключением учетной записи гостя.

Так как пароль пользователя является конфиденциальным, он не возвращается функцией [**нетусеренум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) или функцией [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) . Пароль изначально назначается при вызове [**нетусерадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd).

Сведения об учетной записи пользователя доступны на следующих уровнях:

-   [**\_Сведения о пользователе \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**\_Сведения о пользователе \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**\_Сведения о пользователе \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**\_Сведения о пользователе \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**\_Сведения о пользователе \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**\_Сведения о пользователе \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**\_Сведения о пользователе \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**\_Сведения о пользователе \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**\_Сведения о пользователе \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**\_Сведения о пользователе \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**\_Сведения о пользователе \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

Кроме того, при вызове функции [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) допустимы следующие уровни информации:

-   [**\_Сведения о пользователе \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**\_Сведения о пользователе \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**\_Сведения о пользователе \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**\_Сведения о пользователе \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**\_Сведения о пользователе \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**\_Сведения о пользователе \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**\_Сведения о пользователе \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**\_Сведения о пользователе \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**\_Сведения о пользователе \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**\_Сведения о пользователе \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**\_Сведения о пользователе \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**\_Сведения о пользователе \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**\_Сведения о пользователе \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**\_Сведения о пользователе \_ 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**\_Сведения о пользователе \_ 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**\_Сведения о пользователе \_ 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

Следующие функции позволяют приложениям проверять соответствие паролей.



| Функция                                                               | Описание                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**нетвалидатепассвордполицифри**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Освобождает память, выделенную функцией [**нетвалидатепассвордполици**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) . |
| [**нетвалидатепассвордполици**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Проверяет, что пароли соответствуют сложности, старению, минимальной длине и повторному использованию журнала.            |



 

При программировании для Active Directory можно вызвать определенные методы интерфейса Active Directory (ADSI) для достижения тех же функций, которые можно достичь, вызвав функции пользователя управления сетью. Дополнительные сведения см. в разделе [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) и [**иадскомпутер**](/windows/desktop/api/iads/nn-iads-iadscomputer).

 

 