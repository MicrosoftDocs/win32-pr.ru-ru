---
description: Реализация транзакционной NTFS (TxF) и транзакционного реестра (TxR). TxF позволяет выполнять транзакционные операции файловой системы в файловой системе NTFS. TxR позволяет выполнять транзакционные операции реестра. Координирование операций файловой системы и реестра с транзакцией.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Диспетчер транзакций ядра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651112"
---
# <a name="kernel-transaction-manager"></a><span data-ttu-id="2da4b-106">Диспетчер транзакций ядра</span><span class="sxs-lookup"><span data-stu-id="2da4b-106">Kernel Transaction Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="2da4b-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="2da4b-107">Purpose</span></span>

<span data-ttu-id="2da4b-108">Диспетчер транзакций ядра (KTM) позволяет разрабатывать приложения, использующие транзакции.</span><span class="sxs-lookup"><span data-stu-id="2da4b-108">The Kernel Transaction Manager (KTM) enables the development of applications that use transactions.</span></span> <span data-ttu-id="2da4b-109">Ядро транзакций находится в ядре, но транзакции могут разрабатываться для транзакций ядра или пользовательского режима, а также внутри одного узла или между распределенными узлами.</span><span class="sxs-lookup"><span data-stu-id="2da4b-109">The transaction engine itself is within the kernel, but transactions can be developed for kernel- or user-mode transactions, and within a single host or among distributed hosts.</span></span>

<span data-ttu-id="2da4b-110">KTM используется для реализации транзакционной NTFS (TxF) и транзакционного реестра (TxR).</span><span class="sxs-lookup"><span data-stu-id="2da4b-110">The KTM is used to implement Transactional NTFS (TxF) and Transactional Registry (TxR).</span></span> <span data-ttu-id="2da4b-111">TxF позволяет выполнять транзакционные операции файловой системы в файловой системе NTFS.</span><span class="sxs-lookup"><span data-stu-id="2da4b-111">TxF allows transacted file system operations within the NTFS file system.</span></span> <span data-ttu-id="2da4b-112">TxR позволяет выполнять транзакционные операции реестра.</span><span class="sxs-lookup"><span data-stu-id="2da4b-112">TxR allows transacted registry operations.</span></span> <span data-ttu-id="2da4b-113">KTM позволяет клиентским приложениям координировать операции файловой системы и реестра с транзакцией.</span><span class="sxs-lookup"><span data-stu-id="2da4b-113">KTM enables client applications to coordinate file system and registry operations with a transaction.</span></span>

<span data-ttu-id="2da4b-114">Чтобы разработать приложение, которое координирует транзакции с ресурсами, отличными от TxF или TxR, сначала необходимо разработать службу, поддерживающую транзакции Win32, также называемую диспетчером ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2da4b-114">To develop an application that coordinates transactions with resources other than TxF or TxR, you must first develop a Win32 transaction-aware service, also called a resource manager.</span></span>

<span data-ttu-id="2da4b-115">Управляемые приложения и COM+ должны использовать собственные диспетчеры транзакций.</span><span class="sxs-lookup"><span data-stu-id="2da4b-115">Managed and COM+ applications should use their native transaction managers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="2da4b-116">Где применимо</span><span class="sxs-lookup"><span data-stu-id="2da4b-116">Where applicable</span></span>

<span data-ttu-id="2da4b-117">KTM можно использовать с приложениями и диспетчерами ресурсов, размещенными в Windows Vista или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2da4b-117">KTM can be used with applications and resource managers hosted on Windows Vista or Windows Server 2008.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2da4b-118">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="2da4b-118">Developer audience</span></span>

<span data-ttu-id="2da4b-119">API KTM предназначен для использования программистами C и C++.</span><span class="sxs-lookup"><span data-stu-id="2da4b-119">The KTM API is designed for use by C and C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2da4b-120">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="2da4b-120">Run-time requirements</span></span>

<span data-ttu-id="2da4b-121">KTM поддерживается начиная с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2da4b-121">KTM is supported starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2da4b-122">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="2da4b-122">In this section</span></span>



| <span data-ttu-id="2da4b-123">Раздел</span><span class="sxs-lookup"><span data-stu-id="2da4b-123">Topic</span></span>                                     | <span data-ttu-id="2da4b-124">Описание</span><span class="sxs-lookup"><span data-stu-id="2da4b-124">Description</span></span>                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2da4b-125">О программе</span><span class="sxs-lookup"><span data-stu-id="2da4b-125">About</span></span>](about-ktm.md)<br/>         | <span data-ttu-id="2da4b-126">Общие сведения о транзакциях и возможностях, предоставляемых KTM.</span><span class="sxs-lookup"><span data-stu-id="2da4b-126">General information about transactions and the capabilities provided by KTM.</span></span><br/>                           |
| [<span data-ttu-id="2da4b-127">Ссылки</span><span class="sxs-lookup"><span data-stu-id="2da4b-127">Reference</span></span>](ktm-reference.md)<br/> | <span data-ttu-id="2da4b-128">Документация по функциям, структурам данных, перечислениям и другим программным элементам KTM.</span><span class="sxs-lookup"><span data-stu-id="2da4b-128">Documentation for the functions, data structures, enumerations, and other programming elements of KTM.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2da4b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2da4b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da4b-130">файловая система CLFS</span><span class="sxs-lookup"><span data-stu-id="2da4b-130">Common Log File System</span></span>](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[<span data-ttu-id="2da4b-131">Транзакционная NTFS (TxF)</span><span class="sxs-lookup"><span data-stu-id="2da4b-131">Transactional NTFS (TxF)</span></span>](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

<span data-ttu-id="2da4b-132">[Координатор распределенных транзакций](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2da4b-132">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> </dl>

 

