---
description: Интерфейс IUpdateSession3 определяет следующие методы.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Методы IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 845af7bc4858aa713a3c044562c91325d337e49da0f413a3b2536c0129a85bc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896744"
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

 

 



