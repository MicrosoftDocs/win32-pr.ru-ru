---
description: Интерфейс Иинсталлатионбехавиор определяет следующие свойства.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Свойства Иинсталлатионбехавиор
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991172"
---
# <a name="iinstallationbehavior-properties"></a>Свойства Иинсталлатионбехавиор

Интерфейс [**иинсталлатионбехавиор**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) определяет следующие свойства.



| Свойство                                                                                 | Описание                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**канрекуестусеринпут**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | Возвращает логическое значение САСТ, указывающее, может ли установка или удаление обновления запрашивать ввод данных пользователем.                                                        |
| [**Влияние**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | Возвращает перечисление [**инсталлатионимпакт**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) , которое указывает, как установка или удаление обновления затрагивает компьютер.                 |
| [**RebootBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | Возвращает перечисление [**инсталлатионребутбехавиор**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) , указывающее поведение при перезапуске, которое происходит при установке или удалении обновления. |
| [**рекуиреснетворкконнективити**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | Возвращает логическое значение, указывающее, требуется ли сетевое подключение для установки или удаления обновления.                                                     |



 

 

 



