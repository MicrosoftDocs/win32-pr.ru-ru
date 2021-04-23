---
title: XTYP_REQUESTная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию запроса кстип для запроса данных с сервера. Функция обратного вызова сервера платформа динамических данных Exchange (DDE), Ддекаллбакк, получает эту транзакцию, когда клиент указывает \_ запрос кстип в функции ддеклиенттрансактион.
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- XTYP_REQUEST обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801396"
---
# <a name="xtyp_request-transaction"></a><span data-ttu-id="7d986-105">\_Транзакция запроса кстип</span><span class="sxs-lookup"><span data-stu-id="7d986-105">XTYP\_REQUEST transaction</span></span>

<span data-ttu-id="7d986-106">Клиент использует транзакцию **\_ запроса кстип** для запроса данных с сервера.</span><span class="sxs-lookup"><span data-stu-id="7d986-106">A client uses the **XTYP\_REQUEST** transaction to request data from a server.</span></span> <span data-ttu-id="7d986-107">Функция обратного вызова сервера платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), получает эту транзакцию, когда клиент указывает **\_ запрос кстип** в функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="7d986-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_REQUEST** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a><span data-ttu-id="7d986-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d986-109">*утипе*</span><span class="sxs-lookup"><span data-stu-id="7d986-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="7d986-110">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="7d986-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="7d986-111">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="7d986-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="7d986-112">Формат, в котором сервер должен отправлять данные клиенту.</span><span class="sxs-lookup"><span data-stu-id="7d986-112">The format in which the server should submit data to the client.</span></span>

</dd> <dt>

<span data-ttu-id="7d986-113">*хконв*</span><span class="sxs-lookup"><span data-stu-id="7d986-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="7d986-114">Обработчик диалога.</span><span class="sxs-lookup"><span data-stu-id="7d986-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="7d986-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="7d986-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="7d986-116">Маркер имени раздела.</span><span class="sxs-lookup"><span data-stu-id="7d986-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="7d986-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="7d986-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="7d986-118">Маркер имени элемента.</span><span class="sxs-lookup"><span data-stu-id="7d986-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="7d986-119">*хдата*</span><span class="sxs-lookup"><span data-stu-id="7d986-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="7d986-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7d986-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d986-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="7d986-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="7d986-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7d986-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7d986-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="7d986-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="7d986-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="7d986-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d986-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d986-125">Return value</span></span>

<span data-ttu-id="7d986-126">Сервер должен вызвать функцию [**ддекреатедатахандле**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) для создания маркера данных, определяющего данные, а затем возвращающего маркер.</span><span class="sxs-lookup"><span data-stu-id="7d986-126">The server should call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the data and then return the handle.</span></span> <span data-ttu-id="7d986-127">Сервер должен вернуть **значение NULL** , если не удается завершить транзакцию.</span><span class="sxs-lookup"><span data-stu-id="7d986-127">The server should return **NULL** if it is unable to complete the transaction.</span></span> <span data-ttu-id="7d986-128">Если сервер возвращает **значение NULL**, клиент получит \_ флаг DDE фнотпроцессед.</span><span class="sxs-lookup"><span data-stu-id="7d986-128">If the server returns **NULL**, the client will receive a DDE\_FNOTPROCESSED flag.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d986-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d986-129">Remarks</span></span>

<span data-ttu-id="7d986-130">Эта транзакция фильтруется, если серверное приложение указало флаг " **КБФ \_ сбой \_ запросов** " в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="7d986-130">This transaction is filtered if the server application specified the **CBF\_FAIL\_REQUESTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="7d986-131">Если ответ на эту транзакцию требует длительной обработки, сервер может вернуть \_ код возврата блока CBR, чтобы приостановить будущие транзакции в текущем диалоге, а затем обработать транзакцию асинхронно.</span><span class="sxs-lookup"><span data-stu-id="7d986-131">If responding to this transaction requires lengthy processing, the server can return the CBR\_BLOCK return code to suspend future transactions on the current conversation and then process the transaction asynchronously.</span></span> <span data-ttu-id="7d986-132">Когда сервер завершит работу и данные готовы к передаче клиенту, сервер может вызвать функцию [**ддинаблекаллбакк**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) для возобновления диалога.</span><span class="sxs-lookup"><span data-stu-id="7d986-132">When the server has finished and the data is ready to pass to the client, the server can call the [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) function to resume the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d986-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7d986-133">Requirements</span></span>



| <span data-ttu-id="7d986-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7d986-134">Requirement</span></span> | <span data-ttu-id="7d986-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7d986-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d986-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d986-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7d986-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d986-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7d986-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d986-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7d986-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d986-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7d986-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7d986-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d986-141"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d986-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d986-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d986-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d986-143">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="7d986-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7d986-144">**ддеклиенттрансактион**</span><span class="sxs-lookup"><span data-stu-id="7d986-144">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="7d986-145">**ддекреатедатахандле**</span><span class="sxs-lookup"><span data-stu-id="7d986-145">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="7d986-146">**ддинаблекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="7d986-146">**DdeEnableCallback**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[<span data-ttu-id="7d986-147">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="7d986-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="7d986-148">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="7d986-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7d986-149">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="7d986-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

