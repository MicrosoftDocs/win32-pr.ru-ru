---
title: Ифилллоккбитес — реализация
description: Система предоставляет реализацию Ифилллоккбитес в составе реализации составных файлов.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- Ифилллоккбитес Стрктд STG, реализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986445"
---
# <a name="ifilllockbytes---implementation"></a><span data-ttu-id="5fc42-104">Ифилллоккбитес — реализация</span><span class="sxs-lookup"><span data-stu-id="5fc42-104">IFillLockBytes - Implementation</span></span>

<span data-ttu-id="5fc42-105">Система предоставляет реализацию [**ифилллоккбитес**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) в составе реализации составных файлов.</span><span class="sxs-lookup"><span data-stu-id="5fc42-105">The system provides an [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation as part of the Compound Files implementation.</span></span>

<span data-ttu-id="5fc42-106">При скачивании кода можно создать экземпляр объекта асинхронного составного файла, вызвав [**стгопенасинкдокфилеонифилллоккбитес**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span><span class="sxs-lookup"><span data-stu-id="5fc42-106">Downloading code can create an instance of an asynchronous Compound File object by calling [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span></span> <span data-ttu-id="5fc42-107">Скачивание кода также может создать экземпляр объекта-оболочки асинхронного массива байтов для существующего файла или массива байтов, вызвав либо функцию [**стгжетифилллоккбитесонфиле**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) , либо функцию [**стгжетифилллоккбитесонилоккбитес**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="5fc42-107">Downloading code can also create an instance of an asynchronous byte array wrapper object on an existing file or byte array by calling either the [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) function or the [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) function.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="5fc42-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="5fc42-108">When to Use</span></span>

<span data-ttu-id="5fc42-109">Сейчас моникеры URL-адресов являются единственными пользователями реализации асинхронного хранилища COM.</span><span class="sxs-lookup"><span data-stu-id="5fc42-109">Currently, URL monikers are the only users of the COM asynchronous storage implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc42-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5fc42-110">Remarks</span></span>

<span data-ttu-id="5fc42-111">Ниже приведены четыре метода реализации [**ифилллоккбитес**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) .</span><span class="sxs-lookup"><span data-stu-id="5fc42-111">The following are the four methods of the [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation.</span></span>

<dl> <dt>

<span data-ttu-id="5fc42-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**Ифилллоккбитес:: Филлаппенд**</span><span class="sxs-lookup"><span data-stu-id="5fc42-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span></span>
</dt> <dd>

<span data-ttu-id="5fc42-113">Записывает новый блок байтов в конец массива байтов.</span><span class="sxs-lookup"><span data-stu-id="5fc42-113">Writes a new block of bytes to the end of a byte array.</span></span> <span data-ttu-id="5fc42-114">Размер блока указывается в качестве параметра для [**филлаппенд**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span><span class="sxs-lookup"><span data-stu-id="5fc42-114">The size of the block is specified as a parameter to [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span></span>

</dd> <dt>

<span data-ttu-id="5fc42-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**Ифилллоккбитес:: Филлат**</span><span class="sxs-lookup"><span data-stu-id="5fc42-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span></span>
</dt> <dd>

<span data-ttu-id="5fc42-116">Записывает новый блок данных в указанное расположение в массиве байтов.</span><span class="sxs-lookup"><span data-stu-id="5fc42-116">Writes a new block of data to a specified location in the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="5fc42-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**Ифилллоккбитес:: Сетфиллсизе**</span><span class="sxs-lookup"><span data-stu-id="5fc42-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span></span>
</dt> <dd>

<span data-ttu-id="5fc42-118">Задает размер массива байтов.</span><span class="sxs-lookup"><span data-stu-id="5fc42-118">Sets the size of the byte array.</span></span> <span data-ttu-id="5fc42-119">Возвращает значение E \_ Fail из вызовов [**ILockBytes:: реадат**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) , пытающихся получить доступ к данным за пределами верхней границы, заданной методом.</span><span class="sxs-lookup"><span data-stu-id="5fc42-119">Returns E\_FAIL from calls to [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) that attempt to access data beyond the upper limit specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="5fc42-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**Ифилллоккбитес:: Terminate**</span><span class="sxs-lookup"><span data-stu-id="5fc42-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**</span></span>
</dt> <dd>

<span data-ttu-id="5fc42-121">Информирует массив байтов о том, что скачивание было завершено успешно или неудачно.</span><span class="sxs-lookup"><span data-stu-id="5fc42-121">Informs the byte array that a download has been terminated, either successfully or unsuccessfully.</span></span>

</dd> </dl>

 

 




