---
description: Предоставляет методы, необходимые для поддержки пользователей других интерфейсов COM смарт-карты.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Интерфейс Искардтипеконв (Скарддат. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909656"
---
# <a name="iscardtypeconv-interface"></a><span data-ttu-id="2d0d9-103">Интерфейс Искардтипеконв</span><span class="sxs-lookup"><span data-stu-id="2d0d9-103">ISCardTypeConv interface</span></span>

<span data-ttu-id="2d0d9-104">\[Интерфейс **искардтипеконв** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="2d0d9-104">\[The **ISCardTypeConv** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2d0d9-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2d0d9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2d0d9-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="2d0d9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2d0d9-107">Интерфейс **искардтипеконв** предоставляет методы, необходимые для поддержки пользователей других интерфейсов COM [*смарт-карты*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2d0d9-107">The **ISCardTypeConv** interface provides the methods needed to support the users of the other [*smart card*](../secgloss/s-gly.md) COM interfaces.</span></span> <span data-ttu-id="2d0d9-108">Этот интерфейс предоставляется только для обратной совместимости и больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="2d0d9-108">This interface is provided for backward compatibility only and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="2d0d9-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="2d0d9-109">Members</span></span>

<span data-ttu-id="2d0d9-110">Интерфейс **искардтипеконв** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="2d0d9-110">The **ISCardTypeConv** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="2d0d9-111">**Искардтипеконв** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2d0d9-111">**ISCardTypeConv** also has these types of members:</span></span>

-   [<span data-ttu-id="2d0d9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="2d0d9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2d0d9-113">Методы</span><span class="sxs-lookup"><span data-stu-id="2d0d9-113">Methods</span></span>

<span data-ttu-id="2d0d9-114">Интерфейс **искардтипеконв** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2d0d9-114">The **ISCardTypeConv** interface has these methods.</span></span>



| <span data-ttu-id="2d0d9-115">Метод</span><span class="sxs-lookup"><span data-stu-id="2d0d9-115">Method</span></span>                                                                              | <span data-ttu-id="2d0d9-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2d0d9-116">Description</span></span>                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d0d9-117">**конвертбитеаррайтобитебуффер**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-117">**ConvertByteArrayToByteBuffer**</span></span>](iscardtypeconv-convertbytearraytobytebuffer.md) | <span data-ttu-id="2d0d9-118">Преобразует стандартный массив байтов C/C++ в универсальный буфер байтов (объект **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="2d0d9-118">Converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span><br/>                                   |
| [<span data-ttu-id="2d0d9-119">**конвертбитебуффертобитеаррай**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-119">**ConvertByteBufferToByteArray**</span></span>](iscardtypeconv-convertbytebuffertobytearray.md) | <span data-ttu-id="2d0d9-120">Преобразует массив байтов, сопоставленный в универсальный буфер байтов (объект **IStream** ), в типичный массив байтов C/C++.</span><span class="sxs-lookup"><span data-stu-id="2d0d9-120">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span><br/>          |
| [<span data-ttu-id="2d0d9-121">**конвертбитебуффертосафеаррай**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-121">**ConvertByteBufferToSafeArray**</span></span>](iscardtypeconv-convertbytebuffertosafearray.md) | <span data-ttu-id="2d0d9-122">Преобразует массив байтов, сопоставленный в универсальный буфер байтов (объект **IStream** ), в массив SafeArray неподписанного char (Byte).</span><span class="sxs-lookup"><span data-stu-id="2d0d9-122">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span><br/> |
| [<span data-ttu-id="2d0d9-123">**конвертсафеаррайтобитебуффер**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-123">**ConvertSafeArrayToByteBuffer**</span></span>](iscardtypeconv-convertsafearraytobytebuffer.md) | <span data-ttu-id="2d0d9-124">Преобразует массив байтов, определенный как SAFEARRAY, в универсальный буфер байтов (объект **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="2d0d9-124">Converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span><br/>                          |
| [<span data-ttu-id="2d0d9-125">**креатебитеаррай**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-125">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)                           | <span data-ttu-id="2d0d9-126">Создает массив байтов.</span><span class="sxs-lookup"><span data-stu-id="2d0d9-126">Creates an array of bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="2d0d9-127">**креатебитебуффер**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-127">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)                         | <span data-ttu-id="2d0d9-128">Создает универсальный буфер байтов, сопоставленный с объектом **IStream** ([**ибитебуффер**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="2d0d9-128">Creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span><br/>                  |
| [<span data-ttu-id="2d0d9-129">**креатесафеаррай**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-129">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)                           | <span data-ttu-id="2d0d9-130">Создает SAFEARRAY автоматизации для неподписанных символов (в байтах).</span><span class="sxs-lookup"><span data-stu-id="2d0d9-130">Creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span><br/>                                                              |
| [<span data-ttu-id="2d0d9-131">**фриистреаммемориптр**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-131">**FreeIStreamMemoryPtr**</span></span>](iscardtypeconv-freeistreammemoryptr.md)                 | <span data-ttu-id="2d0d9-132">Освобождает указатель памяти на блок памяти ХГЛОБАЛ, управляемый интерфейсом **IStream** com.</span><span class="sxs-lookup"><span data-stu-id="2d0d9-132">Frees a memory pointer to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span><br/>                                  |
| [<span data-ttu-id="2d0d9-133">**жетатистреаммемори**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-133">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)                     | <span data-ttu-id="2d0d9-134">Получает указатель на байт для блока памяти ХГЛОБАЛ, управляемого интерфейсом **IStream** com.</span><span class="sxs-lookup"><span data-stu-id="2d0d9-134">Acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span><br/>                        |
| [<span data-ttu-id="2d0d9-135">**сизеофистреам**</span><span class="sxs-lookup"><span data-stu-id="2d0d9-135">**SizeOfIStream**</span></span>](iscardtypeconv-sizeofistream.md)                               | <span data-ttu-id="2d0d9-136">Определяет размер (число байтов) интерфейса **IStream** com.</span><span class="sxs-lookup"><span data-stu-id="2d0d9-136">Determines the size (number of bytes) of an **IStream** COM interface.</span></span><br/>                                                       |



 

## <a name="requirements"></a><span data-ttu-id="2d0d9-137">Требования</span><span class="sxs-lookup"><span data-stu-id="2d0d9-137">Requirements</span></span>



| <span data-ttu-id="2d0d9-138">Требование</span><span class="sxs-lookup"><span data-stu-id="2d0d9-138">Requirement</span></span> | <span data-ttu-id="2d0d9-139">Значение</span><span class="sxs-lookup"><span data-stu-id="2d0d9-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d0d9-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d0d9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2d0d9-141">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2d0d9-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2d0d9-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d0d9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2d0d9-143">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d0d9-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2d0d9-144">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2d0d9-144">End of client support</span></span><br/>    | <span data-ttu-id="2d0d9-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2d0d9-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2d0d9-146">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="2d0d9-146">End of server support</span></span><br/>    | <span data-ttu-id="2d0d9-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d0d9-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2d0d9-148">Header</span><span class="sxs-lookup"><span data-stu-id="2d0d9-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d0d9-149"><dt>Скарддат. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d0d9-149"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d0d9-150">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="2d0d9-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d0d9-151"><dt>Скарддат. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2d0d9-151"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2d0d9-152">DLL</span><span class="sxs-lookup"><span data-stu-id="2d0d9-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d0d9-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d0d9-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2d0d9-154">IID</span><span class="sxs-lookup"><span data-stu-id="2d0d9-154">IID</span></span><br/>                      | <span data-ttu-id="2d0d9-155">IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2d0d9-155">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



 

 
