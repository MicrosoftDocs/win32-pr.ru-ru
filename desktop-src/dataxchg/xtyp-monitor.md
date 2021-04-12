---
title: XTYP_MONITORная транзакция (Ддемл. h)
description: Функция обратного вызова DDE в отладчике платформа динамических данных Exchange (DDE), Ддекаллбакк, получает \_ транзакцию монитора кстип при каждом возникновении в системе события DDE.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- XTYP_MONITOR обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415309"
---
# <a name="xtyp_monitor-transaction"></a><span data-ttu-id="c37d6-104">\_Транзакция монитора кстип</span><span class="sxs-lookup"><span data-stu-id="c37d6-104">XTYP\_MONITOR transaction</span></span>

<span data-ttu-id="c37d6-105">Функция обратного вызова DDE в отладчике платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), Получает транзакцию **\_ монитора кстип** при каждом возникновении в системе события DDE.</span><span class="sxs-lookup"><span data-stu-id="c37d6-105">A Dynamic Data Exchange (DDE) debugger's DDE callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_MONITOR** transaction whenever a DDE event occurs in the system.</span></span> <span data-ttu-id="c37d6-106">Чтобы получить эту транзакцию, приложение должно указать значение **\_ монитора APPCLASS** при вызове функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="c37d6-106">To receive this transaction, an application must specify the **APPCLASS\_MONITOR** value when it calls the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="c37d6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c37d6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c37d6-108">*утипе*</span><span class="sxs-lookup"><span data-stu-id="c37d6-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="c37d6-109">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="c37d6-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="c37d6-110">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="c37d6-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c37d6-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c37d6-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c37d6-112">*хконв*</span><span class="sxs-lookup"><span data-stu-id="c37d6-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="c37d6-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c37d6-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c37d6-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="c37d6-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="c37d6-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c37d6-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c37d6-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="c37d6-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="c37d6-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c37d6-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c37d6-118">*хдата*</span><span class="sxs-lookup"><span data-stu-id="c37d6-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="c37d6-119">Маркер объекта DDE, который содержит сведения о событии DDE.</span><span class="sxs-lookup"><span data-stu-id="c37d6-119">A handle to a DDE object that contains information about the DDE event.</span></span> <span data-ttu-id="c37d6-120">Приложение должно использовать функцию [**ддеакцессдата**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) для получения указателя на объект.</span><span class="sxs-lookup"><span data-stu-id="c37d6-120">The application should use the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function to obtain a pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="c37d6-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="c37d6-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="c37d6-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c37d6-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c37d6-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="c37d6-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="c37d6-124">Событие DDE.</span><span class="sxs-lookup"><span data-stu-id="c37d6-124">The DDE event.</span></span> <span data-ttu-id="c37d6-125">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="c37d6-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c37d6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c37d6-126">Value</span></span>                                                                                                                                                                                                                      | <span data-ttu-id="c37d6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c37d6-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <span data-ttu-id="c37d6-128"><dt>**MF \_ ОБРАТные вызовы**</dt> <dt>0x08000000</dt></span><span class="sxs-lookup"><span data-stu-id="c37d6-128"><dt>**MF\_CALLBACKS**</dt> <dt>0x08000000</dt></span></span> </dl> | <span data-ttu-id="c37d6-129">Система послала транзакцию функции обратного вызова DDE.</span><span class="sxs-lookup"><span data-stu-id="c37d6-129">The system sent a transaction to a DDE callback function.</span></span> <span data-ttu-id="c37d6-130">Объект DDE содержит структуру [**монкбструкт**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) , которая предоставляет сведения о транзакции.</span><span class="sxs-lookup"><span data-stu-id="c37d6-130">The DDE object contains a [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) structure that provides information about the transaction.</span></span><br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <span data-ttu-id="c37d6-131"><dt>**MF \_**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="c37d6-131"><dt>**MF\_CONV**</dt> <dt>0x40000000</dt></span></span> </dl>                | <span data-ttu-id="c37d6-132">Сеанс DDE был установлен или прерван.</span><span class="sxs-lookup"><span data-stu-id="c37d6-132">A DDE conversation was established or terminated.</span></span> <span data-ttu-id="c37d6-133">Объект DDE содержит структуру [**монконвструкт**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) , которая предоставляет сведения о диалоге.</span><span class="sxs-lookup"><span data-stu-id="c37d6-133">The DDE object contains a [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) structure that provides information about the conversation.</span></span><br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <span data-ttu-id="c37d6-134"><dt>**MF \_ ОШИБКИ**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="c37d6-134"><dt>**MF\_ERRORS**</dt> <dt>0x10000000</dt></span></span> </dl>          | <span data-ttu-id="c37d6-135">Произошла ошибка DDE.</span><span class="sxs-lookup"><span data-stu-id="c37d6-135">A DDE error occurred.</span></span> <span data-ttu-id="c37d6-136">Объект DDE содержит структуру [**монеррструкт**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) , которая предоставляет сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c37d6-136">The DDE object contains a [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) structure that provides information about the error.</span></span><br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <span data-ttu-id="c37d6-137"><dt>**MF \_ ХСЗ \_ info**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="c37d6-137"><dt>**MF\_HSZ\_INFO**</dt> <dt>0x01000000</dt></span></span> </dl>   | <span data-ttu-id="c37d6-138">Приложение DDE, которое было создано, освобождено или увеличило число использований строкового маркера, или маркер строки был освобожден в результате вызова функции [**ддеунинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="c37d6-138">A DDE application created, freed, or incremented the usage count of a string handle, or a string handle was freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> <span data-ttu-id="c37d6-139">Объект DDE содержит структуру [**монхсзструкт**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) , которая предоставляет сведения о строковом маркере.</span><span class="sxs-lookup"><span data-stu-id="c37d6-139">The DDE object contains a [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure that provides information about the string handle.</span></span><br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <span data-ttu-id="c37d6-140"><dt>**MF \_ ССЫЛКИ**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="c37d6-140"><dt>**MF\_LINKS**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="c37d6-141">Приложение DDE запустило или остановило цикл рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="c37d6-141">A DDE application started or stopped an advise loop.</span></span> <span data-ttu-id="c37d6-142">Объект DDE содержит структуру [**монлинкструкт**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) , которая предоставляет сведения о цикле рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="c37d6-142">The DDE object contains a [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) structure that provides information about the advise loop.</span></span><br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <span data-ttu-id="c37d6-143"><dt>**MF \_ ПОСТМСГС**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="c37d6-143"><dt>**MF\_POSTMSGS**</dt> <dt>0x04000000</dt></span></span> </dl>    | <span data-ttu-id="c37d6-144">Система или приложение разместили сообщение DDE.</span><span class="sxs-lookup"><span data-stu-id="c37d6-144">The system or an application posted a DDE message.</span></span> <span data-ttu-id="c37d6-145">Объект DDE содержит структуру [**монмсгструкт**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) , которая предоставляет сведения о сообщении.</span><span class="sxs-lookup"><span data-stu-id="c37d6-145">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <span data-ttu-id="c37d6-146"><dt>**MF \_ СЕНДМСГС**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="c37d6-146"><dt>**MF\_SENDMSGS**</dt> <dt>0x02000000</dt></span></span> </dl>    | <span data-ttu-id="c37d6-147">Система или приложение отправили сообщение DDE.</span><span class="sxs-lookup"><span data-stu-id="c37d6-147">The system or an application sent a DDE message.</span></span> <span data-ttu-id="c37d6-148">Объект DDE содержит структуру [**монмсгструкт**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) , которая предоставляет сведения о сообщении.</span><span class="sxs-lookup"><span data-stu-id="c37d6-148">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c37d6-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c37d6-149">Return value</span></span>

<span data-ttu-id="c37d6-150">Если функция обратного вызова обрабатывает эту транзакцию, она должна возвращать значение 0.</span><span class="sxs-lookup"><span data-stu-id="c37d6-150">If the callback function processes this transaction, it should return 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="c37d6-151">Требования</span><span class="sxs-lookup"><span data-stu-id="c37d6-151">Requirements</span></span>



| <span data-ttu-id="c37d6-152">Требование</span><span class="sxs-lookup"><span data-stu-id="c37d6-152">Requirement</span></span> | <span data-ttu-id="c37d6-153">Значение</span><span class="sxs-lookup"><span data-stu-id="c37d6-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c37d6-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c37d6-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c37d6-155">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c37d6-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c37d6-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c37d6-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c37d6-157">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c37d6-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c37d6-158">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c37d6-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="c37d6-159"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c37d6-159"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c37d6-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c37d6-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="c37d6-161">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="c37d6-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c37d6-162">**ддеакцессдата**</span><span class="sxs-lookup"><span data-stu-id="c37d6-162">**DdeAccessData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[<span data-ttu-id="c37d6-163">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="c37d6-163">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="c37d6-164">**ддеунинитиализе**</span><span class="sxs-lookup"><span data-stu-id="c37d6-164">**DdeUninitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[<span data-ttu-id="c37d6-165">**монкбструкт**</span><span class="sxs-lookup"><span data-stu-id="c37d6-165">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[<span data-ttu-id="c37d6-166">**монконвструкт**</span><span class="sxs-lookup"><span data-stu-id="c37d6-166">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[<span data-ttu-id="c37d6-167">**монеррструкт**</span><span class="sxs-lookup"><span data-stu-id="c37d6-167">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[<span data-ttu-id="c37d6-168">**монхсзструкт**</span><span class="sxs-lookup"><span data-stu-id="c37d6-168">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[<span data-ttu-id="c37d6-169">**монлинкструкт**</span><span class="sxs-lookup"><span data-stu-id="c37d6-169">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[<span data-ttu-id="c37d6-170">**монмсгструкт**</span><span class="sxs-lookup"><span data-stu-id="c37d6-170">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

<span data-ttu-id="c37d6-171">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="c37d6-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c37d6-172">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="c37d6-172">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

