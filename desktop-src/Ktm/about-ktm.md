---
description: Диспетчер транзакций ядра (KTM) — это служба управления транзакциями. Она делает транзакции доступными как объекты ядра и предоставляет службы управления транзакциями системным компонентам, таким как транзакционная NTFS (TxF).
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: О программе KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081496"
---
# <a name="about-ktm"></a><span data-ttu-id="2acb4-104">О программе KTM</span><span class="sxs-lookup"><span data-stu-id="2acb4-104">About KTM</span></span>

<span data-ttu-id="2acb4-105">Диспетчер транзакций ядра (KTM) — это служба управления транзакциями.</span><span class="sxs-lookup"><span data-stu-id="2acb4-105">Kernel Transaction Manager (KTM) is a transaction management service.</span></span> <span data-ttu-id="2acb4-106">Она делает транзакции доступными как объекты ядра и предоставляет службы управления транзакциями системным компонентам, таким как [транзакционная NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span><span class="sxs-lookup"><span data-stu-id="2acb4-106">It makes transactions available as kernel objects and provides transaction management services to system components such as [Transactional NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span></span>

<span data-ttu-id="2acb4-107">В следующих разделах описываются варианты использования и функции KTM:</span><span class="sxs-lookup"><span data-stu-id="2acb4-107">The following topics describe the uses and features of KTM:</span></span>

-   [<span data-ttu-id="2acb4-108">Что такое транзакция?</span><span class="sxs-lookup"><span data-stu-id="2acb4-108">What is a Transaction?</span></span>](what-is-a-transaction.md)
-   [<span data-ttu-id="2acb4-109">Работа с транзакциями</span><span class="sxs-lookup"><span data-stu-id="2acb4-109">Working With Transactions</span></span>](programming-model.md)
-   [<span data-ttu-id="2acb4-110">Запись диспетчер ресурсов</span><span class="sxs-lookup"><span data-stu-id="2acb4-110">Writing a Resource Manager</span></span>](writing-a-resource-manager.md)
-   [<span data-ttu-id="2acb4-111">Взаимодействие с другими функциями Windows</span><span class="sxs-lookup"><span data-stu-id="2acb4-111">Interoperability With Other Windows Features</span></span>](interoperability-with-other-windows-features.md)
-   [<span data-ttu-id="2acb4-112">Права доступа и безопасности KTM</span><span class="sxs-lookup"><span data-stu-id="2acb4-112">KTM Security and Access Rights</span></span>](ktm-security-and-access-rights.md)

<span data-ttu-id="2acb4-113">Для работы KTM используется [Файловая система CLFS](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) .</span><span class="sxs-lookup"><span data-stu-id="2acb4-113">KTM relies on the [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) for its operation.</span></span> <span data-ttu-id="2acb4-114">CLFS — это система ведения журналов, которая может включать транзакции.</span><span class="sxs-lookup"><span data-stu-id="2acb4-114">CLFS is a logging system that is capable of enabling transactions.</span></span>

 

 
