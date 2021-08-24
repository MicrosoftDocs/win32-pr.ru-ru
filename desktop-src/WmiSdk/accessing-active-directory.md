---
description: Active Directory является службой каталогов для Windows и является основой Windows распределенных сетей.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Доступ к Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a5e60899e07335795d9728045f1e53876b013bb62c85176479fa7953ac45d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131967"
---
# <a name="accessing-active-directory"></a>Доступ к Active Directory

Active Directory является службой каталогов для Windows и является основой Windows распределенных сетей. Active Directory можно использовать для нахождение объектов в доменной сети компьютера, таких как пользователи, политики безопасности, принтеры, распределенные компоненты и другие ресурсы. Имя Active Directory ссылается как на службу каталогов, так и на сам каталог.

> [!Note]  
> Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).

 

Windows делает Active Directory доступным через WMI, создавая набор ссылок на каждый класс и объект, содержащийся в Active Directory. Доступ к поставщику служб каталогов через инструментарий WMI позволяет создавать приложения с поддержкой WMI, которые могут получать доступ к обширным сведениям, содержащимся в Active Directory.

С помощью этих интерфейсов можно:

-   Извлечение классов и экземпляров.
-   Перечисление классов и экземпляров.
-   Создайте новые экземпляры.
-   Изменение существующих экземпляров.
-   Удаление существующих экземпляров.
-   Active Directory запроса.

Следующие разделы помогут вам в использовании Active Directory с WMI:

-   [Использование правильного синтаксиса Active Directory](using-the-proper-active-directory-syntax.md)
-   [Сопоставление Active Directory WMI](mapping-active-directory-to-wmi.md)

 

 



