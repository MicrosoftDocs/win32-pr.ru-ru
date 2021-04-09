---
title: XTYP_EXECUTEная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию кстип Execute для отправки командной строки на сервер. Функция обратного вызова сервера платформа динамических данных Exchange (DDE), Ддекаллбакк, получает эту транзакцию, когда клиент указывает КСТИП \_ EXECUTE в функции ддеклиенттрансактион.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- XTYP_EXECUTE обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071879"
---
# <a name="xtyp_execute-transaction"></a><span data-ttu-id="904d2-105">КСТИП \_ выполнить транзакцию</span><span class="sxs-lookup"><span data-stu-id="904d2-105">XTYP\_EXECUTE transaction</span></span>

<span data-ttu-id="904d2-106">Клиент использует транзакцию **кстип \_ EXECUTE** для отправки командной строки на сервер.</span><span class="sxs-lookup"><span data-stu-id="904d2-106">A client uses the **XTYP\_EXECUTE** transaction to send a command string to the server.</span></span> <span data-ttu-id="904d2-107">Функция обратного вызова сервера платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), получает эту транзакцию, когда клиент указывает **кстип \_ EXECUTE** в функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="904d2-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_EXECUTE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="904d2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="904d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="904d2-109">*утипе*</span><span class="sxs-lookup"><span data-stu-id="904d2-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="904d2-110">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="904d2-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="904d2-111">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="904d2-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="904d2-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="904d2-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="904d2-113">*хконв*</span><span class="sxs-lookup"><span data-stu-id="904d2-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="904d2-114">Обработчик диалога.</span><span class="sxs-lookup"><span data-stu-id="904d2-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="904d2-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="904d2-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="904d2-116">Маркер имени раздела.</span><span class="sxs-lookup"><span data-stu-id="904d2-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="904d2-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="904d2-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="904d2-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="904d2-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="904d2-119">*хдата*</span><span class="sxs-lookup"><span data-stu-id="904d2-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="904d2-120">Маркер командной строки.</span><span class="sxs-lookup"><span data-stu-id="904d2-120">A handle to the command string.</span></span>

</dd> <dt>

<span data-ttu-id="904d2-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="904d2-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="904d2-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="904d2-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="904d2-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="904d2-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="904d2-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="904d2-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="904d2-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="904d2-125">Return value</span></span>

<span data-ttu-id="904d2-126">Функция обратного вызова сервера должна возвращать **DDE \_ факк** , если обрабатывает эту транзакцию, **DDE \_ фбуси** , если она слишком занята для обработки этой транзакции, или **DDE \_ фнотпроцессед** , если она отклоняет эту транзакцию.</span><span class="sxs-lookup"><span data-stu-id="904d2-126">A server callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="904d2-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="904d2-127">Remarks</span></span>

<span data-ttu-id="904d2-128">Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ \_ Failed** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="904d2-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_EXECUTES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="904d2-129">Приложение должно освободить полученный во время этой транзакции обработчик данных.</span><span class="sxs-lookup"><span data-stu-id="904d2-129">An application must free the data handle obtained during this transaction.</span></span> <span data-ttu-id="904d2-130">Однако приложение должно копировать командную строку, связанную с этим обработчиком данных, если приложение должно обработать строку после возвращения функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="904d2-130">An application must, however, copy the command string associated with the data handle if the application must process the string after the callback function returns.</span></span> <span data-ttu-id="904d2-131">Приложение может использовать функцию [**ддежетдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) для копирования данных.</span><span class="sxs-lookup"><span data-stu-id="904d2-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

<span data-ttu-id="904d2-132">Поскольку большинство клиентских приложений предполагают, что серверное приложение выполняет **кстип \_** транзакцию синхронно, сервер должен попытаться выполнить всю обработку транзакции **кстип \_ EXECUTE** либо из функции обратного вызова DDE, либо путем возвращения кода возврата **CBR \_ блока** .</span><span class="sxs-lookup"><span data-stu-id="904d2-132">Because most client applications expect a server application to perform an **XTYP\_EXECUTE** transaction synchronously, a server should attempt to perform all processing of the **XTYP\_EXECUTE** transaction either from within the DDE callback function or by returning the **CBR\_BLOCK** return code.</span></span> <span data-ttu-id="904d2-133">Если параметр *хдата* является командой, которая указывает серверу завершить работу, сервер должен сделать это после обработки транзакции **кстип \_ EXECUTE** .</span><span class="sxs-lookup"><span data-stu-id="904d2-133">If the *hdata* parameter is a command that instructs the server to terminate, the server should do so after processing the **XTYP\_EXECUTE** transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="904d2-134">Требования</span><span class="sxs-lookup"><span data-stu-id="904d2-134">Requirements</span></span>



| <span data-ttu-id="904d2-135">Требование</span><span class="sxs-lookup"><span data-stu-id="904d2-135">Requirement</span></span> | <span data-ttu-id="904d2-136">Значение</span><span class="sxs-lookup"><span data-stu-id="904d2-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="904d2-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="904d2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="904d2-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="904d2-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="904d2-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="904d2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="904d2-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="904d2-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="904d2-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="904d2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="904d2-142"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="904d2-142"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904d2-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="904d2-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="904d2-144">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="904d2-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="904d2-145">**ддеклиенттрансактион**</span><span class="sxs-lookup"><span data-stu-id="904d2-145">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="904d2-146">**ддежетдата**</span><span class="sxs-lookup"><span data-stu-id="904d2-146">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="904d2-147">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="904d2-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="904d2-148">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="904d2-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="904d2-149">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="904d2-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

