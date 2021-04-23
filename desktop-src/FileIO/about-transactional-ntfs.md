---
description: Транзакционная NTFS (TxF) интегрирует транзакции в файловую систему NTFS, что упрощает разработчикам приложений и администраторам корректное обработку ошибок и сохранение целостности данных.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: О транзакционной NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343642"
---
# <a name="about-transactional-ntfs"></a><span data-ttu-id="3ac6a-103">О транзакционной NTFS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-103">About Transactional NTFS</span></span>

<span data-ttu-id="3ac6a-104">\[Корпорация Майкрософт настоятельно рекомендует разработчикам использовать альтернативные средства для достижения потребностей вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="3ac6a-105">Многие сценарии, в которых была разработана система TxF, можно получить с помощью более простых и более быстро доступных методов.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="3ac6a-106">Кроме того, TxF может быть недоступен в будущих версиях Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="3ac6a-107">Дополнительные сведения и альтернативы TxF см. [в разделе альтернативы использованию транзакционной NTFS](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="3ac6a-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

<span data-ttu-id="3ac6a-108">Транзакционная NTFS (TxF) интегрирует транзакции в файловую систему NTFS, что упрощает разработчикам приложений и администраторам корректное обработку ошибок и сохранение целостности данных.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-108">Transactional NTFS (TxF) integrates transactions into the NTFS file system, which makes it easier for application developers and administrators to gracefully handle errors and preserve data integrity.</span></span>

<span data-ttu-id="3ac6a-109">TxF может участвовать в распределенных транзакциях с координатами [координатор распределенных транзакций (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) , которые позволяют использовать TxF для следующих действий:</span><span class="sxs-lookup"><span data-stu-id="3ac6a-109">TxF can participate in distributed transactions that the [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) coordinates, which allows you to use TxF for the following:</span></span>

-   <span data-ttu-id="3ac6a-110">Транзакции, охватывающие несколько хранилищ данных, например одну транзакцию для файлов и операций SQL</span><span class="sxs-lookup"><span data-stu-id="3ac6a-110">Transactions that span multiple data stores, for example, a single transaction for file and SQL operations</span></span>
-   <span data-ttu-id="3ac6a-111">Транзакции, охватывающие несколько компьютеров, например единая транзакция для обновления файлов на нескольких компьютерах</span><span class="sxs-lookup"><span data-stu-id="3ac6a-111">Transactions that span multiple computers, for example, a single transaction for file updates on multiple computers</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ac6a-112">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="3ac6a-112">In this section</span></span>



| <span data-ttu-id="3ac6a-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="3ac6a-113">Topic</span></span>                                                                                                                 | <span data-ttu-id="3ac6a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3ac6a-114">Description</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ac6a-115">Когда следует использовать транзакционную NTFS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-115">When to Use Transactional NTFS</span></span>](when-to-use-transactional-ntfs.md)<br/>                                       | <span data-ttu-id="3ac6a-116">Используйте транзакционную NTFS для поддержания целостности данных.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-116">Use Transactional NTFS to maintain data integrity.</span></span><br/>                                                                        |
| [<span data-ttu-id="3ac6a-117">Развертывание транзакционной NTFS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-117">Deploying Transactional NTFS</span></span>](deploying-transactional-ntfs.md)<br/>                                           | <span data-ttu-id="3ac6a-118">Управление кэшированием в транзакционной NTFS.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-118">Caching control in Transactional NTFS.</span></span><br/>                                                                                    |
| [<span data-ttu-id="3ac6a-119">Как использовать транзакционную NTFS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-119">How to Use Transactional NTFS</span></span>](how-to-use-transactional-ntfs.md)<br/>                                         | <span data-ttu-id="3ac6a-120">Управление дескрипторами файлов транзакций в транзакционной NTFS.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-120">Managing transacted file handles in Transactional NTFS.</span></span><br/>                                                                   |
| [<span data-ttu-id="3ac6a-121">Основные понятия TxF</span><span class="sxs-lookup"><span data-stu-id="3ac6a-121">Basic TxF Concepts</span></span>](txf-basic-concepts.md)<br/>                                                               | <span data-ttu-id="3ac6a-122">Описывает согласованность с фиксированной нагрузкой, изоляцию с фиксированным чтением и понятия блокировки транзакций в транзакционной NTFS.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-122">Describes read-committed consistency, read-committed isolation, and transactional locking concepts in Transactional NTFS.</span></span><br/> |
| [<span data-ttu-id="3ac6a-123">Рекомендации по программированию для транзакционной NTFS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-123">Programming Considerations for Transactional NTFS</span></span>](programming-considerations-for-transacted-fileio-.md)<br/> | <span data-ttu-id="3ac6a-124">Описывает различные вопросы программирования транзакционной NTFS.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-124">Describes various programming considerations for Transactional NTFS.</span></span><br/>                                                      |
| [<span data-ttu-id="3ac6a-125">Рекомендации по производительности для транзакционной NTFS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-125">Performance Considerations for Transactional NTFS</span></span>](performance-considerations-for-transactional-ntfs.md)<br/> | <span data-ttu-id="3ac6a-126">Рекомендации по оптимизации транзакций файловой системы.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-126">Recommendations for optimal file system transactions.</span></span><br/>                                                                     |



 

 

