---
title: XTYP_ADVREQная транзакция (Ддемл. h)
description: Транзакция КСТИП \_ Адврек информирует сервер о том, что транзакция advise недоступна по указанному имени раздела и паре имен элементов, а также изменились данные, соответствующие имени раздела и паре имен элементов.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415657"
---
# <a name="xtyp_advreq-transaction"></a><span data-ttu-id="1cef7-104">\_Транзакция кстип Адврек</span><span class="sxs-lookup"><span data-stu-id="1cef7-104">XTYP\_ADVREQ transaction</span></span>

<span data-ttu-id="1cef7-105">Транзакция **кстип \_ Адврек** информирует сервер о том, что транзакция advise недоступна по указанному имени раздела и паре имен элементов, а также изменились данные, соответствующие имени раздела и паре имен элементов.</span><span class="sxs-lookup"><span data-stu-id="1cef7-105">The **XTYP\_ADVREQ** transaction informs the server that an advise transaction is outstanding on the specified topic name and item name pair and that data corresponding to the topic name and item name pair has changed.</span></span> <span data-ttu-id="1cef7-106">Система отправляет эту транзакцию в функцию обратного вызова платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)после того, как сервер вызовет функцию [**ддепостадвисе**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="1cef7-106">The system sends this transaction to the Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), after the server calls the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="1cef7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cef7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cef7-108">*утипе*</span><span class="sxs-lookup"><span data-stu-id="1cef7-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="1cef7-109">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="1cef7-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="1cef7-110">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="1cef7-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1cef7-111">Формат, в котором данные должны отправляться клиенту.</span><span class="sxs-lookup"><span data-stu-id="1cef7-111">The format in which the data should be submitted to the client.</span></span>

</dd> <dt>

<span data-ttu-id="1cef7-112">*хконв*</span><span class="sxs-lookup"><span data-stu-id="1cef7-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="1cef7-113">Обработчик диалога.</span><span class="sxs-lookup"><span data-stu-id="1cef7-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="1cef7-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="1cef7-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="1cef7-115">Маркер имени раздела.</span><span class="sxs-lookup"><span data-stu-id="1cef7-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="1cef7-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="1cef7-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="1cef7-117">Измененный маркер имени элемента.</span><span class="sxs-lookup"><span data-stu-id="1cef7-117">A handle to the item name that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="1cef7-118">*хдата*</span><span class="sxs-lookup"><span data-stu-id="1cef7-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="1cef7-119">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1cef7-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1cef7-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="1cef7-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="1cef7-121">Число (в слове с низким порядком) транзакций **кстип \_ Адврек** , которые продолжают обрабатываться по тому же разделу, элементу и имени формата, заданному в контексте текущего вызова функции [**ддепостадвисе**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="1cef7-121">The count, in the low-order word, of **XTYP\_ADVREQ** transactions that remain to be processed on the same topic, item, and format name set within the context of the current call to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span> <span data-ttu-id="1cef7-122">Значение счетчика равно нулю, если текущая **кстип \_ Адврек** транзакция является последней.</span><span class="sxs-lookup"><span data-stu-id="1cef7-122">The count is zero if the current **XTYP\_ADVREQ** transaction is the last one.</span></span> <span data-ttu-id="1cef7-123">Сервер может использовать это число, чтобы определить, следует ли создать **хдата \_ апповнед** данных для данных рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="1cef7-123">A server can use this count to determine whether to create an **HDATA\_APPOWNED** data handle to the advise data.</span></span>

<span data-ttu-id="1cef7-124">Младшее слово задается равным **кадв \_ латеакк** , если ддемл выдавала транзакцию **кстип \_ Адврек** из-за последовательного \_ сообщения ACK с помощью DDE от клиента, аутрун сервером.</span><span class="sxs-lookup"><span data-stu-id="1cef7-124">The low-order word is set to **CADV\_LATEACK** if the DDEML issued the **XTYP\_ADVREQ** transaction because of a late-arriving DDE\_ACK message from a client being outrun by the server.</span></span>

<span data-ttu-id="1cef7-125">Слово с высоким порядком не используется.</span><span class="sxs-lookup"><span data-stu-id="1cef7-125">The high-order word is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1cef7-126">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="1cef7-126">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="1cef7-127">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1cef7-127">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cef7-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1cef7-128">Return value</span></span>

<span data-ttu-id="1cef7-129">Сервер должен сначала вызвать функцию [**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) , чтобы создать маркер данных, определяющий измененные данные, а затем вернуть этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="1cef7-129">The server should first call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the changed data and then return the handle.</span></span> <span data-ttu-id="1cef7-130">Сервер должен вернуть **значение NULL** , если не удается завершить транзакцию.</span><span class="sxs-lookup"><span data-stu-id="1cef7-130">The server should return **NULL** if it is unable to complete the transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cef7-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1cef7-131">Remarks</span></span>

<span data-ttu-id="1cef7-132">Сервер не может заблокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1cef7-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cef7-133">Требования</span><span class="sxs-lookup"><span data-stu-id="1cef7-133">Requirements</span></span>



| <span data-ttu-id="1cef7-134">Требование</span><span class="sxs-lookup"><span data-stu-id="1cef7-134">Requirement</span></span> | <span data-ttu-id="1cef7-135">Значение</span><span class="sxs-lookup"><span data-stu-id="1cef7-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cef7-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1cef7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1cef7-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1cef7-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1cef7-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1cef7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1cef7-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1cef7-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1cef7-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1cef7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cef7-141"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cef7-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cef7-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cef7-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="1cef7-143">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1cef7-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1cef7-144">**ддекреатедатахандле**</span><span class="sxs-lookup"><span data-stu-id="1cef7-144">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="1cef7-145">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="1cef7-145">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="1cef7-146">**ддепостадвисе**</span><span class="sxs-lookup"><span data-stu-id="1cef7-146">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="1cef7-147">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1cef7-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1cef7-148">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="1cef7-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

