---
title: XTYP_WILDCONNECTная транзакция (Ддемл. h)
description: Позволяет клиенту устанавливать диалог для каждого имени службы сервера и пары имен разделов, совпадающих с указанными именем службы и именем раздела.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- XTYP_WILDCONNECT обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701041"
---
# <a name="xtyp_wildconnect-transaction"></a><span data-ttu-id="b9370-104">\_Транзакция кстип вилдконнект</span><span class="sxs-lookup"><span data-stu-id="b9370-104">XTYP\_WILDCONNECT transaction</span></span>

<span data-ttu-id="b9370-105">Позволяет клиенту устанавливать диалог для каждого имени службы сервера и пары имен разделов, совпадающих с указанными именем службы и именем раздела.</span><span class="sxs-lookup"><span data-stu-id="b9370-105">Enables a client to establish a conversation on each of the server's service name and topic name pairs that match the specified service name and topic name.</span></span> <span data-ttu-id="b9370-106">Функция обратного вызова сервера платформа динамических данных Exchange (DDE) получает эту транзакцию [*, когда*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)клиент указывает **пустое** имя службы, имя раздела **null** или оба метода в вызове функции [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) или [**ддеконнектлист**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="b9370-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a **NULL** service name, a **NULL** topic name, or both in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) or [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="b9370-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9370-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9370-108">*утипе*</span><span class="sxs-lookup"><span data-stu-id="b9370-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="b9370-109">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="b9370-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="b9370-110">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="b9370-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b9370-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b9370-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b9370-112">*хконв*</span><span class="sxs-lookup"><span data-stu-id="b9370-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="b9370-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b9370-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b9370-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="b9370-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="b9370-115">Маркер имени раздела.</span><span class="sxs-lookup"><span data-stu-id="b9370-115">A handle to the topic name.</span></span> <span data-ttu-id="b9370-116">Если этот параметр имеет **значение NULL**, клиент запрашивает диалог по всем именам разделов, которые поддерживает сервер.</span><span class="sxs-lookup"><span data-stu-id="b9370-116">If this parameter is **NULL**, the client is requesting a conversation on all topic names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="b9370-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="b9370-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="b9370-118">Описатель имени службы.</span><span class="sxs-lookup"><span data-stu-id="b9370-118">A handle to the service name.</span></span> <span data-ttu-id="b9370-119">Если этот параметр имеет **значение NULL**, клиент запрашивает диалог по всем именам служб, которые поддерживает сервер.</span><span class="sxs-lookup"><span data-stu-id="b9370-119">If this parameter is **NULL**, the client is requesting a conversation on all service names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="b9370-120">*хдата*</span><span class="sxs-lookup"><span data-stu-id="b9370-120">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="b9370-121">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b9370-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b9370-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="b9370-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="b9370-123">Указатель на структуру [**конвконтекст**](/windows/win32/api/ddeml/ns-ddeml-convcontext) , содержащую сведения о контексте для диалога.</span><span class="sxs-lookup"><span data-stu-id="b9370-123">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="b9370-124">Если клиент не является приложением ДДЕМЛ, этот параметр имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="b9370-124">If the client is not a DDEML application, this parameter is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="b9370-125">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="b9370-125">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="b9370-126">Указывает, является ли клиент тем же экземпляром приложения, что и сервер.</span><span class="sxs-lookup"><span data-stu-id="b9370-126">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="b9370-127">Если параметр равен 1, то клиент является тем же экземпляром.</span><span class="sxs-lookup"><span data-stu-id="b9370-127">If the parameter is 1, the client is same instance.</span></span> <span data-ttu-id="b9370-128">Если параметр равен 0, то клиент является другим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="b9370-128">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9370-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9370-129">Return value</span></span>

<span data-ttu-id="b9370-130">Сервер должен вернуть маркер данных, определяющий массив структур [**хсзпаир**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="b9370-130">The server should return a data handle that identifies an array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="b9370-131">Массив должен содержать одну структуру для каждой пары имя службы и имя раздела, которая соответствует паре имя службы и имя раздела, запрошенного клиентом.</span><span class="sxs-lookup"><span data-stu-id="b9370-131">The array should contain one structure for each service-name and topic-name pair that matches the service-name and topic-name pair requested by the client.</span></span> <span data-ttu-id="b9370-132">Массив должен завершаться с помощью **нулевого** строкового маркера.</span><span class="sxs-lookup"><span data-stu-id="b9370-132">The array must be terminated by a **NULL** string handle.</span></span> <span data-ttu-id="b9370-133">Система отправляет транзакцию [**кстип \_ Connect \_ Confirm**](xtyp-connect-confirm.md) на сервер для подтверждения каждого диалога и передачи дескрипторов диалога на сервер.</span><span class="sxs-lookup"><span data-stu-id="b9370-133">The system sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server to confirm each conversation and to pass the conversation handles to the server.</span></span> <span data-ttu-id="b9370-134">Сервер не будет принимать эти подтверждения, если в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) указан **флаг \_ КБФ \_ Skip \_ Connect** .</span><span class="sxs-lookup"><span data-stu-id="b9370-134">The server will not receive these confirmations if it specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="b9370-135">Сервер должен вернуть **значение NULL** , чтобы отказаться от транзакции **кстип \_ вилдконнект** .</span><span class="sxs-lookup"><span data-stu-id="b9370-135">The server should return **NULL** to refuse the **XTYP\_WILDCONNECT** transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9370-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9370-136">Remarks</span></span>

<span data-ttu-id="b9370-137">Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ Failed \_ Connections** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="b9370-137">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="b9370-138">Сервер не может заблокировать этот тип транзакции; \_код возврата блока CBR игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b9370-138">A server cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9370-139">Требования</span><span class="sxs-lookup"><span data-stu-id="b9370-139">Requirements</span></span>



| <span data-ttu-id="b9370-140">Требование</span><span class="sxs-lookup"><span data-stu-id="b9370-140">Requirement</span></span> | <span data-ttu-id="b9370-141">Значение</span><span class="sxs-lookup"><span data-stu-id="b9370-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9370-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9370-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b9370-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9370-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b9370-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9370-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b9370-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9370-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b9370-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b9370-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9370-147"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9370-147"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9370-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9370-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9370-149">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b9370-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b9370-150">**конвконтекст**</span><span class="sxs-lookup"><span data-stu-id="b9370-150">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="b9370-151">**ддеконнект**</span><span class="sxs-lookup"><span data-stu-id="b9370-151">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="b9370-152">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="b9370-152">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="b9370-153">**хсзпаир**</span><span class="sxs-lookup"><span data-stu-id="b9370-153">**HSZPAIR**</span></span>](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

<span data-ttu-id="b9370-154">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b9370-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b9370-155">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="b9370-155">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

