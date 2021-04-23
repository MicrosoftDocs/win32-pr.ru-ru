---
title: Метод Инапенфорцементклиентбиндинг Процесссохреспонсе (Напенфорцементклиент. h)
description: Используется клиентами принудительного применения для обработки Сохреспонсе при получении большого двоичного объекта Сохреспонсе данных с сервера принудительного применения.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Метод Процесссохреспонсе NAP
- Метод Процесссохреспонсе NAP, интерфейс Инапенфорцементклиентбиндинг
- Инапенфорцементклиентбиндинг интерфейса NAP, метод Процесссохреспонсе
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535531"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a><span data-ttu-id="7fcfb-106">Инапенфорцементклиентбиндинг: метод:P Роцесссохреспонсе</span><span class="sxs-lookup"><span data-stu-id="7fcfb-106">INapEnforcementClientBinding::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="7fcfb-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="7fcfb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7fcfb-108">Метод **инапенфорцементклиентбиндинг::P роцесссохреспонсе** используется клиентами принудительного применения для обработки сохреспонсе каждый раз, когда они получают BLOB-объект сохреспонсе данных с сервера принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-108">The **INapEnforcementClientBinding::ProcessSoHResponse** method is used by enforcement clients to process an SoHResponse whenever they receive an SoHResponse data blob from the enforcement server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fcfb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fcfb-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a><span data-ttu-id="7fcfb-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fcfb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fcfb-111">*Подключение к* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fcfb-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fcfb-112">Указатель COM на интерфейс [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) клиентского соединения.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the client connection.</span></span> <span data-ttu-id="7fcfb-113">Напажент не содержит ссылок на объект, связанный с этим интерфейсом после завершения этого вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-113">The NapAgent does not hold references to the object associated with this interface after this method call completes.</span></span>

<span data-ttu-id="7fcfb-114">Необходимо использовать ранее установленное соединение для обработки больших двоичных объектов данных Сохреспонсе.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-114">You must use a previously established connection for processing SOHResponse data blobs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fcfb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fcfb-115">Return value</span></span>

<span data-ttu-id="7fcfb-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7fcfb-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7fcfb-117">Return code</span></span>                                                                                             | <span data-ttu-id="7fcfb-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7fcfb-118">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fcfb-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-119"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="7fcfb-120">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-120">The operation is successful.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="7fcfb-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="7fcfb-122">На клиенте принудительного применения ранее не было создано ни одного подключения.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-122">No connections have previously been created on the enforcement client.</span></span> <br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="7fcfb-123"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="7fcfb-124">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-124">Permissions error, access denied.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="7fcfb-125"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="7fcfb-126">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-126">System resource limit, could not perform the operation.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="7fcfb-127"><dt>**\_ \_ Недопустимый \_ пакет NAP E**</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-127"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl>  | <span data-ttu-id="7fcfb-128">Если это значение возвращается, клиент принудительного применения должен удалить пакет, если Напажент возвращает \_ \_ Недопустимый \_ пакет NAP E.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-128">If this value is returned the enforcement client must drop the packet if the NapAgent returns NAP\_E\_INVALID\_PACKET.</span></span> <span data-ttu-id="7fcfb-129">В этом случае необходимо предположить, что сервер, на который выполняется речь, не поддерживает NAP и удалил подключение из активного списка (т. е. уведомлять Напажент о состоянии подключения).</span><span class="sxs-lookup"><span data-stu-id="7fcfb-129">In this case, the enforcer must assume that the server it is talking to is not NAP-enabled and remove the connection from the active list (i.e. notify the NapAgent of a connection state down).</span></span><br/> |
| <dl> <span data-ttu-id="7fcfb-130"><dt>**\_ \_ несовпадающий идентификатор NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-130"><dt>**NAP\_E\_MISMATCHED\_ID**</dt></span></span> </dl>   | <span data-ttu-id="7fcfb-131">Если это значение возвращается, это означает, что идентификатор корреляции в пакете SoH-Response не соответствует ожидающему ответу SoH-Response.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-131">If this value is returned it indicates that the correlation id in the SoH-Response packet did not match the outstanding SoH-Response.</span></span> <span data-ttu-id="7fcfb-132">В этом случае необходимо удалить пакет и подождать другой более новый пакет SoH-Response.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-132">In this case, the enforcer should drop the packet and wait for another newer SoH-Response packet.</span></span><br/> <span data-ttu-id="7fcfb-133">Это может быть вызвано ответом на старое сообщение запроса.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-133">This may be caused by a response to an older request message.</span></span><br/>        |
| <dl> <span data-ttu-id="7fcfb-134"><dt>**Защита доступа к сети \_ E \_ не \_ инициализирована**</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-134"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="7fcfb-135">Перед инициализацией не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-135">The enforcer has not been previously initialized.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7fcfb-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fcfb-136">Remarks</span></span>

<span data-ttu-id="7fcfb-137">Напажент запрашивает большой двоичный объект данных SoH-Response из объекта Connection, обрабатывает его и задает полученное решение (например,</span><span class="sxs-lookup"><span data-stu-id="7fcfb-137">The NapAgent queries the SoH-Response data blob from the connection object, processes it, and sets the resulting decision (eg.</span></span> <span data-ttu-id="7fcfb-138">полный/ограниченный доступ и т. д.) для объекта соединения.</span><span class="sxs-lookup"><span data-stu-id="7fcfb-138">full/restricted access/etc) on the connection object.</span></span>

<span data-ttu-id="7fcfb-139">Клиент принудительного применения должен вызвать метод [**инапенфорцементклиентбиндинг:: Initialize**](inapenforcementclientbinding-initialize-method.md) перед вызовом этого или любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="7fcfb-139">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcfb-140">Требования</span><span class="sxs-lookup"><span data-stu-id="7fcfb-140">Requirements</span></span>



| <span data-ttu-id="7fcfb-141">Требование</span><span class="sxs-lookup"><span data-stu-id="7fcfb-141">Requirement</span></span> | <span data-ttu-id="7fcfb-142">Значение</span><span class="sxs-lookup"><span data-stu-id="7fcfb-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcfb-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fcfb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcfb-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fcfb-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7fcfb-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fcfb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcfb-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7fcfb-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7fcfb-147">Header</span><span class="sxs-lookup"><span data-stu-id="7fcfb-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fcfb-148"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-148"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7fcfb-149">IDL</span><span class="sxs-lookup"><span data-stu-id="7fcfb-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7fcfb-150"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-150"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="7fcfb-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7fcfb-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fcfb-152"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-152"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7fcfb-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fcfb-153">See also</span></span>

<dl> <span data-ttu-id="7fcfb-154"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="7fcfb-154"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="7fcfb-155">**инапенфорцементклиентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="7fcfb-155">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="7fcfb-156">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="7fcfb-156">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





