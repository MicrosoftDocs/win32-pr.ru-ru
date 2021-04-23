---
description: Сообщение ТСПИ LINE \_ невкалл отправляется в функцию обратного вызова линивент всякий раз, когда новый вызов, полученный от TAPI, поступает в строку, открытую TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: Сообщение LINE_NEWCALL (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688809"
---
# <a name="line_newcall-message"></a><span data-ttu-id="21b86-103">Строка \_ сообщения невкалл</span><span class="sxs-lookup"><span data-stu-id="21b86-103">LINE\_NEWCALL message</span></span>

<span data-ttu-id="21b86-104">Сообщение ТСПИ **Line \_ невкалл** отправляется в функцию обратного вызова [**линивент**](/windows/win32/api/tspi/nc-tspi-lineevent) всякий раз, когда новый вызов, полученный от TAPI, поступает в строку, открытую TAPI.</span><span class="sxs-lookup"><span data-stu-id="21b86-104">The TSPI **LINE\_NEWCALL** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function whenever a new call that TAPI has not originated arrives on a line that TAPI has open.</span></span> <span data-ttu-id="21b86-105">Это должно быть первое сообщение, отправленное в отношении этого вызова.</span><span class="sxs-lookup"><span data-stu-id="21b86-105">This must be the first message sent regarding that call.</span></span> <span data-ttu-id="21b86-106">TAPI записывает непрозрачный маркер *хткалл* в расположение, передаваемое поставщиком услуг как *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="21b86-106">TAPI writes the *htCall* opaque handle to the location passed by the service provider as *dwParam2*.</span></span> <span data-ttu-id="21b86-107">Это дает поставщику услуг значение *хткалл* , которое будет использоваться в последующих сообщениях.</span><span class="sxs-lookup"><span data-stu-id="21b86-107">This gives the service provider the *htCall* value to be used in subsequent messages.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="21b86-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="21b86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21b86-109">*хтлине*</span><span class="sxs-lookup"><span data-stu-id="21b86-109">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="21b86-110">Обработчик непрозрачного объекта TAPI для устройства линии.</span><span class="sxs-lookup"><span data-stu-id="21b86-110">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="21b86-111">*хткалл*</span><span class="sxs-lookup"><span data-stu-id="21b86-111">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="21b86-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="21b86-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="21b86-113">*двмсг*</span><span class="sxs-lookup"><span data-stu-id="21b86-113">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="21b86-114">Строка значения \_ невкалл.</span><span class="sxs-lookup"><span data-stu-id="21b86-114">The value LINE\_NEWCALL.</span></span>

</dd> <dt>

<span data-ttu-id="21b86-115">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="21b86-115">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="21b86-116">Непрозрачный маркер поставщика услуг для вызова типа [**хдрвкалл**](hdrvline.md).</span><span class="sxs-lookup"><span data-stu-id="21b86-116">The service provider's opaque handle for the call, of type [**HDRVCALL**](hdrvline.md).</span></span> <span data-ttu-id="21b86-117">TAPI передает это значение как параметр *хдкалл* для обнаружения вызова в последующих процедурах, которые он вызывает для обработки вызова.</span><span class="sxs-lookup"><span data-stu-id="21b86-117">TAPI passes this value as the *hdCall* parameter to identify the call in subsequent procedures it invokes to operate on the call.</span></span>

</dd> <dt>

<span data-ttu-id="21b86-118">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="21b86-118">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="21b86-119">Указатель типа ЛФТАПИКАЛЛ, указывающий на [**хтапикалл**](htapicall.md).</span><span class="sxs-lookup"><span data-stu-id="21b86-119">A pointer of type LPHTAPICALL pointing to a [**HTAPICALL**](htapicall.md).</span></span> <span data-ttu-id="21b86-120">TAPI записывает непрозрачный маркер TAPI для вызова в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="21b86-120">TAPI writes the TAPI opaque handle for the call to the indicated location.</span></span> <span data-ttu-id="21b86-121">Поставщик услуг должен сохранить это значение и передать его в качестве параметра *хткалл* для обнаружения вызова в последующих событиях, которые он сообщает о вызове.</span><span class="sxs-lookup"><span data-stu-id="21b86-121">The service provider must save this value and pass it as the *htCall* parameter to identify the call in subsequent events it reports for the call.</span></span>

<span data-ttu-id="21b86-122">Этот параметр также может получить значение **null** (см. следующий раздел "Примечания").</span><span class="sxs-lookup"><span data-stu-id="21b86-122">This parameter can also acquire a value of **NULL** (see the following Remarks section).</span></span>

</dd> <dt>

<span data-ttu-id="21b86-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="21b86-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="21b86-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="21b86-124">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21b86-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21b86-125">Remarks</span></span>

<span data-ttu-id="21b86-126">Поставщик услуг должен отправить [**строку \_ каллстате**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) сообщение в качестве следующего сообщения для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="21b86-126">The service provider should send the [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) message as the next message for this call.</span></span> <span data-ttu-id="21b86-127">Событие **Line \_ невкалл** нередко в том, что оно также передает значение обратно поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="21b86-127">The **LINE\_NEWCALL** event is unusual in that it also passes a value back to the service provider.</span></span>

<span data-ttu-id="21b86-128">Эта функция сообщает о новых вызовах, которые происходят у поставщика услуг (входящий, исходящий, инициированный на телефоне и т. д.), для которого TAPI и поставщик службы еще не обмениваются непрозрачными дескрипторами.</span><span class="sxs-lookup"><span data-stu-id="21b86-128">This function reports any new calls that originate in the service provider (inbound, outbound, initiated at the phone, and so on) for which TAPI and the service provider have not yet exchanged opaque handles.</span></span> <span data-ttu-id="21b86-129">Эти дескрипторы обмениваются, чтобы TAPI и поставщик служб могли затем выполнять запросы и сообщать о событиях, связанных с вызовом.</span><span class="sxs-lookup"><span data-stu-id="21b86-129">The handles are exchanged so that TAPI and the service provider can subsequently make requests and report events involving the call.</span></span> <span data-ttu-id="21b86-130">Поскольку эти новые вызовы не обязательно являются входящими, вызовы могут изначально находиться в любом состоянии, а не в состоянии *предложения* .</span><span class="sxs-lookup"><span data-stu-id="21b86-130">Because these new calls are not necessarily inbound, the calls can initially be in any state, not necessarily the *offering* state.</span></span> <span data-ttu-id="21b86-131">Если поставщик услуг запускает и обнаруживает, что один или несколько вызовов уже активны в строке, он информирует TAPI о них с сообщениями **Line \_ невкалл** , за которыми следуют сообщения [**Line \_ каллстате**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) , указывающие текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="21b86-131">If the service provider starts and discovers that one or more calls are already active on the line, it informs TAPI of them with **LINE\_NEWCALL** messages followed by [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages indicating the current state.</span></span> <span data-ttu-id="21b86-132">Новый исходящий вызов, инициированный пользователем по телефону, выводится в виде **строки \_ невкалл** сообщение, а в сообщении **\_ каллстате** первоначальной строки указывается, что вызов находился в **диалтоне** состоянии (и затем продолжает работу с него).</span><span class="sxs-lookup"><span data-stu-id="21b86-132">A new outgoing call, initiated on the phone by the user, would be reported with a **LINE\_NEWCALL** message, and the initial **LINE\_CALLSTATE** message would indicate that the call was in **DIALTONE** state (and then continuing on from there).</span></span>

<span data-ttu-id="21b86-133">Если поставщик услуг передает большое количество вызовов в TAPI в очень короткий промежуток времени (во время того же цикла прерывания), TAPI может войти в систему при обработке этих вызовов.</span><span class="sxs-lookup"><span data-stu-id="21b86-133">If the service provider passes a large number of calls to TAPI in a very short amount of time (during the same interrupt cycle), TAPI can become backlogged in processing those calls.</span></span> <span data-ttu-id="21b86-134">В этом случае TAPI передает поставщику услуг на короткое время, прежде чем отправлять вызовы.</span><span class="sxs-lookup"><span data-stu-id="21b86-134">When this happens, TAPI signals to the service provider to wait a short time before sending any more calls.</span></span> <span data-ttu-id="21b86-135">Он сигнализирует об этом, записывая значение **null** вместо допустимого [**хтапикалл**](htapicall.md)в расположение, на которое указывает параметр *dwParam2* **строки \_ невкалл**.</span><span class="sxs-lookup"><span data-stu-id="21b86-135">It signals this by writing a value of **NULL**, instead of a valid [**HTAPICALL**](htapicall.md), into the location pointed to by the *dwParam2* parameter of **LINE\_NEWCALL**.</span></span> <span data-ttu-id="21b86-136">Это означает, что попытка обработать вновь предлагаемый маркер вызова завершилась неудачно, скорее всего из-за временной невозможности выделить память.</span><span class="sxs-lookup"><span data-stu-id="21b86-136">This indicates that the attempt to process the newly offered call handle was not successful, most likely due to a temporary inability to allocate memory.</span></span> <span data-ttu-id="21b86-137">Поставщик услуг может ответить, удалив вызов или повторно **\_ отневкалл сообщение Line** после задержки планирования (в течение которого поставщик услуг должен дать процессору разрешение TAPI на обработку других ожидающих действий).</span><span class="sxs-lookup"><span data-stu-id="21b86-137">The service provider can respond by dropping the call or by resending the **LINE\_NEWCALL** message after a scheduling delay (during which time the service provider should yield the processor to allow TAPI to process other pending actions).</span></span> <span data-ttu-id="21b86-138">В любом случае дальнейшие сообщения о новом вызове могут быть переданы в TAPI до тех пор, пока работа Exchange не завершится успешно.</span><span class="sxs-lookup"><span data-stu-id="21b86-138">In any case, no further messages regarding the new call can be passed to TAPI until the handle exchange succeeds.</span></span> <span data-ttu-id="21b86-139">Когда расположение, на которое указывает *dwParam2* , получает значение, отличное от **null** , поставщик службы знает, что это значение является допустимым обработчиком [**хтапикалл**](htapicall.md) для вызова.</span><span class="sxs-lookup"><span data-stu-id="21b86-139">When the location pointed to by *dwParam2* acquires a non-**NULL** value, the service provider knows that this value is a valid [**HTAPICALL**](htapicall.md) handle to the call.</span></span>

<span data-ttu-id="21b86-140">Непосредственно соответствующего сообщения на уровне TAPI нет.</span><span class="sxs-lookup"><span data-stu-id="21b86-140">There is no directly corresponding message at the TAPI level.</span></span> <span data-ttu-id="21b86-141">Это сообщение используется на уровне ТСПИ для уникальной и однозначной идентификации нового входящего вызова к TAPI и получения непрозрачного идентификатора TAPI для вызова.</span><span class="sxs-lookup"><span data-stu-id="21b86-141">This message is used at the TSPI level to uniquely and unambiguously introduce a new incoming call to TAPI and retrieve the TAPI opaque identifier for the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="21b86-142">Требования</span><span class="sxs-lookup"><span data-stu-id="21b86-142">Requirements</span></span>



| <span data-ttu-id="21b86-143">Требование</span><span class="sxs-lookup"><span data-stu-id="21b86-143">Requirement</span></span> | <span data-ttu-id="21b86-144">Значение</span><span class="sxs-lookup"><span data-stu-id="21b86-144">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="21b86-145">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="21b86-145">TAPI version</span></span><br/> | <span data-ttu-id="21b86-146">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="21b86-146">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="21b86-147">Header</span><span class="sxs-lookup"><span data-stu-id="21b86-147">Header</span></span><br/>       | <dl> <span data-ttu-id="21b86-148"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="21b86-148"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21b86-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21b86-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="21b86-150">[**Строка \_ каллстате**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21b86-150">[**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="21b86-151">**линивент**</span><span class="sxs-lookup"><span data-stu-id="21b86-151">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

