---
title: XTYP_UNREGISTERная транзакция (Ддемл. h)
description: Функция обратного вызова платформа динамических данных Exchange (DDE) получает КСТИП \_ отмену регистрации транзакции, когда платформа динамических данных серверное приложение библиотеки управления Exchange (ддемл) использует функцию дденамесервице для отмены регистрации имени службы или в случае, если не ддемл приложение, поддерживающее системный раздел, завершается.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- XTYP_UNREGISTER обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803304"
---
# <a name="xtyp_unregister-transaction"></a><span data-ttu-id="d7409-104">КСТИП \_ отменить регистрацию транзакции</span><span class="sxs-lookup"><span data-stu-id="d7409-104">XTYP\_UNREGISTER transaction</span></span>

<span data-ttu-id="d7409-105">Функция обратного вызова платформа динамических данных Exchange (DDE) получает **КСТИП \_ отмену регистрации** [*транзакции, когда*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)платформа динамических данных серверное приложение библиотеки управления Exchange (ддемл) использует функцию [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) для отмены регистрации имени службы или в случае, если не ддемл приложение, поддерживающее системный раздел, завершается.</span><span class="sxs-lookup"><span data-stu-id="d7409-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_UNREGISTER** transaction whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to unregister a service name, or whenever a non-DDEML application that supports the System topic is terminated.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="d7409-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7409-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7409-107">*утипе*</span><span class="sxs-lookup"><span data-stu-id="d7409-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="d7409-108">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="d7409-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="d7409-109">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="d7409-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d7409-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d7409-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7409-111">*хконв*</span><span class="sxs-lookup"><span data-stu-id="d7409-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="d7409-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d7409-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7409-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="d7409-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="d7409-114">Описатель для имени базовой службы, регистрация которого отменяется.</span><span class="sxs-lookup"><span data-stu-id="d7409-114">A handle to the base service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="d7409-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="d7409-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="d7409-116">Незарегистрированный обработчик для имени службы, зависящей от экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d7409-116">A handle to the instance-specific service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="d7409-117">*хдата*</span><span class="sxs-lookup"><span data-stu-id="d7409-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="d7409-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d7409-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7409-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="d7409-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="d7409-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d7409-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d7409-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="d7409-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="d7409-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d7409-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7409-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7409-123">Remarks</span></span>

<span data-ttu-id="d7409-124">Эта транзакция фильтруется, если приложение указало флаг **КБФ \_ пропустить \_ регистрации** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="d7409-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="d7409-125">Приложение не может блокировать этот тип транзакции; \_код возврата блока CBR игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d7409-125">A application cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

<span data-ttu-id="d7409-126">Приложение должно использовать параметр *hsz1* для удаления имени службы из списка серверов, доступных пользователю.</span><span class="sxs-lookup"><span data-stu-id="d7409-126">An application should use the *hsz1* parameter to remove the service name from the list of servers available to the user.</span></span> <span data-ttu-id="d7409-127">Приложение должно использовать параметр *hsz2* для указания того, какой экземпляр приложения завершил работу.</span><span class="sxs-lookup"><span data-stu-id="d7409-127">An application should use the *hsz2* parameter to identify which application instance has terminated.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7409-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d7409-128">Requirements</span></span>



| <span data-ttu-id="d7409-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d7409-129">Requirement</span></span> | <span data-ttu-id="d7409-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d7409-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7409-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7409-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d7409-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7409-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7409-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7409-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d7409-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7409-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d7409-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d7409-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7409-136"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7409-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7409-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7409-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7409-138">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d7409-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d7409-139">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="d7409-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="d7409-140">**дденамесервице**</span><span class="sxs-lookup"><span data-stu-id="d7409-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="d7409-141">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d7409-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d7409-142">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="d7409-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

