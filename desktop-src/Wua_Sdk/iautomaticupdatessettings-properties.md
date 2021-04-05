---
description: Интерфейс Иаутоматикупдатессеттингс определяет следующие свойства.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Свойства Иаутоматикупдатессеттингс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991179"
---
# <a name="iautomaticupdatessettings-properties"></a>Свойства Иаутоматикупдатессеттингс

Интерфейс [**иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) определяет следующие свойства.



| Свойство                                                                                 | Описание                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**нотификатионлевел**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | Возвращает и задает, как пользователи получают уведомления о событиях автоматического обновления.                              |
| [**Доступно**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | Возвращает логическое значение, указывающее, доступны ли параметры автоматического обновления только для чтения.         |
| [**Обязательно**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | Возвращает логическое значение, указывающее, требует ли групповая политика службы автоматическое обновление. |
| [**счедулединсталлатиондай**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | Возвращает и задает дни недели, в которые автоматическое обновление устанавливает или удаляет обновления.    |
| [**счедулединсталлатионтиме**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | Возвращает и задает время, когда автоматическое обновление устанавливает или удаляет обновления.                |



 

> [!Note]  
> Windows 8, Windows 8.1, Windows Server 2012 и Windows Server 2012 R2 предоставляют только ограниченную поддержку [**счедулединсталлатиондай**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) и [**счедулединсталлатионтиме**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Если компьютер был настроен с помощью групповая политика для использования запланированного дня установки и времени, свойства **счедулединсталлатиондай** и **счедулединсталлатионтиме** возвращают этот запланированный день и время. Если компьютер не был настроен с помощью групповая политика таким образом, свойства **счедулединсталлатиондай** и **счедулединсталлатионтиме** возвращают значения по умолчанию и ненадежные. Если вы попытаетесь изменить запланированный день установки и время для этих операционных систем, то **счедулединсталлатиондай** и **счедулединсталлатионтиме** будут успешно работать, но не будут действовать.

 

 

 



