---
title: Функция обратного вызова Пксепровидеррекврекуест
description: Вызывается при получении запроса от клиента.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Функция обратного вызова Пксепровидеррекврекуест службы развертывания Windows
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415540"
---
# <a name="pxeproviderrecvrequest-callback-function"></a><span data-ttu-id="84c58-104">Функция обратного вызова Пксепровидеррекврекуест</span><span class="sxs-lookup"><span data-stu-id="84c58-104">PxeProviderRecvRequest callback function</span></span>

<span data-ttu-id="84c58-105">Вызывается при получении запроса от клиента.</span><span class="sxs-lookup"><span data-stu-id="84c58-105">Called when a request is received from a client.</span></span> <span data-ttu-id="84c58-106">Эта функция регистрируется путем вызова функции [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) с параметром *каллбакктипе* , для которого задано значение **\_ \_ \_ запроса recv обратного вызова PXE**.</span><span class="sxs-lookup"><span data-stu-id="84c58-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_RECV\_REQUEST**.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c58-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84c58-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a><span data-ttu-id="84c58-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="84c58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c58-109">*хклиентрекуест* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84c58-109">*hClientRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c58-110">Маркер запроса, полученного от клиента.</span><span class="sxs-lookup"><span data-stu-id="84c58-110">Handle to a request received from a client.</span></span>

</dd> <dt>

<span data-ttu-id="84c58-111">*ппаккет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84c58-111">*pPacket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c58-112">Указатель на буфер памяти, содержащий полученный пакет.</span><span class="sxs-lookup"><span data-stu-id="84c58-112">Pointer to the memory buffer that contains the received packet.</span></span>

</dd> <dt>

<span data-ttu-id="84c58-113">*упаккетлен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84c58-113">*uPacketLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c58-114">Длина (в байтах) буфера, на который указывает параметр *ппаккет* .</span><span class="sxs-lookup"><span data-stu-id="84c58-114">Length, in bytes, of the buffer pointed to by the *pPacket* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="84c58-115">*плокаладдресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84c58-115">*pLocalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c58-116">Указатель на структуру [**\_ адресов PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) , содержащую локальный адрес, на который получен пакет.</span><span class="sxs-lookup"><span data-stu-id="84c58-116">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the local address on which the packet was received.</span></span>

</dd> <dt>

<span data-ttu-id="84c58-117">*премотеаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84c58-117">*pRemoteAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c58-118">Указатель на структуру [**\_ адресов PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) , содержащую исходный адрес пакета.</span><span class="sxs-lookup"><span data-stu-id="84c58-118">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the source address of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="84c58-119">*пактион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="84c58-119">*pAction* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84c58-120">Указывает действие, которое должна предпринять система.</span><span class="sxs-lookup"><span data-stu-id="84c58-120">Specifies the action that the system should take.</span></span>



| <span data-ttu-id="84c58-121">Значение</span><span class="sxs-lookup"><span data-stu-id="84c58-121">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="84c58-122">Значение</span><span class="sxs-lookup"><span data-stu-id="84c58-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <span data-ttu-id="84c58-123"><dt>**PXE \_ BA \_ NBP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="84c58-123"><dt>**PXE\_BA\_NBP**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="84c58-124">Поставщик ответил клиенту с помощью стандартного пакета ответа DHCP, который содержит путь к программе сетевой загрузки.</span><span class="sxs-lookup"><span data-stu-id="84c58-124">The provider replied to a client with a standard DHCP response packet that contains a path to the Network Boot Program.</span></span> <span data-ttu-id="84c58-125">Возврат этого действия означает, что поставщик успешно завершил запрос клиента, вызвав функцию [**пксесендрепли**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) по крайней мере один раз.</span><span class="sxs-lookup"><span data-stu-id="84c58-125">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <span data-ttu-id="84c58-126"><dt>**PXE \_ BA \_ пользовательское**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="84c58-126"><dt>**PXE\_BA\_CUSTOM**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="84c58-127">Поставщик ответил клиенту с помощью пользовательского ответа, который не соответствует спецификациям DHCP.</span><span class="sxs-lookup"><span data-stu-id="84c58-127">The provider replied to a client by using a custom response that does not conform to DHCP specifications.</span></span> <span data-ttu-id="84c58-128">Возврат этого действия означает, что поставщик успешно завершил запрос клиента, вызвав функцию [**пксесендрепли**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) по крайней мере один раз.</span><span class="sxs-lookup"><span data-stu-id="84c58-128">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <span data-ttu-id="84c58-129"><dt>**PXE \_ Не \_ учитывать**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="84c58-129"><dt>**PXE\_BA\_IGNORE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="84c58-130">Поставщик не хочет обслуживать клиентский запрос, и запрос не должен передаваться следующему поставщику.</span><span class="sxs-lookup"><span data-stu-id="84c58-130">The provider does not want to service the client request and the request should not be passed to the next provider.</span></span> <span data-ttu-id="84c58-131">Освобождаются все ресурсы, связанные с запросом клиента, и запрос клиента игнорируется.</span><span class="sxs-lookup"><span data-stu-id="84c58-131">All resources associated with the client request are released and the client request is ignored.</span></span> <span data-ttu-id="84c58-132">Поставщики также могут использовать это значение, если они распознают клиент, но запрос был сформирован неправильно.</span><span class="sxs-lookup"><span data-stu-id="84c58-132">Providers can also use this value if they recognize the client but the request was malformed.</span></span><br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <span data-ttu-id="84c58-133"><dt>**PXE \_ BA \_ отклоненное**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="84c58-133"><dt>**PXE\_BA\_REJECTED**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="84c58-134">Поставщик не хочет обслуживать клиентский запрос.</span><span class="sxs-lookup"><span data-stu-id="84c58-134">The provider does not want to service the client request.</span></span> <span data-ttu-id="84c58-135">Система передает запрос следующему поставщику в списке зарегистрированных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="84c58-135">The system passes the request to the next provider in the list of registered providers.</span></span> <span data-ttu-id="84c58-136">Если это последний поставщик в списке, то освобождаются все ресурсы, связанные с запросом клиента, и клиентский запрос игнорируется.</span><span class="sxs-lookup"><span data-stu-id="84c58-136">If this was the last provider in the list, then all resources associated with the client request are released and client request is ignored.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="84c58-137">*пконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84c58-137">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c58-138">Значение контекста, передаваемое функции [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="84c58-138">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c58-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84c58-139">Return value</span></span>

<span data-ttu-id="84c58-140">Если поставщик успешно обработал запрос клиента, обратный вызов должен вернуть **ошибку, \_** а **\_ \_ действие загрузки PXE** , на которое указывает параметр *пактион* , содержит соответствующее действие загрузки для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="84c58-140">If the provider successfully processed the client request, the callback should return **ERROR\_SUCCESS** and the **PXE\_BOOT\_ACTION** pointed to by the *pAction* parameter contains the appropriate boot action for this request.</span></span> <span data-ttu-id="84c58-141">Если поставщик будет обрабатывать клиентский запрос асинхронно, обратный вызов должен возвращать **ошибку \_ ввода-вывода \_ в ожидании** и вызывать функцию [**пксеасинкреквдоне**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) при обработке запроса клиента.</span><span class="sxs-lookup"><span data-stu-id="84c58-141">If the provider will process the client request asynchronously, the callback should return **ERROR\_IO\_PENDING** and call the [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) function when the client request has been processed.</span></span> <span data-ttu-id="84c58-142">В случае сбоя должен возвращаться соответствующий код ошибки, и система продолжит работу, как если бы было указано действие **PXE \_ BA « \_ отклонено** загрузка».</span><span class="sxs-lookup"><span data-stu-id="84c58-142">In case of failure, an appropriate error code should be returned and the system will proceed as if the **PXE\_BA\_REJECTED** boot action was specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="84c58-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84c58-143">Remarks</span></span>

<span data-ttu-id="84c58-144">Тип пакетов, отображаемых поставщиком, можно изменить с помощью функции [**пксепровидерсетаттрибуте**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) .</span><span class="sxs-lookup"><span data-stu-id="84c58-144">The type of packets seen by a provider can be changed with the [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c58-145">Требования</span><span class="sxs-lookup"><span data-stu-id="84c58-145">Requirements</span></span>



| <span data-ttu-id="84c58-146">Требование</span><span class="sxs-lookup"><span data-stu-id="84c58-146">Requirement</span></span> | <span data-ttu-id="84c58-147">Значение</span><span class="sxs-lookup"><span data-stu-id="84c58-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84c58-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84c58-148">Minimum supported client</span></span><br/> | <span data-ttu-id="84c58-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="84c58-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="84c58-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84c58-150">Minimum supported server</span></span><br/> | <span data-ttu-id="84c58-151">Windows Server 2008, Windows Server 2003 с пакетом обновления 2 (SP2), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="84c58-151">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84c58-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84c58-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c58-153">Функции сервера служб развертывания Windows</span><span class="sxs-lookup"><span data-stu-id="84c58-153">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="84c58-154">**пксерегистеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="84c58-154">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[<span data-ttu-id="84c58-155">**пксесендрепли**</span><span class="sxs-lookup"><span data-stu-id="84c58-155">**PxeSendReply**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[<span data-ttu-id="84c58-156">**пксепровидерсетаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="84c58-156">**PxeProviderSetAttribute**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





