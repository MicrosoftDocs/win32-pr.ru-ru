---
description: Интерфейс Ибитебуффер предназначен для чтения, записи и управления объектами потоков. Этот объект по сути является оболочкой для объекта IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Интерфейс Ибитебуффер (Скардссп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999302"
---
# <a name="ibytebuffer-interface"></a><span data-ttu-id="4e000-104">Интерфейс Ибитебуффер</span><span class="sxs-lookup"><span data-stu-id="4e000-104">IByteBuffer interface</span></span>

<span data-ttu-id="4e000-105">\[Интерфейс **ибитебуффер** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4e000-105">\[The **IByteBuffer** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4e000-106">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4e000-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4e000-107">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="4e000-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="4e000-108">Интерфейс **ибитебуффер** предназначен для чтения, записи и управления объектами потоков.</span><span class="sxs-lookup"><span data-stu-id="4e000-108">The **IByteBuffer** interface is provided to read, write and manage stream objects.</span></span> <span data-ttu-id="4e000-109">Этот объект по сути является оболочкой для объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="4e000-109">This object essentially is a wrapper for the **IStream** object.</span></span>

## <a name="members"></a><span data-ttu-id="4e000-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="4e000-110">Members</span></span>

<span data-ttu-id="4e000-111">Интерфейс **ибитебуффер** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4e000-111">The **IByteBuffer** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4e000-112">**Ибитебуффер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4e000-112">**IByteBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="4e000-113">Методы</span><span class="sxs-lookup"><span data-stu-id="4e000-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4e000-114">Методы</span><span class="sxs-lookup"><span data-stu-id="4e000-114">Methods</span></span>

<span data-ttu-id="4e000-115">Интерфейс **ибитебуффер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4e000-115">The **IByteBuffer** interface has these methods.</span></span>



| <span data-ttu-id="4e000-116">Метод</span><span class="sxs-lookup"><span data-stu-id="4e000-116">Method</span></span>                                           | <span data-ttu-id="4e000-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4e000-117">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e000-118">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="4e000-118">**Clone**</span></span>](ibytebuffer-clone.md)               | <span data-ttu-id="4e000-119">Создает точную копию объекта **ибитебуффер** .</span><span class="sxs-lookup"><span data-stu-id="4e000-119">Clones an **IByteBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="4e000-120">**Сохраните**</span><span class="sxs-lookup"><span data-stu-id="4e000-120">**Commit**</span></span>](ibytebuffer-commit.md)             | <span data-ttu-id="4e000-121">Фиксирует [*транзакцию*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="4e000-121">Commits a [*transaction*](/windows/desktop/SecGloss/t-gly).</span></span><br/> |
| [<span data-ttu-id="4e000-122">**CopyTo**</span><span class="sxs-lookup"><span data-stu-id="4e000-122">**CopyTo**</span></span>](ibytebuffer-copyto.md)             | <span data-ttu-id="4e000-123">Копирует байты в другой объект.</span><span class="sxs-lookup"><span data-stu-id="4e000-123">Copies bytes to another object.</span></span><br/>                                                                |
| [<span data-ttu-id="4e000-124">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="4e000-124">**Initialize**</span></span>](ibytebuffer-initialize.md)     | <span data-ttu-id="4e000-125">Инициализирует объект **ибитебуффер** .</span><span class="sxs-lookup"><span data-stu-id="4e000-125">Initializes the **IByteBuffer** object.</span></span><br/>                                                        |
| [<span data-ttu-id="4e000-126">**LockRegion**</span><span class="sxs-lookup"><span data-stu-id="4e000-126">**LockRegion**</span></span>](ibytebuffer-lockregion.md)     | <span data-ttu-id="4e000-127">Разрешает доступ к диапазону байтов.</span><span class="sxs-lookup"><span data-stu-id="4e000-127">Restricts access to a range of bytes.</span></span><br/>                                                          |
| [<span data-ttu-id="4e000-128">**Просмотр**</span><span class="sxs-lookup"><span data-stu-id="4e000-128">**Read**</span></span>](ibytebuffer-read.md)                 | <span data-ttu-id="4e000-129">Считывает байты в память.</span><span class="sxs-lookup"><span data-stu-id="4e000-129">Reads bytes into memory.</span></span><br/>                                                                       |
| [<span data-ttu-id="4e000-130">**Верните**</span><span class="sxs-lookup"><span data-stu-id="4e000-130">**Revert**</span></span>](ibytebuffer-revert.md)             | <span data-ttu-id="4e000-131">Отклоняет изменения с момента последнего вызова [**фиксации**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="4e000-131">Discards changes since the last [**Commit**](ibytebuffer-commit.md) call.</span></span><br/>                     |
| [<span data-ttu-id="4e000-132">**Seek**</span><span class="sxs-lookup"><span data-stu-id="4e000-132">**Seek**</span></span>](ibytebuffer-seek.md)                 | <span data-ttu-id="4e000-133">Изменяет указатель поиска.</span><span class="sxs-lookup"><span data-stu-id="4e000-133">Changes the seek pointer.</span></span><br/>                                                                      |
| [<span data-ttu-id="4e000-134">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="4e000-134">**SetSize**</span></span>](ibytebuffer-setsize.md)           | <span data-ttu-id="4e000-135">Изменяет размер объекта-потока.</span><span class="sxs-lookup"><span data-stu-id="4e000-135">Changes the size of the stream object.</span></span><br/>                                                         |
| [<span data-ttu-id="4e000-136">**STAT**</span><span class="sxs-lookup"><span data-stu-id="4e000-136">**Stat**</span></span>](ibytebuffer-stat.md)                 | <span data-ttu-id="4e000-137">Получает статистические сведения о потоке.</span><span class="sxs-lookup"><span data-stu-id="4e000-137">Retrieves statistical information about a stream.</span></span><br/>                                              |
| [<span data-ttu-id="4e000-138">**UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="4e000-138">**UnlockRegion**</span></span>](ibytebuffer-unlockregion.md) | <span data-ttu-id="4e000-139">Удаляет ограничение доступа, установленное ранее [**LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="4e000-139">Removes access restriction previously set by [**LockRegion**](ibytebuffer-lockregion.md).</span></span><br/>     |
| [<span data-ttu-id="4e000-140">**Будет**</span><span class="sxs-lookup"><span data-stu-id="4e000-140">**Write**</span></span>](ibytebuffer-write.md)               | <span data-ttu-id="4e000-141">Записывает байты в поток.</span><span class="sxs-lookup"><span data-stu-id="4e000-141">Writes bytes to the stream.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="4e000-142">Требования</span><span class="sxs-lookup"><span data-stu-id="4e000-142">Requirements</span></span>



| <span data-ttu-id="4e000-143">Требование</span><span class="sxs-lookup"><span data-stu-id="4e000-143">Requirement</span></span> | <span data-ttu-id="4e000-144">Значение</span><span class="sxs-lookup"><span data-stu-id="4e000-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e000-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e000-145">Minimum supported client</span></span><br/> | <span data-ttu-id="4e000-146">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4e000-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4e000-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e000-147">Minimum supported server</span></span><br/> | <span data-ttu-id="4e000-148">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e000-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e000-149">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4e000-149">End of client support</span></span><br/>    | <span data-ttu-id="4e000-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4e000-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4e000-151">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4e000-151">End of server support</span></span><br/>    | <span data-ttu-id="4e000-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4e000-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4e000-153">Header</span><span class="sxs-lookup"><span data-stu-id="4e000-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e000-154"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e000-154"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e000-155">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4e000-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="4e000-156"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4e000-156"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4e000-157">DLL</span><span class="sxs-lookup"><span data-stu-id="4e000-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e000-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e000-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4e000-159">IID</span><span class="sxs-lookup"><span data-stu-id="4e000-159">IID</span></span><br/>                      | <span data-ttu-id="4e000-160">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="4e000-160">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

