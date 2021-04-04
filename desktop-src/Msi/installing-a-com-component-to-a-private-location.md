---
description: Чтобы заставить приложение COM-клиента всегда использовать одну и ту же копию COM-сервера, создайте пакет установки приложения, чтобы указать отношение изолированных компонентов между сервером и клиентом COM.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Установка COM-компонента в Закрытое расположение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898050"
---
# <a name="installing-a-com-component-to-a-private-location"></a><span data-ttu-id="c066a-103">Установка COM-компонента в Закрытое расположение</span><span class="sxs-lookup"><span data-stu-id="c066a-103">Installing a COM Component to a Private Location</span></span>

<span data-ttu-id="c066a-104">Чтобы заставить приложение COM-клиента всегда использовать одну и ту же копию COM-сервера, создайте пакет установки приложения, чтобы указать отношение [изолированных компонентов](isolated-components.md) между сервером и клиентом COM.</span><span class="sxs-lookup"><span data-stu-id="c066a-104">To force a COM-client application to always use the same copy of a COM-server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="c066a-105">При этом устанавливается частная копия компонента COM-Server в расположение, используемое только клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="c066a-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="c066a-106">При создании пакета выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c066a-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="c066a-107">Размещение DLL-сервера COM и клиента exe в отдельных компонентах.</span><span class="sxs-lookup"><span data-stu-id="c066a-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="c066a-108">Введите запись в [таблицу исолатедкомпонент](isolatedcomponent-table.md) с компонентом COM-Client в \_ столбце Component Shared и в клиентском приложении в \_ столбце приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="c066a-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="c066a-109">Включите [действие исолатекомпонентс](isolatecomponents-action.md) в таблицы последовательности.</span><span class="sxs-lookup"><span data-stu-id="c066a-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="c066a-110">Установите бит Мсидбкомпонентаттрибутесшареддллрефкаунт в записи [таблицы компонентов](component-table.md) для общего доступа к компоненту \_ .</span><span class="sxs-lookup"><span data-stu-id="c066a-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="c066a-111">Установщику требуется этот глобальный параметр refcount в общем расположении для защиты общих файлов и регистрации в случаях, когда используется совместно с другими технологиями установки.</span><span class="sxs-lookup"><span data-stu-id="c066a-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



