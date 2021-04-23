---
title: ILockBytes — реализация глобальной памяти
description: Реализация глобальной памяти ILockBytes реализуется для объекта массива байтов, лежащего в основе объекта хранилища составных файлов COM и предназначенного для чтения и записи непосредственно в глобальной памяти.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Стрктд STG, реализации, глобальная память
- ILockBytes Стрктд STG, реализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328864"
---
# <a name="ilockbytes---global-memory-implementation"></a><span data-ttu-id="45f4c-105">ILockBytes — реализация глобальной памяти</span><span class="sxs-lookup"><span data-stu-id="45f4c-105">ILockBytes - Global Memory Implementation</span></span>

<span data-ttu-id="45f4c-106">Реализация глобальной памяти ILockBytes реализуется для объекта массива байтов, лежащего в основе объекта хранилища составных файлов COM и предназначенного для чтения и записи непосредственно в глобальной памяти.</span><span class="sxs-lookup"><span data-stu-id="45f4c-106">The ILockBytes global memory implementation is implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to global memory.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="45f4c-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="45f4c-107">When to Use</span></span>

<span data-ttu-id="45f4c-108">Методы [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) вызываются из составных реализаций файлов класса [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) и [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) для объекта хранилища составных файлов, созданного с помощью вызова [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span><span class="sxs-lookup"><span data-stu-id="45f4c-108">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span></span>

## <a name="remarks"></a><span data-ttu-id="45f4c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45f4c-109">Remarks</span></span>

<span data-ttu-id="45f4c-110">Ниже приведены методы реализации глобальной памяти [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="45f4c-110">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Global Memory Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="45f4c-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: Реадат**</span><span class="sxs-lookup"><span data-stu-id="45f4c-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="45f4c-112">Считывает блок байтов из указанного смещения в начале массива байтов.</span><span class="sxs-lookup"><span data-stu-id="45f4c-112">Reads a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="45f4c-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: Вритеат**</span><span class="sxs-lookup"><span data-stu-id="45f4c-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="45f4c-114">Записывает блок байтов из указанного смещения в начале массива байтов.</span><span class="sxs-lookup"><span data-stu-id="45f4c-114">Writes the block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="45f4c-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**</span><span class="sxs-lookup"><span data-stu-id="45f4c-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="45f4c-116">В отличие от реализации на основе файлов, вызов этого метода в реализации глобальной памяти не имеет силы.</span><span class="sxs-lookup"><span data-stu-id="45f4c-116">Unlike file-based implementation, calling this method in global memory implementation has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="45f4c-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**</span><span class="sxs-lookup"><span data-stu-id="45f4c-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="45f4c-118">Задает размер массива байтов.</span><span class="sxs-lookup"><span data-stu-id="45f4c-118">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="45f4c-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="45f4c-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="45f4c-120">Эта реализация не поддерживает блокировку, поэтому *двлоккстипе* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="45f4c-120">This implementation does not support locking, so *dwLocksType* is set to zero.</span></span> <span data-ttu-id="45f4c-121">Вызывающий объект должен обеспечивать допустимые и взаимоисключающие обращения.</span><span class="sxs-lookup"><span data-stu-id="45f4c-121">The caller must ensure accesses are valid and mutually exclusive.</span></span>

</dd> <dt>

<span data-ttu-id="45f4c-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="45f4c-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="45f4c-123">Эта реализация не поддерживает блокировку.</span><span class="sxs-lookup"><span data-stu-id="45f4c-123">This implementation does not support locking.</span></span>

</dd> <dt>

<span data-ttu-id="45f4c-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**</span><span class="sxs-lookup"><span data-stu-id="45f4c-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="45f4c-125">Реализация метода [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) , предоставляемая моделью COM, вызывает метод [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) для получения данных о объекте массива байтов.</span><span class="sxs-lookup"><span data-stu-id="45f4c-125">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve data about the byte array object.</span></span> <span data-ttu-id="45f4c-126">Если для массива байтов нет допустимого имени, метод **ILockBytes:: stat** , ПРЕДОСТАВЛЕННЫЙ моделью COM, возвращает **значение NULL** в элемент **пвкснаме** структуры [**статстг**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="45f4c-126">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="45f4c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="45f4c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45f4c-128">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="45f4c-128">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="45f4c-129">**Метод IStorage**</span><span class="sxs-lookup"><span data-stu-id="45f4c-129">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="45f4c-130">**IStream**</span><span class="sxs-lookup"><span data-stu-id="45f4c-130">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




