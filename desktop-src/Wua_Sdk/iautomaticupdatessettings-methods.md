---
description: Интерфейс Иаутоматикупдатессеттингс определяет следующие методы.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Методы Иаутоматикупдатессеттингс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ae30a987dcf9d6573c179e7ef453c10c35a84b915b76a16439ba83a7174fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049472"
---
# <a name="iautomaticupdatessettings-methods"></a>Методы Иаутоматикупдатессеттингс

Интерфейс [**иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) определяет следующие методы.



| Метод                                               | Описание                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Обновить**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Извлекает последние параметры автоматическое обновление. |
| [**Сохранить**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Применяет текущие параметры автоматическое обновление.  |



 

> [!Note]  
> на Windows RT больше нельзя использовать метод [**иаутоматикупдатессеттингс:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) для настройки параметров Центр обновления Windows программным способом. Операция настройки завершается сбоем, если для задания любого значения, отличного от 4 ([**аунлсчедулединсталлатион**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)), используется команда **Save** .

 

 

 



