---
description: Сообщение TAPI LINE \_ аппневкалл отправляется для информирования приложения о неограниченном создании нового маркера вызова от его имени.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: Сообщение LINE_APPNEWCALL (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679591"
---
# <a name="line_appnewcall-message"></a><span data-ttu-id="8f0de-103">Строка \_ сообщения аппневкалл</span><span class="sxs-lookup"><span data-stu-id="8f0de-103">LINE\_APPNEWCALL message</span></span>

<span data-ttu-id="8f0de-104">Сообщение TAPI **Line \_ аппневкалл** отправляется для информирования приложения о недостаточном создании нового обработчика вызова от его имени (за исключением вызова API из приложения. в этом случае этот маркер был бы возвращен через параметр указателя, переданный в функцию).</span><span class="sxs-lookup"><span data-stu-id="8f0de-104">The TAPI **LINE\_APPNEWCALL** message is sent to inform an application when a new call handle has been spontaneously created on its behalf (other than through an API call from the application, in which case the handle would have been returned through a pointer parameter passed into the function).</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="8f0de-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f0de-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f0de-106">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="8f0de-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8f0de-107">Маркер приложения для линейного устройства, на котором был создан вызов.</span><span class="sxs-lookup"><span data-stu-id="8f0de-107">The application's handle to the line device on which the call has been created.</span></span>

</dd> <dt>

<span data-ttu-id="8f0de-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="8f0de-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8f0de-109">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="8f0de-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="8f0de-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8f0de-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8f0de-111">Идентификатор адреса в строке, в которой отображается вызов.</span><span class="sxs-lookup"><span data-stu-id="8f0de-111">Identifier of the address on the line on which the call appears.</span></span> <span data-ttu-id="8f0de-112">Идентификатор адреса постоянно связан с адресом; Идентификатор остается постоянным при обновлении операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8f0de-112">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="8f0de-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8f0de-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8f0de-114">Маркер приложения для нового вызова.</span><span class="sxs-lookup"><span data-stu-id="8f0de-114">The application's handle to the new call.</span></span>

</dd> <dt>

<span data-ttu-id="8f0de-115">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8f0de-115">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8f0de-116">Привилегии приложений для нового вызова (ЛИНЕКАЛЛПРИВИЛЕЖЕ \_ owner или линекаллпривилеже \_ Monitor).</span><span class="sxs-lookup"><span data-stu-id="8f0de-116">The applications privilege to the new call (LINECALLPRIVILEGE\_OWNER or LINECALLPRIVILEGE\_MONITOR).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f0de-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f0de-117">Return value</span></span>

<span data-ttu-id="8f0de-118">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8f0de-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f0de-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f0de-119">Remarks</span></span>

<span data-ttu-id="8f0de-120">Приложения, поддерживающие TAPI версии 2,0 или более поздней, отправляют сообщение **Line \_ аппневкалл** всякий раз, когда приложению неограниченно задается маркер нового вызова.</span><span class="sxs-lookup"><span data-stu-id="8f0de-120">Applications supporting TAPI version 2.0 or later are sent a **LINE\_APPNEWCALL** message whenever the application is spontaneously given a handle to a new call.</span></span> <span data-ttu-id="8f0de-121">Так как сообщение содержит параметры *хлине* и *дваддрессид* , для которых существует вызов, приложение может легко создать новый объект Call в правильном контексте.</span><span class="sxs-lookup"><span data-stu-id="8f0de-121">Because the message includes the *hLine* and *dwAddressID* parameters on which the call exists, the application can readily create a new call object in the correct context.</span></span> <span data-ttu-id="8f0de-122">Сразу за сообщением **Line \_ аппневкалл** всегда следует [**строка \_ каллстате**](line-callstate.md) , указывающая начальное состояние вызова.</span><span class="sxs-lookup"><span data-stu-id="8f0de-122">The **LINE\_APPNEWCALL** message is always immediately followed by a [**LINE\_CALLSTATE**](line-callstate.md) message indicating the initial state of the call.</span></span>

<span data-ttu-id="8f0de-123">Более старые приложения (которые согласовывают версию API, предшествующую 2,0), отправляют только [**строку \_ каллстате**](line-callstate.md) , как описано в предыдущих версиях API.</span><span class="sxs-lookup"><span data-stu-id="8f0de-123">Older applications (that negotiated an API version earlier than 2.0) are sent only a [**LINE\_CALLSTATE**](line-callstate.md) message, as documented in previous versions of the API.</span></span> <span data-ttu-id="8f0de-124">Такие приложения создают новый объект Call при получении [**строки \_ каллстате**](line-callstate.md) сообщения, у которого *dwParam3* задано ненулевое значение и содержащего маркер вызова, который в настоящее время не известен приложением.</span><span class="sxs-lookup"><span data-stu-id="8f0de-124">Such applications would create a new call object upon receiving a [**LINE\_CALLSTATE**](line-callstate.md) message that has *dwParam3* set to a nonzero value and containing a call handle not presently known by the application.</span></span> <span data-ttu-id="8f0de-125">Недостатки — это то, что приложение должно вызывать [**линежеткаллинфо**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) для определения параметров *хлине* и *дваддрессид* , связанных с вызовом. (б) приложение должно проверять все известные дескрипторы вызовов, чтобы определить, что вызов является новым вызовом; и (c) это возможно, при определенных условиях, чтобы приложение было считать, что оно получает новый маркер вызова, когда в реальности он просто освобождает свой обработчик вызова (например, приложение просто освобождает обработчик вызова, но [**строка \_ каллстате**](line-callstate.md) сообщения, вызывающая владение приложением для вызова из-за [**линехандофф**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) из другого приложения, уже находится в очереди сообщений TAPI приложения).</span><span class="sxs-lookup"><span data-stu-id="8f0de-125">The disadvantages are that (a) the application must call [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the *hLine* and *dwAddressID* parameters associated with the call; (b) the application must scan all known call handles to determine that the call is a new call; and (c) it is possible, under certain conditions, for the application to think it is receiving a new call handle when in reality it has just deallocated its handle to the call (for example, the application has just deallocated a call handle, but a [**LINE\_CALLSTATE**](line-callstate.md) message giving the application ownership of the call due to a [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) from another application was already in the application's TAPI message queue).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f0de-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8f0de-126">Requirements</span></span>



| <span data-ttu-id="8f0de-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8f0de-127">Requirement</span></span> | <span data-ttu-id="8f0de-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8f0de-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8f0de-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8f0de-129">TAPI version</span></span><br/> | <span data-ttu-id="8f0de-130">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8f0de-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8f0de-131">Header</span><span class="sxs-lookup"><span data-stu-id="8f0de-131">Header</span></span><br/>       | <dl> <span data-ttu-id="8f0de-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f0de-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f0de-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f0de-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f0de-134">**Строка \_ каллстате**</span><span class="sxs-lookup"><span data-stu-id="8f0de-134">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="8f0de-135">**линежеткаллинфо**</span><span class="sxs-lookup"><span data-stu-id="8f0de-135">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="8f0de-136">**линехандофф**</span><span class="sxs-lookup"><span data-stu-id="8f0de-136">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




