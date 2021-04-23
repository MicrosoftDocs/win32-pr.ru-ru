---
description: Дополнительные сведения о подсистеме расширяемого хранилища
title: Сведения о расширяемой подсистеме хранилища
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990853"
---
# <a name="about-extensible-storage-engine"></a><span data-ttu-id="4963b-103">Сведения о расширяемой подсистеме хранилища</span><span class="sxs-lookup"><span data-stu-id="4963b-103">About Extensible Storage Engine</span></span>


<span data-ttu-id="4963b-104">_**Применимо к:** Exchange Server 2013 | Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4963b-104">_**Applies to:** Exchange Server 2013 | Windows | Windows Server_</span></span>

## <a name="about-extensible-storage-engine"></a><span data-ttu-id="4963b-105">Сведения о расширяемой подсистеме хранилища</span><span class="sxs-lookup"><span data-stu-id="4963b-105">About Extensible Storage Engine</span></span>

<span data-ttu-id="4963b-106">Подсистема расширенного хранилища (ESE) — это ядро СУБД, в котором данные хранятся в логической последовательности.</span><span class="sxs-lookup"><span data-stu-id="4963b-106">The extensible storage engine (ESE) is a database engine that stores information in a logical sequence.</span></span> <span data-ttu-id="4963b-107">Сведения могут быть получены либо последовательно, либо путем доступа к определенным индексам.</span><span class="sxs-lookup"><span data-stu-id="4963b-107">Information can be retrieved either sequentially or by accessing defined indices.</span></span> <span data-ttu-id="4963b-108">Для обеспечения безопасных операций обновления базы данных реализуются с помощью транзакции.</span><span class="sxs-lookup"><span data-stu-id="4963b-108">Updates to the database are implemented with a transaction in order to ensure secure operations.</span></span> <span data-ttu-id="4963b-109">ESE обеспечивает одновременный доступ к нескольким базам данных, включая базы данных журналов транзакций, которые можно использовать для восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="4963b-109">ESE enables simultaneous access to multiple databases, including transaction-log file databases that can be used for system recovery.</span></span> <span data-ttu-id="4963b-110">ESE масштабируется для больших или небольших приложений.</span><span class="sxs-lookup"><span data-stu-id="4963b-110">ESE is scalable to large or small applications.</span></span> <span data-ttu-id="4963b-111">В ПРИКЛАДном программном интерфейсе ESE доступны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="4963b-111">The following features are available with the ESE application programming interface (API):</span></span>

  - <span data-ttu-id="4963b-112">Резервное копирование и восстановление. приложение может создавать последовательные копии состояния данных, пока оно находится в режиме «в системе» и активно изменяет состояние данных.</span><span class="sxs-lookup"><span data-stu-id="4963b-112">Backup and restore: An application can make consistent copies of the data state while it is on-line and actively modifying data state.</span></span>

  - <span data-ttu-id="4963b-113">Навигация по курсору: приложение может перемещаться с помощью курсора, чтобы получить доступ к данным последовательно или с помощью индексов.</span><span class="sxs-lookup"><span data-stu-id="4963b-113">Cursor Navigation: The application can navigate with the cursor to access data either sequentially or by using indices.</span></span>

  - <span data-ttu-id="4963b-114">База данных. Коллекция таблиц, резервное копирование и восстановление которых выполняется как единое целое.</span><span class="sxs-lookup"><span data-stu-id="4963b-114">Database: A collection of tables that are backed up and restored as a single unit.</span></span>

  - <span data-ttu-id="4963b-115">Ведение журнала и восстановление после сбоя. API ESE гарантирует, что согласованность данных, определяемая приложением, будет учитываться даже в случае сбоя системы.</span><span class="sxs-lookup"><span data-stu-id="4963b-115">Logging and crash recovery: The ESE API ensures that application-defined data consistency is honored even in the event of a system crash.</span></span>

  - <span data-ttu-id="4963b-116">Таблицы — фундаментальная структура базы данных ESE, используемая для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="4963b-116">Tables: The fundamental structure of the ESE database that is used to store data.</span></span>

  - <span data-ttu-id="4963b-117">Транзакция. ядро базы данных ESE предоставляет атомарные устойчивые транзакции, которые позволяют приложениям получать данные только из надежных состояний данных и поддерживать согласованность данных в случае непредвиденного завершения процесса или завершения работы системы.</span><span class="sxs-lookup"><span data-stu-id="4963b-117">Transaction: The ESE database engine provides Atomic Consistent Isolated Durable (ACID) transactions that allow applications to retrieve data only from reliable data states and maintains data consistency in the event of an unexpected process termination or system shutdown.</span></span>

  - <span data-ttu-id="4963b-118">Масштабируемое: приложение может создавать базы данных размером до 100 ГБ или с небольшим объемом до 1 МБ.</span><span class="sxs-lookup"><span data-stu-id="4963b-118">Scalable: The application can create databases as large as 100 GB or as small as 1MB.</span></span>

