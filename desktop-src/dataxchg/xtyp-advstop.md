---
title: XTYP_ADVSTOPная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию кстип адвстоп для завершения цикла рекомендаций с сервером. Функция обратного вызова сервера платформа динамических данных Exchange (DDE), Ддекаллбакк, получает эту транзакцию, когда клиент указывает КСТИП \_ адвстоп в функции ддеклиенттрансактион.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- XTYP_ADVSTOP обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61292683377cd6c7243c3e41c5dbd9332a671163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710507"
---
# <a name="xtyp_advstop-transaction"></a><span data-ttu-id="1c156-105">\_Транзакция кстип адвстоп</span><span class="sxs-lookup"><span data-stu-id="1c156-105">XTYP\_ADVSTOP transaction</span></span>

<span data-ttu-id="1c156-106">Клиент использует транзакцию **кстип \_ адвстоп** для завершения цикла рекомендаций с сервером.</span><span class="sxs-lookup"><span data-stu-id="1c156-106">A client uses the **XTYP\_ADVSTOP** transaction to end an advise loop with a server.</span></span> <span data-ttu-id="1c156-107">Функция обратного вызова сервера платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), получает эту транзакцию, когда клиент указывает **кстип \_ адвстоп** в функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="1c156-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTOP** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a><span data-ttu-id="1c156-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c156-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c156-109">*утипе*</span><span class="sxs-lookup"><span data-stu-id="1c156-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="1c156-110">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="1c156-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="1c156-111">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="1c156-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1c156-112">Формат данных, связанный с завершенным циклом рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="1c156-112">The data format associated with the advise loop being ended.</span></span>

</dd> <dt>

<span data-ttu-id="1c156-113">*хконв*</span><span class="sxs-lookup"><span data-stu-id="1c156-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="1c156-114">Обработчик диалога.</span><span class="sxs-lookup"><span data-stu-id="1c156-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="1c156-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="1c156-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="1c156-116">Маркер имени раздела.</span><span class="sxs-lookup"><span data-stu-id="1c156-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="1c156-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="1c156-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="1c156-118">Маркер имени элемента.</span><span class="sxs-lookup"><span data-stu-id="1c156-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="1c156-119">*хдата*</span><span class="sxs-lookup"><span data-stu-id="1c156-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="1c156-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1c156-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1c156-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="1c156-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="1c156-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1c156-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1c156-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="1c156-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="1c156-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1c156-124">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c156-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c156-125">Remarks</span></span>

<span data-ttu-id="1c156-126">Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ Failed \_ advise** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="1c156-126">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c156-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1c156-127">Requirements</span></span>



| <span data-ttu-id="1c156-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1c156-128">Requirement</span></span> | <span data-ttu-id="1c156-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1c156-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c156-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c156-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1c156-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1c156-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1c156-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c156-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1c156-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1c156-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1c156-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1c156-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c156-135"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c156-135"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c156-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c156-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c156-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1c156-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1c156-138">**ддеклиенттрансактион**</span><span class="sxs-lookup"><span data-stu-id="1c156-138">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="1c156-139">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="1c156-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="1c156-140">**ддепостадвисе**</span><span class="sxs-lookup"><span data-stu-id="1c156-140">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="1c156-141">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1c156-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1c156-142">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="1c156-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

