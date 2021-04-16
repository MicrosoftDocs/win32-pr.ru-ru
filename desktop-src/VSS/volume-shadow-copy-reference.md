---
description: Служба теневого копирования томов (VSS) — это набор API-интерфейсов COM и C++, которые позволяют выполнять резервное копирование томов, когда приложения в системе (называемые модулями записи) продолжают записывать данные в тома.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Справочник по API теневого копирования томов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541751"
---
# <a name="volume-shadow-copy-api-reference"></a><span data-ttu-id="cf63d-103">Справочник по API теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="cf63d-103">Volume Shadow Copy API Reference</span></span>

<span data-ttu-id="cf63d-104">Служба теневого копирования томов (VSS) — это набор API-интерфейсов COM и C++, которые позволяют выполнять резервное копирование томов, когда приложения в системе (называемые модулями записи) продолжают записывать данные в тома.</span><span class="sxs-lookup"><span data-stu-id="cf63d-104">The Volume Shadow Copy Service (VSS) is a set of COM and C++ APIs that enable volume backups to be performed while applications on the system (called writers) continue to write to the volumes.</span></span>

<span data-ttu-id="cf63d-105">VSS поддерживает эти резервные копии посредством создания теневых копий, дубликата исходного тома в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="cf63d-105">VSS supports these backups through the creation of shadow copies, a duplicate of the original volume at a given point in time.</span></span>

<span data-ttu-id="cf63d-106">Сторонние разработчики могут использовать API VSS для создания инициаторов запроса (например, приложения резервного копирования) для создания и управления теневыми копиями.</span><span class="sxs-lookup"><span data-stu-id="cf63d-106">Third-party developers can use the VSS API to create requesters (such as a backup application) to create and manage shadow copies.</span></span>

<span data-ttu-id="cf63d-107">Фактическая работа по созданию и представляя теневые копии осуществляется приложениями уровня системы, известными как поставщики.</span><span class="sxs-lookup"><span data-stu-id="cf63d-107">The actual work of creating and representing shadow copies is conducted by system-level applications known as providers.</span></span>

<span data-ttu-id="cf63d-108">Разработчики также могут использовать API для создания модулей записи: приложений, поддерживающих VSS, которые могут координировать операции ввода-вывода с созданием и управлением теневыми копиями.</span><span class="sxs-lookup"><span data-stu-id="cf63d-108">Developers can also use the API to construct writers: VSS-aware applications that are able to coordinate I/O operations with the creation and manipulation of shadow copies.</span></span>

-   [<span data-ttu-id="cf63d-109">Классы API теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="cf63d-109">Volume Shadow Copy API Classes</span></span>](volume-shadow-copy-api-classes.md)
-   [<span data-ttu-id="cf63d-110">Типы данных API теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="cf63d-110">Volume Shadow Copy API Data Types</span></span>](volume-shadow-copy-api-data-types.md)
-   [<span data-ttu-id="cf63d-111">Перечисления API теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="cf63d-111">Volume Shadow Copy API Enumerations</span></span>](volume-shadow-copy-api-enumeration-types.md)
-   [<span data-ttu-id="cf63d-112">Функции API теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="cf63d-112">Volume Shadow Copy API Functions</span></span>](volume-shadow-copy-api-functions.md)
-   [<span data-ttu-id="cf63d-113">Интерфейсы API теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="cf63d-113">Volume Shadow Copy API Interfaces</span></span>](volume-shadow-copy-api-interfaces.md)
-   [<span data-ttu-id="cf63d-114">Структуры API теневого копирования томов</span><span class="sxs-lookup"><span data-stu-id="cf63d-114">Volume Shadow Copy API Structures</span></span>](volume-shadow-copy-api-structures.md)
-   [<span data-ttu-id="cf63d-115">Глоссарий по теневым копиям томов</span><span class="sxs-lookup"><span data-stu-id="cf63d-115">Volume Shadow Copy Glossary</span></span>](volume-shadow-copy-glossary.md)

<span data-ttu-id="cf63d-116">Дополнительные сведения о создании запрашивающих и модулей записи см. [в разделе использование служба теневого копирования томов](using-the-volume-shadow-copy-service.md).</span><span class="sxs-lookup"><span data-stu-id="cf63d-116">For more information on writing requesters and writers, see [Using the Volume Shadow Copy Service](using-the-volume-shadow-copy-service.md).</span></span>

 

 



