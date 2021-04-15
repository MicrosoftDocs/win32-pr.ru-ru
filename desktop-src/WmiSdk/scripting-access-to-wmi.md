---
description: Скрипты могут обращаться ко всем классам WMI для аппаратных и программных объектов.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Создание сценариев для доступа к инструментарию WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263814"
---
# <a name="scripting-access-to-wmi"></a><span data-ttu-id="36d39-103">Создание сценариев для доступа к инструментарию WMI</span><span class="sxs-lookup"><span data-stu-id="36d39-103">Scripting Access to WMI</span></span>

<span data-ttu-id="36d39-104">Скрипты могут обращаться ко всем классам WMI для аппаратных и программных объектов.</span><span class="sxs-lookup"><span data-stu-id="36d39-104">Scripts can access all WMI classes for hardware and software objects.</span></span> <span data-ttu-id="36d39-105">Сценарии сервера сценариев Windows (WSH) могут выполнять операции с объектами файловой системы, управлять сетевыми принтерами или изменять переменные среды.</span><span class="sxs-lookup"><span data-stu-id="36d39-105">Windows Script Host (WSH) scripts can perform operations on file system objects, manipulate network printers, or change environment variables.</span></span> <span data-ttu-id="36d39-106">Вы можете найти разнообразные задачи администратора и краткое руководство по их выполнению в инструментарии WMI в [задачах WMI для сценариев и приложений](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="36d39-106">You can find a variety of administrator tasks and brief guidance on how to accomplish them in WMI at [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="36d39-107">Дополнительные сведения и примеры см. в [репозитории сценариев](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)TechNet скриптцентер.</span><span class="sxs-lookup"><span data-stu-id="36d39-107">For more information and examples, see the TechNet ScriptCenter [Script Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).</span></span>

<span data-ttu-id="36d39-108">Если вы не знакомы со сценариями или с помощью сценариев для WMI, см. раздел [Начало работы](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx)TechNet скриптцентер.</span><span class="sxs-lookup"><span data-stu-id="36d39-108">If you are new to scripting or to WMI-specific scripting, see the TechNet ScriptCenter section [Getting Started](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span></span>

<span data-ttu-id="36d39-109">С помощью [API скриптов для WMI](scripting-api-for-wmi.md)можно разрабатывать быстрые, простые сценарии или сложные приложения.</span><span class="sxs-lookup"><span data-stu-id="36d39-109">With the [Scripting API for WMI](scripting-api-for-wmi.md), you can develop quick, simple scripts or complex applications.</span></span> <span data-ttu-id="36d39-110">Создание сценариев предоставляет такую же возможность для получения информации или настройки большинства объектов на предприятии, как и с помощью приложения C++ или C#.</span><span class="sxs-lookup"><span data-stu-id="36d39-110">Scripting gives you the same capability of getting information or of configuring most objects in an enterprise as you would have through a C++ or C# application.</span></span> <span data-ttu-id="36d39-111">Дополнительные сведения см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="36d39-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="36d39-112">Невозможно создать [*поставщик WMI*](gloss-p.md) в скрипте.</span><span class="sxs-lookup"><span data-stu-id="36d39-112">You cannot write a [*WMI provider*](gloss-p.md) in script.</span></span> <span data-ttu-id="36d39-113">Дополнительные сведения см. [в разделе Предоставление данных инструментарию WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="36d39-113">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="36d39-114">Сценарии WMI могут быть написаны на любом языке сценариев, который может взаимодействовать с объектами ActiveX.</span><span class="sxs-lookup"><span data-stu-id="36d39-114">WMI scripts can be written in any scripting language that can interact with ActiveX objects.</span></span>

<span data-ttu-id="36d39-115">Windows PowerShell предоставляет простую среду для администрирования WMI и создания сценариев.</span><span class="sxs-lookup"><span data-stu-id="36d39-115">Windows PowerShell provides a simple environment for WMI administration and scripting.</span></span> <span data-ttu-id="36d39-116">Дополнительные сведения об PowerShell см. [в разделе Начало работы with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="36d39-116">For more information about PowerShell, see [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span>

<span data-ttu-id="36d39-117">Сценарии интерфейсов служб Active Directory (ADSI) предоставляют доступ к объектам домен Active Directory служб (AD DS).</span><span class="sxs-lookup"><span data-stu-id="36d39-117">Active Directory Service Interfaces (ADSI) scripts provides access to Active Directory Domain Services (AD DS) objects.</span></span> <span data-ttu-id="36d39-118">Скрипты WSH и ADSI обращаются к объектам и разрешают процедуры, недоступные через пакетные файлы.</span><span class="sxs-lookup"><span data-stu-id="36d39-118">Both WSH and ADSI scripts access objects and allow procedures not available through batch files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36d39-119">См. также</span><span class="sxs-lookup"><span data-stu-id="36d39-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36d39-120">Сведения об инструментарии WMI</span><span class="sxs-lookup"><span data-stu-id="36d39-120">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="36d39-121">API сценариев для инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="36d39-121">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
