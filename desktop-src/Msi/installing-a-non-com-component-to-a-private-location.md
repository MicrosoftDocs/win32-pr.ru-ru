---
description: Чтобы заставить клиентское приложение всегда использовать ту же копию сервера, который не является COM-сервером, создайте пакет установки приложения, чтобы указать связь между сервером и клиентом.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Установка компонента, не являющегося компонентом COM, в Закрытое расположение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913496"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a><span data-ttu-id="93306-103">Установка компонента, не являющегося компонентом COM, в Закрытое расположение</span><span class="sxs-lookup"><span data-stu-id="93306-103">Installing a non-COM Component to a Private Location</span></span>

<span data-ttu-id="93306-104">Чтобы заставить клиентское приложение всегда использовать ту же копию сервера, который не является COM-сервером, создайте пакет установки приложения, чтобы [указать связь между](isolated-components.md) сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="93306-104">To force a client application to always use the same copy of a non-COM server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="93306-105">При этом устанавливается частная копия компонента сервера в расположение, используемое только клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="93306-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="93306-106">При создании пакета выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="93306-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="93306-107">Разместите библиотеки DLL сервера и exe-клиент в отдельных компонентах.</span><span class="sxs-lookup"><span data-stu-id="93306-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="93306-108">Введите запись в [таблицу исолатедкомпонент](isolatedcomponent-table.md) с клиентским компонентом в \_ столбце компонент общий и клиентское приложение в \_ столбце приложение компонента.</span><span class="sxs-lookup"><span data-stu-id="93306-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="93306-109">Включите [действие исолатекомпонентс](isolatecomponents-action.md) в таблицы последовательности.</span><span class="sxs-lookup"><span data-stu-id="93306-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="93306-110">Установите бит Мсидбкомпонентаттрибутесшареддллрефкаунт в записи [таблицы компонентов](component-table.md) для общего доступа к компоненту \_ .</span><span class="sxs-lookup"><span data-stu-id="93306-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="93306-111">Установщику требуется этот глобальный параметр refcount в общем расположении для защиты общих файлов и регистрации в случаях, когда используется совместно с другими технологиями установки.</span><span class="sxs-lookup"><span data-stu-id="93306-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>
-   <span data-ttu-id="93306-112">Избегайте создания общего зарегистрированного пути для компонентов.</span><span class="sxs-lookup"><span data-stu-id="93306-112">Avoid authoring a shared registered path across components.</span></span>

 

 



