---
title: Реализация ILockBytes-File-Based
description: Реализуется для объекта массива байтов, лежащего в основе объекта хранилища составных файлов COM и предназначенного для чтения и записи непосредственно в файл на диске.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Стрктд STG, реализации, на основе файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410697"
---
# <a name="ilockbytes---file-based-implementation"></a><span data-ttu-id="b8e34-104">Реализация ILockBytes-File-Based</span><span class="sxs-lookup"><span data-stu-id="b8e34-104">ILockBytes - File-Based Implementation</span></span>

<span data-ttu-id="b8e34-105">Реализуется для объекта массива байтов, лежащего в основе объекта хранилища составных файлов COM и предназначенного для чтения и записи непосредственно в файл на диске.</span><span class="sxs-lookup"><span data-stu-id="b8e34-105">Implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to a disk file.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b8e34-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="b8e34-106">When to Use</span></span>

<span data-ttu-id="b8e34-107">Методы [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) вызываются из составных реализаций файлов класса [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) и [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) для объекта хранилища составных файлов, созданного с помощью вызова [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), поэтому вам не нужно вызывать их напрямую.</span><span class="sxs-lookup"><span data-stu-id="b8e34-107">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), so you do not need to call them directly.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8e34-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8e34-108">Remarks</span></span>

<span data-ttu-id="b8e34-109">Ниже приведены методы реализации File-Based [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="b8e34-109">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) File-Based Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="b8e34-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: Реадат**</span><span class="sxs-lookup"><span data-stu-id="b8e34-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="b8e34-111">Считывает блок байтов из указанного смещения в начале массива байтов.</span><span class="sxs-lookup"><span data-stu-id="b8e34-111">Reads a block of bytes from a specified offset at the beginning of the byte-array.</span></span>

</dd> <dt>

<span data-ttu-id="b8e34-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: Вритеат**</span><span class="sxs-lookup"><span data-stu-id="b8e34-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="b8e34-113">Записывает блок байтов из указанного смещения в начале массива байтов.</span><span class="sxs-lookup"><span data-stu-id="b8e34-113">Writes a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="b8e34-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**</span><span class="sxs-lookup"><span data-stu-id="b8e34-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="b8e34-115">Гарантирует, что все внутренние буферы, поддерживаемые реализацией [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) , записываются в базовое физическое хранилище.</span><span class="sxs-lookup"><span data-stu-id="b8e34-115">Ensures that any internal buffers maintained by the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) implementation are written out to the underlying physical storage.</span></span>

</dd> <dt>

<span data-ttu-id="b8e34-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**</span><span class="sxs-lookup"><span data-stu-id="b8e34-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="b8e34-117">Задает размер массива байтов.</span><span class="sxs-lookup"><span data-stu-id="b8e34-117">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="b8e34-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="b8e34-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="b8e34-119">Параметр *двлокктипес* имеет значение Lock \_ онлйонце или Lock \_ монопольно, что разрешает или ограничивает доступ к заблокированным регионам.</span><span class="sxs-lookup"><span data-stu-id="b8e34-119">The *dwLockTypes* parameter is set to LOCK\_ONLYONCE or LOCK\_EXCLUSIVE, which will allow or restrict access to locked regions.</span></span>

</dd> <dt>

<span data-ttu-id="b8e34-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="b8e34-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="b8e34-121">Этот метод разблокирует область, Заблокированную [**ILockBytes:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span><span class="sxs-lookup"><span data-stu-id="b8e34-121">This method unlocks the region locked by [**ILockBytes::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="b8e34-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**</span><span class="sxs-lookup"><span data-stu-id="b8e34-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="b8e34-123">Реализация метода [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) , предоставляемая моделью COM, вызывает метод [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) для получения сведений о объекте массива байтов.</span><span class="sxs-lookup"><span data-stu-id="b8e34-123">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve information about the byte array object.</span></span> <span data-ttu-id="b8e34-124">Если для массива байтов нет допустимого имени, метод **ILockBytes:: stat** , ПРЕДОСТАВЛЕННЫЙ моделью COM, возвращает **значение NULL** в элемент **пвкснаме** структуры [**статстг**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="b8e34-124">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b8e34-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b8e34-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8e34-126">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="b8e34-126">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="b8e34-127">**Метод IStorage**</span><span class="sxs-lookup"><span data-stu-id="b8e34-127">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="b8e34-128">**IStream**</span><span class="sxs-lookup"><span data-stu-id="b8e34-128">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




