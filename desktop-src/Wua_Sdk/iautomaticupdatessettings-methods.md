---
description: Интерфейс Иаутоматикупдатессеттингс определяет следующие методы.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Методы Иаутоматикупдатессеттингс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898514"
---
# <a name="iautomaticupdatessettings-methods"></a>Методы Иаутоматикупдатессеттингс

Интерфейс [**иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) определяет следующие методы.



| Метод                                               | Описание                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Обновить**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Извлекает последние параметры автоматическое обновление. |
| [**Сохранить**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Применяет текущие параметры автоматическое обновление.  |



 

> [!Note]  
> В Windows RT вы больше не можете использовать метод [**иаутоматикупдатессеттингс:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) для настройки параметров центр обновления Windows программным способом. Операция настройки завершается сбоем, если для задания любого значения, отличного от 4 ([**аунлсчедулединсталлатион**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)), используется команда **Save** .

 

 

 



