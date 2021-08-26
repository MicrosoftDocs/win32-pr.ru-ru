---
description: Интерфейс Иинсталлатионжоб определяет следующие свойства.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Свойства Иинсталлатионжоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb1604e69efc1d716b77be7303fc2148e93c0fe6d4fe2bc1ccd299f18ed9d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896984"
---
# <a name="iinstallationjob-properties"></a>Свойства Иинсталлатионжоб

Интерфейс [**иинсталлатионжоб**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) определяет следующие свойства.



| Свойство                                            | Описание                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Возвращает объект состояния, относящегося к вызывающему объекту, который передается в метод [**иупдатеинсталлер. бегининсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) или [**иупдатеинсталлер. бегинунинсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Возвращает значение, указывающее, полностью ли обрабатывается вызов метода [**иупдатеинсталлер. бегининсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) или [**иупдатеинсталлер. бегинунинсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) . |
| [**Обновляем**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Возвращает интерфейс, содержащий доступную только для чтения коллекцию обновлений, указанных в установке или удалении.                                                                                                        |



 

 

 



