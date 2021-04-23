---
title: Восстановление приложений и перезагрузка
description: Создание пользовательских установщиков для автоматического перезапуска приложения, которое было завершено для завершения обновления. Сохраните данные и настройте восстановление приложения перед выходом из программы.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- надежность
- надежность программного обеспечения
- Восстановление приложения
- перезапуск приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889039"
---
# <a name="application-recovery-and-restart"></a><span data-ttu-id="62910-111">Восстановление приложений и перезагрузка</span><span class="sxs-lookup"><span data-stu-id="62910-111">Application Recovery and Restart</span></span>

## <a name="purpose"></a><span data-ttu-id="62910-112">Назначение</span><span class="sxs-lookup"><span data-stu-id="62910-112">Purpose</span></span>

<span data-ttu-id="62910-113">Приложение может использовать восстановление и перезагрузку приложения (ARR) для сохранения данных и сведений о состоянии до завершения работы приложения из-за необработанного исключения или зависания приложения.</span><span class="sxs-lookup"><span data-stu-id="62910-113">An application can use Application Recovery and Restart (ARR) to save data and state information before the application exits due to an unhandled exception or when the application stops responding.</span></span> <span data-ttu-id="62910-114">При запросе приложение также перезапускается.</span><span class="sxs-lookup"><span data-stu-id="62910-114">The application is also restarted, if requested.</span></span>

<span data-ttu-id="62910-115">Приложение также может быть перезапущено, если установщик обновляет компонент приложения или если компьютер должен перезапуститься в результате обновления.</span><span class="sxs-lookup"><span data-stu-id="62910-115">An application can also be restarted if an installer updates a component of the application, or if the computer needs to restart as the result of an update.</span></span> <span data-ttu-id="62910-116">Обратите внимание, что для поддержки автоматического перезапуска приложения после того, как установщик обновит приложение, необходимо соответствующим образом создать приложение и установщик.</span><span class="sxs-lookup"><span data-stu-id="62910-116">Note that to support automatic application restart after an installer updates an application, both the application and installer need to be authored appropriately.</span></span> <span data-ttu-id="62910-117">Дополнительные сведения см. в разделе [Регистрация для перезапуска приложения](registering-for-application-restart.md).</span><span class="sxs-lookup"><span data-stu-id="62910-117">For details, see [Registering for Application Restart](registering-for-application-restart.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="62910-118">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="62910-118">Developer audience</span></span>

<span data-ttu-id="62910-119">ARR предназначен для разработчиков на C и C++.</span><span class="sxs-lookup"><span data-stu-id="62910-119">ARR is designed for C and C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="62910-120">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="62910-120">Run-time requirements</span></span>

<span data-ttu-id="62910-121">Параметр ARR доступен, начиная с операционной системы Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="62910-121">ARR is available starting with the Windows Vista operating system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="62910-122">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="62910-122">In this section</span></span>



| <span data-ttu-id="62910-123">Раздел</span><span class="sxs-lookup"><span data-stu-id="62910-123">Topic</span></span>                                                                                                   | <span data-ttu-id="62910-124">Описание</span><span class="sxs-lookup"><span data-stu-id="62910-124">Description</span></span>                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="62910-125">Использование восстановления и перезапуска приложения</span><span class="sxs-lookup"><span data-stu-id="62910-125">Using Application Recovery and Restart</span></span>](using-application-recovery-and-restart.md)<br/>         | <span data-ttu-id="62910-126">Процедурное пошаговое описание регистрации для восстановления и перезапуска.</span><span class="sxs-lookup"><span data-stu-id="62910-126">Procedural guide for registering for recovery and restart.</span></span><br/> |
| [<span data-ttu-id="62910-127">Справочник по восстановлению и перезапуску приложений</span><span class="sxs-lookup"><span data-stu-id="62910-127">Application Recovery and Restart Reference</span></span>](application-recovery-and-restart-reference.md)<br/> | <span data-ttu-id="62910-128">Справочные сведения по API ARR.</span><span class="sxs-lookup"><span data-stu-id="62910-128">Reference information for the ARR API.</span></span> <br/>                    |



 

 

 





