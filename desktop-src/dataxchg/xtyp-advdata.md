---
title: XTYP_ADVDATAная транзакция (Ддемл. h)
description: Информирует клиента о том, что значение элемента данных изменилось. Функция обратного вызова клиента платформа динамических данных Exchange (DDE), Ддекаллбакк, получает эту транзакцию после установления цикла рекомендаций с сервером.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681774"
---
# <a name="xtyp_advdata-transaction"></a><span data-ttu-id="92707-105">\_Транзакция кстип адвдата</span><span class="sxs-lookup"><span data-stu-id="92707-105">XTYP\_ADVDATA transaction</span></span>

<span data-ttu-id="92707-106">Информирует клиента о том, что значение элемента данных изменилось.</span><span class="sxs-lookup"><span data-stu-id="92707-106">Informs the client that the value of the data item has changed.</span></span> <span data-ttu-id="92707-107">Функция обратного вызова клиента платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), получает эту транзакцию после установления цикла рекомендаций с сервером.</span><span class="sxs-lookup"><span data-stu-id="92707-107">The Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction after establishing an advise loop with a server.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="92707-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="92707-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92707-109">*утипе*</span><span class="sxs-lookup"><span data-stu-id="92707-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="92707-110">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="92707-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="92707-111">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="92707-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="92707-112">Формат Atom данных, отправляемых с сервера.</span><span class="sxs-lookup"><span data-stu-id="92707-112">The format atom of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="92707-113">*хконв*</span><span class="sxs-lookup"><span data-stu-id="92707-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="92707-114">Обработчик диалога.</span><span class="sxs-lookup"><span data-stu-id="92707-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="92707-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="92707-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="92707-116">Маркер имени раздела.</span><span class="sxs-lookup"><span data-stu-id="92707-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="92707-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="92707-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="92707-118">Маркер имени элемента.</span><span class="sxs-lookup"><span data-stu-id="92707-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="92707-119">*хдата*</span><span class="sxs-lookup"><span data-stu-id="92707-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="92707-120">Маркер для данных, связанных с именем раздела и парой имя элемента.</span><span class="sxs-lookup"><span data-stu-id="92707-120">A handle to the data associated with the topic name and item name pair.</span></span> <span data-ttu-id="92707-121">Этот параметр имеет **значение NULL** , если клиент указал флаг **кстипф \_ NoData** при запросе цикла рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="92707-121">This parameter is **NULL** if the client specified the **XTYPF\_NODATA** flag when it requested the advise loop.</span></span>

</dd> <dt>

<span data-ttu-id="92707-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="92707-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="92707-123">Не используется.</span><span class="sxs-lookup"><span data-stu-id="92707-123">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="92707-124">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="92707-124">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="92707-125">Не используется.</span><span class="sxs-lookup"><span data-stu-id="92707-125">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92707-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92707-126">Return value</span></span>

<span data-ttu-id="92707-127">Функция обратного вызова DDE должна возвращать **DDE \_ факк** , если обрабатывает эту транзакцию, **DDE \_ фбуси** , если она слишком занята для обработки этой транзакции, или **DDE \_ фнотпроцессед** , если она отклоняет эту транзакцию.</span><span class="sxs-lookup"><span data-stu-id="92707-127">A DDE callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="92707-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92707-128">Remarks</span></span>

<span data-ttu-id="92707-129">Приложение не должно освобождать полученный во время этой транзакции маркер данных.</span><span class="sxs-lookup"><span data-stu-id="92707-129">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="92707-130">Однако приложение должно копировать данные, связанные с этим обработчиком данных, если приложение должно обработать данные после возвращения функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="92707-130">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="92707-131">Приложение может использовать функцию [**ддежетдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) для копирования данных.</span><span class="sxs-lookup"><span data-stu-id="92707-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="92707-132">Требования</span><span class="sxs-lookup"><span data-stu-id="92707-132">Requirements</span></span>



| <span data-ttu-id="92707-133">Требование</span><span class="sxs-lookup"><span data-stu-id="92707-133">Requirement</span></span> | <span data-ttu-id="92707-134">Значение</span><span class="sxs-lookup"><span data-stu-id="92707-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92707-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92707-135">Minimum supported client</span></span><br/> | <span data-ttu-id="92707-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="92707-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="92707-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92707-137">Minimum supported server</span></span><br/> | <span data-ttu-id="92707-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="92707-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="92707-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="92707-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="92707-140"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92707-140"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92707-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92707-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="92707-142">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="92707-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="92707-143">**ддеклиенттрансактион**</span><span class="sxs-lookup"><span data-stu-id="92707-143">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="92707-144">**ддежетдата**</span><span class="sxs-lookup"><span data-stu-id="92707-144">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="92707-145">**ддепостадвисе**</span><span class="sxs-lookup"><span data-stu-id="92707-145">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="92707-146">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="92707-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="92707-147">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="92707-147">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

