---
title: Сообщения в домен Active Directory Services
description: сообщения в домен Active Directory Services работают в Windows 2000 и Windows NT 4,0 с пакетом обновления 6a (sp6a) и более поздней версии с DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory сообщений AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f5a9a5e92048f64cc1b49ea67cae05443eda685d588df0c78bb3f48cf0dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025922"
---
# <a name="messages-in-active-directory-domain-services"></a>Сообщения в домен Active Directory Services

сообщения в домен Active Directory Services работают в Windows 2000 и Windows NT 4,0 с пакетом обновления 6a (sp6a) и более поздней версии с DSClient. они также работают на рабочих станциях Windows 98/95 с ie 4.01 и более поздних версий и DSClient. Однако если в оболочке запускаются страницы свойств из многовариантного выбора, то сообщение [**\_ \_ \_ об ошибке WM адспроп notify**](wm-adsprop-notify-error.md) и соответствующие вспомогательные функции, [**адспропсендеррормессаже**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) и [**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) не работают и не будут отображаться. Если в средстве администрирования запущены страницы свойств, например пользователи и компьютеры AD, то все сообщения будут работать и доступны для отображения на страницах свойств с выборкой.

Службы домен Active Directory Services используют следующие сообщения:

-   [**\_ \_ применение уведомления WM \_ адспроп**](wm-adsprop-notify-apply.md)
-   [**\_ \_ изменение уведомления WM \_ адспроп**](wm-adsprop-notify-change.md)
-   [**\_ \_ ошибка уведомления адспроп \_ WM**](wm-adsprop-notify-error.md)
-   [**\_ \_ выход из уведомления WM адспроп \_**](wm-adsprop-notify-exit.md)
-   [**\_ \_ \_ передний план уведомления WM адспроп**](wm-adsprop-notify-foreground.md)
-   [**WM \_ адспроп \_ Notify \_ пажехвнд**](wm-adsprop-notify-pagehwnd.md)
-   [**WM \_ адспроп \_ Notify \_ пажеинит**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ адспроп \_ уведомлять \_ SETFOCUS**](wm-adsprop-notify-setfocus.md)
-   [**\_ \_ Создание листа WM \_ адспроп**](wm-adsprop-sheet-create.md)
-   [**\_ \_ \_ уведомление о закрытии листа WM DSA \_**](wm-dsa-sheet-close-notify.md)
-   [**\_ \_ \_ уведомление о создании листа WM DSA \_**](wm-dsa-sheet-create-notify.md)

 

 




