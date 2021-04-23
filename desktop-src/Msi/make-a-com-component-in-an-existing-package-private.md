---
description: Администратор может заставить приложение COM-клиента всегда использовать одну и ту же копию COM-сервера в существующем пакете&\# 8212; не влияя на другие приложения&\# 8212; путем указания отношения изолированных компонентов между сервером и клиентом COM.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Сделать компонент COM в существующем пакете частным
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674159"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a><span data-ttu-id="513aa-103">Сделать компонент COM в существующем пакете частным</span><span class="sxs-lookup"><span data-stu-id="513aa-103">Make a COM Component in an Existing Package Private</span></span>

<span data-ttu-id="513aa-104">Администратор может принудительно заставить приложение COM-клиента всегда использовать одну и ту же копию COM-сервера в существующем пакете, не влияя на другие приложения — путем указания отношения [изолированных компонентов](isolated-components.md) между сервером и клиентом COM.</span><span class="sxs-lookup"><span data-stu-id="513aa-104">An administrator can force a COM-client application to always use the same copy of a COM-server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="513aa-105">При этом устанавливается частная копия компонента COM-Server в расположение, используемое только клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="513aa-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="513aa-106">Администратору необходимо использовать преобразования или средство разработки пакетов для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="513aa-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="513aa-107">Размещение DLL-сервера COM и клиента exe в отдельных компонентах.</span><span class="sxs-lookup"><span data-stu-id="513aa-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="513aa-108">Введите запись в [таблицу исолатедкомпонент](isolatedcomponent-table.md) с компонентом COM-Client в \_ столбце Component Shared и в клиентском приложении в \_ столбце приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="513aa-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="513aa-109">Включите [действие исолатекомпонентс](isolatecomponents-action.md) в таблицы последовательности.</span><span class="sxs-lookup"><span data-stu-id="513aa-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="513aa-110">Установите бит **мсидбкомпонентаттрибутесшареддллрефкаунт** в записи [таблицы компонентов](component-table.md) для общего доступа к компоненту \_ .</span><span class="sxs-lookup"><span data-stu-id="513aa-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="513aa-111">Установщику требуется этот глобальный параметр refcount в общем расположении для защиты общих файлов и регистрации в случаях, когда используется совместно с другими технологиями установки.</span><span class="sxs-lookup"><span data-stu-id="513aa-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



