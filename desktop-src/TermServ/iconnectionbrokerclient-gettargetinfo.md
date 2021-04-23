---
title: Метод Иконнектионброкерклиент Жеттаржетинфо (Кбклиент. h)
description: Запрашивает сведения о конечном компьютере, на котором должно быть перенаправлено подключение.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жеттаржетинфо
- Службы удаленных рабочих столов метода Жеттаржетинфо, интерфейс Иконнектионброкерклиент
- Службы удаленных рабочих столов интерфейса Иконнектионброкерклиент, метод Жеттаржетинфо
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533755"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a><span data-ttu-id="d618c-106">Метод Иконнектионброкерклиент:: Жеттаржетинфо</span><span class="sxs-lookup"><span data-stu-id="d618c-106">IConnectionBrokerClient::GetTargetInfo method</span></span>

<span data-ttu-id="d618c-107">Запрашивает сведения о конечном компьютере, на котором должно быть перенаправлено подключение.</span><span class="sxs-lookup"><span data-stu-id="d618c-107">Requests information about the target computer where the connection should be redirected.</span></span> <span data-ttu-id="d618c-108">Этот метод используется перенаправитель для получения сведений о перенаправлении для входящего запроса на подключение.</span><span class="sxs-lookup"><span data-stu-id="d618c-108">This method is used by the redirector to get redirection information for the incoming connection request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d618c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d618c-109">Syntax</span></span>


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a><span data-ttu-id="d618c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d618c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d618c-111">*пконнектионинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d618c-111">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d618c-112">Адрес структуры сведений о [**\_ соединении \_ CB**](cb-connection-info.md) , которая содержит сведения о входящем запросе на подключение.</span><span class="sxs-lookup"><span data-stu-id="d618c-112">The address of a [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure that contains information about the incoming connection request.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-113">*Зарезервировано* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d618c-113">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d618c-114">Этот параметр зарезервирован для будущего использования и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="d618c-114">This parameter is reserved for future use and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-115">*хстатусевент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d618c-115">*hStatusEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d618c-116">Маркер события, который задается при обновлении хода выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="d618c-116">The handle of an event that will get set whenever there is an update to the progress of the request.</span></span> <span data-ttu-id="d618c-117">Вы несете ответственность за создание и закрытие этого события.</span><span class="sxs-lookup"><span data-stu-id="d618c-117">You are responsible for creating and closing this event.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-118">*птаржетинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d618c-118">*pTargetInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d618c-119">Адрес целевой структуры CB, который получает сведения о конечном компьютере, на котором должно быть перенаправлено входящее подключение. [**\_ \_**](cb-target-info.md)</span><span class="sxs-lookup"><span data-stu-id="d618c-119">The address of a [**CB\_TARGET\_INFO**](cb-target-info.md) structure that receives information about the target computer where the incoming connection should be redirected.</span></span> <span data-ttu-id="d618c-120">Так как это асинхронный метод, эта память должна оставаться доступной до завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="d618c-120">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="d618c-121">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="d618c-121">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-122">*пресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d618c-122">*pResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d618c-123">Адрес переменной **типа DWORD** , которая получает код результата.</span><span class="sxs-lookup"><span data-stu-id="d618c-123">The address of a **DWORD** variable that receives a result code.</span></span> <span data-ttu-id="d618c-124">Так как это асинхронный метод, эта память должна оставаться доступной до завершения запроса.</span><span class="sxs-lookup"><span data-stu-id="d618c-124">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="d618c-125">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="d618c-125">For more information, see Remarks.</span></span>

<span data-ttu-id="d618c-126">Этот код результата будет иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d618c-126">This result code will be one of the following values.</span></span>

<dt>

<span data-ttu-id="d618c-127">0</span><span class="sxs-lookup"><span data-stu-id="d618c-127">0</span></span>
</dt> <dd>

<span data-ttu-id="d618c-128">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d618c-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-129">0x0000400</span><span class="sxs-lookup"><span data-stu-id="d618c-129">0x0000400</span></span>
</dt> <dd>

<span data-ttu-id="d618c-130">Не удалось найти конечный компьютер.</span><span class="sxs-lookup"><span data-stu-id="d618c-130">The destination computer could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-131">0x0000401</span><span class="sxs-lookup"><span data-stu-id="d618c-131">0x0000401</span></span>
</dt> <dd>

<span data-ttu-id="d618c-132">Конечный компьютер недоступен.</span><span class="sxs-lookup"><span data-stu-id="d618c-132">The destination computer is not available.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-133">0x0000402</span><span class="sxs-lookup"><span data-stu-id="d618c-133">0x0000402</span></span>
</dt> <dd>

<span data-ttu-id="d618c-134">Ошибка при загрузке конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="d618c-134">Error loading destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-135">0x0000403</span><span class="sxs-lookup"><span data-stu-id="d618c-135">0x0000403</span></span>
</dt> <dd>

<span data-ttu-id="d618c-136">Ошибка при подключении конечного компьютера к сети.</span><span class="sxs-lookup"><span data-stu-id="d618c-136">Error bringing destination computer online.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-137">0x0000404</span><span class="sxs-lookup"><span data-stu-id="d618c-137">0x0000404</span></span>
</dt> <dd>

<span data-ttu-id="d618c-138">Ошибка при перенаправлении на конечный компьютер.</span><span class="sxs-lookup"><span data-stu-id="d618c-138">Error redirecting to destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-139">0x0000405</span><span class="sxs-lookup"><span data-stu-id="d618c-139">0x0000405</span></span>
</dt> <dd>

<span data-ttu-id="d618c-140">Ошибка при пробуждении виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d618c-140">Error waking virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-141">0x0000406</span><span class="sxs-lookup"><span data-stu-id="d618c-141">0x0000406</span></span>
</dt> <dd>

<span data-ttu-id="d618c-142">Ошибка при загрузке виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d618c-142">Error booting virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-143">0x0000407</span><span class="sxs-lookup"><span data-stu-id="d618c-143">0x0000407</span></span>
</dt> <dd>

<span data-ttu-id="d618c-144">Ошибка при поиске IP-адреса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d618c-144">Error finding the IP address of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-145">0x0000408</span><span class="sxs-lookup"><span data-stu-id="d618c-145">0x0000408</span></span>
</dt> <dd>

<span data-ttu-id="d618c-146">Посреднику сеансов не удалось найти доступные компьютеры в пуле.</span><span class="sxs-lookup"><span data-stu-id="d618c-146">The session broker could not find any available computers in the pool.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-147">0x0000409</span><span class="sxs-lookup"><span data-stu-id="d618c-147">0x0000409</span></span>
</dt> <dd>

<span data-ttu-id="d618c-148">Посредник сеансов отменил подключение.</span><span class="sxs-lookup"><span data-stu-id="d618c-148">The session broker canceled the connection.</span></span>

</dd> <dt>

<span data-ttu-id="d618c-149">0x0000410</span><span class="sxs-lookup"><span data-stu-id="d618c-149">0x0000410</span></span>
</dt> <dd>

<span data-ttu-id="d618c-150">Посреднику сеансов не удалось проверить параметры подключения.</span><span class="sxs-lookup"><span data-stu-id="d618c-150">The session broker could not validate the connection settings.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d618c-151">*ппкбрек* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d618c-151">*ppCbReq* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d618c-152">Адрес указателя интерфейса [**иконнектионброкеррекуест**](iconnectionbrokerrequest.md) , который используется для получения обновлений состояния для асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="d618c-152">The address of an [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) interface pointer that you use to obtain status updates for an asynchronous operation.</span></span> <span data-ttu-id="d618c-153">Этот интерфейс используется в сочетании с параметром *хстатусевент* для ожидания и получения результатов этой асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="d618c-153">This interface is used in conjunction with the *hStatusEvent* parameter to wait for and get the results of this asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d618c-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d618c-154">Return value</span></span>

<span data-ttu-id="d618c-155">Возвращает значение " **E \_ Pending** ", если создается асинхронный запрос.</span><span class="sxs-lookup"><span data-stu-id="d618c-155">Returns **E\_PENDING** if the asynchronous request is created.</span></span> <span data-ttu-id="d618c-156">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d618c-156">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d618c-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d618c-157">Remarks</span></span>

<span data-ttu-id="d618c-158">Этот метод является асинхронным.</span><span class="sxs-lookup"><span data-stu-id="d618c-158">This method is asynchronous.</span></span> <span data-ttu-id="d618c-159">Параметры *птаржетинфо* и *пресулт* должны оставаться действительными до тех пор, пока метод [**иконнектионброкеррекуест:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) не получит **\_ \_ запрос \_ о состоянии CB**.</span><span class="sxs-lookup"><span data-stu-id="d618c-159">The *pTargetInfo* and *pResult* parameters must remain valid until the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method obtains **CB\_STATUS\_REQUEST\_COMPLETED**.</span></span>

<span data-ttu-id="d618c-160">Дополнительные сведения об использовании этого метода см. в разделе [Использование API клиента компонента Подключение к удаленному рабочему столу Broker](use-the-remote-desktop-connection-broker-client-api.md).</span><span class="sxs-lookup"><span data-stu-id="d618c-160">For more information about how to use this method, see [How to use the Remote Desktop Connection Broker client API](use-the-remote-desktop-connection-broker-client-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d618c-161">Требования</span><span class="sxs-lookup"><span data-stu-id="d618c-161">Requirements</span></span>



| <span data-ttu-id="d618c-162">Требование</span><span class="sxs-lookup"><span data-stu-id="d618c-162">Requirement</span></span> | <span data-ttu-id="d618c-163">Значение</span><span class="sxs-lookup"><span data-stu-id="d618c-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d618c-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d618c-164">Minimum supported client</span></span><br/> | <span data-ttu-id="d618c-165">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d618c-165">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="d618c-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d618c-166">Minimum supported server</span></span><br/> | <span data-ttu-id="d618c-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d618c-167">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="d618c-168">Header</span><span class="sxs-lookup"><span data-stu-id="d618c-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="d618c-169"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="d618c-169"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="d618c-170">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d618c-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="d618c-171"><dt>Кбклиент. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d618c-171"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="d618c-172">DLL</span><span class="sxs-lookup"><span data-stu-id="d618c-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d618c-173"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d618c-173"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d618c-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d618c-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d618c-175">**иконнектионброкерклиент**</span><span class="sxs-lookup"><span data-stu-id="d618c-175">**IConnectionBrokerClient**</span></span>](iconnectionbrokerclient.md)
</dt> </dl>

 

 





