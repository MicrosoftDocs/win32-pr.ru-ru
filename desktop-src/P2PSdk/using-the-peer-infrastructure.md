---
description: В этом разделе обсуждаются практические рекомендации по разработке приложений с помощью одноранговой инфраструктуры, а также конкретные методы более эффективного использования API.
ms.assetid: 5ce0f8a6-ab61-4091-809f-2e4a990f4886
title: Использование одноранговой инфраструктуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6cbcaab4044aa1f0b3e3ca017c824bf304f634
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663276"
---
# <a name="using-the-peer-infrastructure"></a><span data-ttu-id="9af05-103">Использование одноранговой инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="9af05-103">Using the Peer Infrastructure</span></span>

<span data-ttu-id="9af05-104">В этом разделе обсуждаются практические рекомендации по разработке приложений с помощью одноранговой инфраструктуры, а также конкретные методы более эффективного использования API.</span><span class="sxs-lookup"><span data-stu-id="9af05-104">This section discusses practical considerations for developing applications with the Peer infrastructure, as well as specific techniques to use the APIs more efficiently.</span></span>

<span data-ttu-id="9af05-105">В следующих разделах приведены решения распространенных задач по разработке приложений с помощью одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9af05-105">The following topics identify solutions to common tasks for developing applications using the Peer Infrastructure.</span></span>



| <span data-ttu-id="9af05-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="9af05-106">Topic</span></span>                                                                                                        | <span data-ttu-id="9af05-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9af05-107">Description</span></span>                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9af05-108">Установка одноранговой инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="9af05-108">Installing the Peer Infrastructure</span></span>](installing-the-peer-infrastructure.md)                                 | <span data-ttu-id="9af05-109">Определяет, как установить одноранговую инфраструктуру в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9af05-109">Identifies how to install the Peer Infrastructure in Windows XP.</span></span>                                                        |
| [<span data-ttu-id="9af05-110">Вопросы программирования</span><span class="sxs-lookup"><span data-stu-id="9af05-110">Programming Considerations</span></span>](programming-considerations.md)                                                 | <span data-ttu-id="9af05-111">Определяет важные вопросы программирования при разработке приложений с помощью одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9af05-111">Identifies important programming considerations for developing applications using the Peer Infrastructure.</span></span>              |
| [<span data-ttu-id="9af05-112">Вопросы безопасности</span><span class="sxs-lookup"><span data-stu-id="9af05-112">Security Considerations</span></span>](security-considerations.md)                                                       | <span data-ttu-id="9af05-113">Определяет важные вопросы безопасности при разработке приложений с помощью одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9af05-113">Identifies important security considerations for developing applications using the Peer Infrastructure.</span></span>                 |
| [<span data-ttu-id="9af05-114">Импорт и экспорт базы данных</span><span class="sxs-lookup"><span data-stu-id="9af05-114">Database Import and Export</span></span>](database-import-and-export.md)                                                 | <span data-ttu-id="9af05-115">Определяет способ импорта и экспорта баз данных записей.</span><span class="sxs-lookup"><span data-stu-id="9af05-115">Identifies how to import and export record databases.</span></span>                                                                   |
| [<span data-ttu-id="9af05-116">Прямые подключения</span><span class="sxs-lookup"><span data-stu-id="9af05-116">Direct Connections</span></span>](direct-connections.md)                                                                 | <span data-ttu-id="9af05-117">Определяет, как работать с прямыми соединениями между и между одноранговыми узлами в интерфейсах API одноранговой диаграммы и группирования.</span><span class="sxs-lookup"><span data-stu-id="9af05-117">Identifies how to work with direct connections between and among peers from within the Peer Graphing and Grouping APIs.</span></span> |
| [<span data-ttu-id="9af05-118">Перечисления</span><span class="sxs-lookup"><span data-stu-id="9af05-118">Enumerations</span></span>](enumerations.md)                                                                             | <span data-ttu-id="9af05-119">Определяет, как работать с функциями перечисления, используемыми одноранговой инфраструктурой.</span><span class="sxs-lookup"><span data-stu-id="9af05-119">Identifies how to work with the enumeration functions that the Peer Infrastructure uses.</span></span>                                |
| [<span data-ttu-id="9af05-120">Освобождение данных однорангового узла</span><span class="sxs-lookup"><span data-stu-id="9af05-120">Freeing Peer Data</span></span>](freeing-peer-data.md)                                                                   | <span data-ttu-id="9af05-121">Определяет способ выпуска общих вызовов функций одноранговой инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9af05-121">Identifies how to release data common Peer Infrastructure function calls returned.</span></span>                                      |
| [<span data-ttu-id="9af05-122">Инфраструктура событий</span><span class="sxs-lookup"><span data-stu-id="9af05-122">Events Infrastructure</span></span>](peer-events-infrastructure.md)                                                      | <span data-ttu-id="9af05-123">Определяет способ работы с событиями одноранговых узлов и интерпретации событий, определяемых интерфейсами API одноранговых диаграмм и диаграмм.</span><span class="sxs-lookup"><span data-stu-id="9af05-123">Identifies how to work with the peer events, and interpret the events that the Peer Graphing and Graphing APIs define.</span></span>  |
| [<span data-ttu-id="9af05-124">Импорт и экспорт конфигурации удостоверений и групп</span><span class="sxs-lookup"><span data-stu-id="9af05-124">Identity and Group Configuration Import and Export</span></span>](identity-and-group-configuration-import-and-export.md) | <span data-ttu-id="9af05-125">Определяет способ импорта и экспорта конфигураций удостоверений одноранговых узлов и групп.</span><span class="sxs-lookup"><span data-stu-id="9af05-125">Identifies how to import and export peer identity and group identity configurations.</span></span>                                    |
| [<span data-ttu-id="9af05-126">Записи</span><span class="sxs-lookup"><span data-stu-id="9af05-126">Records</span></span>](records.md)                                                                                       | <span data-ttu-id="9af05-127">Определяет, как работать с одноранговой записью и базой данных записи.</span><span class="sxs-lookup"><span data-stu-id="9af05-127">Identifies how to work with peer records and the record database.</span></span>                                                       |



 

 

 



