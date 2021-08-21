---
description: API управления учетными данными
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API управления учетными данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a290cf9d7e5a2d527368c2fd7350fa1bb9549af862c7da7c3845ceae9efc8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008842"
---
# <a name="credential-management-api"></a>API управления учетными данными

Функции управления учетными данными составляют набор функций, которые должен реализовать Диспетчер учетных данных. А именно:

-   [**Нплогоннотифи**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)— функция обработчика событий, которая вызывается многопротокольным маршрутизатором при входе пользователя в систему.
-   [**Нппассвордчанженотифи**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), функция обработчика событий, которая вызывается многопротокольной организацией при изменении пароля учетной записи.

Функции управления учетными данными всегда вызываются в системном контексте (LocalSystem), а не в контексте пользователя.

Дополнительные сведения о создании и регистрации приложения диспетчера учетных данных см. в разделе [Реализация диспетчера учетных данных](implementing-a-credential-manager.md) и [Регистрация поставщиков сетевых услуг и диспетчеров учетных данных](registering-network-providers-and-credential-managers.md).

 

 



