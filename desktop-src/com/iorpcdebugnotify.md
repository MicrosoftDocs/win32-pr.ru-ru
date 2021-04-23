---
title: Интерфейс Иорпкдебугнотифи
description: Предоставляет функции удаленной отладки.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- COM интерфейса Иорпкдебугнотифи
- Интерфейс COM интерфейса Иорпкдебугнотифи, описание
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535441"
---
# <a name="iorpcdebugnotify-interface"></a><span data-ttu-id="e56fe-105">Интерфейс Иорпкдебугнотифи</span><span class="sxs-lookup"><span data-stu-id="e56fe-105">IOrpcDebugNotify interface</span></span>

<span data-ttu-id="e56fe-106">Предоставляет функции удаленной отладки.</span><span class="sxs-lookup"><span data-stu-id="e56fe-106">Provides remote debugging functionality.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="e56fe-107">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="e56fe-107">When to implement</span></span>

<span data-ttu-id="e56fe-108">Реализуйте этот интерфейс, чтобы включить удаленную отладку через RPC.</span><span class="sxs-lookup"><span data-stu-id="e56fe-108">Implement this interface to enable remote debugging over RPC.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e56fe-109">Назначение</span><span class="sxs-lookup"><span data-stu-id="e56fe-109">When to use</span></span>

<span data-ttu-id="e56fe-110">Этот интерфейс следует использовать для внутрипроцессного удаленной отладки, когда программные исключения не следует использовать для уведомлений отладчика COM.</span><span class="sxs-lookup"><span data-stu-id="e56fe-110">This interface should be used for in-process remote debugging when software exceptions should not be used for the COM debugger notifications.</span></span> <span data-ttu-id="e56fe-111">Он позволяет выполнять внутрипроцессный отладчики для получения уведомлений от прямых вызовов, использующих эти методы.</span><span class="sxs-lookup"><span data-stu-id="e56fe-111">It enables in-process debuggers to be notified by direct calls using these methods.</span></span>

## <a name="members"></a><span data-ttu-id="e56fe-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="e56fe-112">Members</span></span>

<span data-ttu-id="e56fe-113">Интерфейс **иорпкдебугнотифи** наследует от интерфейса [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e56fe-113">The **IOrpcDebugNotify** interface inherits from the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e56fe-114">**Иорпкдебугнотифи** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e56fe-114">**IOrpcDebugNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="e56fe-115">Методы</span><span class="sxs-lookup"><span data-stu-id="e56fe-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e56fe-116">Методы</span><span class="sxs-lookup"><span data-stu-id="e56fe-116">Methods</span></span>

<span data-ttu-id="e56fe-117">Интерфейс **иорпкдебугнотифи** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e56fe-117">The **IOrpcDebugNotify** interface has these methods.</span></span>



| <span data-ttu-id="e56fe-118">Метод</span><span class="sxs-lookup"><span data-stu-id="e56fe-118">Method</span></span>                                                              | <span data-ttu-id="e56fe-119">Описание</span><span class="sxs-lookup"><span data-stu-id="e56fe-119">Description</span></span>                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="e56fe-120">**клиентфиллбуффер**</span><span class="sxs-lookup"><span data-stu-id="e56fe-120">**ClientFillBuffer**</span></span>](iorpcdebugnotify-clientfillbuffer.md)       | <span data-ttu-id="e56fe-121">Отправляет данные из клиентского отладчика в отладчик сервера.</span><span class="sxs-lookup"><span data-stu-id="e56fe-121">Sends data from the client debugger to the server debugger.</span></span><br/>         |
| [<span data-ttu-id="e56fe-122">**клиентжетбуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="e56fe-122">**ClientGetBufferSize**</span></span>](iorpcdebugnotify-clientgetbuffersize.md) | <span data-ttu-id="e56fe-123">Извлекает размер буфера RPC из клиентского отладчика.</span><span class="sxs-lookup"><span data-stu-id="e56fe-123">Retrieves the RPC buffer size from the client-side debugger.</span></span><br/>        |
| [<span data-ttu-id="e56fe-124">**клиентнотифи**</span><span class="sxs-lookup"><span data-stu-id="e56fe-124">**ClientNotify**</span></span>](iorpcdebugnotify-clientnotify.md)               | <span data-ttu-id="e56fe-125">Информирует клиента о том, что исходящий запрос отладчика к серверу.</span><span class="sxs-lookup"><span data-stu-id="e56fe-125">Informs the client of an outgoing debugger request to the server.</span></span><br/>   |
| [<span data-ttu-id="e56fe-126">**серверфиллбуффер**</span><span class="sxs-lookup"><span data-stu-id="e56fe-126">**ServerFillBuffer**</span></span>](iorpcdebugnotify-serverfillbuffer.md)       | <span data-ttu-id="e56fe-127">Отправляет данные из отладчика сервера в клиентский отладчик.</span><span class="sxs-lookup"><span data-stu-id="e56fe-127">Sends data from the server debugger to the client debugger.</span></span><br/>         |
| [<span data-ttu-id="e56fe-128">**сервержетбуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="e56fe-128">**ServerGetBufferSize**</span></span>](iorpcdebugnotify-servergetbuffersize.md) | <span data-ttu-id="e56fe-129">Извлекает размер буфера RPC из отладчика на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="e56fe-129">Retrieves the RPC buffer size from the server-side debugger.</span></span><br/>        |
| [<span data-ttu-id="e56fe-130">**сервернотифи**</span><span class="sxs-lookup"><span data-stu-id="e56fe-130">**ServerNotify**</span></span>](iorpcdebugnotify-servernotify.md)               | <span data-ttu-id="e56fe-131">Информирует сервер о входящем запросе отладчика от клиента.</span><span class="sxs-lookup"><span data-stu-id="e56fe-131">Informs the server of an incoming debugger request from the client.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e56fe-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e56fe-132">Remarks</span></span>

<span data-ttu-id="e56fe-133">Библиотека импорта, содержащая интерфейс **иорпкдебугнотифи** , не включена в пакет средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="e56fe-133">An import library containing the **IOrpcDebugNotify** interface is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e56fe-134">Приложение может использовать функции [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) для получения указателя на функцию [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) из oleaut.dll и предоставления этих методов через интерфейс **иорпкдебугнотифи** .</span><span class="sxs-lookup"><span data-stu-id="e56fe-134">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide these methods via the **IOrpcDebugNotify** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e56fe-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e56fe-135">Requirements</span></span>



| <span data-ttu-id="e56fe-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e56fe-136">Requirement</span></span> | <span data-ttu-id="e56fe-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e56fe-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e56fe-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e56fe-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e56fe-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e56fe-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="e56fe-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e56fe-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e56fe-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e56fe-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e56fe-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e56fe-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e56fe-143"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="e56fe-143"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="e56fe-144">IDL</span><span class="sxs-lookup"><span data-stu-id="e56fe-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e56fe-145"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="e56fe-145"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e56fe-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e56fe-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e56fe-147">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="e56fe-147">**IUnknown**</span></span>](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="e56fe-148">**ОРПК \_ dbg \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="e56fe-148">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="e56fe-149">**\_БУФЕР ОРПК dbg \_**</span><span class="sxs-lookup"><span data-stu-id="e56fe-149">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="e56fe-150">**\_аргументы инициализации \_ ОРПК**</span><span class="sxs-lookup"><span data-stu-id="e56fe-150">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="e56fe-151">**дллдебугобжектрпчук**</span><span class="sxs-lookup"><span data-stu-id="e56fe-151">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> </dl>

 

