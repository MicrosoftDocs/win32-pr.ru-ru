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
# <a name="registering-for-power-events"></a><span data-ttu-id="475a3-103">Регистрация для событий питания</span><span class="sxs-lookup"><span data-stu-id="475a3-103">Registering for Power Events</span></span>

<span data-ttu-id="475a3-104">Приложения могут лучше адаптировать свое поведение к текущему состоянию электропитания компьютера путем регистрации событий питания.</span><span class="sxs-lookup"><span data-stu-id="475a3-104">Applications can better adapt their behavior to the current power state of the computer by registering for power events.</span></span> <span data-ttu-id="475a3-105">Приложение должно регистрироваться для каждого события изменения питания, которое может повлиять на его поведение.</span><span class="sxs-lookup"><span data-stu-id="475a3-105">An application should register for each power change event that might impact its behavior.</span></span>

<span data-ttu-id="475a3-106">Приложение или служба использует функцию [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="475a3-106">An application or service uses the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function to register for notifications.</span></span> <span data-ttu-id="475a3-107">При изменении соответствующего параметра питания система отправляет уведомления следующим образом:</span><span class="sxs-lookup"><span data-stu-id="475a3-107">When the corresponding power setting changes, the system sends notifications as follows:</span></span>

-   <span data-ttu-id="475a3-108">Приложение получает сообщение [**WM \_ поверброадкаст**](wm-powerbroadcast.md) с [**\_ параметром**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) *wParam* [ПБТ \_ поверсеттингчанже](pbt-powersettingchange.md) и *lParam* , который указывает на структуру параметров поверброадкаст.</span><span class="sxs-lookup"><span data-stu-id="475a3-108">An application receives a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message with a *wParam* of [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) and an *lParam* that points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>
-   <span data-ttu-id="475a3-109">Служба получает вызов функции обратного вызова [*хандлерекс*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) , которая была зарегистрирована путем вызова функции [**регистерсервицектрлхандлерекс**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) .</span><span class="sxs-lookup"><span data-stu-id="475a3-109">A service receives a call to the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) callback function it registered by calling the [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function.</span></span> <span data-ttu-id="475a3-110">Параметр *лпевентдата* , передаваемый в функцию обратного вызова *хандлерекс* , указывает на структуру [**\_ параметра поверброадкаст**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="475a3-110">The *lpEventData* parameter sent to the *HandlerEx* callback function points to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

<span data-ttu-id="475a3-111">В структуре [**\_ параметра Поверброадкаст**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) элемент **поверсеттинг** содержит идентификатор GUID, определяющий уведомление, а элемент **данных** содержит новое значение параметра питания.</span><span class="sxs-lookup"><span data-stu-id="475a3-111">In the [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure, the **PowerSetting** member contains the GUID that identifies the notification and the **Data** member contains the new value of the power setting.</span></span>

<span data-ttu-id="475a3-112">Список идентификаторов GUID параметров питания для наиболее полезных в приложениях уведомлений см. в разделе [**идентификаторы GUID параметров питания**](power-setting-guids.md).</span><span class="sxs-lookup"><span data-stu-id="475a3-112">For a list of power setting GUIDs for notifications that are most useful to applications, see [**Power Setting GUIDs**](power-setting-guids.md).</span></span>

 

 
