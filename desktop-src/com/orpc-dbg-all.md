---
title: Структура ORPC_DBG_ALL
description: Структура ОРПК \_ dbg \_ ALL используется для передачи параметров методам интерфейса иорпкдебугнотифи.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- ORPC_DBG_ALL структуры COM
- COM LPORPC_DBG_ALL указателя структуры
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135494"
---
# <a name="orpc_dbg_all-structure"></a><span data-ttu-id="223c1-105">ОРПК \_ \_ структуру dbg ALL</span><span class="sxs-lookup"><span data-stu-id="223c1-105">ORPC\_DBG\_ALL structure</span></span>

<span data-ttu-id="223c1-106">Структура **ОРПК \_ dbg \_ ALL** используется для передачи параметров методам интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-106">The **ORPC\_DBG\_ALL** structure is used to pass parameters to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="223c1-107">Каждый метод интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) использует другое сочетание членов, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="223c1-107">Each method of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface uses a different combination of the members below.</span></span> <span data-ttu-id="223c1-108">Если член не обозначен как используемый методом, он не определен при передаче в этот метод.</span><span class="sxs-lookup"><span data-stu-id="223c1-108">If a member is not indicated as used by a method, it is undefined when passed to that method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="223c1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="223c1-109">Syntax</span></span>


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a><span data-ttu-id="223c1-110">Члены</span><span class="sxs-lookup"><span data-stu-id="223c1-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="223c1-111">**псигнатуре**</span><span class="sxs-lookup"><span data-stu-id="223c1-111">**pSignature**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-112">Указатель на буфер **байтов** , содержащий:</span><span class="sxs-lookup"><span data-stu-id="223c1-112">A pointer to a **BYTE** buffer that contains:</span></span>

-   <span data-ttu-id="223c1-113">Первые четыре байта: символы ASCII "МАРБ" при увеличении порядка памяти.</span><span class="sxs-lookup"><span data-stu-id="223c1-113">First four bytes: the ASCII characters "MARB" in increasing memory order.</span></span>
-   <span data-ttu-id="223c1-114">Следующие 16 байт: **идентификатор GUID** , определяющий вызываемое уведомление.</span><span class="sxs-lookup"><span data-stu-id="223c1-114">Next 16 bytes: A **GUID** that identifies the notification being called.</span></span> <span data-ttu-id="223c1-115">Он содержит один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="223c1-115">It contains one of the following:</span></span>
    1.  <span data-ttu-id="223c1-116">[**Клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="223c1-116">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11</span></span>
    2.  <span data-ttu-id="223c1-117">[**Клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="223c1-117">[**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):DA45F3E0-9673-101A-B07B-00DD01113F11</span></span>
    3.  <span data-ttu-id="223c1-118">[**Клиентнотифи**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="223c1-118">[**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11</span></span>
    4.  <span data-ttu-id="223c1-119">[**Сервернотифи**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="223c1-119">[**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11</span></span>
    5.  <span data-ttu-id="223c1-120">[**Сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="223c1-120">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11</span></span>
    6.  <span data-ttu-id="223c1-121">[**Серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11</span><span class="sxs-lookup"><span data-stu-id="223c1-121">[**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11</span></span>
-   <span data-ttu-id="223c1-122">Следующие четыре байта: зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="223c1-122">Next four-bytes: Reserved for future use.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-123">Используется всеми методами интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-123">Used by all methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-124">**пмессаже**</span><span class="sxs-lookup"><span data-stu-id="223c1-124">**pMessage**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-125">Указатель на структуру [**рпколемессаже**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) , содержащую сведения о маршалинге данных RPC.</span><span class="sxs-lookup"><span data-stu-id="223c1-125">A pointer to an [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) structure that contains RPC data marshalling information.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-126">Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md), [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-126">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-127">**рефиид**</span><span class="sxs-lookup"><span data-stu-id="223c1-127">**refiid**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-128">Указатель на идентификатор IID интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-128">A pointer to the IID of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-129">Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md), [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**ServerNotify**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-129">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-130">**пчаннел**</span><span class="sxs-lookup"><span data-stu-id="223c1-130">**pChannel**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-131">Указатель на интерфейс [**ирпкчаннелбуффер**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) реализации com-канала RPC на сервере.</span><span class="sxs-lookup"><span data-stu-id="223c1-131">A pointer to the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface of the COM RPC channel implementation on the server.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-132">Используется методами [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-132">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-133">**пункпроксимгр**</span><span class="sxs-lookup"><span data-stu-id="223c1-133">**pUnkProxyMgr**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-134">Указатель на интерфейс [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) объекта, участвующий в этом вызове отладчика.</span><span class="sxs-lookup"><span data-stu-id="223c1-134">A pointer to the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface of the object involved in this debugger invocation.</span></span> <span data-ttu-id="223c1-135">Может иметь **значение NULL**, однако это сокращает функциональность отладчика.</span><span class="sxs-lookup"><span data-stu-id="223c1-135">May be **NULL**, however, this reduces debugger functionality.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-136">Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md)и [**клиентнотифи**](iorpcdebugnotify-clientnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-136">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), and [**ClientNotify**](iorpcdebugnotify-clientnotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-137">**пинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="223c1-137">**pInterface**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-138">Указатель на COM-интерфейс метода, который будет вызываться этим RPC.</span><span class="sxs-lookup"><span data-stu-id="223c1-138">A pointer to the COM interface of the method that will be invoked by this RPC.</span></span> <span data-ttu-id="223c1-139">Не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="223c1-139">Must not be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-140">Используется методами [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-140">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-141">**Объект punkObject**</span><span class="sxs-lookup"><span data-stu-id="223c1-141">**pUnkObject**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-142">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="223c1-142">Must be **NULL**.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-143">Используется методами [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md), [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-143">Used by the [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-144">**состав**</span><span class="sxs-lookup"><span data-stu-id="223c1-144">**hresult**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-145">Назначение этого участника изменяется для каждого из уведомлений ниже:</span><span class="sxs-lookup"><span data-stu-id="223c1-145">This member's purpose changes for each of the notifications below:</span></span>

<span data-ttu-id="223c1-146">[**Клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md): число байтов, которое клиентский отладчик будет передавать в серверный отладчик.</span><span class="sxs-lookup"><span data-stu-id="223c1-146">[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="223c1-147">Если значение равно нулю, сведения не передаются.</span><span class="sxs-lookup"><span data-stu-id="223c1-147">If zero, no information need be transmitted.</span></span>

<span data-ttu-id="223c1-148">[**Клиентнотифи**](iorpcdebugnotify-clientnotify.md): значение **HRESULT** последнего удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="223c1-148">[**ClientNotify**](iorpcdebugnotify-clientnotify.md): the **HRESULT** of the last RPC.</span></span>

<span data-ttu-id="223c1-149">[**Сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md): число байтов, которое клиентский отладчик будет передавать в серверный отладчик.</span><span class="sxs-lookup"><span data-stu-id="223c1-149">[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): the number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="223c1-150">Если значение равно нулю, сведения не передаются.</span><span class="sxs-lookup"><span data-stu-id="223c1-150">If zero, no information need be transmitted.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-151">Используется методами [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md)и [**сервержетбуфферсизе**](iorpcdebugnotify-servergetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-151">Used by the [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), and [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-152">**пвбуффер**</span><span class="sxs-lookup"><span data-stu-id="223c1-152">**pvBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-153">Указатель на структуру [**буфера ОРПК \_ dbg \_**](orpc-dbg-buffer.md) , содержащую сведения об упакованной отладке RPC.</span><span class="sxs-lookup"><span data-stu-id="223c1-153">A pointer to an [**ORPC\_DBG\_BUFFER**](orpc-dbg-buffer.md) structure that contains the RPC marshalled debug information.</span></span> <span data-ttu-id="223c1-154">Не определен, если **кббуффер** равен нулю.</span><span class="sxs-lookup"><span data-stu-id="223c1-154">Is undefined if **cbBuffer** is zero.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-155">Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md), [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-155">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-156">**кббуффер**</span><span class="sxs-lookup"><span data-stu-id="223c1-156">**cbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-157">Длина (в байтах) данных, на которые указывает **пвбуффер**.</span><span class="sxs-lookup"><span data-stu-id="223c1-157">The length, in bytes, of the data pointed to by **pvBuffer**.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-158">Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентнотифи**](iorpcdebugnotify-clientnotify.md), [**серверфиллбуффер**](iorpcdebugnotify-serverfillbuffer.md)и [**сервернотифи**](iorpcdebugnotify-servernotify.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-158">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), and [**ServerNotify**](iorpcdebugnotify-servernotify.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-159">**лпкббуффер**</span><span class="sxs-lookup"><span data-stu-id="223c1-159">**lpcbBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-160">Число байтов, которое клиентский отладчик будет передавать в серверный отладчик.</span><span class="sxs-lookup"><span data-stu-id="223c1-160">The number of bytes the client debugger will transmit to the server debugger.</span></span> <span data-ttu-id="223c1-161">Если значение равно нулю, сведения не передаются.</span><span class="sxs-lookup"><span data-stu-id="223c1-161">If zero, no information need be transmitted.</span></span> <span data-ttu-id="223c1-162">Это значение заменяет значение, возвращаемое в **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="223c1-162">This value supersedes the value returned in **hresult**.</span></span>

> [!Note]
>
> <span data-ttu-id="223c1-163">Используется методами [**клиентфиллбуффер**](iorpcdebugnotify-clientfillbuffer.md), [**клиентжетбуфферсизе**](iorpcdebugnotify-clientgetbuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="223c1-163">Used by the [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) methods.</span></span>

 

</dd> <dt>

<span data-ttu-id="223c1-164">**процессу**</span><span class="sxs-lookup"><span data-stu-id="223c1-164">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="223c1-165">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="223c1-165">Reserved.</span></span> <span data-ttu-id="223c1-166">Не используется.</span><span class="sxs-lookup"><span data-stu-id="223c1-166">Do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="223c1-167">Требования</span><span class="sxs-lookup"><span data-stu-id="223c1-167">Requirements</span></span>



| <span data-ttu-id="223c1-168">Требование</span><span class="sxs-lookup"><span data-stu-id="223c1-168">Requirement</span></span> | <span data-ttu-id="223c1-169">Значение</span><span class="sxs-lookup"><span data-stu-id="223c1-169">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="223c1-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="223c1-170">Minimum supported client</span></span><br/> | <span data-ttu-id="223c1-171">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="223c1-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="223c1-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="223c1-172">Minimum supported server</span></span><br/> | <span data-ttu-id="223c1-173">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="223c1-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="223c1-174">Заголовок</span><span class="sxs-lookup"><span data-stu-id="223c1-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="223c1-175"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="223c1-175"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="223c1-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="223c1-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223c1-177">**\_БУФЕР ОРПК dbg \_**</span><span class="sxs-lookup"><span data-stu-id="223c1-177">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="223c1-178">**\_аргументы инициализации \_ ОРПК**</span><span class="sxs-lookup"><span data-stu-id="223c1-178">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="223c1-179">**дллдебугобжектрпчук**</span><span class="sxs-lookup"><span data-stu-id="223c1-179">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="223c1-180">**иорпкдебугнотифи**</span><span class="sxs-lookup"><span data-stu-id="223c1-180">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

