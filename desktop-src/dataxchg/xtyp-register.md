---
title: XTYP_REGISTERная транзакция (Ддемл. h)
description: Функция обратного вызова платформа динамических данных Exchange (DDE) получает \_ тип транзакции Register кстип каждый раз, когда платформа динамических данных серверное приложение библиотеки управления Exchange (ддемл) использует функцию дденамесервице для регистрации имени службы или при каждом запуске приложения, не ЯВЛЯЮЩЕГОСЯ ддемл, которое поддерживает системный раздел.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd56bf4f5ac2b4eb0f714e5348174942f685c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490071"
---
# <a name="xtyp_register-transaction"></a><span data-ttu-id="5480f-104">КСТИП \_ зарегистрировать транзакцию</span><span class="sxs-lookup"><span data-stu-id="5480f-104">XTYP\_REGISTER transaction</span></span>

<span data-ttu-id="5480f-105">Функция обратного вызова платформа динамических данных Exchange (DDE) получает тип транзакции **\_ Register кстип** каждый [*раз, когда*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)платформа динамических данных серверное приложение библиотеки управления Exchange (ддемл) использует функцию [**дденамесервице**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) для регистрации имени службы или при каждом запуске приложения, не являющегося ддемл, которое поддерживает системный раздел.</span><span class="sxs-lookup"><span data-stu-id="5480f-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_REGISTER** transaction type whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to register a service name, or whenever a non-DDEML application that supports the System topic is started.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="5480f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5480f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5480f-107">*утипе*</span><span class="sxs-lookup"><span data-stu-id="5480f-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="5480f-108">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="5480f-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="5480f-109">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="5480f-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5480f-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5480f-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5480f-111">*хконв*</span><span class="sxs-lookup"><span data-stu-id="5480f-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="5480f-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5480f-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5480f-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="5480f-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="5480f-114">Регистрируемое имя базовой службы.</span><span class="sxs-lookup"><span data-stu-id="5480f-114">A handle to the base service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="5480f-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="5480f-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="5480f-116">Регистрация регистрируемого имени службы для конкретного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5480f-116">A handle to the instance-specific service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="5480f-117">*хдата*</span><span class="sxs-lookup"><span data-stu-id="5480f-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="5480f-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5480f-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5480f-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="5480f-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="5480f-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5480f-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5480f-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="5480f-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="5480f-122">Не используется.</span><span class="sxs-lookup"><span data-stu-id="5480f-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5480f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5480f-123">Remarks</span></span>

<span data-ttu-id="5480f-124">Эта транзакция фильтруется, если приложение указало флаг **КБФ \_ пропустить \_ регистрации** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="5480f-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="5480f-125">Приложение не может блокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="5480f-125">A application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

<span data-ttu-id="5480f-126">Приложение должно использовать параметр *hsz1* , чтобы добавить имя службы в список серверов, доступных пользователю.</span><span class="sxs-lookup"><span data-stu-id="5480f-126">An application should use the *hsz1* parameter to add the service name to the list of servers available to the user.</span></span> <span data-ttu-id="5480f-127">Приложение должно использовать параметр *hsz2* для указания того, какой экземпляр приложения запущен.</span><span class="sxs-lookup"><span data-stu-id="5480f-127">An application should use the *hsz2* parameter to identify which application instance has started.</span></span>

## <a name="requirements"></a><span data-ttu-id="5480f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="5480f-128">Requirements</span></span>



| <span data-ttu-id="5480f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="5480f-129">Requirement</span></span> | <span data-ttu-id="5480f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5480f-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5480f-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5480f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5480f-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5480f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5480f-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5480f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5480f-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5480f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5480f-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5480f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5480f-136"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5480f-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5480f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5480f-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="5480f-138">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5480f-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5480f-139">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="5480f-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="5480f-140">**дденамесервице**</span><span class="sxs-lookup"><span data-stu-id="5480f-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="5480f-141">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5480f-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5480f-142">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="5480f-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

