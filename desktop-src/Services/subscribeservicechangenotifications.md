---
description: Подписывается на уведомления об изменении состояния службы с помощью функции обратного вызова.
ms.assetid: d67113eb-2141-444c-9f09-eaa772bcad8a
title: Функция Субскрибесервицечанженотификатионс (Винсвкп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscribeServiceChangeNotifications
api_type:
- DllExport
api_location:
- SecHost.dll
- API-MS-Win-Service-Private-L1-1-0.dll
- API-MS-Win-Service-Private-L1-1-1.dll
- Advapi32.dll
- API-MS-Win-Service-Private-L1-1-2.dll
ms.openlocfilehash: e327a44d613b514123862b1ddcb1bf302fea63ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664092"
---
# <a name="subscribeservicechangenotifications-function"></a><span data-ttu-id="713f1-103">Функция Субскрибесервицечанженотификатионс</span><span class="sxs-lookup"><span data-stu-id="713f1-103">SubscribeServiceChangeNotifications function</span></span>

<span data-ttu-id="713f1-104">Подписывается на уведомления об изменении состояния службы с помощью функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="713f1-104">Subscribes for service status change notifications using a callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="713f1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="713f1-105">Syntax</span></span>


```C++
DWORD WINAPI SubscribeServiceChangeNotifications(
  _In_     SC_HANDLE                     hService,
  _In_     SC_EVENT_TYPE                 eEventType,
  _In_     PSC_NOTIFICATION_CALLBACK     pCallback,
  _In_opt_ PVOID                         pCallbackContext,
  _Out_    PSC_NOTIFICATION_REGISTRATION *pSubscription
);
```



## <a name="parameters"></a><span data-ttu-id="713f1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="713f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="713f1-107">*хсервице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713f1-107">*hService* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713f1-108">Обработчик для службы или обработчик диспетчера управления службами (SCM), который отслеживает изменения.</span><span class="sxs-lookup"><span data-stu-id="713f1-108">A handle to the service or a handle to the service control manager (SCM) to monitor for changes.</span></span>

<span data-ttu-id="713f1-109">Дескрипторы служб возвращаются функцией [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) и [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) и должны иметь права доступа к **\_ \_ состоянию запроса на обслуживание** .</span><span class="sxs-lookup"><span data-stu-id="713f1-109">Handles to services are returned by the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) and [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function and must have the **SERVICE\_QUERY\_STATUS** access right.</span></span> <span data-ttu-id="713f1-110">Дескрипторы диспетчера управления службами возвращаются функцией [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) и должны иметь право на **\_ \_ Перечисление \_ доступа к службе в диспетчере SC** .</span><span class="sxs-lookup"><span data-stu-id="713f1-110">Handles to the service control manager are returned by the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function and must have the **SC\_MANAGER\_ENUMERATE\_SERVICE** access right.</span></span>

</dd> <dt>

<span data-ttu-id="713f1-111">*ивенттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713f1-111">*eEventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713f1-112">Указывает тип изменений состояния, о которых следует сообщать.</span><span class="sxs-lookup"><span data-stu-id="713f1-112">Specifies the type of status changes that should be reported.</span></span> <span data-ttu-id="713f1-113">Для этого параметра задается одно из значений, указанных [**в \_ \_ типе событий SC**](sc-event-type.md).</span><span class="sxs-lookup"><span data-stu-id="713f1-113">This parameter is set to one of the values specified in [**SC\_EVENT\_TYPE**](sc-event-type.md).</span></span> <span data-ttu-id="713f1-114">Поведение этой функции отличается в зависимости от типа события, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="713f1-114">The behavior for this function is different depending on the event type as follows.</span></span>



| <span data-ttu-id="713f1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="713f1-115">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="713f1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="713f1-116">Meaning</span></span>                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span><dl> <span data-ttu-id="713f1-117"><dt>**SC \_ \_ \_ Изменение базы данных событий**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="713f1-117"><dt>**SC\_EVENT\_DATABASE\_CHANGE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="713f1-118">Служба была добавлена или удалена.</span><span class="sxs-lookup"><span data-stu-id="713f1-118">A service has been added or deleted.</span></span> <span data-ttu-id="713f1-119">Параметр *хсервице* должен быть обработчиком SCM.</span><span class="sxs-lookup"><span data-stu-id="713f1-119">The *hService* parameter must be a handle to the SCM.</span></span><br/>                  |
| <span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span><dl> <span data-ttu-id="713f1-120"><dt>**SC \_ \_ \_ Изменение свойства события**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="713f1-120"><dt>**SC\_EVENT\_PROPERTY\_CHANGE**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="713f1-121">Одно или несколько свойств службы были обновлены.</span><span class="sxs-lookup"><span data-stu-id="713f1-121">One or more service properties have been updated.</span></span> <span data-ttu-id="713f1-122">Параметр *хсервице* должен быть маркером службы.</span><span class="sxs-lookup"><span data-stu-id="713f1-122">The *hService* parameter must be a handle to the service.</span></span><br/> |
| <span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span><dl> <span data-ttu-id="713f1-123"><dt>**SC \_ \_ \_ Изменение состояния события**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="713f1-123"><dt>**SC\_EVENT\_STATUS\_CHANGE**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="713f1-124">Состояние службы изменилось.</span><span class="sxs-lookup"><span data-stu-id="713f1-124">The status of a service has changed.</span></span> <span data-ttu-id="713f1-125">Параметр *хсервице* должен быть маркером службы.</span><span class="sxs-lookup"><span data-stu-id="713f1-125">The *hService* parameter must be a handle to the service.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="713f1-126">*пкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713f1-126">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713f1-127">Указывает функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="713f1-127">Specifies the callback function.</span></span> <span data-ttu-id="713f1-128">Обратный вызов должен быть определен как имеющий тип **\_ \_ обратного вызова для уведомлений SC**.</span><span class="sxs-lookup"><span data-stu-id="713f1-128">The callback must be defined as having a type of **SC\_NOTIFICATION\_CALLBACK**.</span></span> <span data-ttu-id="713f1-129">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="713f1-129">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="713f1-130">*пкаллбаккконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="713f1-130">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="713f1-131">Указатель, представляющий контекст для этого обратного вызова уведомления.</span><span class="sxs-lookup"><span data-stu-id="713f1-131">A pointer representing the context for this notification callback.</span></span>

</dd> <dt>

<span data-ttu-id="713f1-132">*псубскриптион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="713f1-132">*pSubscription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="713f1-133">Возвращает указатель на подписку, полученную при регистрации обратного вызова уведомлений.</span><span class="sxs-lookup"><span data-stu-id="713f1-133">Returns a pointer to the subscription resulting from the notification callback registration.</span></span> <span data-ttu-id="713f1-134">Вызывающий объект отвечает за вызов [**унсубскрибесервицечанженотификатионс**](unsubscribeservicechangenotifications.md) для отмены получения уведомлений.</span><span class="sxs-lookup"><span data-stu-id="713f1-134">The caller is responsible for calling [**UnsubscribeServiceChangeNotifications**](unsubscribeservicechangenotifications.md) to stop receiving notifications.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="713f1-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="713f1-135">Return value</span></span>

<span data-ttu-id="713f1-136">Если функция завершается успешно, возвращается значение **ошибки \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="713f1-136">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="713f1-137">Если функция завершается ошибкой, возвращаемое значение является одним из [кодов системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="713f1-137">If the function fails, the return value is one of the [system error codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="remarks"></a><span data-ttu-id="713f1-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="713f1-138">Remarks</span></span>

<span data-ttu-id="713f1-139">Функция обратного вызова объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="713f1-139">The callback function is declared as follows:</span></span>


```C++
typedef VOID CALLBACK SC_NOTIFICATION_CALLBACK(
    _In_    DWORD                   dwNotify,
    _In_    PVOID                   pCallbackContext
);
typedef SC_NOTIFICATION_CALLBACK* PSC_NOTIFICATION_CALLBACK;
```



<span data-ttu-id="713f1-140">Функция обратного вызова получает указатель на контекст, предоставленный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="713f1-140">The callback function receives a pointer to the context provided by the caller.</span></span> <span data-ttu-id="713f1-141">Обратный вызов вызывается в результате события изменения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="713f1-141">The callback is invoked as a result of the service status change event.</span></span> <span data-ttu-id="713f1-142">При вызове обратного вызова он предоставляется с битовой маской для значений \*\*службы \_ Notify \_ \* xxx\*\*\*, указывающей на тип изменения состояния службы.</span><span class="sxs-lookup"><span data-stu-id="713f1-142">When the callback is invoked, it is provided with a bitmask of **SERVICE\_NOTIFY\_\*XXX**\* values that indicating the type of service status change.</span></span> <span data-ttu-id="713f1-143">Если обратный вызов предоставляется с нулевым значением вместо допустимого значения \*\*службы \_ Notify \_ \* xxx\*\*\*, приложение должно проверить, что было изменено.</span><span class="sxs-lookup"><span data-stu-id="713f1-143">When the callback is provided with zero instead of a valid **SERVICE\_NOTIFY\_\*XXX**\* value, the application must verify what was changed.</span></span>

<span data-ttu-id="713f1-144">Функция обратного вызова не должна блокировать выполнение.</span><span class="sxs-lookup"><span data-stu-id="713f1-144">The callback function must not block execution.</span></span> <span data-ttu-id="713f1-145">Если предполагается, что выполнение функции ответного вызова займет некоторое время, разгрузите работу, выполняемую в функции обратного вызова, в отдельный поток, поочередно добавив рабочий элемент в поток в пуле потоков.</span><span class="sxs-lookup"><span data-stu-id="713f1-145">If you expect the execution of the callback function to take time, offload the work that you perform in the callback function to a separate thread by queuing a work item to a thread in a thread pool.</span></span> <span data-ttu-id="713f1-146">Некоторые виды работы, которые могут сделать функцию обратного вызова, занимают некоторое время, включают выполнение файлового ввода-вывода, ожидание события и выполнение внешних вызовов удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="713f1-146">Some types of work that can make the callback function take time include performing file I/O, waiting on an event, and making external remote procedure calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="713f1-147">Требования</span><span class="sxs-lookup"><span data-stu-id="713f1-147">Requirements</span></span>



| <span data-ttu-id="713f1-148">Требование</span><span class="sxs-lookup"><span data-stu-id="713f1-148">Requirement</span></span> | <span data-ttu-id="713f1-149">Значение</span><span class="sxs-lookup"><span data-stu-id="713f1-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="713f1-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="713f1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="713f1-151">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="713f1-151">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="713f1-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="713f1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="713f1-153">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="713f1-153">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="713f1-154">Header</span><span class="sxs-lookup"><span data-stu-id="713f1-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="713f1-155"><dt>Винсвкп. h</dt></span><span class="sxs-lookup"><span data-stu-id="713f1-155"><dt>Winsvcp.h</dt></span></span> </dl>   |
| <span data-ttu-id="713f1-156">DLL</span><span class="sxs-lookup"><span data-stu-id="713f1-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="713f1-157"><dt>SecHost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="713f1-157"><dt>SecHost.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="713f1-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="713f1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="713f1-159">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="713f1-159">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)
</dt> <dt>

[<span data-ttu-id="713f1-160">**OpenService**</span><span class="sxs-lookup"><span data-stu-id="713f1-160">**OpenService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)
</dt> <dt>

[<span data-ttu-id="713f1-161">**OpenSCManager**</span><span class="sxs-lookup"><span data-stu-id="713f1-161">**OpenSCManager**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)
</dt> <dt>

[<span data-ttu-id="713f1-162">**унсубскрибесервицечанженотификатионс**</span><span class="sxs-lookup"><span data-stu-id="713f1-162">**UnsubscribeServiceChangeNotifications**</span></span>](unsubscribeservicechangenotifications.md)
</dt> <dt>

[<span data-ttu-id="713f1-163">**куерисервицединамиЦинформатион**</span><span class="sxs-lookup"><span data-stu-id="713f1-163">**QueryServiceDynamicInformation**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation)
</dt> </dl>

 

