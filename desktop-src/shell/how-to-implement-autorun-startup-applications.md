---
description: В основном нет ограничений на написание приложения автозапуска.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Как реализовать запускаемые приложения автозапуска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998453"
---
# <a name="how-to-implement-autorun-startup-applications"></a><span data-ttu-id="6fd52-103">Как реализовать запускаемые приложения автозапуска</span><span class="sxs-lookup"><span data-stu-id="6fd52-103">How to Implement AutoRun Startup Applications</span></span>

<span data-ttu-id="6fd52-104">В основном нет ограничений на написание приложения автозапуска.</span><span class="sxs-lookup"><span data-stu-id="6fd52-104">There are essentially no constraints on how to write an AutoRun startup application.</span></span> <span data-ttu-id="6fd52-105">Вы можете реализовать запускаемое приложение для выполнения любых действий, необходимых для установки, удаления, настройки или запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="6fd52-105">You can implement the startup application to do whatever you find necessary to install, uninstall, configure, or run your application.</span></span> <span data-ttu-id="6fd52-106">Однако следующие советы предоставляют некоторые рекомендации по реализации действующего приложения автозапуска.</span><span class="sxs-lookup"><span data-stu-id="6fd52-106">However, the following tips provide some guidelines to implementing an effective AutoRun startup application.</span></span>

## <a name="instructions"></a><span data-ttu-id="6fd52-107">Инструкции</span><span class="sxs-lookup"><span data-stu-id="6fd52-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="6fd52-108">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="6fd52-108">Step 1:</span></span>

<span data-ttu-id="6fd52-109">Убедитесь, что пользователи получают отзыв как можно скорее после вставки диска с автозапуском в дисковод.</span><span class="sxs-lookup"><span data-stu-id="6fd52-109">Make sure that users receive feedback as soon as possible after they insert an AutoRun disc into the drive.</span></span> <span data-ttu-id="6fd52-110">Запускаемые приложения — это небольшие программы, которые быстро загружаются.</span><span class="sxs-lookup"><span data-stu-id="6fd52-110">Startup applications should be small programs that load quickly.</span></span> <span data-ttu-id="6fd52-111">Они должны четко определить приложение и предоставить простой способ отмены операции.</span><span class="sxs-lookup"><span data-stu-id="6fd52-111">They should clearly identify the application and provide an easy way to cancel the operation.</span></span>

### <a name="step-2"></a><span data-ttu-id="6fd52-112">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="6fd52-112">Step 2:</span></span>

<span data-ttu-id="6fd52-113">Убедитесь, что программа уже установлена.</span><span class="sxs-lookup"><span data-stu-id="6fd52-113">Check to see if the program is already installed.</span></span> <span data-ttu-id="6fd52-114">В противном случае, скорее всего, будет описана процедура установки.</span><span class="sxs-lookup"><span data-stu-id="6fd52-114">If not, the next step will probably be the setup procedure.</span></span> <span data-ttu-id="6fd52-115">Запускаемое приложение может воспользоваться преимуществами времени, затрачиваемого пользователем на чтение диалогового окна, запустив другой поток, чтобы начать загрузку кода установки.</span><span class="sxs-lookup"><span data-stu-id="6fd52-115">The startup application can take advantage of the time the user spends reading the dialog box by starting another thread to begin loading the setup code.</span></span> <span data-ttu-id="6fd52-116">К моменту нажатия пользователем кнопки **ОК** программа установки будет уже частично загружена.</span><span class="sxs-lookup"><span data-stu-id="6fd52-116">By the time the user clicks **OK**, your setup program will already be partly if not fully loaded.</span></span> <span data-ttu-id="6fd52-117">Этот подход значительно уменьшает восприятие пользователем времени, затрачиваемого на загрузку приложения.</span><span class="sxs-lookup"><span data-stu-id="6fd52-117">This approach significantly reduces the user's perception of the amount of time it takes to load your application.</span></span>

> [!Note]  
> <span data-ttu-id="6fd52-118">Как правило, начальная часть запускаемого приложения представляет пользователей с помощью пользовательского интерфейса, например диалогового окна, с вопросом, как они хотели бы продолжить.</span><span class="sxs-lookup"><span data-stu-id="6fd52-118">Typically, the initial part of the startup application presents users with a user interface, such as a dialog box, asking them how they would like to proceed.</span></span>

 

### <a name="step-3"></a><span data-ttu-id="6fd52-119">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="6fd52-119">Step 3:</span></span>

<span data-ttu-id="6fd52-120">Запустите другой поток, чтобы начать загрузку кода приложения, чтобы сократить время ожидания для пользователя.</span><span class="sxs-lookup"><span data-stu-id="6fd52-120">Start another thread to begin loading application code to shorten the waiting time for the user.</span></span> <span data-ttu-id="6fd52-121">Если приложение уже установлено, пользователь, вероятно, вставил диск для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="6fd52-121">If the application has already been installed, the user probably inserted the disk to run the application.</span></span>

### <a name="step-4"></a><span data-ttu-id="6fd52-122">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="6fd52-122">Step 4:</span></span>

<span data-ttu-id="6fd52-123">Используйте следующие указания для минимального использования жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="6fd52-123">Use the following hints to minimize hard disk usage:</span></span>

-   <span data-ttu-id="6fd52-124">Необходимо, чтобы количество файлов на жестком диске не минимально.</span><span class="sxs-lookup"><span data-stu-id="6fd52-124">Keep the number of files that must be on the hard disk to a minimum.</span></span> <span data-ttu-id="6fd52-125">Они должны быть ограничены файлами, которые необходимы для запуска программы или для считывания с носителя неприемлемым большим временем.</span><span class="sxs-lookup"><span data-stu-id="6fd52-125">They should be restricted to files that are essential to running the program or that would take an unacceptably large amount of time to read from the media.</span></span>
-   <span data-ttu-id="6fd52-126">Во многих случаях установка необязательных файлов на жестком диске не требуется, но может предоставить такие преимущества, как повышение производительности.</span><span class="sxs-lookup"><span data-stu-id="6fd52-126">In many cases, installing nonessential files on the hard disk is not necessary, but might provide benefits such as increased performance.</span></span> <span data-ttu-id="6fd52-127">Предоставьте пользователю возможность выбрать способ принятия компромиссов между затратами и преимуществами дискового хранилища.</span><span class="sxs-lookup"><span data-stu-id="6fd52-127">Give the user the option of deciding how to make the trade-off between the costs and benefits of hard disk storage.</span></span>
-   <span data-ttu-id="6fd52-128">Предоставьте способ удаления всех компонентов, размещенных на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="6fd52-128">Provide a way to uninstall any components that were placed on the hard disk.</span></span>
-   <span data-ttu-id="6fd52-129">Если приложение кэширует данные, предоставьте пользователю некоторый контроль над ним.</span><span class="sxs-lookup"><span data-stu-id="6fd52-129">If your application caches data, give the user some control over it.</span></span> <span data-ttu-id="6fd52-130">Включите параметры в запускаемом приложении, например задание ограничения на максимальный объем кэшированных данных, которые будут храниться на жестком диске, или удаление приложением всех кэшированных данных при его завершении.</span><span class="sxs-lookup"><span data-stu-id="6fd52-130">Include options in the startup application such as setting a limit on the maximum amount of cached data that will be stored on the hard disk, or having the application discard any cached data when it terminates.</span></span>

### <a name="step-5"></a><span data-ttu-id="6fd52-131">Шаг 5.</span><span class="sxs-lookup"><span data-stu-id="6fd52-131">Step 5:</span></span>

<span data-ttu-id="6fd52-132">При необходимости отключите автозапуск.</span><span class="sxs-lookup"><span data-stu-id="6fd52-132">Disable Autorun if needed.</span></span> <span data-ttu-id="6fd52-133">Автозапуск можно подавлять программно или полностью отключить в реестре, даже если на носителе есть файл autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="6fd52-133">AutoRun can be suppressed programmatically or disabled entirely with the registry, even when a medium has an Autorun.inf file.</span></span> <span data-ttu-id="6fd52-134">Дополнительные сведения см. в разделе [Включение и отключение функции autorun](autoplay-reg.md) .</span><span class="sxs-lookup"><span data-stu-id="6fd52-134">See [Enabling and Disabling AutoRun](autoplay-reg.md) for more information.</span></span>

 

 



