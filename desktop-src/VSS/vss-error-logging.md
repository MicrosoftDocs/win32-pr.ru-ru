---
description: 'Следующие сведения об ошибке и состоянии VSS записываются в журнал событий приложений:'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Ведение журнала ошибок VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145223"
---
# <a name="vss-error-logging"></a><span data-ttu-id="e198c-103">Ведение журнала ошибок VSS</span><span class="sxs-lookup"><span data-stu-id="e198c-103">VSS Error Logging</span></span>

<span data-ttu-id="e198c-104">Следующие сведения об ошибке и состоянии VSS записываются в журнал событий приложений:</span><span class="sxs-lookup"><span data-stu-id="e198c-104">The following VSS error and state information is written to the Application Event Log:</span></span>

-   <span data-ttu-id="e198c-105">Ошибки инициатора, созданные с помощью интерфейса [**ивссбаккупкомпонентс**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)</span><span class="sxs-lookup"><span data-stu-id="e198c-105">Requester errors produced using the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
-   <span data-ttu-id="e198c-106">Ошибки модуля записи, возникшие при использовании класса [**квссвритер**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , включая переопределяющие методы</span><span class="sxs-lookup"><span data-stu-id="e198c-106">Writer errors produced in using the [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class, including overriding methods</span></span>
-   <span data-ttu-id="e198c-107">Ошибки, сформированные поставщиком по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e198c-107">Default-provider-generated errors</span></span>
-   <span data-ttu-id="e198c-108">Ошибки службы VSS, созданные при координации действий поставщика, модуля записи и инициатора запроса (например, создание событий).</span><span class="sxs-lookup"><span data-stu-id="e198c-108">VSS service errors generated in coordinating provider, writer, and requester activity (such as the generation of events)</span></span>

<span data-ttu-id="e198c-109">Эти ошибки могут быть вызваны несколькими причинами, включая ошибку программирования в коде сторонних разработчиков или ошибки конфигурации, связанные с VSS.</span><span class="sxs-lookup"><span data-stu-id="e198c-109">These errors might have a number of causes, including a programming error in third-party code or VSS-related configuration errors.</span></span>

<span data-ttu-id="e198c-110">Драйверы VSS и функциональные возможности более низкого уровня записывают ошибки в системный журнал.</span><span class="sxs-lookup"><span data-stu-id="e198c-110">VSS drivers and lower-level implementation functionality write errors to the System Log.</span></span> <span data-ttu-id="e198c-111">Сторонние программы (инициатор запроса, поставщик, модуль записи) могут выбрать журнал приложения, системный журнал или и то, и другое, чтобы записать записи журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="e198c-111">Third-party software (requester, provider, writer) can choose the Application Log, the System Log, or both, to write error log entries.</span></span>

<span data-ttu-id="e198c-112">Рекомендуется, чтобы приложения высокого уровня (например, код пользовательского режима) использовали журнал приложений.</span><span class="sxs-lookup"><span data-stu-id="e198c-112">It is recommended that high-level applications (such as user-mode code) use the Application Log.</span></span> <span data-ttu-id="e198c-113">Для приложений более низкого уровня, таких как аппаратные интерфейсы и драйверы, следует использовать системный журнал.</span><span class="sxs-lookup"><span data-stu-id="e198c-113">Lower-level applications, such as hardware interfaces and drivers, should use the System Log.</span></span>

 

 



