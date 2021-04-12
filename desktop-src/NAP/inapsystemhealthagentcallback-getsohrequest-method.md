---
title: Метод Инапсистемхеалсаженткаллбакк Жетсохрекуест (Напсистемхеалсажент. h)
description: Вызывается с помощью Напажент для запроса агента работоспособности системы.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Метод Жетсохрекуест NAP
- Метод Жетсохрекуест NAP, интерфейс Инапсистемхеалсаженткаллбакк
- Инапсистемхеалсаженткаллбакк интерфейса NAP, метод Жетсохрекуест
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415712"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a><span data-ttu-id="96dd1-106">Метод Инапсистемхеалсаженткаллбакк:: Жетсохрекуест</span><span class="sxs-lookup"><span data-stu-id="96dd1-106">INapSystemHealthAgentCallback::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="96dd1-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="96dd1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="96dd1-108">Метод **инапсистемхеалсаженткаллбакк:: жетсохрекуест** вызывается напажент, чтобы запросить запрос SoH агента работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="96dd1-108">The **INapSystemHealthAgentCallback::GetSoHRequest** method is called by the NapAgent to query the system health agent's SoH request.</span></span>

## <a name="syntax"></a><span data-ttu-id="96dd1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96dd1-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="96dd1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="96dd1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96dd1-111">*запрос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="96dd1-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96dd1-112">Указатель COM на объект [**инапсистемхеалсажентрекуест**](inapsystemhealthagentrequest.md) , который идентифицирует объект запроса.</span><span class="sxs-lookup"><span data-stu-id="96dd1-112">A COM pointer to an [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96dd1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96dd1-113">Return value</span></span>



| <span data-ttu-id="96dd1-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="96dd1-114">Return code</span></span>                                                                                                                      | <span data-ttu-id="96dd1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="96dd1-115">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96dd1-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="96dd1-116"><dt>**S\_OK**</dt></span></span> </dl>                                             | <span data-ttu-id="96dd1-117">Указывает на успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="96dd1-117">Indicates success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="96dd1-118"><dt>**HRESULT \_ из \_ Win32 ( \_ сервер RPC \_ S \_ недоступен)**</dt></span><span class="sxs-lookup"><span data-stu-id="96dd1-118"><dt>**HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**</dt></span></span> </dl> | <span data-ttu-id="96dd1-119">Если этот код возвращается вашей реализацией, Напажент удаляет SHA из списка связанных-SHA и очищает его запись кэша.</span><span class="sxs-lookup"><span data-stu-id="96dd1-119">If this code is returned by your implementation, the NapAgent then removes the SHA from the bound-SHA list and flushes its cache entry.</span></span><br/> |



 

<span data-ttu-id="96dd1-120">Если ваша реализация возвращает любое возвращаемое значение (за исключением **HRESULT \_ из \_ Win32 ( \_ сервер RPC S \_ \_ недоступен)**), система защиты доступа к сети конструирует и возвращает [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) соответствующему SHV со следующими типами атрибутов и значениями:</span><span class="sxs-lookup"><span data-stu-id="96dd1-120">When any return value (except **HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**) is returned by your implementation, the NAP system constructs and returns a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="96dd1-121">[**сохаттрибутетипесистемхеалсид**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="96dd1-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="96dd1-122">[**сохаттрибутетипефаилурекатегори**](sohattributetype-enum.md) =  [ **фаилурекатегориклиенткомпонент**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="96dd1-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="96dd1-123">[**сохаттрибутетипирроркодес**](sohattributetype-enum.md) = <ошибка — код></span><span class="sxs-lookup"><span data-stu-id="96dd1-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <error-code></span></span>

## <a name="remarks"></a><span data-ttu-id="96dd1-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96dd1-124">Remarks</span></span>

<span data-ttu-id="96dd1-125">Этот метод обратного вызова объявляется системой защиты доступа к сети и реализуется модулем записи SHA.</span><span class="sxs-lookup"><span data-stu-id="96dd1-125">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="96dd1-126">Этот метод должен обработать запрос и вернуться немедленно.</span><span class="sxs-lookup"><span data-stu-id="96dd1-126">This method must process the request and return immediately.</span></span> <span data-ttu-id="96dd1-127">Задержка возврата этого метода негативно влияет на производительность и скорость реагирования системы и может привести к истечению времени ожидания других частей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="96dd1-127">Delaying the return of this method negatively impacts system performance and responsiveness, and may cause other parts of the operating system to time out.</span></span>

<span data-ttu-id="96dd1-128">Наблюдение за состоянием работоспособности не следует выполнять в рамках этого вызова, особенно в случае интенсивного выполнения вычислений и занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="96dd1-128">Health state monitoring should not be done as part of this call, especially if it is computation intensive and takes a long time.</span></span> <span data-ttu-id="96dd1-129">Наблюдение за состоянием работоспособности и вычисление работоспособности следует выполнять в отдельном потоке или службе.</span><span class="sxs-lookup"><span data-stu-id="96dd1-129">Health state monitoring and SoH computation should be performed in a separate thread or service.</span></span> <span data-ttu-id="96dd1-130">Единственной функцией этого метода должно быть задание SoH SHA и возврат.</span><span class="sxs-lookup"><span data-stu-id="96dd1-130">The sole function of this method should be to set the SHA's SoH and return.</span></span>

<span data-ttu-id="96dd1-131">Если агент SHA создаст состояние работоспособности, то в Напажент будет возвращено кэшированное состояние работоспособности.</span><span class="sxs-lookup"><span data-stu-id="96dd1-131">If it will take a long time for the SHA to generate a SoH, then the cached SoH should be returned to the NapAgent.</span></span> <span data-ttu-id="96dd1-132">Если нет кэшированного состояния работоспособности для возврата, SHA должен немедленно вернуть SoH со следующими типами атрибутов и значениями:</span><span class="sxs-lookup"><span data-stu-id="96dd1-132">If there is no cached SoH to return, then the SHA should immediately return a SoH with the following attribute types and values:</span></span>

-   <span data-ttu-id="96dd1-133">[**сохаттрибутетипесистемхеалсид**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="96dd1-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="96dd1-134">[**сохаттрибутетипефаилурекатегори**](sohattributetype-enum.md) =  [ **фаилурекатегориклиенткоммуникатион**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="96dd1-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="96dd1-135">[**сохаттрибутетипирроркодес**](sohattributetype-enum.md)  =  [ **Защита доступа к сети \_ E \_ без \_ кэшированного \_ состояния работоспособности**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="96dd1-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NO\_CACHED\_SOH**](nap-error-constants.md)</span></span>

<span data-ttu-id="96dd1-136">После создания SoH агент SHA должен вызвать [**инапсистемхеалсажентбиндинг:: нотифисохчанже**](inapsystemhealthagentbinding-notifysohchange-method.md) , чтобы уведомить напажент об изменении работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="96dd1-136">When the SoH has been generated, the SHA must call [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to notify the NapAgent of the system health change.</span></span>

<span data-ttu-id="96dd1-137">Напажент вызывает этот метод для запроса Сохрекуест агента работоспособности системы.</span><span class="sxs-lookup"><span data-stu-id="96dd1-137">The NapAgent calls this method to query the system health agent's SoHRequest.</span></span> <span data-ttu-id="96dd1-138">SHA может запросить переданный объект [**инапсистемхеалсажентрекуест**](inapsystemhealthagentrequest.md) для параметров, необходимых для расчета сохрекуест.</span><span class="sxs-lookup"><span data-stu-id="96dd1-138">The SHA can query the passed [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object for parameters that it needs to compute the SoHRequest.</span></span> <span data-ttu-id="96dd1-139">SHA должен установить вычисленный Сохрекуест для объекта запроса.</span><span class="sxs-lookup"><span data-stu-id="96dd1-139">The SHA must set the computed SoHRequest on the request object.</span></span> <span data-ttu-id="96dd1-140">По завершении этого вызова SHA не должен содержать ссылки на объект запроса.</span><span class="sxs-lookup"><span data-stu-id="96dd1-140">The SHA must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="96dd1-141">При вызове этого метода, если имеется SoH в кэше Напажент, он задается в объекте запроса.</span><span class="sxs-lookup"><span data-stu-id="96dd1-141">When this method is called, if there is a SoH in the NapAgent's cache, then it is set on the request object.</span></span> <span data-ttu-id="96dd1-142">SHA может запросить его с помощью **жетсохрекуест**.</span><span class="sxs-lookup"><span data-stu-id="96dd1-142">The SHA can query for it using **GetSoHRequest**.</span></span> <span data-ttu-id="96dd1-143">Если агент SHA не устанавливает новое состояние работоспособности, используется кэшированный.</span><span class="sxs-lookup"><span data-stu-id="96dd1-143">If the SHA does not set a new SoH, then the cached one is used.</span></span>

<span data-ttu-id="96dd1-144">Для несвязанных SHA, зарегистрированных в системе, система защиты доступа к сети конструирует и отправляет Сохрекуест в соответствующий SHV со следующими типами атрибутов и значениями:</span><span class="sxs-lookup"><span data-stu-id="96dd1-144">For unbound SHAs which are registered with the system, the NAP system constructs and sends a SoHRequest to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="96dd1-145">[**сохаттрибутетипесистемхеалсид**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="96dd1-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="96dd1-146">[**сохаттрибутетипефаилурекатегори**](sohattributetype-enum.md) =  [ **фаилурекатегориклиенткомпонент**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="96dd1-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="96dd1-147">[**сохаттрибутетипирроркодес**](sohattributetype-enum.md)  =  [ **Защита доступа к сети \_ E \_ не \_ инициализирована**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="96dd1-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NOT\_INITIALIZED**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="96dd1-148">Требования</span><span class="sxs-lookup"><span data-stu-id="96dd1-148">Requirements</span></span>



| <span data-ttu-id="96dd1-149">Требование</span><span class="sxs-lookup"><span data-stu-id="96dd1-149">Requirement</span></span> | <span data-ttu-id="96dd1-150">Значение</span><span class="sxs-lookup"><span data-stu-id="96dd1-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96dd1-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96dd1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="96dd1-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96dd1-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="96dd1-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96dd1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="96dd1-154">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96dd1-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="96dd1-155">Header</span><span class="sxs-lookup"><span data-stu-id="96dd1-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="96dd1-156"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="96dd1-156"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="96dd1-157">IDL</span><span class="sxs-lookup"><span data-stu-id="96dd1-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96dd1-158"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96dd1-158"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96dd1-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96dd1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96dd1-160">**инапсистемхеалсаженткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="96dd1-160">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





