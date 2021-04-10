---
description: Приложения могут лучше адаптировать свое поведение к текущему состоянию электропитания компьютера путем регистрации событий питания.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Регистрация для событий питания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da084592414d1c58ab4ab43dd2b5c35f028552b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264502"
---
# <a name="registering-for-power-events"></a>Регистрация для событий питания

Приложения могут лучше адаптировать свое поведение к текущему состоянию электропитания компьютера путем регистрации событий питания. Приложение должно регистрироваться для каждого события изменения питания, которое может повлиять на его поведение.

Приложение или служба использует функцию [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) для регистрации уведомлений. При изменении соответствующего параметра питания система отправляет уведомления следующим образом:

-   Приложение получает сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) с [**\_ параметром**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) *wParam* [ПБТ \_ поверсеттингчанже](pbt-powersettingchange.md) и *lParam* , который указывает на структуру параметров поверброадкаст.
-   Служба получает вызов функции обратного вызова [*хандлерекс*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) , которая была зарегистрирована путем вызова функции [**регистерсервицектрлхандлерекс**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) . Параметр *лпевентдата* , передаваемый в функцию обратного вызова *хандлерекс* , указывает на структуру [**\_ параметра поверброадкаст**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

В структуре [**\_ параметра Поверброадкаст**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) элемент **поверсеттинг** содержит идентификатор GUID, определяющий уведомление, а элемент **данных** содержит новое значение параметра питания.

Список идентификаторов GUID параметров питания для наиболее полезных в приложениях уведомлений см. в разделе [**идентификаторы GUID параметров питания**](power-setting-guids.md).

 

 
