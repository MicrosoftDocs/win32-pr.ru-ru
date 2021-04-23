---
description: Пользователь может запустить службу с помощью служебной программы панели управления "службы". Пользователь может указать аргументы для службы в поле начальные параметры. Программа управления службами может запустить службу и указать ее аргументы с помощью функции StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Запуск служб по требованию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664361"
---
# <a name="starting-services-on-demand"></a><span data-ttu-id="46227-105">Запуск служб по требованию</span><span class="sxs-lookup"><span data-stu-id="46227-105">Starting Services on Demand</span></span>

<span data-ttu-id="46227-106">Пользователь может запустить службу с помощью служебной программы панели управления "службы".</span><span class="sxs-lookup"><span data-stu-id="46227-106">The user can start a service with the Services control panel utility.</span></span> <span data-ttu-id="46227-107">Пользователь может указать аргументы для службы в поле **начальные параметры** .</span><span class="sxs-lookup"><span data-stu-id="46227-107">The user can specify arguments for the service in the **Start parameters** field.</span></span> <span data-ttu-id="46227-108">Программа управления службами может запустить службу и указать ее аргументы с помощью функции [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="46227-108">A service control program can start a service and specify its arguments with the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function.</span></span>

<span data-ttu-id="46227-109">При запуске службы SCM выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="46227-109">When the service is started, the SCM performs the following steps:</span></span>

-   <span data-ttu-id="46227-110">Получение сведений об учетной записи, хранящейся в базе данных.</span><span class="sxs-lookup"><span data-stu-id="46227-110">Retrieve the account information stored in the database.</span></span>
-   <span data-ttu-id="46227-111">Войдите в учетную запись службы.</span><span class="sxs-lookup"><span data-stu-id="46227-111">Log on the service account.</span></span>
-   <span data-ttu-id="46227-112">Загрузите профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="46227-112">Load the user profile.</span></span>
-   <span data-ttu-id="46227-113">Создайте службу в приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="46227-113">Create the service in the suspended state.</span></span>
-   <span data-ttu-id="46227-114">Назначьте процессу маркер входа.</span><span class="sxs-lookup"><span data-stu-id="46227-114">Assign the logon token to the process.</span></span>
-   <span data-ttu-id="46227-115">Разрешить выполнение процесса.</span><span class="sxs-lookup"><span data-stu-id="46227-115">Allow the process to execute.</span></span>

 

 



