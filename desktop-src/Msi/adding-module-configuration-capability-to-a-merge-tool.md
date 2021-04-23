---
description: Разработчики установщик Windows могут создавать средства, позволяющие конечным пользователям использовать настраиваемые модули слияния.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Добавление функции конфигурации модуля в средство слияния
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813361"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a><span data-ttu-id="08da9-103">Добавление функции конфигурации модуля в средство слияния</span><span class="sxs-lookup"><span data-stu-id="08da9-103">Adding Module Configuration Capability to a Merge Tool</span></span>

<span data-ttu-id="08da9-104">Чтобы разрешить конечным пользователям использовать настраиваемые модули слияния, можно создать средства слияния и настройки для выполнения следующих действий.</span><span class="sxs-lookup"><span data-stu-id="08da9-104">To enable end users to use configurable merge modules, you can author merge and configuration tools to do the following:</span></span>

-   <span data-ttu-id="08da9-105">Средства слияния должны вызывать функции в Mergemod.dll версии 2,0 для слияния модуля.</span><span class="sxs-lookup"><span data-stu-id="08da9-105">Merge tools should call the functions in Mergemod.dll version 2.0 to merge the module.</span></span> <span data-ttu-id="08da9-106">Более ранние версии Mergemod.dll нельзя использовать для настройки модулей слияния.</span><span class="sxs-lookup"><span data-stu-id="08da9-106">Earlier versions of Mergemod.dll cannot be used to configure merge modules.</span></span>
-   <span data-ttu-id="08da9-107">Приложения конфигурации клиента должны взаимодействовать с пользователем модуля слияния, чтобы получать выбор пользователей для настраиваемых элементов.</span><span class="sxs-lookup"><span data-stu-id="08da9-107">Client configuration applications should interact with the merge module user to collect the user selections for configurable items.</span></span>
-   <span data-ttu-id="08da9-108">Средства слияния должны предоставлять сведения о конфигурации, созданные в модуле слияния, в клиентское приложение, чтобы клиент мог использовать эти сведения для запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="08da9-108">Merge tools should expose configuration information authored into the merge module to the client application so that the client can use this information to query the user.</span></span>
-   <span data-ttu-id="08da9-109">Когда средство слияния встречает настраиваемый элемент во время слияния, оно должно вызывать средство настройки клиента для получения сведений о настройке, полученных от пользователя.</span><span class="sxs-lookup"><span data-stu-id="08da9-109">When a merge tool encounters a configurable item during a merge, it should call the client configuration tool for customization information obtained from the user.</span></span> <span data-ttu-id="08da9-110">Средство слияния должно внести указанные изменения в модуль слияния.</span><span class="sxs-lookup"><span data-stu-id="08da9-110">The merge tool should make the specified changes to the merge module.</span></span>
-   <span data-ttu-id="08da9-111">Приложения конфигурации должны предоставить пользователю возможность выбирать настраиваемые элементы, но все возможные варианты выбора не нужно раскрывать пользователю.</span><span class="sxs-lookup"><span data-stu-id="08da9-111">Configuration applications should enable the user to provide choices for configurable items, but all the possible choices do not need to be revealed to the user.</span></span> <span data-ttu-id="08da9-112">Средство слияния может использовать значения по умолчанию для настраиваемых элементов, которые не выбираются пользователем.</span><span class="sxs-lookup"><span data-stu-id="08da9-112">The merge tool can use default values for configurable items that the user does not select.</span></span>
-   <span data-ttu-id="08da9-113">Если пользователь не предоставляет сведения о настройке, средства слияния должны использовать значения конфигурации по умолчанию, указанные в модуле слияния.</span><span class="sxs-lookup"><span data-stu-id="08da9-113">If a user does not provide customization information, merge tools should use the default configuration values that are specified in the merge module.</span></span>
-   <span data-ttu-id="08da9-114">После того как пользователь выдаст специальные настройки, средство слияния вызывает Mergemod.dll для выполнения слияния.</span><span class="sxs-lookup"><span data-stu-id="08da9-114">After a user gives the configuration tool specific selections, the merge tool calls Mergemod.dll to perform the merge.</span></span>

 

 



