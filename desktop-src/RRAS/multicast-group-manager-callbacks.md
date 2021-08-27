---
title: Обратные вызовы диспетчера групп многоадресной рассылки
description: Диспетчер групп многоадресной рассылки использует следующие обратные вызовы для уведомления клиентов (обычно протоколы маршрутизации) о событиях и изменениях состояния.
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037281a2cb636b337c5133c2c3a261e2c435a136a30d0ccfdcf0407a9b62509b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036654"
---
# <a name="multicast-group-manager-callbacks"></a>Обратные вызовы диспетчера групп многоадресной рассылки

Диспетчер групп многоадресной рассылки использует следующие обратные вызовы для уведомления клиентов (обычно это протоколы маршрутизации) о событиях и изменениях состояния:

[**\_ \_ обратный вызов оповещения о создании пмгм \_**](/windows/win32/api/mgm/nc-mgm-pmgm_creation_alert_callback)

[**\_обратный вызов пмгм для \_ оповещения о соединении \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback)

[**\_ \_ обратный вызов оповещения пмгм \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback)

[**\_ \_ обратный вызов локального ПРИсоединение пмгм \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback)

[**\_обратный вызов пмгм для локального \_ выхода \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback)

[**\_ \_ обратный вызов пмгм РПФ**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback)

[**ПМГМ \_ неправильный \_ \_ обратный вызов**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback)

Диспетчер групп многоадресной рассылки использует следующие обратные вызовы для уведомления IGMP о событиях и изменениях состояния:

[**ПМГМ \_ Отключить \_ \_ обратный вызов IGMP**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback)

[**ПМГМ \_ включить \_ \_ обратный вызов IGMP**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)

 

 