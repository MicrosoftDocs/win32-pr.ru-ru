---
title: XTYP_DISCONNECTная транзакция (Ддемл. h)
description: Функция обратного вызова платформа динамических данных Exchange (DDE) приложения, Ддекаллбакк, получает \_ транзакцию отключения кстип, когда участник приложения в диалоге использует функцию ддедисконнект для завершения диалога.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- XTYP_DISCONNECT обмена данными транзакций
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801397"
---
# <a name="xtyp_disconnect-transaction"></a><span data-ttu-id="1894b-104">КСТИП \_ Отключить транзакцию</span><span class="sxs-lookup"><span data-stu-id="1894b-104">XTYP\_DISCONNECT transaction</span></span>

<span data-ttu-id="1894b-105">Функция обратного вызова платформа динамических данных Exchange (DDE) приложения, [*ддекаллбакк*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), Получает транзакцию **\_ отключения кстип** , когда участник приложения в диалоге использует функцию [**ддедисконнект**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) для завершения диалога.</span><span class="sxs-lookup"><span data-stu-id="1894b-105">An application's Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_DISCONNECT** transaction when the application's partner in a conversation uses the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function to terminate the conversation.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="1894b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1894b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1894b-107">*утипе*</span><span class="sxs-lookup"><span data-stu-id="1894b-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="1894b-108">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="1894b-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="1894b-109">*уфмт*</span><span class="sxs-lookup"><span data-stu-id="1894b-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1894b-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1894b-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1894b-111">*хконв*</span><span class="sxs-lookup"><span data-stu-id="1894b-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="1894b-112">Маркер для того, что диалог был завершен.</span><span class="sxs-lookup"><span data-stu-id="1894b-112">A handle to that the conversation was terminated.</span></span>

</dd> <dt>

<span data-ttu-id="1894b-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="1894b-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="1894b-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1894b-114">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1894b-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="1894b-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="1894b-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1894b-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1894b-117">*хдата*</span><span class="sxs-lookup"><span data-stu-id="1894b-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="1894b-118">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1894b-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1894b-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="1894b-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="1894b-120">Не используется.</span><span class="sxs-lookup"><span data-stu-id="1894b-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1894b-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="1894b-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="1894b-122">Указывает, являются ли участники диалога одним и тем же экземпляром приложения.</span><span class="sxs-lookup"><span data-stu-id="1894b-122">Specifies whether the partners in the conversation are the same application instance.</span></span> <span data-ttu-id="1894b-123">Если этот параметр равен 1, то партнеры являются одним и тем же экземпляром.</span><span class="sxs-lookup"><span data-stu-id="1894b-123">If this parameter is 1, the partners are the same instance.</span></span> <span data-ttu-id="1894b-124">Если этот параметр равен 0, то участники являются разными экземплярами.</span><span class="sxs-lookup"><span data-stu-id="1894b-124">If this parameter is 0, the partners are different instances.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1894b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1894b-125">Remarks</span></span>

<span data-ttu-id="1894b-126">Эта транзакция фильтруется, если приложение указало флаг **КБФ \_ Skip \_ unconnected** в функции [**ддеинитиализе**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="1894b-126">This transaction is filtered if the application specified the **CBF\_SKIP\_DISCONNECTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="1894b-127">Приложение может получить состояние прерванного диалога, вызвав функцию [**ддекуериконвинфо**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) при обработке этой транзакции.</span><span class="sxs-lookup"><span data-stu-id="1894b-127">The application can obtain the status of the terminated conversation by calling the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function while processing this transaction.</span></span> <span data-ttu-id="1894b-128">После возврата функции обратного вызова этот обработчик станет недействительным.</span><span class="sxs-lookup"><span data-stu-id="1894b-128">The conversation handle becomes invalid after the callback function returns.</span></span>

<span data-ttu-id="1894b-129">Приложение не может блокировать этот тип транзакции; код **возврата \_ блока CBR** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1894b-129">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1894b-130">Требования</span><span class="sxs-lookup"><span data-stu-id="1894b-130">Requirements</span></span>



| <span data-ttu-id="1894b-131">Требование</span><span class="sxs-lookup"><span data-stu-id="1894b-131">Requirement</span></span> | <span data-ttu-id="1894b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="1894b-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1894b-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1894b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1894b-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1894b-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1894b-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1894b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1894b-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1894b-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1894b-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1894b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1894b-138"><dt>Ддемл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1894b-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1894b-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1894b-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="1894b-140">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="1894b-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1894b-141">**ддедисконнект**</span><span class="sxs-lookup"><span data-stu-id="1894b-141">**DdeDisconnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[<span data-ttu-id="1894b-142">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="1894b-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="1894b-143">**ддекуериконвинфо**</span><span class="sxs-lookup"><span data-stu-id="1894b-143">**DdeQueryConvInfo**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

<span data-ttu-id="1894b-144">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="1894b-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1894b-145">Библиотека управления платформа динамических данных Exchange</span><span class="sxs-lookup"><span data-stu-id="1894b-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

