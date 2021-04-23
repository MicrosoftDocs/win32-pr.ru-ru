---
title: XTYP_XACT_COMPLETEная транзакция (Ддемл. h)
description: Функция обратного вызова клиента платформа динамических данных Exchange (DDE), Ддекаллбакк, получает \_ \_ транзакцию транзакции кстип Complete, когда завершается асинхронная транзакция, инициированная вызовом функции ддеклиенттрансактион.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681824"
---
# <a name="xtyp_xact_complete-transaction"></a><span data-ttu-id="a03e9-104">\_Транзакция кстип \_ транзакции завершена</span><span class="sxs-lookup"><span data-stu-id="a03e9-104">XTYP\_XACT\_COMPLETE transaction</span></span>

<span data-ttu-id="a03e9-105">Функция обратного вызова клиента платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), Получает транзакцию транзакции **кстип \_ \_ Complete** , когда завершается асинхронная транзакция, инициированная вызовом функции [**ддеклиенттрансактион**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="a03e9-105">A Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_XACT\_COMPLETE** transaction when an asynchronous transaction, initiated by a call to the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function, has completed.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a><span data-ttu-id="a03e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a03e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a03e9-107">*утипе*</span><span class="sxs-lookup"><span data-stu-id="a03e9-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="a03e9-108">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="a03e9-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="a03e9-109">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="a03e9-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a03e9-110">Формат данных, связанных с завершенной транзакцией (если применимо), или **значение NULL** , если во время транзакции не были переданы данные.</span><span class="sxs-lookup"><span data-stu-id="a03e9-110">The format of the data associated with the completed transaction (if applicable) or **NULL** if no data was exchanged during the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="a03e9-111">*хконв*</span><span class="sxs-lookup"><span data-stu-id="a03e9-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="a03e9-112">Обработчик диалога.</span><span class="sxs-lookup"><span data-stu-id="a03e9-112">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="a03e9-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="a03e9-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="a03e9-114">Маркер имени раздела, участвующего в завершенной транзакции.</span><span class="sxs-lookup"><span data-stu-id="a03e9-114">A handle to the topic name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="a03e9-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="a03e9-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="a03e9-116">Маркер имени элемента, участвующего в завершенной транзакции.</span><span class="sxs-lookup"><span data-stu-id="a03e9-116">A handle to the item name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="a03e9-117">*хдата*</span><span class="sxs-lookup"><span data-stu-id="a03e9-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="a03e9-118">Маркер для данных, вовлеченных в завершенную транзакцию (если применимо).</span><span class="sxs-lookup"><span data-stu-id="a03e9-118">A handle to the data involved in the completed transaction, if applicable.</span></span> <span data-ttu-id="a03e9-119">Если транзакция прошла успешно, но не включала данные, этот параметр имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="a03e9-119">If the transaction was successful but involved no data, this parameter is **TRUE**.</span></span> <span data-ttu-id="a03e9-120">Если транзакция завершилась неудачно, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="a03e9-120">This parameter is **NULL** if the transaction was unsuccessful.</span></span>

</dd> <dt>

<span data-ttu-id="a03e9-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="a03e9-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="a03e9-122">Идентификатор транзакции завершенной транзакции.</span><span class="sxs-lookup"><span data-stu-id="a03e9-122">The transaction identifier of the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="a03e9-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="a03e9-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="a03e9-124">Все применимые флаги состояния **DDE \_** в нижнем слове.</span><span class="sxs-lookup"><span data-stu-id="a03e9-124">Any applicable **DDE\_** status flags in the low word.</span></span> <span data-ttu-id="a03e9-125">Этот параметр обеспечивает поддержку приложений, зависящих от **битов \_ аппстатус DDE** .</span><span class="sxs-lookup"><span data-stu-id="a03e9-125">This parameter provides support for applications dependent on **DDE\_APPSTATUS** bits.</span></span> <span data-ttu-id="a03e9-126">Рекомендуется, чтобы приложения больше не использовали эти биты, они могут не поддерживаться в будущих версиях ДДЕМЛ.</span><span class="sxs-lookup"><span data-stu-id="a03e9-126">It is recommended that applications no longer use these bits   they may not be supported in future versions of the DDEML.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a03e9-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a03e9-127">Remarks</span></span>

<span data-ttu-id="a03e9-128">Приложение не должно освобождать полученный во время этой транзакции маркер данных.</span><span class="sxs-lookup"><span data-stu-id="a03e9-128">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="a03e9-129">Однако приложение должно копировать данные, связанные с этим обработчиком данных, если приложение должно обработать данные после возвращения функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="a03e9-129">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="a03e9-130">Приложение может использовать функцию [**ддежетдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) для копирования данных.</span><span class="sxs-lookup"><span data-stu-id="a03e9-130">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a03e9-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a03e9-131">Requirements</span></span>



| <span data-ttu-id="a03e9-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a03e9-132">Requirement</span></span> | <span data-ttu-id="a03e9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a03e9-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a03e9-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a03e9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a03e9-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a03e9-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a03e9-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a03e9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a03e9-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a03e9-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a03e9-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a03e9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a03e9-139"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a03e9-139"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a03e9-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a03e9-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="a03e9-141">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a03e9-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a03e9-142">**ддеклиенттрансактион**</span><span class="sxs-lookup"><span data-stu-id="a03e9-142">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="a03e9-143">**ддежетдата**</span><span class="sxs-lookup"><span data-stu-id="a03e9-143">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

<span data-ttu-id="a03e9-144">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a03e9-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a03e9-145">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="a03e9-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

