---
title: Позднее связывание, что происходит внутри
description: В этом разделе описывается работа позднего связывания в ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- расширения ADSI, позднее связывание, что происходит внутри
- Привязка к AD, позднее связывание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488276"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Позднее связывание: что происходит внутри?

В следующем списке описан общий процесс выполнения поздней привязки:

-   Что-то связано с объектом каталога ADSI. Например, "LDAP://кН = Жеффсмис, OU = Sales, DC = Fabrikam, DC = COM" привязывается с помощью позднего связывания COM. Это приводит к тому, что ADSI вызывает метод [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в интерфейсе **IDispatch** .
-   ADSI находит объект в классе User и создает объект, поддерживающий соответствующие интерфейсы, такие как [**iAds**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).
-   ADSI выполняет поиск в реестре и находит расширения CLSID для пользователя. Имейте в виду, что ADSI кэширует эти данные.
-   Что-то вызывает метод **миневмесод** . ADSI ищет идентификатор диспетчеризации и идентификаторы диспетчеризации для других расширений ADSI. Затем ADSI находит расширение, которое обслуживает этот вызов, и вызывает интерфейс [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) для этого расширения.
-   Расширение выполняет функцию.
-   Теперь модуль записи клиента вызывает метод **йоурневмесод** , используя интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) для текущего расширения. Реализация расширения **IDispatch** делегирует интерфейсу **IDispatch** для ADSI.
-   Интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) для ADSI снова ищет соответствующее расширение или само себя, а затем вызывает соответствующее расширение с помощью интерфейса [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) для этого расширения.

 

 