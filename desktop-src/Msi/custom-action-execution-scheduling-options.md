---
description: Поскольку пользовательское действие может быть запланировано как в пользовательском интерфейсе, так и для выполнения таблиц последовательности и может выполняться в службе или клиентском процессе, настраиваемое действие может выполняться несколько раз.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Параметры планирования выполнения настраиваемых действий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663529"
---
# <a name="custom-action-execution-scheduling-options"></a><span data-ttu-id="6cdf6-103">Параметры планирования выполнения настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="6cdf6-103">Custom Action Execution Scheduling Options</span></span>

<span data-ttu-id="6cdf6-104">Поскольку пользовательское действие может быть запланировано как в пользовательском интерфейсе, так и для выполнения таблиц последовательности и может выполняться в службе или клиентском процессе, настраиваемое действие может выполняться несколько раз.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-104">Because a custom action can be scheduled in both the UI and execute sequence tables, and can be executed either in the service or client process, a custom action can potentially execute multiple times.</span></span>

<span data-ttu-id="6cdf6-105">Обратите внимание, что установщик:</span><span class="sxs-lookup"><span data-stu-id="6cdf6-105">Note that the installer:</span></span>

-   <span data-ttu-id="6cdf6-106">По умолчанию выполняет действия в таблице последовательности.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-106">Executes actions in a sequence table immediately by default.</span></span>
-   <span data-ttu-id="6cdf6-107">Не выполняет действие, если поле условного выражения в таблице последовательности имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-107">Does not execute an action if the conditional expression field of the sequence table evaluates to False.</span></span>
-   <span data-ttu-id="6cdf6-108">Обрабатывает таблицу последовательности ПОЛЬЗОВАТЕЛЬСКОГО интерфейса в клиентском процессе, если для внутреннего уровня интерфейса пользователя задан режим полного пользовательского интерфейса (см. раздел [**мсисетинтерналуи**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) для описания уровней пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="6cdf6-108">Processes the UI sequence table in the client process if the internal user's interface level is set to the full UI mode (see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) for a description of UI levels).</span></span>
-   <span data-ttu-id="6cdf6-109">— Это служба, зарегистрированная по умолчанию при использовании Windows 2000, и в этом случае таблица выполнения последовательности обрабатывается в службе установщика.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-109">Is a service registered by default when using Windows 2000 and, in this case, the execute sequence table is processed in the installer service.</span></span>

<span data-ttu-id="6cdf6-110">Можно использовать следующие флаги параметров для управления несколькими немедленным выполнением настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-110">You can use the following option flags to control multiple immediate execution of custom actions.</span></span> <span data-ttu-id="6cdf6-111">Чтобы задать параметр, добавьте значение в этой таблице к значению в поле Тип [таблицы CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="6cdf6-111">To set an option, add the value in this table to the value in the Type field of the [CustomAction table](customaction-table.md).</span></span> <span data-ttu-id="6cdf6-112">Не следует использовать ни один из следующих флагов с [отложенными настраиваемыми действиями выполнения](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6cdf6-112">None of the following flags should be used with [deferred execution custom actions](deferred-execution-custom-actions.md).</span></span>

<dl> <dt>

<span data-ttu-id="6cdf6-113"><span id="_default_"></span><span id="_DEFAULT_"></span>параметры</span><span class="sxs-lookup"><span data-stu-id="6cdf6-113"><span id="_default_"></span><span id="_DEFAULT_"></span>(default)</span></span>
</dt> <dd>

<span data-ttu-id="6cdf6-114">Шестнадцатеричное: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="6cdf6-114">Hexadecimal: 0x00000000</span></span>

<span data-ttu-id="6cdf6-115">Десятичное число: 0</span><span class="sxs-lookup"><span data-stu-id="6cdf6-115">Decimal: 0</span></span>

<span data-ttu-id="6cdf6-116">Всегда выполнять.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-116">Always execute.</span></span> <span data-ttu-id="6cdf6-117">Действие может выполняться дважды, если оно есть в обеих таблицах последовательности.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-117">Action may run twice if present in both sequence tables.</span></span>

</dd> <dt>

<span data-ttu-id="6cdf6-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**мсидбкустомактионтипефирстсекуенце**</span><span class="sxs-lookup"><span data-stu-id="6cdf6-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span></span> 
</dt> <dd>

<span data-ttu-id="6cdf6-119">Шестнадцатеричное: 0x00000100</span><span class="sxs-lookup"><span data-stu-id="6cdf6-119">Hexadecimal: 0x00000100</span></span>

<span data-ttu-id="6cdf6-120">Десятичное число: 256</span><span class="sxs-lookup"><span data-stu-id="6cdf6-120">Decimal: 256</span></span>

<span data-ttu-id="6cdf6-121">Выполняется не более одного раза, если оно есть в обеих таблицах последовательности.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-121">Execute no more than once if present in both sequence tables.</span></span> <span data-ttu-id="6cdf6-122">Всегда пропускает действие в последовательности выполнения, если выполнялась последовательность пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-122">Always skips action in execute sequence if UI sequence has run.</span></span> <span data-ttu-id="6cdf6-123">Не влияет на последовательность пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-123">No effect in UI sequence.</span></span> <span data-ttu-id="6cdf6-124">Действие не обязательно должно присутствовать или выполняться в последовательности пользовательского интерфейса для пропуска в последовательности выполнения.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-124">The action is not required to be present or run in the UI sequence to be skipped in the execute sequence.</span></span> <span data-ttu-id="6cdf6-125">Не затрагивается при установке регистрации службы.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-125">Not affected by install service registration.</span></span>

</dd> <dt>

<span data-ttu-id="6cdf6-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**мсидбкустомактионтипеонцеперпроцесс**</span><span class="sxs-lookup"><span data-stu-id="6cdf6-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span></span>
</dt> <dd>

<span data-ttu-id="6cdf6-127">Шестнадцатеричное: 0x00000200</span><span class="sxs-lookup"><span data-stu-id="6cdf6-127">Hexadecimal: 0x00000200</span></span>

<span data-ttu-id="6cdf6-128">Десятичное число: 512</span><span class="sxs-lookup"><span data-stu-id="6cdf6-128">Decimal: 512</span></span>

<span data-ttu-id="6cdf6-129">Выполните один раз для каждого процесса, если они находятся в обеих таблицах последовательности.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-129">Execute once per process if in both sequence tables.</span></span> <span data-ttu-id="6cdf6-130">Пропускает действие в последовательности выполнения, если последовательность пользовательского интерфейса была запущена в том же процессе, например, в процессе выполнения в клиенте.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-130">Skips action in execute sequence if UI sequence has been run in same process, for example both run in the client process.</span></span> <span data-ttu-id="6cdf6-131">Используется для предотвращения выполнения действий, изменяющих состояние сеанса, таких как свойства и данные базы данных, в два раза.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-131">Used to prevent actions that modify the session state, such as property and database data, from running twice.</span></span>

</dd> <dt>

<span data-ttu-id="6cdf6-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**мсидбкустомактионтипеклиентрепеат**</span><span class="sxs-lookup"><span data-stu-id="6cdf6-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span></span>
</dt> <dd>

<span data-ttu-id="6cdf6-133">Шестнадцатеричное: 0x00000300</span><span class="sxs-lookup"><span data-stu-id="6cdf6-133">Hexadecimal: 0x00000300</span></span>

<span data-ttu-id="6cdf6-134">Десятичное число: 768</span><span class="sxs-lookup"><span data-stu-id="6cdf6-134">Decimal: 768</span></span>

<span data-ttu-id="6cdf6-135">Выполнять, только если выполняется на клиенте после выполнения последовательности пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-135">Execute only if running on client after UI sequence has run.</span></span> <span data-ttu-id="6cdf6-136">Действие выполняется только в том случае, если последовательность выполнения выполняется на клиенте в следующем порядке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-136">The action runs only if the execute sequence is run on the client following UI sequence.</span></span> <span data-ttu-id="6cdf6-137">Может использоваться для предоставления логики либо (или), либо для подавления обработки, связанной с ИП, если она уже выполнена для сеанса клиента.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-137">May be used to provide either/or logic, or to suppress the UI-related processing if already done for the client session.</span></span>

</dd> </dl>

<span data-ttu-id="6cdf6-138">Обратите внимание, что для выполнения настраиваемого действия в двух различных режимах выполнения создайте две записи в [таблице CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="6cdf6-138">Note that to run a custom action during two different run modes, author two entries into the [CustomAction table](customaction-table.md) .</span></span> <span data-ttu-id="6cdf6-139">Например, чтобы создать пользовательское действие, которое вызывает библиотеку динамической компоновки C/C++ ( [тип настраиваемого действия 1](custom-action-type-1.md)) как мсирунмоде \_ Scheduled и мсирунмоде \_ Rollback, поставьте две записи в таблицу CustomAction, которые вызывают одну и ту же библиотеку DLL, но имеют разные числовые типы.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-139">For example, to have a custom action that calls a C/C++ dynamic link library (DLL) ( [Custom Action Type 1](custom-action-type-1.md)) both when the mode is MSIRUNMODE\_SCHEDULED and MSIRUNMODE\_ROLLBACK, put two entries in the CustomAction table that call the same DLL but that have different numeric types.</span></span> <span data-ttu-id="6cdf6-140">Включите код, вызывающий [**мсижетмоде**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) , чтобы определить, когда следует запускать настраиваемое действие.</span><span class="sxs-lookup"><span data-stu-id="6cdf6-140">Include code that calls [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) to determine when to run which custom action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cdf6-141">См. также</span><span class="sxs-lookup"><span data-stu-id="6cdf6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cdf6-142">Ссылка на настраиваемое действие</span><span class="sxs-lookup"><span data-stu-id="6cdf6-142">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="6cdf6-143">Сведения о настраиваемых действиях</span><span class="sxs-lookup"><span data-stu-id="6cdf6-143">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="6cdf6-144">Использование настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="6cdf6-144">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



