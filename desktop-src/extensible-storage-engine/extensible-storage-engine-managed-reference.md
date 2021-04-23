---
description: 'Дополнительные сведения о: расширяемый Справочник по управляемому подсистеме хранилища'
title: Управляемый Справочник по расширенному подсистеме хранилища
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080444"
---
# <a name="extensible-storage-engine-managed-reference"></a><span data-ttu-id="06e65-103">Управляемый Справочник по расширенному подсистеме хранилища</span><span class="sxs-lookup"><span data-stu-id="06e65-103">Extensible Storage Engine Managed Reference</span></span>

<span data-ttu-id="06e65-104">Найдите справочные сведения о библиотеке Манажедесент.</span><span class="sxs-lookup"><span data-stu-id="06e65-104">Find reference information for the ManagedESENT library.</span></span> <span data-ttu-id="06e65-105">Библиотека Манажедесент предоставляет управляемый доступ к ESENT, встраиваемому ядру СУБД, который является собственным для Windows.</span><span class="sxs-lookup"><span data-stu-id="06e65-105">The ManagedESENT library provides managed access to ESENT, the embeddable database engine that is native to Windows.</span></span>


<span data-ttu-id="06e65-106">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="06e65-106">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="06e65-107">**В этой статье:**</span><span class="sxs-lookup"><span data-stu-id="06e65-107">**In this article**</span></span>  
<span data-ttu-id="06e65-108">Как библиотека Манажедесент отличается от ESENT?</span><span class="sxs-lookup"><span data-stu-id="06e65-108">How is the ManagedESENT library different than ESENT?</span></span>  
<span data-ttu-id="06e65-109">Требования</span><span class="sxs-lookup"><span data-stu-id="06e65-109">Requirements</span></span>  
<span data-ttu-id="06e65-110">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="06e65-110">In this section</span></span>  

## <a name="how-is-the-managedesent-library-different-than-esent"></a><span data-ttu-id="06e65-111">Как библиотека Манажедесент отличается от ESENT?</span><span class="sxs-lookup"><span data-stu-id="06e65-111">How is the ManagedESENT library different than ESENT?</span></span>

<span data-ttu-id="06e65-112">ESENT — это внедряемое, транзакционное ядро СУБД, которое позволяет создавать пользовательские приложения, требующие надежного хранения данных с высокой производительностью и низкой нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="06e65-112">ESENT is an embeddable, transactional database engine that allows you to create custom applications that need reliable, high-performance, low-overhead storage of data.</span></span> <span data-ttu-id="06e65-113">Подсистема ESENT может помочь в использовании данных в диапазоне от чего-нибудь простого, так же как в хэш таблице, которая слишком велика для хранения в памяти, на нечто более сложное, например в приложении с таблицами, столбцами и индексами.</span><span class="sxs-lookup"><span data-stu-id="06e65-113">The ESENT engine can help with data needs that range from something as simple as a hash table that is too large to store in memory, to something more complex, such as an application with tables, columns, and indexes.</span></span> <span data-ttu-id="06e65-114">Чтобы создать приложение с помощью ESENT, используйте библиотеку DLL esent.dll, которая является частью операционной системы Windows, и напишите код с помощью C/C++.</span><span class="sxs-lookup"><span data-stu-id="06e65-114">To create an application with ESENT, you use the esent.dll DLL that is part of the Windows operating system and write your code with C/C++.</span></span> <span data-ttu-id="06e65-115">Дополнительные сведения о ESENT см. в [справочнике по расширенному подсистеме хранилища](./extensible-storage-engine-reference.md).</span><span class="sxs-lookup"><span data-stu-id="06e65-115">For more information about ESENT, see [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).</span></span>

<span data-ttu-id="06e65-116">Манажедесент построен на esent.dll, который является частью Windows, поэтому дополнительные неуправляемые двоичные файлы для загрузки и установки отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="06e65-116">ManagedESENT is built on top of esent.dll, which is part of Windows, so there are no extra unmanaged binaries to download and install.</span></span> <span data-ttu-id="06e65-117">С помощью библиотеки Манажедесент можно создать приложение с помощью управляемого языка, например C, \# а не c/C++.</span><span class="sxs-lookup"><span data-stu-id="06e65-117">With the ManagedESENT library, you can create your application by using a managed language such as C\# instead of C/C++.</span></span> <span data-ttu-id="06e65-118">Библиотека использует те же имена типов и членов для предоставления API ESE, поэтому, если вы уже знакомы со структурой этого API, вы можете легко перейти к этой управляемой библиотеке.</span><span class="sxs-lookup"><span data-stu-id="06e65-118">The library uses the same type and member names to expose the ESE API, so if you are already familiar with the structure of this API, you can easily transition to this managed library.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e65-119">Требования</span><span class="sxs-lookup"><span data-stu-id="06e65-119">Requirements</span></span>

<span data-ttu-id="06e65-120">Для этой управляемой библиотеки требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="06e65-120">This managed library requires the following:</span></span>

  - <span data-ttu-id="06e65-121">Компьютер под управлением версии Windows, начиная с Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06e65-121">A computer running a version of Windows starting with Windows Vista</span></span>

  - <span data-ttu-id="06e65-122">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="06e65-122">Visual Studio 2012</span></span>

  - <span data-ttu-id="06e65-123">Платформа .NET Framework версии 4.5</span><span class="sxs-lookup"><span data-stu-id="06e65-123">The .NET Framework 4.5</span></span>

## <a name="in-this-section"></a><span data-ttu-id="06e65-124">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="06e65-124">In this section</span></span>

  - [<span data-ttu-id="06e65-125">Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="06e65-125">Microsoft.Isam.Esent</span></span>](./microsoft.isam.esent-namespace.md)

  - [<span data-ttu-id="06e65-126">Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="06e65-126">Microsoft.Isam.Esent.Interop</span></span>](./microsoft.isam.esent.interop-namespace.md)

  - [<span data-ttu-id="06e65-127">Microsoft. ISAM. ESENT. Interop. server2003</span><span class="sxs-lookup"><span data-stu-id="06e65-127">Microsoft.Isam.Esent.Interop.Server2003</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [<span data-ttu-id="06e65-128">Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="06e65-128">Microsoft.Isam.Esent.Interop.Vista</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

  - [<span data-ttu-id="06e65-129">Microsoft. ISAM. ESENT. Interop. Windows7</span><span class="sxs-lookup"><span data-stu-id="06e65-129">Microsoft.Isam.Esent.Interop.Windows7</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [<span data-ttu-id="06e65-130">Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="06e65-130">Microsoft.Isam.Esent.Interop.Windows8</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
