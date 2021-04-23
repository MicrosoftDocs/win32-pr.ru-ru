---
title: Функция Инитиализенапажентнотифиер (Напутил. h)
description: Подписывает вызывающий процесс для Напажент уведомлений об изменении состояния и уведомлений об изменении состояния карантина.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- Инитиализенапажентнотифиер функция NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988438"
---
# <a name="initializenapagentnotifier-function"></a><span data-ttu-id="c958d-104">Функция Инитиализенапажентнотифиер</span><span class="sxs-lookup"><span data-stu-id="c958d-104">InitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="c958d-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="c958d-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c958d-106">Функция **инитиализенапажентнотифиер** подписывает вызывающий процесс для напажент уведомлений об изменении состояния и уведомлений об изменении состояния карантина.</span><span class="sxs-lookup"><span data-stu-id="c958d-106">The **InitializeNapAgentNotifier** function subscribes the calling process to NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="c958d-107">Эти уведомления предоставляются службой Напажент.</span><span class="sxs-lookup"><span data-stu-id="c958d-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c958d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c958d-108">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a><span data-ttu-id="c958d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c958d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c958d-110">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c958d-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c958d-111">Значение [**напнотифитипе**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) , указывающее тип получаемых уведомлений службы.</span><span class="sxs-lookup"><span data-stu-id="c958d-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to receive.</span></span>

</dd> <dt>

<span data-ttu-id="c958d-112">*хнотифевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c958d-112">*hNotifyEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c958d-113">Обработчик событий, используемый для уведомления.</span><span class="sxs-lookup"><span data-stu-id="c958d-113">An event handle used for notification.</span></span> <span data-ttu-id="c958d-114">Вызывающий объект должен передать открытый маркер параметру *хнотифевент* .</span><span class="sxs-lookup"><span data-stu-id="c958d-114">The caller must pass an open handle to the *hNotifyEvent* parameter.</span></span> <span data-ttu-id="c958d-115">Вызывающий объект также должен закрыть обработчик событий, когда он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="c958d-115">The caller must also close the event handle when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c958d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c958d-116">Return value</span></span>



| <span data-ttu-id="c958d-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c958d-117">Return code</span></span>                                                                                                | <span data-ttu-id="c958d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c958d-118">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c958d-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c958d-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c958d-120">Инициализация успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="c958d-120">Initialization completed successfully.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="c958d-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="c958d-121"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="c958d-122">Ошибка инициализации.</span><span class="sxs-lookup"><span data-stu-id="c958d-122">Initialization failed.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="c958d-123"><dt>**Ошибка \_ уже \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="c958d-123"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="c958d-124">Этот процесс уже подписался на уведомления службы Напажент указанного *типа* .</span><span class="sxs-lookup"><span data-stu-id="c958d-124">The process has already subscribed to NapAgent service notifications of the *type* specified.</span></span> <br/> |
| <dl> <span data-ttu-id="c958d-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c958d-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="c958d-126">Передан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="c958d-126">An invalid argument was passed.</span></span> <br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="c958d-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c958d-127">Remarks</span></span>

<span data-ttu-id="c958d-128">Эта функция не является потокобезопасной.</span><span class="sxs-lookup"><span data-stu-id="c958d-128">This function is not thread safe.</span></span>

<span data-ttu-id="c958d-129">Каждый процесс, которому требуется подписка на уведомления службы Напажент указанного *типа* , должен вызвать **инитиализенапажентнотифиер** для подписки на уведомления.</span><span class="sxs-lookup"><span data-stu-id="c958d-129">Each process that requires a subscription to NapAgent service notifications of the specified *type* must call **InitializeNapAgentNotifier** to subscribe to notifications.</span></span> <span data-ttu-id="c958d-130">Если процесс должен подписываться на более одного типа уведомлений, он должен вызывать **инитиализенапажентнотифиер** один раз для каждого типа уведомления.</span><span class="sxs-lookup"><span data-stu-id="c958d-130">If a process must subscribe to more than one type of notification, it must call **InitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="c958d-131">Когда процесс не требует дальнейших уведомлений, процесс должен вызвать [**унинитиализенапажентнотифиер**](uninitializenapagentnotifier.md) для указанного *типа*.</span><span class="sxs-lookup"><span data-stu-id="c958d-131">Once a process does not require further notifications, the process must call [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) for the specified *type*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c958d-132">Требования</span><span class="sxs-lookup"><span data-stu-id="c958d-132">Requirements</span></span>



| <span data-ttu-id="c958d-133">Требование</span><span class="sxs-lookup"><span data-stu-id="c958d-133">Requirement</span></span> | <span data-ttu-id="c958d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="c958d-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c958d-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c958d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c958d-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c958d-136">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c958d-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c958d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c958d-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c958d-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c958d-139">Header</span><span class="sxs-lookup"><span data-stu-id="c958d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c958d-140"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="c958d-140"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="c958d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c958d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c958d-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c958d-142"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c958d-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c958d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c958d-144">**унинитиализенапажентнотифиер**</span><span class="sxs-lookup"><span data-stu-id="c958d-144">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





