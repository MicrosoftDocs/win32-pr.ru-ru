---
title: Создание частного пула датчиков
description: Как использовать API биометрическая платформа Windows для создания частного пула датчиков.
ms.assetid: 79944E30-A3D4-411D-A551-3B309DEA6FEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eda88f8a9bd0befcbf5527e52d572ec7ca55ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411247"
---
# <a name="creating-a-private-sensor-pool"></a><span data-ttu-id="5d1b0-103">Создание частного пула датчиков</span><span class="sxs-lookup"><span data-stu-id="5d1b0-103">Creating a Private Sensor Pool</span></span>

<span data-ttu-id="5d1b0-104">Частный пул датчиков — это набор биометрических блоков, зарезервированных для монопольного использования клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-104">A private sensor pool is a collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="5d1b0-105">Частные пулы поддерживают собственные методы проверки подлинности и позволяют клиентскому приложению получать доступ к биометрической единице с помощью определяемых поставщиком команд управления.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-105">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span>

<span data-ttu-id="5d1b0-106">В следующих разделах содержатся примеры кода, демонстрирующие создание частного пула датчиков.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-106">The following topics contain code examples that show how to create a private sensor pool.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5d1b0-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5d1b0-107">In this section</span></span>



| <span data-ttu-id="5d1b0-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="5d1b0-108">Topic</span></span>                                                                         | <span data-ttu-id="5d1b0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5d1b0-109">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d1b0-110">Пулы датчиков</span><span class="sxs-lookup"><span data-stu-id="5d1b0-110">Sensor Pools</span></span>](sensor-pools.md)<br/>                                   | <span data-ttu-id="5d1b0-111">Описывает три возможных пула датчиков: системные, частные и неназначенные.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-111">Describes three possible sensor pools: system, private, and unassigned.</span></span><br/>                   |
| [<span data-ttu-id="5d1b0-112">Настройка частного пула</span><span class="sxs-lookup"><span data-stu-id="5d1b0-112">Private Pool Setup</span></span>](private-pool-setup.md)<br/>                       | <span data-ttu-id="5d1b0-113">Содержит проект консоли программы установки.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-113">Contains the setup console project.</span></span><br/>                                                       |
| [<span data-ttu-id="5d1b0-114">Удостоверение частного пула</span><span class="sxs-lookup"><span data-stu-id="5d1b0-114">Private Pool Identity</span></span>](private-pool-identity.md)<br/>                 | <span data-ttu-id="5d1b0-115">Содержит проект консоли идентификации.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-115">Contains the identification console project.</span></span><br/>                                              |
| [<span data-ttu-id="5d1b0-116">Регистрация частного пула</span><span class="sxs-lookup"><span data-stu-id="5d1b0-116">Private Pool Enrollment</span></span>](private-pool-enrollment.md)<br/>             | <span data-ttu-id="5d1b0-117">Содержит проект консоли регистрации.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-117">Contains the enrollment console project.</span></span><br/>                                                  |
| [<span data-ttu-id="5d1b0-118">Вспомогательные функции частного пула</span><span class="sxs-lookup"><span data-stu-id="5d1b0-118">Private Pool Helper Functions</span></span>](private-pool-helper-functions.md)<br/> | <span data-ttu-id="5d1b0-119">Содержит вспомогательные функции для проектов консоли установки, идентификации и регистрации.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-119">Contains helper functions for the setup, identification, and enrollment console projects.</span></span><br/> |
| [<span data-ttu-id="5d1b0-120">Создание клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="5d1b0-120">Create client applications</span></span>](creating-client-applications.md)<br/>     | <span data-ttu-id="5d1b0-121">Использование API биометрическая платформа Windows для создания клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="5d1b0-121">How to use the Windows Biometric Framework API to create client applications.</span></span><br/>             |



 

 

 





