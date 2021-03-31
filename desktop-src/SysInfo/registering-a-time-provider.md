---
description: Система загружает поставщик времени на основе сведений о конфигурации, хранящихся в реестре.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Регистрация поставщика времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910324"
---
# <a name="registering-a-time-provider"></a><span data-ttu-id="6418b-103">Регистрация поставщика времени</span><span class="sxs-lookup"><span data-stu-id="6418b-103">Registering a Time Provider</span></span>

<span data-ttu-id="6418b-104">Система загружает поставщик времени на основе сведений о конфигурации, хранящихся в реестре.</span><span class="sxs-lookup"><span data-stu-id="6418b-104">The system loads a time provider based on its configuration information stored in the registry.</span></span> <span data-ttu-id="6418b-105">Каждый поставщик времени должен создать следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="6418b-105">Each time provider should create the following registry key:</span></span>

<span data-ttu-id="6418b-106">**HKey \_ Локальный \_ компьютер \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **тимепровидерс** \\ *providerName*</span><span class="sxs-lookup"><span data-stu-id="6418b-106">**HKEY\_LOCAL\_MACHINE\\System**\\**CurrentControlSet**\\**Services**\\**W32Time**\\**TimeProviders**\\*ProviderName*</span></span>

<span data-ttu-id="6418b-107">В следующей таблице описаны значения, которые должны существовать в ключе каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="6418b-107">The following table describes the values that must exist in each provider's key.</span></span>



| <span data-ttu-id="6418b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6418b-108">Value</span></span>             | <span data-ttu-id="6418b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6418b-109">Description</span></span>                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6418b-110">**DllName**</span><span class="sxs-lookup"><span data-stu-id="6418b-110">**DllName**</span></span>       | <span data-ttu-id="6418b-111">Имя библиотеки DLL, содержащей поставщик.</span><span class="sxs-lookup"><span data-stu-id="6418b-111">The name of the DLL that contains the provider.</span></span> <span data-ttu-id="6418b-112">Это значение имеет тип **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="6418b-112">This value has the type **REG\_SZ**.</span></span>                                                                                                                                     |
| <span data-ttu-id="6418b-113">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="6418b-113">**Enabled**</span></span>       | <span data-ttu-id="6418b-114">Указывает, следует ли запускать поставщик.</span><span class="sxs-lookup"><span data-stu-id="6418b-114">Indicates whether the provider should be started.</span></span> <span data-ttu-id="6418b-115">Если это значение равно 1, то поставщик запускается.</span><span class="sxs-lookup"><span data-stu-id="6418b-115">If this value is 1, the provider is started.</span></span> <span data-ttu-id="6418b-116">В противном случае поставщик не запускается.</span><span class="sxs-lookup"><span data-stu-id="6418b-116">Otherwise, the provider is not started.</span></span> <span data-ttu-id="6418b-117">Это значение имеет тип **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6418b-117">This value has the type **REG\_DWORD**.</span></span>                                           |
| <span data-ttu-id="6418b-118">**InputProvider**</span><span class="sxs-lookup"><span data-stu-id="6418b-118">**InputProvider**</span></span> | <span data-ttu-id="6418b-119">Указывает, является ли поставщик входным поставщиком или поставщиком выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6418b-119">Indicates whether the provider is an input provider or an output provider.</span></span> <span data-ttu-id="6418b-120">Если это значение равно 1, поставщик является поставщиком входных данных.</span><span class="sxs-lookup"><span data-stu-id="6418b-120">If this value is 1, the provider is an input provider.</span></span> <span data-ttu-id="6418b-121">В противном случае поставщик является выходным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="6418b-121">Otherwise, the provider is an output provider.</span></span> <span data-ttu-id="6418b-122">Это значение имеет тип **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6418b-122">This value has the type **REG\_DWORD**.</span></span> |



 

<span data-ttu-id="6418b-123">Диспетчер поставщиков времени перечисляет ключи в ключе **тимепровидерс** и запускает каждый включенный поставщик.</span><span class="sxs-lookup"><span data-stu-id="6418b-123">The time provider manager enumerates the keys under the **TimeProviders** key and starts each enabled provider.</span></span> <span data-ttu-id="6418b-124">Поставщики запускаются при запуске системы и при каждом изменении параметров.</span><span class="sxs-lookup"><span data-stu-id="6418b-124">Providers are started at system startup and whenever there are parameter changes.</span></span>

<span data-ttu-id="6418b-125">Каждый поставщик времени может также хранить в реестре сведения о конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="6418b-125">Each time provider can also store application-specific configuration information in the registry.</span></span>

 

 



