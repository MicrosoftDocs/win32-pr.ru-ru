---
description: Интерфейс IUpdateSession3 определяет следующие методы.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Методы IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143690"
---
# <a name="iupdatesession3-methods"></a>Методы IUpdateSession3

Интерфейс [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) определяет следующие методы.



| Метод                                                                           | Описание                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**креатеупдатесервицеманажер**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | Возвращает указатель на интерфейс [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) для сеанса.                                                                                                                                                                                                                |
| [**куерихистори**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | Возвращает указатель на интерфейс [**иупдатехисторентриколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) . Интерфейс содержит совпадающие записи событий на компьютере. Это приводит к тому, что метод [**куерихистори**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) синхронно запрашивает на компьютере журнал событий обновления. |



 

Сведения о членах, наследуемых этим интерфейсом, см. в следующих интерфейсах:

-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**иупдатесессион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



