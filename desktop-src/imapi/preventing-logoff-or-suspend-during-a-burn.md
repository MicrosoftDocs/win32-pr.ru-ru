---
title: Предотвращение выхода из системы или приостановки во время записи
description: Если в приложении не выполняются правильные меры предосторожности, пользователь может выйти из системы во время операции записи. Это приводит к прерыванию процесса записи, что может привести к потере данных и, возможно, к неработоспособности диска.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5922fbe6dbc27303cee82e7ed745cbaaf2744781
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487600"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a><span data-ttu-id="f4163-104">Предотвращение выхода из системы или приостановки во время записи</span><span class="sxs-lookup"><span data-stu-id="f4163-104">Preventing Logoff or Suspend During a Burn</span></span>

<span data-ttu-id="f4163-105">Если в приложении не выполняются правильные меры предосторожности, пользователь может выйти из системы во время операции записи.</span><span class="sxs-lookup"><span data-stu-id="f4163-105">If proper precautions are not made within an application, it is possible for a user to log off during a burn operation.</span></span> <span data-ttu-id="f4163-106">Это приводит к прерыванию процесса записи, что может привести к потере данных и, возможно, к неработоспособности диска.</span><span class="sxs-lookup"><span data-stu-id="f4163-106">This leads to the interruption of the burn process, which can result in lost data and possibly render the disc unusable.</span></span>

<span data-ttu-id="f4163-107">Чтобы избежать этой проблемы, приложение должно обработать сообщение [**WM \_ куерендсессион**](/windows/desktop/Shutdown/wm-queryendsession) , которое доставляется до выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="f4163-107">To avoid this problem, the application should process the [**WM\_QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) message which is delivered prior to log off.</span></span> <span data-ttu-id="f4163-108">Если приложение получает это сообщение во время выполнения операции записи, возвращается **значение false** , чтобы отменить процедуру выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="f4163-108">If the application receives this message while performing a burn operation, return **FALSE** to cancel the logoff procedure.</span></span> <span data-ttu-id="f4163-109">Если приложение позволяет пользователю решить, следует ли продолжать выход из системы, должно быть указано предупреждение о том, что пользователь потеряет данные.</span><span class="sxs-lookup"><span data-stu-id="f4163-109">If the application allows the user to decide whether to continue logging off, a warning should be provided indicating that user will lose data.</span></span>

<span data-ttu-id="f4163-110">Переходы питания в процессе записи могут также создавать потенциальные проблемы при успешном выполнении действия записи.</span><span class="sxs-lookup"><span data-stu-id="f4163-110">Power transitions during the burn process can also create potential problems in the success of a burn activity.</span></span> <span data-ttu-id="f4163-111">Предотвращение этих осложнений во время процесса записи требует от приложения учитывать время перехода на питание.</span><span class="sxs-lookup"><span data-stu-id="f4163-111">Preventing these complications during the burn process requires an application to be aware of when power transitions are about to take place.</span></span> <span data-ttu-id="f4163-112">Это достигается путем включения приложения для обработки сообщения [**WM \_ поверброадкаст**](/windows/desktop/Power/wm-powerbroadcast) .</span><span class="sxs-lookup"><span data-stu-id="f4163-112">This is accomplished by by enabling the application to process the [**WM\_POWERBROADCAST**](/windows/desktop/Power/wm-powerbroadcast) message.</span></span> <span data-ttu-id="f4163-113">Приложения, разработанные для Windows XP или Windows Server 2003, могут вернуть **широковещательный \_ запрос \_ Deny** в ответ на [**ПБТ \_ апмкуерисуспенд**](/windows/desktop/Power/pbt-apmquerysuspend), предотвращая приостановку в процессе записи.</span><span class="sxs-lookup"><span data-stu-id="f4163-113">Applications developed for Windows XP or Windows Server 2003 can return **BROADCAST\_QUERY\_DENY** in response to [**PBT\_APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend), preventing Suspend during the burn process.</span></span>

<span data-ttu-id="f4163-114">Из-за изменений в модели управления питанием для Windows Vista и Windows Server 2008 событие [**ПБТ \_ апмкуерисуспенд**](/windows/desktop/Power/pbt-apmquerysuspend) больше не доставляется в приложения.</span><span class="sxs-lookup"><span data-stu-id="f4163-114">Due to changes in the Power Management Model for Windows Vista and Windows Server 2008, the [**PBT\_APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) event is no longer delivered to applications.</span></span> <span data-ttu-id="f4163-115">Вместо этого событие [**ПБТ \_ апмсуспенд**](/windows/desktop/Power/pbt-apmsuspend) доставляется, предоставляя приложению две секунды для подготовки к переходу.</span><span class="sxs-lookup"><span data-stu-id="f4163-115">Instead the [**PBT\_APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) event is delivered, providing two seconds for an application to prepare for the transition.</span></span>

<span data-ttu-id="f4163-116">В результате этих изменений мы советуем, чтобы приложения вызывали функцию [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) , чтобы предотвратить время простоя системы, что обычно приводит к приостановке перехода.</span><span class="sxs-lookup"><span data-stu-id="f4163-116">As a result of these changes, it is recommended that applications call the [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) function to prevent a system idle time-out which ordinarily results in the transition to Suspend.</span></span> <span data-ttu-id="f4163-117">Важно помнить, что вызов этой функции с соответствующим набором флагов будет препятствовать простою системы, а не выполняющейся приостановке.</span><span class="sxs-lookup"><span data-stu-id="f4163-117">It is important to remember that calling this function with the appropriate flags set will only prevent system idle, not an in-progress Suspend.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4163-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f4163-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4163-119">Использование IMAPI</span><span class="sxs-lookup"><span data-stu-id="f4163-119">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="f4163-120">**SetThreadExecutionState**</span><span class="sxs-lookup"><span data-stu-id="f4163-120">**SetThreadExecutionState**</span></span>](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 