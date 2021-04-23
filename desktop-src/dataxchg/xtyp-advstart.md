---
title: XTYP_ADVSTARTная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию кстип адвстарт для установки цикла рекомендаций с сервером.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802543"
---
# <a name="xtyp_advstart-transaction"></a><span data-ttu-id="f73b8-104">\_Транзакция кстип адвстарт</span><span class="sxs-lookup"><span data-stu-id="f73b8-104">XTYP\_ADVSTART transaction</span></span>

<span data-ttu-id="f73b8-105">Клиент использует транзакцию **кстип \_ адвстарт** для установки цикла рекомендаций с сервером.</span><span class="sxs-lookup"><span data-stu-id="f73b8-105">A client uses the **XTYP\_ADVSTART** transaction to establish an advise loop with a server.</span></span> <span data-ttu-id="f73b8-106">Функция обратного вызова сервера платформа динамических данных Exchange (DDE) получает эту транзакцию [*, когда*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)клиент указывает **кстип \_ Адвстарт** в качестве параметра *wType* функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="f73b8-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTART** as the *wType* parameter of the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a><span data-ttu-id="f73b8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f73b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f73b8-108">*утипе*</span><span class="sxs-lookup"><span data-stu-id="f73b8-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="f73b8-109">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="f73b8-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="f73b8-110">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="f73b8-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f73b8-111">Формат данных, запрашиваемый клиентом.</span><span class="sxs-lookup"><span data-stu-id="f73b8-111">The data format requested by the client.</span></span>

</dd> <dt>

<span data-ttu-id="f73b8-112">*хконв*</span><span class="sxs-lookup"><span data-stu-id="f73b8-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="f73b8-113">Обработчик диалога.</span><span class="sxs-lookup"><span data-stu-id="f73b8-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="f73b8-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="f73b8-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="f73b8-115">Маркер имени раздела.</span><span class="sxs-lookup"><span data-stu-id="f73b8-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="f73b8-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="f73b8-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="f73b8-117">Маркер имени элемента.</span><span class="sxs-lookup"><span data-stu-id="f73b8-117">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="f73b8-118">*хдата*</span><span class="sxs-lookup"><span data-stu-id="f73b8-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="f73b8-119">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f73b8-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f73b8-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="f73b8-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="f73b8-121">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f73b8-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f73b8-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="f73b8-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="f73b8-123">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f73b8-123">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f73b8-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f73b8-124">Return value</span></span>

<span data-ttu-id="f73b8-125">Функция обратного вызова сервера должна возвращать **значение true** , чтобы разрешить цикл рекомендаций по заданному имени раздела и паре имен элементов, или **false** для запрета цикла рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="f73b8-125">A server callback function should return **TRUE** to allow an advise loop on the specified topic name and item name pair, or **FALSE** to deny the advise loop.</span></span> <span data-ttu-id="f73b8-126">Если функция обратного вызова возвращает **значение true**, любые последующие вызовы функции [**ддепостадвисе**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) на сервере с тем же именем раздела и парой имен элементов приводят к тому, что система отправляет транзакции [**кстип \_ Адврек**](xtyp-advreq.md) на сервер.</span><span class="sxs-lookup"><span data-stu-id="f73b8-126">If the callback function returns **TRUE**, any subsequent calls to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function by the server on the same topic name and item name pair causes the system to send [**XTYP\_ADVREQ**](xtyp-advreq.md) transactions to the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="f73b8-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f73b8-127">Remarks</span></span>

<span data-ttu-id="f73b8-128">Если клиент запрашивает цикл рекомендаций по имени раздела, имени элемента и формату данных для уже установленного цикла рекомендаций, то платформа динамических данных Библиотека управления Exchange (ДДЕМЛ) не создает дублирующийся цикл рекомендаций, а изменяет флаги цикла рекомендаций (**кстипф \_ Аккрек** и **кстипф \_ NoData**) для соответствия последнему запросу.</span><span class="sxs-lookup"><span data-stu-id="f73b8-128">If a client requests an advise loop on a topic name, item name, and data format for an advise loop that is already established, the Dynamic Data Exchange Management Library (DDEML) does not create a duplicate advise loop but instead alters the advise loop flags (**XTYPF\_ACKREQ** and **XTYPF\_NODATA**) to match the latest request.</span></span>

<span data-ttu-id="f73b8-129">Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ Failed \_ advise** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="f73b8-129">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f73b8-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f73b8-130">Requirements</span></span>



| <span data-ttu-id="f73b8-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f73b8-131">Requirement</span></span> | <span data-ttu-id="f73b8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f73b8-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f73b8-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f73b8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f73b8-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f73b8-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f73b8-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f73b8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f73b8-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f73b8-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f73b8-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f73b8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f73b8-138"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f73b8-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f73b8-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f73b8-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="f73b8-140">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f73b8-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f73b8-141">**ддеклиенттрансактион**</span><span class="sxs-lookup"><span data-stu-id="f73b8-141">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="f73b8-142">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="f73b8-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="f73b8-143">**ддепостадвисе**</span><span class="sxs-lookup"><span data-stu-id="f73b8-143">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="f73b8-144">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f73b8-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f73b8-145">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="f73b8-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

