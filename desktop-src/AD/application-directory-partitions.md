---
title: Разделы каталога приложений
description: В Windows Server 2003 службы домен Active Directory Services поддерживают разделы каталога приложений.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- Разделы каталога приложений AD
- Разделы каталога приложений AD, использование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069819"
---
# <a name="application-directory-partitions"></a>Разделы каталога приложений

В Windows Server 2003 службы домен Active Directory Services поддерживают разделы каталога приложений. Раздел каталога приложений может содержать иерархию объектов любого типа, за исключением субъектов безопасности, и может быть настроена для репликации на любой набор контроллеров домена в лесу. В отличие от раздела домена, раздел каталога приложений не требуется для репликации на все контроллеры домена в домене, и этот раздел может реплицироваться на контроллеры домена в разных доменах леса. Дополнительные сведения о разделах каталога приложений см. в разделе [сведения о разделах каталога приложений](about-application-directory-partitions.md).

Можно создать раздел каталога приложений. изменены и удалены с помощью стандартных операций ADSI, LDAP и [System. DirectoryServices](/dotnet/api/system.directoryservices) . Контекст безопасности, необходимый для создания и изменения раздела каталога приложений, такой же, как и для создания раздела домена.

В следующих разделах описывается работа с разделами каталога приложений.

-   [Репликация разделов каталога приложений](application-directory-partition-replication.md)
-   [Безопасность раздела каталога приложений](application-directory-partition-security.md)
-   [Создание раздела каталога приложений](creating-an-application-directory-partition.md)
-   [Удаление раздела каталога приложений](deleting-an-application-directory-partition.md)
-   [Перечисление разделов каталога приложений в лесу](enumerating-application-directory-partitions-in-a-forest.md)
-   [Поиск сервера узла раздела каталога приложений](locating-an-application-directory-partition-host-server.md)
-   [Добавление или удаление реплики раздела каталога приложений](adding-or-deleting-an-application-directory-partition-replica.md)
-   [Перечисление реплик раздела каталога приложений](enumerating-replicas-of-an-application-directory-partition.md)
-   [Изменение конфигурации раздела каталога приложений](modifying-application-directory-partition-configuration.md)

 

 