---
description: Существует два метода, с помощью которых приложение размещения может искать параллельные сборки.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Поиск сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647627"
---
# <a name="searching-for-assemblies"></a><span data-ttu-id="de558-103">Поиск сборок</span><span class="sxs-lookup"><span data-stu-id="de558-103">Searching for Assemblies</span></span>

<span data-ttu-id="de558-104">Существует два метода, с помощью которых приложение размещения может искать параллельные сборки.</span><span class="sxs-lookup"><span data-stu-id="de558-104">There are two methods by which a hosting application can search for side-by-side assemblies.</span></span>

<span data-ttu-id="de558-105">Размещенные модули могут зарегистрироваться в ведущем приложении, расширяя некоторые общие сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="de558-105">Hosted modules can register themselves with the hosting application by extending some shared configuration information.</span></span> <span data-ttu-id="de558-106">Затем приложение может использовать эти сведения о конфигурации для загрузки сборок, необходимых для новой функциональности.</span><span class="sxs-lookup"><span data-stu-id="de558-106">The application can then use this configuration information to load the assemblies required for the new functionality.</span></span> <span data-ttu-id="de558-107">Это можно сделать, вызвав [**креатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) для манифестов, указанных в регистрационных данных, а затем вызвав [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы попасть в новый модуль.</span><span class="sxs-lookup"><span data-stu-id="de558-107">This could be done by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) on manifests specified in the registration data, followed by calling [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get into the new module.</span></span> <span data-ttu-id="de558-108">Обратите внимание, что при использовании этого метода новые компоненты должны обновить некоторое состояние общего приложения, чтобы указать их присутствие.</span><span class="sxs-lookup"><span data-stu-id="de558-108">Note that with this method, the new components have to update some shared application state to indicate their presence.</span></span>

<span data-ttu-id="de558-109">Приложение размещения может активно искать сборки при запуске с помощью [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) и [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) , чтобы искать библиотеки DLL или манифесты в указанном расположении, а затем использовать [**креатеакткткс**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) для доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="de558-109">The hosting application can actively search for the assemblies on startup using [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) to look for DLLs or manifests in a specified location, and then use [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) to access the information.</span></span> <span data-ttu-id="de558-110">Для этого метода не требуется регистрация компонента.</span><span class="sxs-lookup"><span data-stu-id="de558-110">This method requires no registration of the component.</span></span>

 

 
