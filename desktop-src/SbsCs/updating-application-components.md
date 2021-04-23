---
description: Параллельные закрытые сборки можно использовать для создания компонентов, которые можно легко обновлять без обновления приложения размещения.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Обновление компонентов приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991033"
---
# <a name="updating-application-components"></a><span data-ttu-id="f5723-103">Обновление компонентов приложения</span><span class="sxs-lookup"><span data-stu-id="f5723-103">Updating Application Components</span></span>

<span data-ttu-id="f5723-104">Параллельные закрытые сборки можно использовать для создания компонентов, которые можно легко обновлять без обновления приложения размещения.</span><span class="sxs-lookup"><span data-stu-id="f5723-104">Side-by-side private assemblies can be used to create components that can be easily updated without also updating the hosting application.</span></span> <span data-ttu-id="f5723-105">Это позволяет обновленной службе устанавливать обновленные компоненты приложения, перезапускать приложение и использовать эти изменения в приложении.</span><span class="sxs-lookup"><span data-stu-id="f5723-105">This allows an updating service to install the application's updated components, restart the application, and have the application use the changes.</span></span> <span data-ttu-id="f5723-106">При использовании манифестов приложений функциональность компонентов, размещенных в приложении, может быть обновлена без необходимости изменения кода ведущего приложения.</span><span class="sxs-lookup"><span data-stu-id="f5723-106">When using application manifests, the functionality of components hosted by an application can be updated without having to change the hosting application's code.</span></span>

<span data-ttu-id="f5723-107">Этот метод можно использовать для обновления версии ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="f5723-107">This method can be used to update the version of an application's resources.</span></span> <span data-ttu-id="f5723-108">Например, если приложение содержит сборку, манифест приложения может указать зависимость от этой сборки.</span><span class="sxs-lookup"><span data-stu-id="f5723-108">For example, if an application contains an assembly, the application's manifest can specify a dependency on this assembly.</span></span> <span data-ttu-id="f5723-109">Приложение может получить сборку, вызвав [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) для поиска и загрузки необходимых файлов.</span><span class="sxs-lookup"><span data-stu-id="f5723-109">The application can get the assembly by calling [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) to find and load the files it requires.</span></span> <span data-ttu-id="f5723-110">Для этого необходимо, чтобы для сборки выводились новые биты, которые могут существовать параллельно с более ранней версией сборки.</span><span class="sxs-lookup"><span data-stu-id="f5723-110">An updater simply has to bring down the newest bits for the assembly, which can exist side-by-side with an earlier version of the assembly.</span></span>

 

 
