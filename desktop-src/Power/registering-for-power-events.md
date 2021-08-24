---
description: Приложения могут лучше адаптировать свое поведение к текущему состоянию электропитания компьютера путем регистрации событий питания.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Регистрация для событий питания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c360905800ad3fdce047e16a0244cd3dbf1ca312f18154f0be0c36b75e546d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143327"
---
# <a name="registering-for-power-events"></a>Регистрация для событий питания

Приложения могут лучше адаптировать свое поведение к текущему состоянию электропитания компьютера путем регистрации событий питания. Приложение должно регистрироваться для каждого события изменения питания, которое может повлиять на его поведение.

Приложение или служба использует функцию [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) для регистрации уведомлений. При изменении соответствующего параметра питания система отправляет уведомления следующим образом:

-   Приложение получает сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) с [**\_ параметром**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) *wParam* [ПБТ \_ поверсеттингчанже](pbt-powersettingchange.md) и *lParam* , который указывает на структуру параметров поверброадкаст.
-   Служба получает вызов функции обратного вызова [*хандлерекс*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) , которая была зарегистрирована путем вызова функции [**регистерсервицектрлхандлерекс**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) . Параметр *лпевентдата* , передаваемый в функцию обратного вызова *хандлерекс* , указывает на структуру [**\_ параметра поверброадкаст**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .

В структуре [**\_ параметра Поверброадкаст**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) элемент **поверсеттинг** содержит идентификатор GUID, определяющий уведомление, а элемент **данных** содержит новое значение параметра питания.

Список идентификаторов GUID параметров питания для наиболее полезных в приложениях уведомлений см. в разделе [**идентификаторы GUID параметров питания**](power-setting-guids.md).

 

 
