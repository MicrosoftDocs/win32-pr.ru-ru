---
description: Интерфейс Иинсталлатионжоб определяет следующие свойства.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Свойства Иинсталлатионжоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810222"
---
# <a name="iinstallationjob-properties"></a>Свойства Иинсталлатионжоб

Интерфейс [**иинсталлатионжоб**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) определяет следующие свойства.



| Свойство                                            | Описание                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Возвращает объект состояния, относящегося к вызывающему объекту, который передается в метод [**иупдатеинсталлер. бегининсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) или [**иупдатеинсталлер. бегинунинсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Возвращает значение, указывающее, полностью ли обрабатывается вызов метода [**иупдатеинсталлер. бегининсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) или [**иупдатеинсталлер. бегинунинсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) . |
| [**Обновления**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Возвращает интерфейс, содержащий доступную только для чтения коллекцию обновлений, указанных в установке или удалении.                                                                                                        |



 

 

 



