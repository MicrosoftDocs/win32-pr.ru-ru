---
title: Обратные вызовы диспетчера групп многоадресной рассылки
description: Диспетчер групп многоадресной рассылки использует следующие обратные вызовы для уведомления клиентов (обычно протоколы маршрутизации) о событиях и изменениях состояния.
ms.assetid: ebabdfaf-8f5f-45be-9f01-f1dbc01a376c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ba18f874005e23aef6daca6071362362312e8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890861"
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

 

 