---
title: XTYP_ERRORная транзакция (Ддемл. h)
description: Функция обратного вызова платформа динамических данных Exchange (DDE), Ддекаллбакк, получает \_ транзакцию ошибки кстип при возникновении критической ошибки.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- XTYP_ERROR обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701042"
---
# <a name="xtyp_error-transaction"></a><span data-ttu-id="38cbf-104">КСТИП \_ Ошибка транзакции</span><span class="sxs-lookup"><span data-stu-id="38cbf-104">XTYP\_ERROR transaction</span></span>

<span data-ttu-id="38cbf-105">Функция обратного вызова платформа динамических данных Exchange (DDE), [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), Получает транзакцию **\_ ошибки кстип** при возникновении критической ошибки.</span><span class="sxs-lookup"><span data-stu-id="38cbf-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_ERROR** transaction when a critical error occurs.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="38cbf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38cbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38cbf-107">*утипе*</span><span class="sxs-lookup"><span data-stu-id="38cbf-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="38cbf-108">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="38cbf-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="38cbf-109">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="38cbf-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="38cbf-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="38cbf-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="38cbf-111">*хконв*</span><span class="sxs-lookup"><span data-stu-id="38cbf-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="38cbf-112">Обработчик диалога, связанный с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="38cbf-112">A handle to the conversation associated with the error.</span></span> <span data-ttu-id="38cbf-113">Этот параметр имеет **значение NULL** , если ошибка не связана с диалогом.</span><span class="sxs-lookup"><span data-stu-id="38cbf-113">This parameter is **NULL** if the error is not associated with a conversation.</span></span>

</dd> <dt>

<span data-ttu-id="38cbf-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="38cbf-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="38cbf-115">Не используется.</span><span class="sxs-lookup"><span data-stu-id="38cbf-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="38cbf-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="38cbf-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="38cbf-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="38cbf-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="38cbf-118">*хдата*</span><span class="sxs-lookup"><span data-stu-id="38cbf-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="38cbf-119">Не используется.</span><span class="sxs-lookup"><span data-stu-id="38cbf-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="38cbf-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="38cbf-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="38cbf-121">Код ошибки в слове низкого порядка.</span><span class="sxs-lookup"><span data-stu-id="38cbf-121">The error code in the low-order word.</span></span> <span data-ttu-id="38cbf-122">В настоящее время поддерживается только следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="38cbf-122">Currently, only the following error code is supported.</span></span>



| <span data-ttu-id="38cbf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="38cbf-123">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="38cbf-124">Значение</span><span class="sxs-lookup"><span data-stu-id="38cbf-124">Meaning</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <span data-ttu-id="38cbf-125"><dt>**ДМЛЕРР \_ нехватка \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="38cbf-125"><dt>**DMLERR\_LOW\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="38cbf-126">Недостаточно памяти; может быть потеряно предложение, вставка или выполнение данных, иначе может произойти сбой системы.</span><span class="sxs-lookup"><span data-stu-id="38cbf-126">Memory is low; advise, poke, or execute data may be lost, or the system may fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="38cbf-127">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="38cbf-127">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="38cbf-128">Не используется.</span><span class="sxs-lookup"><span data-stu-id="38cbf-128">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38cbf-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38cbf-129">Remarks</span></span>

<span data-ttu-id="38cbf-130">Приложение не может блокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="38cbf-130">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span> <span data-ttu-id="38cbf-131">Библиотека управления платформа динамических данных Exchange (ДДЕМЛ) пытается освободить память путем удаления некритических ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38cbf-131">The Dynamic Data Exchange Management Library (DDEML) attempts to free memory by removing noncritical resources.</span></span> <span data-ttu-id="38cbf-132">Приложение с заблокированными диалогами должно разблокировать их.</span><span class="sxs-lookup"><span data-stu-id="38cbf-132">An application that has blocked conversations should unblock them.</span></span>

## <a name="requirements"></a><span data-ttu-id="38cbf-133">Требования</span><span class="sxs-lookup"><span data-stu-id="38cbf-133">Requirements</span></span>



| <span data-ttu-id="38cbf-134">Требование</span><span class="sxs-lookup"><span data-stu-id="38cbf-134">Requirement</span></span> | <span data-ttu-id="38cbf-135">Значение</span><span class="sxs-lookup"><span data-stu-id="38cbf-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38cbf-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38cbf-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38cbf-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38cbf-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="38cbf-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38cbf-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38cbf-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="38cbf-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="38cbf-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="38cbf-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="38cbf-141"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38cbf-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38cbf-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38cbf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38cbf-143">Общие сведения о библиотеке управления Exchange платформа динамических данных</span><span class="sxs-lookup"><span data-stu-id="38cbf-143">Dynamic Data Exchange Management Library Overview</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

