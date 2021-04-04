---
title: XTYP_POKEная транзакция (Ддемл. h)
description: Клиент использует \_ транзакцию кстип, чтобы отправить незапрошенные данные на сервер. Функция обратного вызова сервера платформа динамических данных Exchange (DDE) получает эту транзакцию, когда клиент указывает КСТИП \_ в функции ддеклиенттрансактион.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- XTYP_POKE обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988566"
---
# <a name="xtyp_poke-transaction"></a><span data-ttu-id="50d4c-105">КСТИП \_ Вставка транзакции</span><span class="sxs-lookup"><span data-stu-id="50d4c-105">XTYP\_POKE transaction</span></span>

<span data-ttu-id="50d4c-106">Клиент использует транзакцию **кстип \_** , чтобы отправить незапрошенные данные на сервер.</span><span class="sxs-lookup"><span data-stu-id="50d4c-106">A client uses the **XTYP\_POKE** transaction to send unsolicited data to the server.</span></span> <span data-ttu-id="50d4c-107">Функция обратного вызова сервера платформа динамических данных Exchange (DDE) получает эту транзакцию [*, когда*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)клиент указывает **Кстип \_** в функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="50d4c-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_POKE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="50d4c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="50d4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d4c-109">*утипе*</span><span class="sxs-lookup"><span data-stu-id="50d4c-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="50d4c-110">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="50d4c-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="50d4c-111">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="50d4c-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="50d4c-112">Формат данных, отправляемых с сервера.</span><span class="sxs-lookup"><span data-stu-id="50d4c-112">The format of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="50d4c-113">*хконв*</span><span class="sxs-lookup"><span data-stu-id="50d4c-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="50d4c-114">Обработчик диалога.</span><span class="sxs-lookup"><span data-stu-id="50d4c-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="50d4c-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="50d4c-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="50d4c-116">Маркер имени раздела.</span><span class="sxs-lookup"><span data-stu-id="50d4c-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="50d4c-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="50d4c-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="50d4c-118">Маркер имени элемента.</span><span class="sxs-lookup"><span data-stu-id="50d4c-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="50d4c-119">*хдата*</span><span class="sxs-lookup"><span data-stu-id="50d4c-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="50d4c-120">Обработчик данных, отправляемых клиентом на сервер.</span><span class="sxs-lookup"><span data-stu-id="50d4c-120">A handle to the data that the client is sending to the server.</span></span>

</dd> <dt>

<span data-ttu-id="50d4c-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="50d4c-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="50d4c-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="50d4c-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="50d4c-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="50d4c-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="50d4c-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="50d4c-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d4c-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50d4c-125">Return value</span></span>

<span data-ttu-id="50d4c-126">Функция обратного вызова сервера должна возвращать флаг **DDE \_ факк** , если он обрабатывает эту транзакцию, флаг **DDE \_ фбуси** , если он слишком занят для обработки этой транзакции, или флаг **\_ фнотпроцессед DDE** , если он отклоняет эту транзакцию.</span><span class="sxs-lookup"><span data-stu-id="50d4c-126">A server callback function should return the **DDE\_FACK** flag if it processes this transaction, the **DDE\_FBUSY** flag if it is too busy to process this transaction, or the **DDE\_FNOTPROCESSED** flag if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="50d4c-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50d4c-127">Remarks</span></span>

<span data-ttu-id="50d4c-128">Эта транзакция фильтруется, если серверное приложение указало флаг **КБФ \_ \_ Failed** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="50d4c-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_POKES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="50d4c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="50d4c-129">Requirements</span></span>



| <span data-ttu-id="50d4c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="50d4c-130">Requirement</span></span> | <span data-ttu-id="50d4c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="50d4c-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d4c-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50d4c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="50d4c-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50d4c-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="50d4c-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50d4c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="50d4c-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50d4c-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="50d4c-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="50d4c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d4c-137"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50d4c-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d4c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50d4c-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="50d4c-139">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="50d4c-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="50d4c-140">**ддеклиенттрансактион**</span><span class="sxs-lookup"><span data-stu-id="50d4c-140">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="50d4c-141">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="50d4c-141">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="50d4c-142">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="50d4c-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="50d4c-143">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="50d4c-143">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

