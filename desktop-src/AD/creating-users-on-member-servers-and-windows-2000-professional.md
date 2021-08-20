---
title: создание пользователей на рядовых серверах и Windows 2000 Professional
description: в этом разделе описаны действия по созданию пользователя на рядовом сервере или компьютере с Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- создание пользователей на рядовых серверах и Windows 2000 Professional AD
- пользователи AD, создание пользователя на рядовых серверах и Windows 2000 Professional
- Active Directory, использование, пользователи, создание пользователя на рядовых серверах и Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d57bfee4c03aa930ef499b7776fcddb8ce1642ec90d1b376a6b2a934bf93b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020145"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>создание пользователей на рядовых серверах и Windows 2000 Professional

**Создание пользователя**

1.  Выполните привязку к компьютеру, используя следующие правила.
    1.  Используйте учетную запись с достаточными правами для доступа к этому компьютеру.
    2.  Используйте следующий формат строки привязки с помощью поставщика WinNT, имени компьютера и дополнительного параметра, чтобы указать ADSI, что он привязывает к компьютеру: "WinNT:// <computer name> <computer> ". Компьютер " &lt; имя компьютера &gt; " — это имя компьютера, к которому нужно получить доступ. Этот параметр указывает интерфейсу ADSI, что он привязывается к компьютеру, и позволяет средству синтаксического анализа поставщика WinNT пропустить некоторые запросы разрешения неоднозначности, чтобы определить тип объекта, к которому выполняется привязка.
    3.  Привязка к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Укажите "User" в качестве класса с помощью [**иадсконтаинер. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) , чтобы добавить пользователя.
3.  Запишите пользователя в базу данных безопасности компьютера с помощью метода [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 