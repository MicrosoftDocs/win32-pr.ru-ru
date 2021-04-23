---
title: Настройка восстановления системы
description: Средство восстановления системы использует инструментарий управления Windows (WMI) (WMI) для предоставления сценариям возможности настройки и использования его функциональных возможностей. Он предоставляет два класса, SystemRestore и Системрестореконфиг, в корневом \\ пространстве имен по умолчанию.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413201"
---
# <a name="configuring-system-restore"></a><span data-ttu-id="ffc26-104">Настройка восстановления системы</span><span class="sxs-lookup"><span data-stu-id="ffc26-104">Configuring System Restore</span></span>

<span data-ttu-id="ffc26-105">Средство восстановления системы использует [инструментарий управления Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page) (WMI) для предоставления сценариям возможности настройки и использования его функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="ffc26-105">System Restore uses [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to provide a scriptable way of configuring and using its functionality.</span></span> <span data-ttu-id="ffc26-106">Он предоставляет два класса, [**SystemRestore**](systemrestore.md) и [**системрестореконфиг**](systemrestoreconfig.md), в корневом \\ пространстве имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ffc26-106">It exposes two classes, [**SystemRestore**](systemrestore.md) and [**SystemRestoreConfig**](systemrestoreconfig.md), in the root\\default namespace.</span></span>

<span data-ttu-id="ffc26-107">Класс [**SystemRestore**](systemrestore.md) предоставляет методы для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="ffc26-107">The [**SystemRestore**](systemrestore.md) class provides methods for the following tasks:</span></span>

-   <span data-ttu-id="ffc26-108">Отключение и включение мониторинга</span><span class="sxs-lookup"><span data-stu-id="ffc26-108">Disabling and enabling monitoring</span></span>
-   <span data-ttu-id="ffc26-109">Перечисление доступных точек восстановления</span><span class="sxs-lookup"><span data-stu-id="ffc26-109">Listing available restore points</span></span>
-   <span data-ttu-id="ffc26-110">Запуск восстановления в локальной системе</span><span class="sxs-lookup"><span data-stu-id="ffc26-110">Initiating a restore on the local system</span></span>
-   <span data-ttu-id="ffc26-111">Получение состояния последнего восстановления системы</span><span class="sxs-lookup"><span data-stu-id="ffc26-111">Retrieving the status of the last system restore</span></span>

<span data-ttu-id="ffc26-112">Класс [**системрестореконфиг**](systemrestoreconfig.md) предоставляет свойства для управления частотой создания точек восстановления по расписанию и объемом дискового пространства, занятого восстановлением системы на каждом диске.</span><span class="sxs-lookup"><span data-stu-id="ffc26-112">The [**SystemRestoreConfig**](systemrestoreconfig.md) class provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed by System Restore on each drive.</span></span>

<span data-ttu-id="ffc26-113">Доступ к обоим классам можно получить удаленно с помощью стандартных методов WMI.</span><span class="sxs-lookup"><span data-stu-id="ffc26-113">Both classes can be accessed remotely using standard WMI techniques.</span></span> <span data-ttu-id="ffc26-114">Полное описание инструментария WMI см. в разделе [инструментарий управления Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="ffc26-114">For a complete description of WMI, see [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

 

 