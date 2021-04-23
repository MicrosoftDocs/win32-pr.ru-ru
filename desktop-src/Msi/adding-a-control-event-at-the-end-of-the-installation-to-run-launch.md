---
description: Установщик запускает последовательность мастера установки примера только в том случае, если для установки приложения используется полный уровень пользовательского интерфейса.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Добавление события элемента управления в конце установки для запуска запуска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998309"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a><span data-ttu-id="e2d2f-103">Добавление события элемента управления в конце установки для запуска запуска</span><span class="sxs-lookup"><span data-stu-id="e2d2f-103">Adding a Control Event at the End of the Installation to Run Launch</span></span>

<span data-ttu-id="e2d2f-104">Установщик запускает последовательность мастера установки примера только в том случае, если для установки приложения используется [*полный уровень пользовательского интерфейса*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e2d2f-104">The installer runs the sample's installation wizard sequence only if the [*full UI*](f-gly.md) level is used to install the application.</span></span> <span data-ttu-id="e2d2f-105">Последним диалоговым окном примера последовательности диалогового окна является [диалоговое окно выхода](exit-dialog.md) с именем екситдиалог.</span><span class="sxs-lookup"><span data-stu-id="e2d2f-105">The last dialog box of the sample dialog sequence is an [Exit Dialog](exit-dialog.md) named ExitDialog.</span></span> <span data-ttu-id="e2d2f-106">Когда пользователь взаимодействует с кнопкой ОК в Екситдиалог, сначала публикуется [EndDialog таблице ControlEvent событие](enddialog-controlevent.md) , возвращающий управление в установщик.</span><span class="sxs-lookup"><span data-stu-id="e2d2f-106">When a user interacts with the OK button on ExitDialog, this first publishes an [EndDialog ControlEvent](enddialog-controlevent.md) that returns control to the installer.</span></span> <span data-ttu-id="e2d2f-107">Затем элемент управления публикует [DoAction таблице ControlEvent событие](doaction-controlevent.md) , который запускает настраиваемое действие запуска.</span><span class="sxs-lookup"><span data-stu-id="e2d2f-107">The control then publishes a [DoAction ControlEvent](doaction-controlevent.md) that runs the Launch custom action.</span></span> <span data-ttu-id="e2d2f-108">Каждому событию элемента управления требуется запись в [таблице таблице ControlEvent событие](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="e2d2f-108">Each control event requires a record in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="e2d2f-109">См. [Обзор таблице ControlEvent событие](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e2d2f-109">See [ControlEvent Overview](controlevent-overview.md).</span></span>

[<span data-ttu-id="e2d2f-110">Таблица таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="e2d2f-110">ControlEvent Table</span></span>](controlevent-table.md)



| <span data-ttu-id="e2d2f-111">Диалог</span><span class="sxs-lookup"><span data-stu-id="e2d2f-111">Dialog</span></span>     | <span data-ttu-id="e2d2f-112">элементом управления\_</span><span class="sxs-lookup"><span data-stu-id="e2d2f-112">Control\_</span></span> | <span data-ttu-id="e2d2f-113">Событие</span><span class="sxs-lookup"><span data-stu-id="e2d2f-113">Event</span></span>     | <span data-ttu-id="e2d2f-114">Аргумент</span><span class="sxs-lookup"><span data-stu-id="e2d2f-114">Argument</span></span> | <span data-ttu-id="e2d2f-115">Условие</span><span class="sxs-lookup"><span data-stu-id="e2d2f-115">Condition</span></span>                     | <span data-ttu-id="e2d2f-116">Упорядочение</span><span class="sxs-lookup"><span data-stu-id="e2d2f-116">Ordering</span></span> |
|------------|-----------|-----------|----------|-------------------------------|----------|
| <span data-ttu-id="e2d2f-117">екситдиалог</span><span class="sxs-lookup"><span data-stu-id="e2d2f-117">ExitDialog</span></span> | <span data-ttu-id="e2d2f-118">ОК</span><span class="sxs-lookup"><span data-stu-id="e2d2f-118">OK</span></span>        | <span data-ttu-id="e2d2f-119">EndDialog</span><span class="sxs-lookup"><span data-stu-id="e2d2f-119">EndDialog</span></span> | <span data-ttu-id="e2d2f-120">Возвращает</span><span class="sxs-lookup"><span data-stu-id="e2d2f-120">Return</span></span>   | <span data-ttu-id="e2d2f-121">1</span><span class="sxs-lookup"><span data-stu-id="e2d2f-121">1</span></span>                             | <span data-ttu-id="e2d2f-122">1</span><span class="sxs-lookup"><span data-stu-id="e2d2f-122">1</span></span>        |
| <span data-ttu-id="e2d2f-123">екситдиалог</span><span class="sxs-lookup"><span data-stu-id="e2d2f-123">ExitDialog</span></span> | <span data-ttu-id="e2d2f-124">ОК</span><span class="sxs-lookup"><span data-stu-id="e2d2f-124">OK</span></span>        | <span data-ttu-id="e2d2f-125">DoAction</span><span class="sxs-lookup"><span data-stu-id="e2d2f-125">DoAction</span></span>  | <span data-ttu-id="e2d2f-126">Launch</span><span class="sxs-lookup"><span data-stu-id="e2d2f-126">Launch</span></span>   | <span data-ttu-id="e2d2f-127">НЕ установлено и $Tutorial = 3</span><span class="sxs-lookup"><span data-stu-id="e2d2f-127">NOT Installed AND $Tutorial=3</span></span> | <span data-ttu-id="e2d2f-128">2</span><span class="sxs-lookup"><span data-stu-id="e2d2f-128">2</span></span>        |



 

<span data-ttu-id="e2d2f-129">Условие в элементе управления DoAction гарантирует, что настраиваемое действие выполняется только во время первой установки приложения и устанавливается локально.</span><span class="sxs-lookup"><span data-stu-id="e2d2f-129">The condition on the DoAction control ensures the custom action only runs during the first installation of the application and that it is being installed locally.</span></span> <span data-ttu-id="e2d2f-130">Фраза $Tutorial = 3 означает, что для состояния действия компонента учебника задано значение Local.</span><span class="sxs-lookup"><span data-stu-id="e2d2f-130">The phrase $Tutorial=3 means the action state of the Tutorial component is set to local.</span></span> <span data-ttu-id="e2d2f-131">См. раздел [Синтаксис условных инструкций](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e2d2f-131">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="e2d2f-132">Это завершает пример.</span><span class="sxs-lookup"><span data-stu-id="e2d2f-132">This completes the sample.</span></span>

 

 



