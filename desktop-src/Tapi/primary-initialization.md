---
description: Приложение TAPI должно вызывать операцию инициализации, которая предлагает ряд действий от TAPI и поставщиков услуг, которые настроили среду связи для приложения.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Основная инициализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684051"
---
# <a name="primary-initialization"></a><span data-ttu-id="a75d4-103">Основная инициализация</span><span class="sxs-lookup"><span data-stu-id="a75d4-103">Primary Initialization</span></span>

<span data-ttu-id="a75d4-104">Приложение TAPI должно вызывать операцию инициализации, которая предлагает ряд действий от TAPI и поставщиков услуг, которые настроили среду связи для приложения.</span><span class="sxs-lookup"><span data-stu-id="a75d4-104">A TAPI application must call an initialization operation, which prompts a series of actions from TAPI and the service providers that set up the communication environment for the application.</span></span>

-   <span data-ttu-id="a75d4-105">Инициализация является синхронной и не возвращает значение до завершения или сбоя операции.</span><span class="sxs-lookup"><span data-stu-id="a75d4-105">Initialization is synchronous and does not return until the operation is complete or has failed.</span></span>
-   <span data-ttu-id="a75d4-106">Если ТАПИСРВ еще не запущен, TAPI запускает его.</span><span class="sxs-lookup"><span data-stu-id="a75d4-106">If TAPISRV is not already running, TAPI starts it.</span></span>
-   <span data-ttu-id="a75d4-107">TAPI настраивает подключение к процессу ТАПИСРВ.</span><span class="sxs-lookup"><span data-stu-id="a75d4-107">TAPI sets up a connection to the TAPISRV process.</span></span>
-   <span data-ttu-id="a75d4-108">ТАПИСВР загружает поставщики служб, указанные в реестре, и предлагает им инициализировать устройства, которые они поддерживают.</span><span class="sxs-lookup"><span data-stu-id="a75d4-108">TAPISVR loads the service providers specified in the registry and prompts them to initialize the devices they support.</span></span>

<span data-ttu-id="a75d4-109">**Интерфейс TAPI 2. x:** Приложения выполняют инициализацию путем вызова [**линеинитиализикс**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="a75d4-109">**TAPI 2.x:** Applications perform initialization by calling [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="a75d4-110">**Интерфейс TAPI 3. x:** Приложения вызывают [**иттапи:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span><span class="sxs-lookup"><span data-stu-id="a75d4-110">**TAPI 3.x:** Applications call [**ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span></span>

 

 
