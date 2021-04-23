---
title: Константы СТГМ (Обжбасе. h)
description: Флаги, указывающие условия создания и удаления объекта и режимов доступа для объекта.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489372"
---
# <a name="stgm-constants"></a><span data-ttu-id="55696-103">Константы СТГМ</span><span class="sxs-lookup"><span data-stu-id="55696-103">STGM Constants</span></span>

<span data-ttu-id="55696-104">Константы СТГМ — это флаги, указывающие условия создания и удаления объекта и режимов доступа для объекта.</span><span class="sxs-lookup"><span data-stu-id="55696-104">The STGM constants are flags that indicate conditions for creating and deleting the object and access modes for the object.</span></span> <span data-ttu-id="55696-105">Константы СТГМ включены в интерфейсы [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)и [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , а также в функции [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**стгкреатедокфилеонилоккбитес**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)и [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .</span><span class="sxs-lookup"><span data-stu-id="55696-105">The STGM constants are included in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces and in the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), and [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) functions.</span></span>

<span data-ttu-id="55696-106">Эти элементы часто объединяются с помощью оператора **или**.</span><span class="sxs-lookup"><span data-stu-id="55696-106">These elements are often combined using an **OR** operator.</span></span> <span data-ttu-id="55696-107">Они обрабатываются в группах, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="55696-107">They are interpreted in groups as listed in the following table.</span></span> <span data-ttu-id="55696-108">Недопустимо использовать более одного элемента из одной группы.</span><span class="sxs-lookup"><span data-stu-id="55696-108">It is not valid to use more than one element from a single group.</span></span>

<span data-ttu-id="55696-109">Используйте флаг из группы создания при создании объекта, например с помощью [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) или [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="55696-109">Use a flag from the creation group when creating an object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span>

<span data-ttu-id="55696-110">Дополнительные сведения о транзакциях см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="55696-110">For more information about transactioning, see the Remarks section.</span></span>



| <span data-ttu-id="55696-111">Группа</span><span class="sxs-lookup"><span data-stu-id="55696-111">Group</span></span>                      | <span data-ttu-id="55696-112">Флаг</span><span class="sxs-lookup"><span data-stu-id="55696-112">Flag</span></span>                         | <span data-ttu-id="55696-113">Значение</span><span class="sxs-lookup"><span data-stu-id="55696-113">Value</span></span>       |
|----------------------------|------------------------------|-------------|
| <span data-ttu-id="55696-114">Access</span><span class="sxs-lookup"><span data-stu-id="55696-114">Access</span></span>                     | <span data-ttu-id="55696-115">**СТГМ \_ чтение**</span><span class="sxs-lookup"><span data-stu-id="55696-115">**STGM\_READ**</span></span>               | <span data-ttu-id="55696-116">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55696-116">0x00000000L</span></span> |
|                            | <span data-ttu-id="55696-117">**СТГМ \_ запись**</span><span class="sxs-lookup"><span data-stu-id="55696-117">**STGM\_WRITE**</span></span>              | <span data-ttu-id="55696-118">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="55696-118">0x00000001L</span></span> |
|                            | <span data-ttu-id="55696-119">**СТГМ \_ ReadWrite**</span><span class="sxs-lookup"><span data-stu-id="55696-119">**STGM\_READWRITE**</span></span>          | <span data-ttu-id="55696-120">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="55696-120">0x00000002L</span></span> |
| <span data-ttu-id="55696-121">Совместное использование</span><span class="sxs-lookup"><span data-stu-id="55696-121">Sharing</span></span>                    | <span data-ttu-id="55696-122">**СТГМ \_ Share \_ Deny \_ None**</span><span class="sxs-lookup"><span data-stu-id="55696-122">**STGM\_SHARE\_DENY\_NONE**</span></span>  | <span data-ttu-id="55696-123">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="55696-123">0x00000040L</span></span> |
|                            | <span data-ttu-id="55696-124">**СТГМ \_ общего ресурса \_ блокировки \_ чтения**</span><span class="sxs-lookup"><span data-stu-id="55696-124">**STGM\_SHARE\_DENY\_READ**</span></span>  | <span data-ttu-id="55696-125">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="55696-125">0x00000030L</span></span> |
|                            | <span data-ttu-id="55696-126">**СТГМ \_ \_ запретить \_ запись в общую папку**</span><span class="sxs-lookup"><span data-stu-id="55696-126">**STGM\_SHARE\_DENY\_WRITE**</span></span> | <span data-ttu-id="55696-127">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="55696-127">0x00000020L</span></span> |
|                            | <span data-ttu-id="55696-128">**СТГМ \_ \_ монопольный доступ**</span><span class="sxs-lookup"><span data-stu-id="55696-128">**STGM\_SHARE\_EXCLUSIVE**</span></span>   | <span data-ttu-id="55696-129">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="55696-129">0x00000010L</span></span> |
|                            | <span data-ttu-id="55696-130">**\_приоритет стгм**</span><span class="sxs-lookup"><span data-stu-id="55696-130">**STGM\_PRIORITY**</span></span>           | <span data-ttu-id="55696-131">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="55696-131">0x00040000L</span></span> |
| <span data-ttu-id="55696-132">Создание</span><span class="sxs-lookup"><span data-stu-id="55696-132">Creation</span></span>                   | <span data-ttu-id="55696-133">**\_Создание стгм**</span><span class="sxs-lookup"><span data-stu-id="55696-133">**STGM\_CREATE**</span></span>             | <span data-ttu-id="55696-134">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="55696-134">0x00001000L</span></span> |
|                            | <span data-ttu-id="55696-135">**\_Преобразование стгм**</span><span class="sxs-lookup"><span data-stu-id="55696-135">**STGM\_CONVERT**</span></span>            | <span data-ttu-id="55696-136">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="55696-136">0x00020000L</span></span> |
|                            | <span data-ttu-id="55696-137">**СТГМ \_ фаилифсере**</span><span class="sxs-lookup"><span data-stu-id="55696-137">**STGM\_FAILIFTHERE**</span></span>        | <span data-ttu-id="55696-138">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55696-138">0x00000000L</span></span> |
| <span data-ttu-id="55696-139">Транзакционная операция</span><span class="sxs-lookup"><span data-stu-id="55696-139">Transactioning</span></span>             | <span data-ttu-id="55696-140">**СТГМ \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="55696-140">**STGM\_DIRECT**</span></span>             | <span data-ttu-id="55696-141">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55696-141">0x00000000L</span></span> |
|                            | <span data-ttu-id="55696-142">**СТГМ \_ транзакционная**</span><span class="sxs-lookup"><span data-stu-id="55696-142">**STGM\_TRANSACTED**</span></span>         | <span data-ttu-id="55696-143">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="55696-143">0x00010000L</span></span> |
| <span data-ttu-id="55696-144">Производительность транзакций</span><span class="sxs-lookup"><span data-stu-id="55696-144">Transactioning Performance</span></span> | <span data-ttu-id="55696-145">**СТГМ \_**</span><span class="sxs-lookup"><span data-stu-id="55696-145">**STGM\_NOSCRATCH**</span></span>          | <span data-ttu-id="55696-146">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="55696-146">0x00100000L</span></span> |
|                            | <span data-ttu-id="55696-147">**\_моментальный снимок стгм**</span><span class="sxs-lookup"><span data-stu-id="55696-147">**STGM\_NOSNAPSHOT**</span></span>         | <span data-ttu-id="55696-148">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="55696-148">0x00200000L</span></span> |
| <span data-ttu-id="55696-149">Прямые СВМР и простые</span><span class="sxs-lookup"><span data-stu-id="55696-149">Direct SWMR and Simple</span></span>     | <span data-ttu-id="55696-150">**СТГМ \_ Simple**</span><span class="sxs-lookup"><span data-stu-id="55696-150">**STGM\_SIMPLE**</span></span>             | <span data-ttu-id="55696-151">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="55696-151">0x08000000L</span></span> |
|                            | <span data-ttu-id="55696-152">**СТГМ \_ Direct \_ свмр**</span><span class="sxs-lookup"><span data-stu-id="55696-152">**STGM\_DIRECT\_SWMR**</span></span>       | <span data-ttu-id="55696-153">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="55696-153">0x00400000L</span></span> |
| <span data-ttu-id="55696-154">Удалить в выпуске</span><span class="sxs-lookup"><span data-stu-id="55696-154">Delete On Release</span></span>          | <span data-ttu-id="55696-155">**СТГМ \_ делетеонрелеасе**</span><span class="sxs-lookup"><span data-stu-id="55696-155">**STGM\_DELETEONRELEASE**</span></span>    | <span data-ttu-id="55696-156">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="55696-156">0x04000000L</span></span> |



 

<dl> <dt>

<span data-ttu-id="55696-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**СТГМ \_ чтение**</span><span class="sxs-lookup"><span data-stu-id="55696-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-158">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55696-158">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-159">Указывает, что объект доступен только для чтения, что означает невозможность внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="55696-159">Indicates that the object is read-only, meaning that modifications cannot be made.</span></span> <span data-ttu-id="55696-160">Например, если объект потока открыт с помощью **стгм \_ Read**, можно вызвать метод [**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) , но метод [**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) может не быть.</span><span class="sxs-lookup"><span data-stu-id="55696-160">For example, if a stream object is opened with **STGM\_READ**, the [**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) method may be called, but the [**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) method may not.</span></span> <span data-ttu-id="55696-161">Аналогичным образом, если объект хранилища, Открытый с помощью **стгм \_ Read**, может вызываться метод [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) и [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , но методы [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) и [**IStorage:: креатестораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) могут не поддерживаться.</span><span class="sxs-lookup"><span data-stu-id="55696-161">Similarly, if a storage object opened with **STGM\_READ**, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) and [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) methods may be called, but the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) and [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) methods may not.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**СТГМ \_ запись**</span><span class="sxs-lookup"><span data-stu-id="55696-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-163">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="55696-163">0x00000001L</span></span>
</dt> <dt>



<span data-ttu-id="55696-164">Позволяет сохранять изменения в объекте, но не разрешает доступ к его данным.</span><span class="sxs-lookup"><span data-stu-id="55696-164">Enables you to save changes to the object, but does not permit access to its data.</span></span> <span data-ttu-id="55696-165">Предоставленные реализации интерфейсов [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) и [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) не поддерживают этот режим только для записи.</span><span class="sxs-lookup"><span data-stu-id="55696-165">The provided implementations of the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces do not support this write-only mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**СТГМ \_ ReadWrite**</span><span class="sxs-lookup"><span data-stu-id="55696-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM\_READWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-167">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="55696-167">0x00000002L</span></span>
</dt> <dt>



<span data-ttu-id="55696-168">Обеспечивает доступ и изменение данных объекта.</span><span class="sxs-lookup"><span data-stu-id="55696-168">Enables access and modification of object data.</span></span> <span data-ttu-id="55696-169">Например, если объект потока создается или открывается в этом режиме, можно вызвать методы [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) и **IStream:: Write**.</span><span class="sxs-lookup"><span data-stu-id="55696-169">For example, if a stream object is created or opened in this mode, it is possible to call both [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) and **IStream::Write**.</span></span> <span data-ttu-id="55696-170">Имейте в виду, что эта константа не является простой двоичной **или** операцией **Стгм \_ Write** и **стгм \_ Read** Elements.</span><span class="sxs-lookup"><span data-stu-id="55696-170">Be aware that this constant is not a simple binary **OR** operation of the **STGM\_WRITE** and **STGM\_READ** elements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**СТГМ \_ Share \_ Deny \_ None**</span><span class="sxs-lookup"><span data-stu-id="55696-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM\_SHARE\_DENY\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-172">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="55696-172">0x00000040L</span></span>
</dt> <dt>



<span data-ttu-id="55696-173">Указывает, что последующие открытия объекта не запрещают доступ на чтение или запись.</span><span class="sxs-lookup"><span data-stu-id="55696-173">Specifies that subsequent openings of the object are not denied read or write access.</span></span> <span data-ttu-id="55696-174">Если не указан флаг из группы доступа, то используется этот флаг.</span><span class="sxs-lookup"><span data-stu-id="55696-174">If no flag from the sharing group is specified, this flag is assumed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**СТГМ \_ общего ресурса \_ блокировки \_ чтения**</span><span class="sxs-lookup"><span data-stu-id="55696-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM\_SHARE\_DENY\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-176">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="55696-176">0x00000030L</span></span>
</dt> <dt>



<span data-ttu-id="55696-177">Предотвращает последующее открытие объекта в режиме **\_ чтения стгм** .</span><span class="sxs-lookup"><span data-stu-id="55696-177">Prevents others from subsequently opening the object in **STGM\_READ** mode.</span></span> <span data-ttu-id="55696-178">Обычно он используется в объекте корневого хранилища.</span><span class="sxs-lookup"><span data-stu-id="55696-178">It is typically used on a root storage object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**СТГМ \_ \_ запретить \_ запись в общую папку**</span><span class="sxs-lookup"><span data-stu-id="55696-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM\_SHARE\_DENY\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-180">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="55696-180">0x00000020L</span></span>
</dt> <dt>



<span data-ttu-id="55696-181">Предотвращает последующее открытие объекта для доступа к **стгм \_ Write** или **стгм \_ ReadWrite** .</span><span class="sxs-lookup"><span data-stu-id="55696-181">Prevents others from subsequently opening the object for **STGM\_WRITE** or **STGM\_READWRITE** access.</span></span> <span data-ttu-id="55696-182">В режиме транзакций совместное использование общей **папки \_ стгм \_ Deny \_ Write** или **стгм \_ может \_** значительно повысить производительность, так как для них не требуются моментальные снимки.</span><span class="sxs-lookup"><span data-stu-id="55696-182">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="55696-183">Дополнительные сведения о транзакциях см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="55696-183">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**СТГМ \_ \_ монопольный доступ**</span><span class="sxs-lookup"><span data-stu-id="55696-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM\_SHARE\_EXCLUSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-185">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="55696-185">0x00000010L</span></span>
</dt> <dt>



<span data-ttu-id="55696-186">Предотвращает последующее открытие объекта в любом режиме другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="55696-186">Prevents others from subsequently opening the object in any mode.</span></span> <span data-ttu-id="55696-187">Следует иметь в виду, что это значение не является простой побитовой операцией **или** операции **стгм \_ Share \_ Deny \_ Read** и **стгм \_ Share \_ Deny \_ Write** .</span><span class="sxs-lookup"><span data-stu-id="55696-187">Be aware that this value is not a simple bitwise **OR** operation of the **STGM\_SHARE\_DENY\_READ** and **STGM\_SHARE\_DENY\_WRITE** values.</span></span> <span data-ttu-id="55696-188">В режиме транзакций совместное использование общей **папки \_ стгм \_ Deny \_ Write** или **стгм \_ может \_** значительно повысить производительность, так как для них не требуются моментальные снимки.</span><span class="sxs-lookup"><span data-stu-id="55696-188">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="55696-189">Дополнительные сведения о транзакциях см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="55696-189">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**\_приоритет стгм**</span><span class="sxs-lookup"><span data-stu-id="55696-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-191">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="55696-191">0x00040000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-192">Открывает объект хранилища с монопольным доступом к последней зафиксированной версии.</span><span class="sxs-lookup"><span data-stu-id="55696-192">Opens the storage object with exclusive access to the most recently committed version.</span></span> <span data-ttu-id="55696-193">Таким же другим пользователям не удастся зафиксировать изменения в объекте, пока он открыт в режиме приоритета.</span><span class="sxs-lookup"><span data-stu-id="55696-193">Thus, other users cannot commit changes to the object while you have it open in priority mode.</span></span> <span data-ttu-id="55696-194">Вы получаете выигрыш в производительности операций копирования, но не можете предотвратить внесение изменений другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="55696-194">You gain performance benefits for copy operations, but you prevent others from committing changes.</span></span> <span data-ttu-id="55696-195">Ограничьте время открытия объектов в режиме приоритета.</span><span class="sxs-lookup"><span data-stu-id="55696-195">Limit the time that objects are open in priority mode.</span></span> <span data-ttu-id="55696-196">Необходимо указать **стгм \_ Direct** и **стгм \_ Read** в режиме приоритета, а также нельзя указать **стгм \_ делетеонрелеасе**.</span><span class="sxs-lookup"><span data-stu-id="55696-196">You must specify **STGM\_DIRECT** and **STGM\_READ** with priority mode, and you cannot specify **STGM\_DELETEONRELEASE**.</span></span> <span data-ttu-id="55696-197">**Стгм \_ ДЕЛЕТЕОНРЕЛЕАСЕ** допустим только при создании корневого объекта, например с помощью [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="55696-197">**STGM\_DELETEONRELEASE** is only valid when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="55696-198">Он недействителен при открытии существующего корневого объекта, например с помощью [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span><span class="sxs-lookup"><span data-stu-id="55696-198">It is not valid when opening an existing root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span> <span data-ttu-id="55696-199">Он также недействителен при создании или открытии подэлемента, например при использовании [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span><span class="sxs-lookup"><span data-stu-id="55696-199">It is also not valid when creating or opening a subelement, such as with [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**\_Создание стгм**</span><span class="sxs-lookup"><span data-stu-id="55696-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-201">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="55696-201">0x00001000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-202">Указывает, что существующий объект или поток хранения следует удалить до того, как новый объект заменит его.</span><span class="sxs-lookup"><span data-stu-id="55696-202">Indicates that an existing storage object or stream should be removed before the new object replaces it.</span></span> <span data-ttu-id="55696-203">Новый объект создается, если этот флаг указан только в том случае, если существующий объект был успешно удален.</span><span class="sxs-lookup"><span data-stu-id="55696-203">A new object is created when this flag is specified only if the existing object has been successfully removed.</span></span>

<span data-ttu-id="55696-204">Этот флаг используется при попытке создать:</span><span class="sxs-lookup"><span data-stu-id="55696-204">This flag is used when attempting to create:</span></span>

-   <span data-ttu-id="55696-205">Объект хранилища на диске, но существует файл с таким именем.</span><span class="sxs-lookup"><span data-stu-id="55696-205">A storage object on a disk, but a file of that name exists.</span></span>
-   <span data-ttu-id="55696-206">Объект в объекте хранилища, но существует объект с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="55696-206">An object inside a storage object, but an object with the specified name exists.</span></span>
-   <span data-ttu-id="55696-207">Объект массива байтов, но он существует с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="55696-207">A byte array object, but one with the specified name exists.</span></span>

<span data-ttu-id="55696-208">Этот флаг нельзя использовать с операциями открытия, такими как [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) или [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span><span class="sxs-lookup"><span data-stu-id="55696-208">This flag cannot be used with open operations, such as [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) or [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**\_Преобразование стгм**</span><span class="sxs-lookup"><span data-stu-id="55696-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM\_CONVERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-210">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="55696-210">0x00020000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-211">Создает новый объект, сохраняя существующие данные в потоке с именем "содержимое".</span><span class="sxs-lookup"><span data-stu-id="55696-211">Creates the new object while preserving existing data in a stream named "Contents".</span></span> <span data-ttu-id="55696-212">В случае объекта хранилища или массива байтов старые данные форматируются в поток независимо от того, содержит ли существующий файл или массив байтов объект многослойного хранилища.</span><span class="sxs-lookup"><span data-stu-id="55696-212">In the case of a storage object or a byte array, the old data is formatted into a stream regardless of whether the existing file or byte array currently contains a layered storage object.</span></span> <span data-ttu-id="55696-213">Этот флаг можно использовать только при создании корневого объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="55696-213">This flag can only be used when creating a root storage object.</span></span> <span data-ttu-id="55696-214">Его нельзя использовать в объекте хранилища; Например, в [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="55696-214">It cannot be used within a storage object; for example, in [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="55696-215">Также нельзя использовать этот флаг и одновременно флаг **стгм \_ делетеонрелеасе** .</span><span class="sxs-lookup"><span data-stu-id="55696-215">It is also not valid to use this flag and the **STGM\_DELETEONRELEASE** flag simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**СТГМ \_ фаилифсере**</span><span class="sxs-lookup"><span data-stu-id="55696-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM\_FAILIFTHERE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55696-217">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-218">Приводит к сбою операции Create, если существующий объект с указанным именем существует.</span><span class="sxs-lookup"><span data-stu-id="55696-218">Causes the create operation to fail if an existing object with the specified name exists.</span></span> <span data-ttu-id="55696-219">В этом случае возвращается **STG \_ E \_ филеалреадексистс** .</span><span class="sxs-lookup"><span data-stu-id="55696-219">In this case, **STG\_E\_FILEALREADYEXISTS** is returned.</span></span> <span data-ttu-id="55696-220">Это режим создания по умолчанию. то есть если ни один другой флаг CREATE не указан, подразумевается **стгм \_ фаилифсере** .</span><span class="sxs-lookup"><span data-stu-id="55696-220">This is the default creation mode; that is, if no other create flag is specified, **STGM\_FAILIFTHERE** is implied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**СТГМ \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="55696-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="55696-222">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-223">Указывает, что в режиме Direct каждое изменение в элементе хранения или потока записывается, как это происходит.</span><span class="sxs-lookup"><span data-stu-id="55696-223">Indicates that, in direct mode, each change to a storage or stream element is written as it occurs.</span></span> <span data-ttu-id="55696-224">Это значение по умолчанию, если не указаны ни **стгм \_ Direct** , ни **стгм \_** .</span><span class="sxs-lookup"><span data-stu-id="55696-224">This is the default if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**СТГМ \_ транзакционная**</span><span class="sxs-lookup"><span data-stu-id="55696-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM\_TRANSACTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-226">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="55696-226">0x00010000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-227">Указывает, что в режиме транзакций изменения буферизуются и записываются только при вызове явной операции фиксации.</span><span class="sxs-lookup"><span data-stu-id="55696-227">Indicates that, in transacted mode, changes are buffered and written only if an explicit commit operation is called.</span></span> <span data-ttu-id="55696-228">Чтобы игнорировать изменения, вызовите метод [**revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) в интерфейсе [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)или [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) .</span><span class="sxs-lookup"><span data-stu-id="55696-228">To ignore the changes, call the [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) method in the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), or [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface.</span></span> <span data-ttu-id="55696-229">Реализация составного файла COM класса **IStorage** не поддерживает транзакционные потоки. Это означает, что потоки можно открывать только в режиме Direct, и вы не можете отменить изменения для них, однако поддерживаются Транзакционные хранилища.</span><span class="sxs-lookup"><span data-stu-id="55696-229">The COM compound file implementation of **IStorage** does not support transacted streams, which means that streams can be opened only in direct mode, and you cannot revert changes to them, however transacted storages are supported.</span></span> <span data-ttu-id="55696-230">Реализации [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) составного файла, автономной и файловой системы NTFS также не поддерживают транзакционные, простые наборы свойств, поскольку эти наборы свойств хранятся в потоках.</span><span class="sxs-lookup"><span data-stu-id="55696-230">The compound file, stand-alone, and NTFS file system implementations of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) similarly do not support transacted, simple property sets because these property sets are stored in streams.</span></span> <span data-ttu-id="55696-231">Однако поддерживаются действия непростых наборов свойств, которые можно создать, указав **\_ непростой флаг пропсетфлаг** в параметре *грффлагс* параметра [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).</span><span class="sxs-lookup"><span data-stu-id="55696-231">However, transactioning of nonsimple property sets, which can be created by specifying the **PROPSETFLAG\_NONSIMPLE** flag in the *grfFlags* parameter of [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), are supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**СТГМ \_**</span><span class="sxs-lookup"><span data-stu-id="55696-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM\_NOSCRATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-233">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="55696-233">0x00100000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-234">Указывает, что в режиме транзакций временный файл рабочей области обычно используется для сохранения изменений до вызова метода **commit** .</span><span class="sxs-lookup"><span data-stu-id="55696-234">Indicates that, in transacted mode, a temporary scratch file is usually used to save modifications until the **Commit** method is called.</span></span> <span data-ttu-id="55696-235">Указание **СТГМ \_ "без нуля** " позволяет использовать неиспользуемую часть исходного файла в качестве рабочего пространства вместо создания нового файла для этой цели.</span><span class="sxs-lookup"><span data-stu-id="55696-235">Specifying **STGM\_NOSCRATCH** permits the unused portion of the original file to be used as work space instead of creating a new file for that purpose.</span></span> <span data-ttu-id="55696-236">Это не влияет на данные в исходном файле, и в некоторых случаях это может привести к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="55696-236">This does not affect the data in the original file, and in certain cases can result in improved performance.</span></span> <span data-ttu-id="55696-237">Нельзя указывать этот флаг без указания **стгм в \_ транзакционном** режиме, и этот флаг можно использовать только в корневом открытом режиме.</span><span class="sxs-lookup"><span data-stu-id="55696-237">It is not valid to specify this flag without also specifying **STGM\_TRANSACTED**, and this flag may only be used in a root open.</span></span> <span data-ttu-id="55696-238">Дополнительные сведения о режиме "Вспомогательная" см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="55696-238">For more information about NoScratch mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**\_моментальный снимок стгм**</span><span class="sxs-lookup"><span data-stu-id="55696-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM\_NOSNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-240">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="55696-240">0x00200000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-241">Этот флаг используется при открытии объекта хранилища с **СТГМ \_ транзакционной** и без **стгм \_ \_ монопольного доступа** или **стгм \_ общий доступ \_ \_ для записи**.</span><span class="sxs-lookup"><span data-stu-id="55696-241">This flag is used when opening a storage object with **STGM\_TRANSACTED** and without **STGM\_SHARE\_EXCLUSIVE** or **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="55696-242">В этом случае при указании параметра **СТГМ \_ snapshot** реализация, предоставляемая системой, не создает копию файла моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="55696-242">In this case, specifying **STGM\_NOSNAPSHOT** prevents the system-provided implementation from creating a snapshot copy of the file.</span></span> <span data-ttu-id="55696-243">Вместо этого изменения в файле записываются в конец файла.</span><span class="sxs-lookup"><span data-stu-id="55696-243">Instead, changes to the file are written to the end of the file.</span></span> <span data-ttu-id="55696-244">Неиспользуемое пространство не освобождается, если только не выполняется консолидация во время фиксации, а в файле имеется только один текущий модуль записи.</span><span class="sxs-lookup"><span data-stu-id="55696-244">Unused space is not reclaimed unless consolidation is performed during the commit, and there is only one current writer on the file.</span></span> <span data-ttu-id="55696-245">Когда файл открывается в режиме без моментального снимка, невозможно выполнить другую операцию, не указывая параметр **СТГМ \_ snapshot**.</span><span class="sxs-lookup"><span data-stu-id="55696-245">When the file is opened in no snapshot mode, another open operation cannot be performed without specifying **STGM\_NOSNAPSHOT**.</span></span> <span data-ttu-id="55696-246">Этот флаг может использоваться только в корневой операции открытия.</span><span class="sxs-lookup"><span data-stu-id="55696-246">This flag may only be used in a root open operation.</span></span> <span data-ttu-id="55696-247">Дополнительные сведения о режиме snapshot см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="55696-247">For more information about NoSnapshot mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**СТГМ \_ Simple**</span><span class="sxs-lookup"><span data-stu-id="55696-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM\_SIMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-249">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="55696-249">0x08000000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-250">Обеспечивает более быструю реализацию составного файла в ограниченном, но часто используемом случае.</span><span class="sxs-lookup"><span data-stu-id="55696-250">Provides a faster implementation of a compound file in a limited, but frequently used, case.</span></span> <span data-ttu-id="55696-251">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="55696-251">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**СТГМ \_ Direct \_ свмр**</span><span class="sxs-lookup"><span data-stu-id="55696-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM\_DIRECT\_SWMR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-253">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="55696-253">0x00400000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-254">Поддерживает прямой режим для операций с файлами с одним модулем записи и чтения.</span><span class="sxs-lookup"><span data-stu-id="55696-254">Supports direct mode for single-writer, multireader file operations.</span></span> <span data-ttu-id="55696-255">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="55696-255">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="55696-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**СТГМ \_ делетеонрелеасе**</span><span class="sxs-lookup"><span data-stu-id="55696-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM\_DELETEONRELEASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55696-257">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="55696-257">0x04000000L</span></span>
</dt> <dt>



<span data-ttu-id="55696-258">Указывает, что базовый файл должен быть автоматически уничтожен при освобождении объекта корневого хранилища.</span><span class="sxs-lookup"><span data-stu-id="55696-258">Indicates that the underlying file is to be automatically destroyed when the root storage object is released.</span></span> <span data-ttu-id="55696-259">Эта функция наиболее полезна для создания временных файлов.</span><span class="sxs-lookup"><span data-stu-id="55696-259">This feature is most useful for creating temporary files.</span></span> <span data-ttu-id="55696-260">Этот флаг можно использовать только при создании корневого объекта, например с помощью [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="55696-260">This flag can only be used when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="55696-261">Это недопустимо при открытии корневого объекта, например с [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), или при создании или открытии подэлемента, например при использовании [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="55696-261">It is not valid when opening a root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), or when creating or opening a subelement, such as with [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="55696-262">Также недопустимо использовать этот флаг и \_ флаг стгм Convert одновременно.</span><span class="sxs-lookup"><span data-stu-id="55696-262">It is also not valid to use this flag and the STGM\_CONVERT flag simultaneously.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55696-263">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55696-263">Remarks</span></span>

<span data-ttu-id="55696-264">Эти флаги можно объединить, но можно выбрать только один флаг из каждой группы связанных флагов.</span><span class="sxs-lookup"><span data-stu-id="55696-264">You can combine these flags, but you can only choose one flag from each group of related flags.</span></span> <span data-ttu-id="55696-265">Обычно один флаг из каждой группы доступа и общего доступа должен быть указан для всех функций и методов, использующих эти константы.</span><span class="sxs-lookup"><span data-stu-id="55696-265">Typically one flag from each of the access and sharing groups must be specified for all functions and methods which use these constants.</span></span> <span data-ttu-id="55696-266">Флаги из других групп являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="55696-266">Flags from other groups are optional.</span></span>

### <a name="transacted-mode"></a><span data-ttu-id="55696-267">Режим транзакций</span><span class="sxs-lookup"><span data-stu-id="55696-267">Transacted Mode</span></span>

<span data-ttu-id="55696-268">Если указан флаг **стгм \_ Direct**, в группах доступа и совместного доступа можно указать только одно из следующих сочетаний флагов.</span><span class="sxs-lookup"><span data-stu-id="55696-268">When the **STGM\_DIRECT** flag is specified, only one of the following combination of flags may be specified from the access and sharing groups.</span></span>

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

<span data-ttu-id="55696-269">Имейте в виду, что режим Direct подразумевает отсутствие **\_ транзакции стгм**.</span><span class="sxs-lookup"><span data-stu-id="55696-269">Be aware that direct mode is implied by the absence of **STGM\_TRANSACTED**.</span></span> <span data-ttu-id="55696-270">То есть если не указаны ни **стгм \_ Direct** , ни стгм, то предполагается, что используется значение **стгм \_ Direct** . **\_**</span><span class="sxs-lookup"><span data-stu-id="55696-270">That is, if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified, **STGM\_DIRECT** is assumed.</span></span>

<span data-ttu-id="55696-271">При указании флага **\_ транзакций стгм** объекты создаются или открываются в режиме транзакций.</span><span class="sxs-lookup"><span data-stu-id="55696-271">When the **STGM\_TRANSACTED** flag is specified, objects are created or opened in transacted mode.</span></span> <span data-ttu-id="55696-272">В этом режиме изменения объекта не сохраняются до тех пор, пока они не будут зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="55696-272">In this mode, changes to an object do not persist until they are committed.</span></span> <span data-ttu-id="55696-273">Например, изменения в объекте хранилища транзакций не сохраняются до тех пор, пока не будет вызван метод [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) .</span><span class="sxs-lookup"><span data-stu-id="55696-273">For example, changes to a transacted storage object are not persisted until the [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) method is called.</span></span> <span data-ttu-id="55696-274">Изменения такого объекта хранилища будут потеряны, если объект хранилища освобожден (окончательный выпуск) перед вызовом метода **commit** или если вызывается метод [**IStorage:: revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) .</span><span class="sxs-lookup"><span data-stu-id="55696-274">Changes to such a storage object will be lost if the storage object is released (final release) before the **Commit** method is called, or if the [**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) method is called.</span></span>

<span data-ttu-id="55696-275">При создании или открытии объекта в режиме транзакций реализация должна хранить как исходные данные, так и обновления этих данных, чтобы при необходимости можно было отменить изменения.</span><span class="sxs-lookup"><span data-stu-id="55696-275">When an object is created or opened in transacted mode, the implementation must keep both the original data and updates to this data, so that updates can be reverted if necessary.</span></span> <span data-ttu-id="55696-276">Обычно это выполняется путем записи изменений во вспомогательную область до их фиксации или создания копии, называемой моментальным снимком, из последних зафиксированных данных.</span><span class="sxs-lookup"><span data-stu-id="55696-276">This is typically performed by writing changes to a scratch area until they are committed, or by creating a copy, called a snapshot, of the most recently committed data.</span></span>

<span data-ttu-id="55696-277">При открытии объекта корневого хранилища в режиме транзакций расположение и поведение вспомогательных данных и копий моментальных снимков можно контролировать для оптимизации производительности с помощью флагов **стгм \_** и **стгм \_ snapshot** .</span><span class="sxs-lookup"><span data-stu-id="55696-277">When a root storage object is opened in transacted mode, the location and behavior of the scratch data and the snapshot copies can be controlled to optimize performance with the **STGM\_NOSCRATCH** and **STGM\_NOSNAPSHOT** flags.</span></span> <span data-ttu-id="55696-278">(Объект корневого хранилища получен из, например функции [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ; объект хранилища, полученный из метода [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , является объектом подхранилища.) Как правило, данные и моментальные снимки хранятся во временных файлах, отделенных от хранилища.</span><span class="sxs-lookup"><span data-stu-id="55696-278">(A root storage object is obtained from, for example, the [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function; a storage object obtained from the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method is a substorage object.) Typically, the scratch data and snapshots are stored in temporary files, separate from the storage.</span></span>

<span data-ttu-id="55696-279">Воздействие этих флагов зависит от числа читателей и/или модулей записи, обращающихся к корневому хранилищу.</span><span class="sxs-lookup"><span data-stu-id="55696-279">The effect of these flags depends on the number of readers and/or writers accessing the root storage.</span></span>

<span data-ttu-id="55696-280">В случае с однозаписывающим режимом объект хранилища в режиме транзакций открывается для доступа на запись и не может быть другим доступом к файлу.</span><span class="sxs-lookup"><span data-stu-id="55696-280">In the "single-writer" case, a transacted mode storage object is opened for write access and there can be no other access to the file.</span></span> <span data-ttu-id="55696-281">Это значит, что файл открыт с использованием **СТГМ \_ транзакций**, доступа **стгм \_ Write** или **стгм \_ ReadWrite** и совместного использования **стгм \_ общего ресурса \_**.</span><span class="sxs-lookup"><span data-stu-id="55696-281">That is, the file is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_EXCLUSIVE**.</span></span> <span data-ttu-id="55696-282">В этом случае изменения объекта хранилища записываются во вспомогательную область.</span><span class="sxs-lookup"><span data-stu-id="55696-282">In this case, changes to the storage object are written to the scratch area.</span></span> <span data-ttu-id="55696-283">Когда эти изменения фиксируются, они копируются в исходное хранилище.</span><span class="sxs-lookup"><span data-stu-id="55696-283">When those changes are committed, they are copied to the original storage.</span></span> <span data-ttu-id="55696-284">Таким образом, если в объект хранилища фактически не вносятся никакие изменения, ненужная перенаправление данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55696-284">Therefore, if no changes are actually made to the storage object, there will be no unnecessary data transfer.</span></span>

<span data-ttu-id="55696-285">В случае с несколькими модулями записи объект хранилища транзакций открывается для доступа на запись, но используется совместно в таких асвай, как и для других модулей записи.</span><span class="sxs-lookup"><span data-stu-id="55696-285">In the "multiple-writer" case, a transacted storage object is opened for write access, but is shared in such asway as to allow other writers.</span></span> <span data-ttu-id="55696-286">Это значит, что объект хранилища открыт с помощью **СТГМ \_ транзакций**, доступа к **стгм \_ Write** или **стгм \_ ReadWrite** и совместного использования **стгм \_ Share \_ \_ Reread**.</span><span class="sxs-lookup"><span data-stu-id="55696-286">That is, the storage object is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_DENY\_READ**.</span></span> <span data-ttu-id="55696-287">Если вместо этого используется совместное использование **стгм \_ Share \_ Deny \_ None** , то используется вариант "множественный модуль записи, несколько модулей чтения".</span><span class="sxs-lookup"><span data-stu-id="55696-287">If sharing of **STGM\_SHARE\_DENY\_NONE** is specified instead, then the case is "multiple-writer, multiple-reader".</span></span> <span data-ttu-id="55696-288">В таких случаях во время операции открытия будет создан моментальный снимок исходных данных.</span><span class="sxs-lookup"><span data-stu-id="55696-288">In these cases, a snapshot of the original data will be made during the open operation.</span></span> <span data-ttu-id="55696-289">Таким образом, даже если в хранилище не вносятся какие-либо изменения и (или) они не открываются одновременно с другим модулем записи, при открытии все еще необходимо передавать данные.</span><span class="sxs-lookup"><span data-stu-id="55696-289">Therefore, even if no changes are actually made to the storage and/or it is not actually opened by another writer simultaneously, data transfer is still necessary during the open.</span></span> <span data-ttu-id="55696-290">В результате можно получить лучшую производительность с открытым временем, открыв объект хранилища в **стгм \_ Share \_ запретить \_ запись** или **стгм \_ Общий \_ монопольный** режим.</span><span class="sxs-lookup"><span data-stu-id="55696-290">As a result the best open-time performance can be obtained by opening the storage object in **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** modes.</span></span> <span data-ttu-id="55696-291">Дополнительные сведения о том, как изменения фиксируются при наличии нескольких модулей записи, см. в разделе [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span><span class="sxs-lookup"><span data-stu-id="55696-291">For more information about how changes are committed when there are multiple writers, see [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span></span>

<span data-ttu-id="55696-292">В варианте "один модуль записи, несколько читающих" объект хранилища транзакций открывается для доступа на запись, но совместно используется читателями.</span><span class="sxs-lookup"><span data-stu-id="55696-292">In the "single-writer, multiple-reader" case, a transacted storage object is opened for write access, but is shared with readers.</span></span> <span data-ttu-id="55696-293">Это значит, что объект хранилища открывается модулем записи с **СТГМ \_ транзакционной**, доступом к **стгм \_ ReadWrite** или **стгм \_ Write**, а также совместное использование **стгм \_ Share \_ Deny \_ Write**.</span><span class="sxs-lookup"><span data-stu-id="55696-293">That is, the storage object is opened by the writer with **STGM\_TRANSACTED**, access of **STGM\_READWRITE** or **STGM\_WRITE**, and sharing of **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="55696-294">Хранилище открывается модулями чтения с **СТГМ \_ транзакций**, доступом **стгм \_ Read** и совместной работы **стгм \_ Share \_ Deny \_ None**.</span><span class="sxs-lookup"><span data-stu-id="55696-294">The storage is opened by readers with **STGM\_TRANSACTED**, access of **STGM\_READ**, and sharing of **STGM\_SHARE\_DENY\_NONE**.</span></span> <span data-ttu-id="55696-295">В этом случае модуль записи использует вспомогательную область для хранения незафиксированных изменений.</span><span class="sxs-lookup"><span data-stu-id="55696-295">In this case the writer uses the scratch area to store uncommitted changes.</span></span> <span data-ttu-id="55696-296">Как и в приведенных выше случаях, средство чтения приводит к снижению производительности при создании копии моментального снимка данных.</span><span class="sxs-lookup"><span data-stu-id="55696-296">As in the cases above, the reader incurs an open-time performance penalty while a snapshot copy of the data is created.</span></span>

<span data-ttu-id="55696-297">Обычно вспомогательная область является временным файлом, отделенным от исходных данных.</span><span class="sxs-lookup"><span data-stu-id="55696-297">Typically, the scratch area is a temporary file, separate from the original data.</span></span> <span data-ttu-id="55696-298">При фиксации изменений в исходном файле данные должны быть переданы из временного файла.</span><span class="sxs-lookup"><span data-stu-id="55696-298">When changes are committed to the original file, the data must be transferred from the temporary file.</span></span> <span data-ttu-id="55696-299">Чтобы избежать этой пересылки данных, **можно \_ указать флаг стгм**.</span><span class="sxs-lookup"><span data-stu-id="55696-299">To avoid this data transfer, the **STGM\_NOSCRATCH** flag may be specified.</span></span> <span data-ttu-id="55696-300">Если этот флаг указан, для вспомогательной области используются части файлового файла хранилища, а не отдельный временный файл.</span><span class="sxs-lookup"><span data-stu-id="55696-300">When this flag is specified, portions of the storage object file are used for the scratch area, rather than a separate temporary file.</span></span> <span data-ttu-id="55696-301">В результате фиксация изменений может выполняться быстро, так как требуется небольшое перемещение данных.</span><span class="sxs-lookup"><span data-stu-id="55696-301">As a result, committing changes can be performed quickly, because little data transfer is required.</span></span> <span data-ttu-id="55696-302">Недостаток заключается в том, что размер файла хранилища может быть больше, чем в противном случае, поскольку он должен быть достаточно большим для исходных данных и вспомогательной области.</span><span class="sxs-lookup"><span data-stu-id="55696-302">The disadvantage is that the storage file can become larger than it would otherwise be, because it must be grown to be large enough for both the original data and the scratch area.</span></span> <span data-ttu-id="55696-303">Чтобы консолидировать данные и удалить ненужную область, повторно откройте корневое хранилище в режиме транзакций, но без установки флага **стгм. \_**</span><span class="sxs-lookup"><span data-stu-id="55696-303">To consolidate the data and remove this unnecessary area, reopen the root storage in transacted mode, but without setting the **STGM\_NOSCRATCH** flag.</span></span> <span data-ttu-id="55696-304">Затем вызовите метод [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) с установленным флагом **\_ консолидации стгк** .</span><span class="sxs-lookup"><span data-stu-id="55696-304">Then, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) with the **STGC\_CONSOLIDATE** flag set.</span></span>

<span data-ttu-id="55696-305">Область моментального снимка, как и вспомогательная область, также обычно является временным файлом, и это тоже может повлиять на флаг СТГМ.</span><span class="sxs-lookup"><span data-stu-id="55696-305">The snapshot area, like the scratch area, is also, typically, a temporary file, and this too can be affected with a STGM flag.</span></span> <span data-ttu-id="55696-306">При указании флага Стгм не создается отдельный временный файл моментального снимка. **\_**</span><span class="sxs-lookup"><span data-stu-id="55696-306">By specifying the **STGM\_NOSNAPSHOT** flag, a separate temporary snapshot file is not created.</span></span> <span data-ttu-id="55696-307">Вместо этого исходные данные никогда не изменяются, даже если имеется один или несколько модулей записи для каждого объекта.</span><span class="sxs-lookup"><span data-stu-id="55696-307">Instead, the original data is never modified, even if there are one or more writers per object.</span></span> <span data-ttu-id="55696-308">После фиксации изменений они добавляются в файл, но исходные данные остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="55696-308">When changes are committed, they are added to the file, but the original data remains intact.</span></span> <span data-ttu-id="55696-309">Этот режим повышает эффективность, поскольку сокращает время выполнения, устраняя необходимость создания моментального снимка во время операции открытия.</span><span class="sxs-lookup"><span data-stu-id="55696-309">This mode increases efficiency because it reduces run time by eliminating the requirement of creating a snapshot during the open operation.</span></span> <span data-ttu-id="55696-310">Однако использование этого режима может привести к созданию очень большого файла хранилища, поскольку данные в файле никогда не могут быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="55696-310">However, using this mode may result in a very large storage file because data in the file can never be overwritten.</span></span> <span data-ttu-id="55696-311">Это ограничение не ограничивает размер файлов, открытых в режиме "без моментальных снимков".</span><span class="sxs-lookup"><span data-stu-id="55696-311">This is no limit to the size of files opened in NoSnapshot mode.</span></span>

### <a name="direct-single-writer-multiple-reader-mode"></a><span data-ttu-id="55696-312">Прямой однозаписывающий, Multiple-Readerный режим</span><span class="sxs-lookup"><span data-stu-id="55696-312">Direct Single-Writer, Multiple-Reader Mode</span></span>

<span data-ttu-id="55696-313">Как уже говорилось, возможно наличие одного модуля записи и нескольких модулей чтения объекта хранилища, если этот объект открыт в режиме транзакций.</span><span class="sxs-lookup"><span data-stu-id="55696-313">As described, it is possible to have a single writer and multiple readers of a storage object, if that object is opened in transacted mode.</span></span> <span data-ttu-id="55696-314">Кроме того, можно выполнить одномодульный режим с одним модулем чтения в прямом режиме, указав флаг **стгм \_ Direct \_ свмр** .</span><span class="sxs-lookup"><span data-stu-id="55696-314">It is also possible to achieve the single-writer, multireader case in direct mode, by specifying the **STGM\_DIRECT\_SWMR** flag.</span></span>

<span data-ttu-id="55696-315">В режиме **стгм \_ Direct \_ свмр** один вызывающий элемент может открыть объект для доступа на чтение и запись, тогда как другие вызывающие объекты одновременно открывают файл для доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="55696-315">In **STGM\_DIRECT\_SWMR** mode, it is possible for one caller to open an object for read/write access, while other callers simultaneously have the file open for read-only access.</span></span> <span data-ttu-id="55696-316">Использование этого флага в сочетании с флагом **\_ транзакций стгм** не допускается.</span><span class="sxs-lookup"><span data-stu-id="55696-316">It is not valid to use this flag in combination with the **STGM\_TRANSACTED** flag.</span></span> <span data-ttu-id="55696-317">В этом режиме модуль записи открывает объект со следующими флагами:</span><span class="sxs-lookup"><span data-stu-id="55696-317">In this mode, the writer opens the object with the following flags:</span></span>

<span data-ttu-id="55696-318">**Стгм \_ Direct \_ свмр** \| **стгм \_ ReadWrite** \| **стгм \_ Share \_ дениврите**</span><span class="sxs-lookup"><span data-stu-id="55696-318">**STGM\_DIRECT\_SWMR** \| **STGM\_READWRITE** \| **STGM\_SHARE\_DENYWRITE**</span></span>

<span data-ttu-id="55696-319">Каждый из читателей открывает объект со следующими флагами:</span><span class="sxs-lookup"><span data-stu-id="55696-319">and each of the readers opens the object with these flags:</span></span>

<span data-ttu-id="55696-320">**Стгм \_ Direct \_ свмр** \| **стгм \_ Read** \| **стгм \_ Share \_ Deny \_ None**</span><span class="sxs-lookup"><span data-stu-id="55696-320">**STGM\_DIRECT\_SWMR** \| **STGM\_READ** \| **STGM\_SHARE\_DENY\_NONE**</span></span>

<span data-ttu-id="55696-321">В этом режиме для изменения объекта хранилища модуль записи должен получить монопольный доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="55696-321">In this mode, to modify the storage object, the writer must get exclusive access to the object.</span></span> <span data-ttu-id="55696-322">Это возможно, когда все читатели закрыли его.</span><span class="sxs-lookup"><span data-stu-id="55696-322">This is possible when all the readers have closed it.</span></span> <span data-ttu-id="55696-323">Для получения этого эксклюзивного доступа модуль записи использует интерфейс [**идиректвритерлокк**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) .</span><span class="sxs-lookup"><span data-stu-id="55696-323">The writer uses the [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) interface to obtain this exclusive access.</span></span>

### <a name="simple-mode"></a><span data-ttu-id="55696-324">Простой режим</span><span class="sxs-lookup"><span data-stu-id="55696-324">Simple Mode</span></span>

<span data-ttu-id="55696-325">Простой режим (**стгм \_ Simple**) удобен для приложений, выполняющих полную операцию сохранения.</span><span class="sxs-lookup"><span data-stu-id="55696-325">Simple mode (**STGM\_SIMPLE**) is useful for applications that perform complete save operations.</span></span> <span data-ttu-id="55696-326">Он эффективен, но имеет следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="55696-326">It is efficient, but has the following constraints:</span></span>

-   <span data-ttu-id="55696-327">Для подхранилищ не существует поддержки.</span><span class="sxs-lookup"><span data-stu-id="55696-327">No support exists for substorages.</span></span>
-   <span data-ttu-id="55696-328">Объект хранилища и полученные из него объекты потока не могут быть упакованы.</span><span class="sxs-lookup"><span data-stu-id="55696-328">The storage object, and stream objects obtained from it, cannot be marshaled.</span></span>
-   <span data-ttu-id="55696-329">Каждый поток имеет минимальный размер.</span><span class="sxs-lookup"><span data-stu-id="55696-329">Each stream has a minimum size.</span></span> <span data-ttu-id="55696-330">Если при освобождении потока в поток записывается меньшее количество байтов, размер потока увеличивается до минимального.</span><span class="sxs-lookup"><span data-stu-id="55696-330">If fewer than the minimum bytes are written into a stream when the stream is released, the stream is extended to the minimum size.</span></span> <span data-ttu-id="55696-331">Например, минимальный размер для конкретной реализации [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) — 4 КБ.</span><span class="sxs-lookup"><span data-stu-id="55696-331">For example, the minimum size for a particular [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) implementation is 4 KB.</span></span> <span data-ttu-id="55696-332">Создается поток, и в него записывается 1 КБ.</span><span class="sxs-lookup"><span data-stu-id="55696-332">A stream is created and 1 KB is written to it.</span></span> <span data-ttu-id="55696-333">В окончательном выпуске этого **IStream** размер потока будет автоматически расширен до 4 КБ.</span><span class="sxs-lookup"><span data-stu-id="55696-333">At the final release of that **IStream**, the stream size will be automatically extended to 4 KB.</span></span> <span data-ttu-id="55696-334">Затем, открыв поток и вызвав метод [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) , вы увидите размер 4 КБ.</span><span class="sxs-lookup"><span data-stu-id="55696-334">Subsequently, opening the stream and calling the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method will show a size of 4 KB.</span></span>
-   <span data-ttu-id="55696-335">Реализация не поддерживает все методы [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) и [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="55696-335">Not all methods of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) will be supported by the implementation.</span></span> <span data-ttu-id="55696-336">Дополнительные сведения см. в статьях [реализация составного файла IStorage](istorage-compound-file-implementation.md)и [реализация составного файла IStream](istream-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="55696-336">For more information, see [IStorage - Compound File Implementation](istorage-compound-file-implementation.md), and [IStream - Compound File Implementation](istream-compound-file-implementation.md).</span></span>

<span data-ttu-id="55696-337">[Маршалирование](/windows/desktop/Midl/marshaling-ole-data-types) — это процесс упаковки, распаковки и отправки параметров метода интерфейса через границы потока или процесса в рамках удаленного вызова процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="55696-337">[Marshaling](/windows/desktop/Midl/marshaling-ole-data-types) is the process of packaging, unpackaging, and sending interface method parameters across thread or process boundaries within a Remote Procedure Call (RPC).</span></span> <span data-ttu-id="55696-338">Дополнительные сведения см. в разделе [сведения о маршалировании](../com/marshaling-details.md) и [маршалирование интерфейса](../com/interface-marshaling.md).</span><span class="sxs-lookup"><span data-stu-id="55696-338">For more information, see [Marshaling Details](../com/marshaling-details.md) and [Interface Marshaling](../com/interface-marshaling.md).</span></span>

<span data-ttu-id="55696-339">Когда объект хранилища получается операцией Create в простом режиме:</span><span class="sxs-lookup"><span data-stu-id="55696-339">When a storage object is obtained by a Create operation in simple mode:</span></span>

-   <span data-ttu-id="55696-340">Элементы потока можно создавать, но нельзя открывать.</span><span class="sxs-lookup"><span data-stu-id="55696-340">Stream elements can be created, but not opened.</span></span>
-   <span data-ttu-id="55696-341">При создании элемента потока путем вызова метода [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)невозможно создать другой поток, пока не будет освобожден объект потока.</span><span class="sxs-lookup"><span data-stu-id="55696-341">When a stream element is created by calling [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), it is not possible to create another stream until that stream object is released.</span></span>
-   <span data-ttu-id="55696-342">После записи всех потоков вызовите метод [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) , чтобы сбросить изменения.</span><span class="sxs-lookup"><span data-stu-id="55696-342">After all streams are written, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) to flush the changes.</span></span>

<span data-ttu-id="55696-343">Когда объект хранилища получается операцией открытия в простом режиме:</span><span class="sxs-lookup"><span data-stu-id="55696-343">When a storage object is obtained by an Open operation in simple mode:</span></span>

-   <span data-ttu-id="55696-344">В каждый момент времени можно открыть только один элемент потока.</span><span class="sxs-lookup"><span data-stu-id="55696-344">It is possible to open only one stream element at a time.</span></span>
-   <span data-ttu-id="55696-345">Изменить размер потока путем вызова метода [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) или путем поиска или записи после конца потока невозможно.</span><span class="sxs-lookup"><span data-stu-id="55696-345">It is not possible to change the size of a stream by calling the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method or by seeking or writing beyond the end of the stream.</span></span> <span data-ttu-id="55696-346">Однако, поскольку все потоки имеют минимальный размер, можно использовать поток вплоть до такого размера, даже если в него были записаны меньше данных.</span><span class="sxs-lookup"><span data-stu-id="55696-346">However, because all streams are of a minimum size, it is possible to use the stream up to that size, even if less data was originally written to it.</span></span> <span data-ttu-id="55696-347">Чтобы определить размер потока, используйте метод [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) .</span><span class="sxs-lookup"><span data-stu-id="55696-347">To determine the size of a stream, use the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method.</span></span>

<span data-ttu-id="55696-348">Имейте в виду, что если элемент хранения изменяется объектом хранилища, который не находится в простом режиме, невозможно снова открыть этот элемент хранилища в простом режиме.</span><span class="sxs-lookup"><span data-stu-id="55696-348">Be aware that, if a storage element is modified by a storage object that is not in simple mode, it will not be possible, again, to open that storage element in simple mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="55696-349">Требования</span><span class="sxs-lookup"><span data-stu-id="55696-349">Requirements</span></span>



| <span data-ttu-id="55696-350">Требование</span><span class="sxs-lookup"><span data-stu-id="55696-350">Requirement</span></span> | <span data-ttu-id="55696-351">Значение</span><span class="sxs-lookup"><span data-stu-id="55696-351">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55696-352">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55696-352">Minimum supported client</span></span><br/> | <span data-ttu-id="55696-353">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55696-353">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="55696-354">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55696-354">Minimum supported server</span></span><br/> | <span data-ttu-id="55696-355">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55696-355">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="55696-356">Заголовок</span><span class="sxs-lookup"><span data-stu-id="55696-356">Header</span></span><br/>                   | <dl> <span data-ttu-id="55696-357"><dt>Обжбасе. h</dt></span><span class="sxs-lookup"><span data-stu-id="55696-357"><dt>ObjBase.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55696-358">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55696-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55696-359">**ISequentialStream:: Read**</span><span class="sxs-lookup"><span data-stu-id="55696-359">**ISequentialStream::Read**</span></span>](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[<span data-ttu-id="55696-360">**Метод IStorage**</span><span class="sxs-lookup"><span data-stu-id="55696-360">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="55696-361">**стгкреатедокфиле**</span><span class="sxs-lookup"><span data-stu-id="55696-361">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="55696-362">**стгкреатедокфилеонилоккбитес**</span><span class="sxs-lookup"><span data-stu-id="55696-362">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[<span data-ttu-id="55696-363">**стгкреатесторажеекс**</span><span class="sxs-lookup"><span data-stu-id="55696-363">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="55696-364">**стгопенстораже**</span><span class="sxs-lookup"><span data-stu-id="55696-364">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="55696-365">**стгопенсторажеекс**</span><span class="sxs-lookup"><span data-stu-id="55696-365">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[<span data-ttu-id="55696-366">**стгопенсторажеонилоккбитес**</span><span class="sxs-lookup"><span data-stu-id="55696-366">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

