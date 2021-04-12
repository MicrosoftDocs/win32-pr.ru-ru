---
title: XTYP_CONNECTная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию кстип Connect для создания диалога.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- XTYP_CONNECT обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136163"
---
# <a name="xtyp_connect-transaction"></a><span data-ttu-id="b6017-104">\_Транзакция кстип Connect</span><span class="sxs-lookup"><span data-stu-id="b6017-104">XTYP\_CONNECT transaction</span></span>

<span data-ttu-id="b6017-105">Клиент использует транзакцию **кстип \_ Connect** для создания диалога.</span><span class="sxs-lookup"><span data-stu-id="b6017-105">A client uses the **XTYP\_CONNECT** transaction to establish a conversation.</span></span> <span data-ttu-id="b6017-106">Функция обратного вызова сервера платформа динамических данных Exchange (DDE) получает эту транзакцию [*, когда*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)клиент указывает имя службы, которое поддерживает сервер (и имя раздела, не равное **null**) в вызове функции [**ддеконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .</span><span class="sxs-lookup"><span data-stu-id="b6017-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a service name that the server supports (and a topic name that is not **NULL**) in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="b6017-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6017-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6017-108">*утипе*</span><span class="sxs-lookup"><span data-stu-id="b6017-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="b6017-109">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="b6017-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="b6017-110">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="b6017-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b6017-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b6017-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b6017-112">*хконв*</span><span class="sxs-lookup"><span data-stu-id="b6017-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="b6017-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b6017-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b6017-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="b6017-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="b6017-115">Маркер имени раздела.</span><span class="sxs-lookup"><span data-stu-id="b6017-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="b6017-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="b6017-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="b6017-117">Описатель имени службы.</span><span class="sxs-lookup"><span data-stu-id="b6017-117">A handle to the service name.</span></span>

</dd> <dt>

<span data-ttu-id="b6017-118">*хдата*</span><span class="sxs-lookup"><span data-stu-id="b6017-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="b6017-119">Не используется.</span><span class="sxs-lookup"><span data-stu-id="b6017-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b6017-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="b6017-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="b6017-121">Указатель на структуру [**конвконтекст**](/windows/win32/api/ddeml/ns-ddeml-convcontext) , содержащую сведения о контексте для диалога.</span><span class="sxs-lookup"><span data-stu-id="b6017-121">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="b6017-122">Если клиент не является приложением ДДЕМЛ, этот параметр равен 0.</span><span class="sxs-lookup"><span data-stu-id="b6017-122">If the client is not a DDEML application, this parameter is 0.</span></span>

</dd> <dt>

<span data-ttu-id="b6017-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="b6017-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="b6017-124">Указывает, является ли клиент тем же экземпляром приложения, что и сервер.</span><span class="sxs-lookup"><span data-stu-id="b6017-124">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="b6017-125">Если параметр равен 1, то клиент является тем же экземпляром.</span><span class="sxs-lookup"><span data-stu-id="b6017-125">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="b6017-126">Если параметр равен 0, то клиент является другим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="b6017-126">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6017-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6017-127">Return value</span></span>

<span data-ttu-id="b6017-128">Функция обратного вызова сервера должна возвращать **значение true** , чтобы позволить клиенту устанавливать диалог с заданной парой имени службы и имени раздела, или функция должна возвращать **значение false** , чтобы запретить диалог.</span><span class="sxs-lookup"><span data-stu-id="b6017-128">A server callback function should return **TRUE** to allow the client to establish a conversation on the specified service name and topic name pair, or the function should return **FALSE** to deny the conversation.</span></span> <span data-ttu-id="b6017-129">Если функция обратного вызова возвращает **значение true** и диалог успешно установлен, система передает этот обработчик на сервер, выполняя транзакцию [**кстип \_ Connect \_ Confirm**](xtyp-connect-confirm.md) для функции обратного вызова сервера (если только сервер не указал флаг **КБФ \_ Skip \_ Connect \_** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).</span><span class="sxs-lookup"><span data-stu-id="b6017-129">If the callback function returns **TRUE** and a conversation is successfully established, the system passes the conversation handle to the server by issuing an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's callback function (unless the server specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6017-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6017-130">Remarks</span></span>

<span data-ttu-id="b6017-131">Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ Failed \_ Connections** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="b6017-131">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="b6017-132">Сервер не может заблокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b6017-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6017-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b6017-133">Requirements</span></span>



| <span data-ttu-id="b6017-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b6017-134">Requirement</span></span> | <span data-ttu-id="b6017-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b6017-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6017-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6017-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b6017-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6017-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b6017-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6017-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b6017-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6017-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="b6017-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b6017-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6017-141"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6017-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6017-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6017-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6017-143">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b6017-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6017-144">**конвконтекст**</span><span class="sxs-lookup"><span data-stu-id="b6017-144">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="b6017-145">**ддеконнект**</span><span class="sxs-lookup"><span data-stu-id="b6017-145">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="b6017-146">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="b6017-146">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="b6017-147">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b6017-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b6017-148">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="b6017-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

