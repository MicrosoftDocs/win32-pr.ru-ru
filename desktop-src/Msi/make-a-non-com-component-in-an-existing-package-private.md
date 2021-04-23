---
description: Администратор может заставить клиентское приложение всегда использовать одну и ту же копию сервера, отличного от COM, в существующем пакете&\# 8212; не влияя на другие приложения&\# 8212; путем указания отношения между сервером и клиентом.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Создание частного компонента, не являющегося компонентом COM, в существующем пакете
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673372"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a><span data-ttu-id="24ef3-103">Создание частного компонента, не являющегося компонентом COM, в существующем пакете</span><span class="sxs-lookup"><span data-stu-id="24ef3-103">Make a non-COM Component in an Existing Package Private</span></span>

<span data-ttu-id="24ef3-104">Администратор может принудительно заставить клиентское приложение всегда использовать одну и ту же копию сервера, отличного от COM, в существующем пакете, не затрагивая другие приложения — путем [указания отношения между](isolated-components.md) сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="24ef3-104">An administrator can force a client application to always use the same copy of a non-COM server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="24ef3-105">При этом устанавливается частная копия компонента сервера в расположение, используемое только клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="24ef3-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="24ef3-106">Администратору необходимо использовать преобразования или средство разработки пакетов для следующих задач:</span><span class="sxs-lookup"><span data-stu-id="24ef3-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="24ef3-107">Разместите библиотеки DLL сервера и exe-клиент в отдельных компонентах.</span><span class="sxs-lookup"><span data-stu-id="24ef3-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="24ef3-108">Введите запись в [таблицу исолатедкомпонент](isolatedcomponent-table.md) с клиентским компонентом в \_ столбце компонент общий и клиентское приложение в \_ столбце приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="24ef3-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="24ef3-109">Включите [действие исолатекомпонентс](isolatecomponents-action.md) в таблицы последовательности.</span><span class="sxs-lookup"><span data-stu-id="24ef3-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="24ef3-110">Установите бит **мсидбкомпонентаттрибутесшареддллрефкаунт** в записи [таблицы компонентов](component-table.md) для общего доступа к компоненту \_ .</span><span class="sxs-lookup"><span data-stu-id="24ef3-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="24ef3-111">Установщику требуется этот глобальный параметр refcount в общем расположении для защиты общих файлов и регистрации в случаях, когда используется совместно с другими технологиями установки.</span><span class="sxs-lookup"><span data-stu-id="24ef3-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



