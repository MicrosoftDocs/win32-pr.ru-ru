---
title: Удаление пользователей на рядовых серверах и Windows 2000 Professional
description: В этом разделе показано, как удалить пользователя с рядового сервера или компьютера, работающего под Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- Пользователи AD, удаление пользователя на рядовых серверах и Windows 2000 Professional
- Active Directory, использование, пользователи, удаление пользователей на рядовых серверах и Windows 2000 Professional
- Удаление пользователя
- сервер, удаление пользователя
- Удаление пользователей на рядовых серверах и Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069784"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>Удаление пользователей на рядовых серверах и Windows 2000 Professional

В этом разделе показано, как удалить пользователя с рядового сервера или компьютера, работающего под Windows 2000 Professional.

**Удаление пользователя**

1.  Выполните привязку к компьютеру, используя следующие правила.
    1.  Используйте учетную запись с достаточными правами для доступа к этому компьютеру.
    2.  Используйте следующий формат строки привязки с помощью поставщика WinNT, имени компьютера и дополнительного параметра, чтобы указать ADSI, что он привязывает к компьютеру: "WinNT:// <computer name> <computer> ". &lt;Параметр Computer Name &gt; — это имя компьютера, к которому необходимо получить доступ. Этот параметр уведомляет ADSI о том, что он привязывается к компьютеру, и позволяет средству синтаксического анализа поставщика WinNT пропустить некоторые запросы разрешения неоднозначности, чтобы определить тип объекта, к которому выполняется привязка.
    3.  Привязка к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Укажите "User" в качестве класса с помощью [**иадсконтаинер. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) , чтобы удалить пользователя.

    Имейте в виду, что не нужно вызывать функцию [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) для фиксации изменений в контейнере. Вызов [**иадсконтаинер. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) фиксирует удаление пользователя непосредственно в каталоге.

 

 