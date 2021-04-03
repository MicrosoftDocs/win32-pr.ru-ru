---
description: Служба теневого копирования томов (VSS) предоставляет системную инфраструктуру для запуска приложений VSS в системах на базе Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: служба теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809851"
---
# <a name="the-volume-shadow-copy-service"></a><span data-ttu-id="02337-103">служба теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="02337-103">The Volume Shadow Copy Service</span></span>

<span data-ttu-id="02337-104">Служба теневого копирования томов (VSS) предоставляет системную инфраструктуру для запуска приложений VSS в системах на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="02337-104">The Volume Shadow Copy Service (VSS) provides the system infrastructure for running VSS applications on Windows-based systems.</span></span>

<span data-ttu-id="02337-105">Хотя служба VSS в значительной степени прозрачна для пользователей и разработчиков, она выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="02337-105">Though largely transparent to user and developer, VSS does the following:</span></span>

-   <span data-ttu-id="02337-106">Координирует действия поставщиков, модулей записи и инициаторов запроса при создании и использовании теневых копий</span><span class="sxs-lookup"><span data-stu-id="02337-106">Coordinates activities of providers, writers, and requesters in the creation and use of shadow copies</span></span>
-   <span data-ttu-id="02337-107">Предоставление поставщика системы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="02337-107">Furnishes the default system provider</span></span>
-   <span data-ttu-id="02337-108">Реализует низкоуровневые функции драйверов, необходимые для работы любого поставщика</span><span class="sxs-lookup"><span data-stu-id="02337-108">Implements low-level driver functionality necessary for any provider to work</span></span>

<span data-ttu-id="02337-109">Служба VSS запускается по запросу, поэтому для успешного выполнения операций VSS эта служба должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="02337-109">The VSS service starts on demand; therefore, for VSS operations to be successful, this service must be enabled.</span></span>

 

 



