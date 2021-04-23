---
description: Транзакционная NTFS (TxF) позволяет выполнять операции с файлами на томе файловой системы NTFS в транзакции.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: Транзакционная NTFS (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539927"
---
# <a name="transactional-ntfs-txf"></a><span data-ttu-id="865d5-103">Транзакционная NTFS (TxF)</span><span class="sxs-lookup"><span data-stu-id="865d5-103">Transactional NTFS (TxF)</span></span>

<span data-ttu-id="865d5-104">\[Корпорация Майкрософт настоятельно рекомендует разработчикам использовать альтернативные средства для достижения потребностей вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="865d5-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="865d5-105">Многие сценарии, в которых была разработана система TxF, можно получить с помощью более простых и более быстро доступных методов.</span><span class="sxs-lookup"><span data-stu-id="865d5-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="865d5-106">Кроме того, TxF может быть недоступен в будущих версиях Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="865d5-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="865d5-107">Дополнительные сведения и альтернативы TxF см. [в разделе альтернативы использованию транзакционной NTFS](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="865d5-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="865d5-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="865d5-108">Purpose</span></span>

<span data-ttu-id="865d5-109">Транзакционная NTFS (TxF) позволяет выполнять операции с файлами на томе файловой системы NTFS в транзакции.</span><span class="sxs-lookup"><span data-stu-id="865d5-109">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span> <span data-ttu-id="865d5-110">Транзакции TxF увеличивают надежность приложения за счет защиты целостности данных в случае сбоев и упрощения разработки приложений за счет значительного уменьшения объема кода обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="865d5-110">TxF transactions increase application reliability by protecting data integrity across failures and simplify application development by greatly reducing the amount of error handling code.</span></span>

<span data-ttu-id="865d5-111">TxF использует платформу транзакций, предоставляемую [диспетчером транзакций ядра](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM).</span><span class="sxs-lookup"><span data-stu-id="865d5-111">TxF uses the transaction framework provided by the [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM).</span></span> <span data-ttu-id="865d5-112">Это позволяет операциям с файлами TxF входить в транзакцию, включающую другие источники данных, такие как SQL Server и реестр транзакций (TxR).</span><span class="sxs-lookup"><span data-stu-id="865d5-112">This allows TxF file operations to be part of a transaction involving other data sources such as SQL Server and Transacted Registry (TxR).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="865d5-113">Где применимо</span><span class="sxs-lookup"><span data-stu-id="865d5-113">Where applicable</span></span>

<span data-ttu-id="865d5-114">Приложение может использовать TxF, чтобы сохранить целостность данных на диске из-за непредвиденных условий ошибки и помочь в разрешении параллельных сценариев пользователя файловой системы, изолируя изменения от других пользователей во время внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="865d5-114">An application can use TxF to preserve the integrity of data on disk caused by unexpected error conditions and help resolve concurrent file-system user scenarios by isolating your changes from others while the changes are being made.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="865d5-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="865d5-115">Developer audience</span></span>

<span data-ttu-id="865d5-116">Перед использованием TxF необходимо иметь опыт работы с транзакциями с помощью KTM или [координатор распределенных транзакций (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="865d5-116">Before using TxF, you should have a working knowledge of transactions using either KTM or [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="865d5-117">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="865d5-117">Run-time requirements</span></span>

<span data-ttu-id="865d5-118">Система TxF доступна начиная с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="865d5-118">TxF is available starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="865d5-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="865d5-119">In this section</span></span>



| <span data-ttu-id="865d5-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="865d5-120">Topic</span></span>                                                    | <span data-ttu-id="865d5-121">Описание</span><span class="sxs-lookup"><span data-stu-id="865d5-121">Description</span></span>                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="865d5-122">О программе</span><span class="sxs-lookup"><span data-stu-id="865d5-122">About</span></span>](about-transactional-ntfs.md)<br/>         | <span data-ttu-id="865d5-123">Общие сведения о транзакционной NTFS.</span><span class="sxs-lookup"><span data-stu-id="865d5-123">General information about Transactional NTFS.</span></span><br/>                                                   |
| [<span data-ttu-id="865d5-124">Ссылки</span><span class="sxs-lookup"><span data-stu-id="865d5-124">Reference</span></span>](transactional-ntfs-reference.md)<br/> | <span data-ttu-id="865d5-125">Документация по функциям, структурам данных, перечислениям и другим программным элементам.</span><span class="sxs-lookup"><span data-stu-id="865d5-125">Documentation for the functions, data structures, enumerations, and other programming elements.</span></span><br/> |



 

 

