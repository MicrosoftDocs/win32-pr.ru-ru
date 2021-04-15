---
description: Ниже приведен список кодов ошибок, которые может возвращать TAPI при вызове операций в строках, адресах или вызовах.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: Константы LINEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689472"
---
# <a name="lineerr_-constants"></a><span data-ttu-id="b7d9e-103">\_Константы линирр</span><span class="sxs-lookup"><span data-stu-id="b7d9e-103">LINEERR\_ Constants</span></span>

<span data-ttu-id="b7d9e-104">Ниже приведен список кодов ошибок, которые может возвращать TAPI при вызове операций в строках, адресах или вызовах.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-104">The following is a list of error codes that TAPI can return when invoking operations on lines, addresses, or calls.</span></span> <span data-ttu-id="b7d9e-105">Дополнительные сведения о том, как определить, какие из этих кодов ошибок может возвращать конкретная функция, см. в описании отдельных функций.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-105">For more information about how to determine which of these error codes a particular function can return, see the individual function descriptions.</span></span>

<dl> <dt>

<span data-ttu-id="b7d9e-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**ЛИНИРР \_ аддрессблоккед**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-106"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-107">Указанный адрес заблокирован из-за указанного вызова.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-107">The specified address is blocked from being dialed on the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**ЛИНИРР \_ аддрессблоккед**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-108"><span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR\_ADDRESSBLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-109">Для целевого адреса вызова включена блокировка вызовов.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-109">The target call address has call blocking enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**ЛИНИРР \_ выделен**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-110"><span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-111">Строка не может быть открыта из-за устойчивого состояния, например в том, что последовательный порт открыт в монопольном режиме другим процессом.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-111">The line cannot be opened due to a persistent condition, such as that of a serial port being exclusively opened by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**ЛИНИРР \_ баддевицеид**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-112"><span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-113">Указанный идентификатор устройства или строки идентификатора устройства, например в параметре *двдевицеид* , является недопустимым или выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-113">The specified device identifier or line device identifier, such as in a *dwDeviceID* parameter, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**ЛИНИРР \_ беарермодеунаваил**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-114"><span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR\_BEARERMODEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-115">Недопустимый член режима носителя в [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) , режим носителя, указанный в **линекаллпарамс** , недоступен, или режим носителя вызова не может быть изменен на указанный режим носителя.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-115">The bearer mode member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) is invalid, the bearer mode specified in **LINECALLPARAMS** is not available, or the call bearer mode cannot be changed to the specified bearer mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**ЛИНИРР \_ биллингрежектед**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-116"><span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR\_BILLINGREJECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-117">Режим выставления счетов для вызова был отклонен.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-117">The billing mode of the call was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**ЛИНИРР \_ каллунаваил**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-118"><span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR\_CALLUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-119">Все представления вызовов по указанному адресу сейчас используются.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-119">All call appearances on the specified address are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**ЛИНИРР \_ комплетионоверрун**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-120"><span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR\_COMPLETIONOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-121">Превышено максимальное число незавершенных завершений вызова.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-121">The maximum number of outstanding call completions has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**ЛИНИРР \_ конференцефулл**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-122"><span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR\_CONFERENCEFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-123">Достигнуто максимальное число сторон для Конференции, или запрошенное число сторон не может быть удовлетворено.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-123">The maximum number of parties for a conference has been reached, or the requested number of parties cannot be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**ЛИНИРР \_ диалбиллинг**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-124"><span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-125">Параметр адреса с набором номера содержит управляющие символы, не обрабатываемые поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-125">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**ЛИНИРР \_ диалдиалтоне**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-126"><span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-127">Параметр адреса с набором номера содержит управляющие символы, не обрабатываемые поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-127">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**ЛИНИРР \_ диалпромпт**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-128"><span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-129">Параметр адреса с набором номера содержит управляющие символы, не обрабатываемые поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-129">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**ЛИНИРР \_ диалкуиет**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-130"><span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-131">Параметр адреса с набором номера содержит управляющие символы, не обрабатываемые поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-131">The dialable address parameter contains dialing control characters not processed by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**ЛИНИРР \_ диалвоицедетект**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-132"><span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR\_DIALVOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-133">Использование модификатора набора номера (:) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-133">Use of the dial modifier (:) is not supported.</span></span> <span data-ttu-id="b7d9e-134">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-134">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**ЛИНИРР \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-135"><span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-136">Вызов был отключен.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-136">The call has been disconnected.</span></span> <span data-ttu-id="b7d9e-137">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,2 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-137">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**ЛИНИРР \_ инкомпатиблеапиверсион**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-138"><span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-139">Приложение запросило версию или диапазон версий TAPI, которые либо несовместимы с, либо не поддерживаются в, реализацией API телефонии и соответствующим поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-139">The application requested a TAPI version or version range that is either incompatible with, or cannot be supported by, the Telephony API implementation and the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**ЛИНИРР \_ инкомпатибликстверсион**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-140"><span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-141">Приложение запросило диапазон версий расширения, которое либо недопустимо, либо не может поддерживаться соответствующим поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-141">The application requested an extension version range that is either invalid or cannot be supported by the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**ЛИНИРР \_ инифилекоррупт**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-142"><span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-143">TAPI-файл не может быть правильно прочитан или понят из-за внутренних несоответствий или ошибок форматирования. Telephon.ini</span><span class="sxs-lookup"><span data-stu-id="b7d9e-143">The Telephon.ini file cannot be read or understood properly by TAPI because of internal inconsistencies or formatting problems.</span></span> <span data-ttu-id="b7d9e-144">Например, \[ \] раздел расположения, \[ карточки \] или \[ страны \] Telephon.ini файла может быть поврежден или непоследовательен.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-144">For example, the \[Locations\], \[Cards\], or \[Countries\] section of the Telephon.ini file may be corrupted or inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**ЛИНИРР \_ INUSE**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-145"><span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-146">Линейное устройство используется и сейчас не может быть настроено, допускает добавление стороны, позволяет получить ответ на вызов, разрешить помещение вызова или разрешить передачу вызова.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-146">The line device is in use and cannot currently be configured, allow a party to be added, allow a call to be answered, allow a call to be placed, or allow a call to be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**ЛИНИРР \_ инваладдресс**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-147"><span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR\_INVALADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-148">Указанный адрес недопустим или запрещен.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-148">A specified address is either invalid or not allowed.</span></span> <span data-ttu-id="b7d9e-149">Если значение недопустимо, адрес содержит недопустимые символы или цифры, либо адрес назначения содержит управляющие символы набора номера (W, @, $ или?), которые не поддерживаются поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-149">If invalid, the address contains invalid characters or digits, or the destination address contains dialing control characters (W, @, $, or ?) that are not supported by the service provider.</span></span> <span data-ttu-id="b7d9e-150">Если не разрешено, указанный адрес либо не назначается указанной строке, либо недопустим для перенаправления адреса.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-150">If not allowed, the specified address is either not assigned to the specified line or is not valid for address redirection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**ЛИНИРР \_ инваладдрессид**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-151"><span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR\_INVALADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-152">Указанный идентификатор адреса недопустим или выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-152">The specified address identifier is either invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**ЛИНИРР \_ инваладдрессмоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-153"><span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR\_INVALADDRESSMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-154">Указан недопустимый режим адреса.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-154">The specified address mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**ЛИНИРР \_ инваладдрессстате**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-155"><span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR\_INVALADDRESSSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-156">Указанное состояние адреса содержит один или несколько битов, которые не являются [**\_ константами линеаддрессстате**](lineaddressstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b7d9e-156">The specified address state contains one or more bits that are not [**LINEADDRESSSTATE\_ constants**](lineaddressstate--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**ЛИНИРР \_ инваладдресстипе**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-157"><span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR\_INVALADDRESSTYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-158">Приложение ссылается на недопустимый тип адреса.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-158">The application referenced an address type that is not valid.</span></span> <span data-ttu-id="b7d9e-159">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 3,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-159">This value is exposed only to applications that negotiate a TAPI version of 3.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**ЛИНИРР \_ инвалажентактивити**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-160"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-161">Указанное действие агента недопустимо.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-161">The specified agent activity is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**ЛИНИРР \_ инвалажентактивити**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-162"><span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR\_INVALAGENTACTIVITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-163">Приложение, вызывающее эту операцию, является целевым объектом косвенной передачи.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-163">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="b7d9e-164">То есть TAPI определил, что вызывающее приложение также является приложением с наивысшим приоритетом для данного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-164">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span> <span data-ttu-id="b7d9e-165">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-165">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**ЛИНИРР \_ инвалажентграуп**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-166"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-167">Указанные сведения о группе агентов недопустимы или содержат ошибки.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-167">The specified agent group information is not valid or contains errors.</span></span> <span data-ttu-id="b7d9e-168">Запрошенное действие не выполнено.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-168">The requested action has not been performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**ЛИНИРР \_ инвалажентграуп**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-169"><span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR\_INVALAGENTGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-170">Приложение ссылается на недопустимую группу агентов.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-170">The application referenced an agent group that is not valid.</span></span> <span data-ttu-id="b7d9e-171">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-171">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**ЛИНИРР \_ инвалажентид**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-172"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-173">Указан недопустимый идентификатор агента.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-173">The specified agent identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**ЛИНИРР \_ инвалажентид**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-174"><span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR\_INVALAGENTID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-175">Использован недопустимый идентификатор агента.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-175">An invalid agent identifier was used.</span></span> <span data-ttu-id="b7d9e-176">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-176">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**ЛИНИРР \_ инвалажентсессионстате**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-177"><span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR\_INVALAGENTSESSIONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-178">Недопустимое состояние сеанса агента.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-178">The agent session state is invalid.</span></span> <span data-ttu-id="b7d9e-179">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,2 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-179">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**ЛИНИРР \_ инвалажентстате**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-180"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-181">Указанное состояние агента недопустимо или содержит ошибки.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-181">The specified agent state is not valid or contains errors.</span></span> <span data-ttu-id="b7d9e-182">В состояние агента указанного адреса не внесены изменения.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-182">No changes have been made to the agent state of the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**ЛИНИРР \_ инвалажентстате**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-183"><span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR\_INVALAGENTSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-184">Приложение ссылается на недопустимое состояние агента.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-184">The application referenced an agent state that is not valid.</span></span> <span data-ttu-id="b7d9e-185">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-185">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**ЛИНИРР \_ инвалапфандле**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-186"><span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-187">Недопустимый маркер приложения (например, заданный параметром *хлинеапп* ) или регистрационный маркер приложения.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-187">The application handle (such as specified by a *hLineApp* parameter) or the application registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**ЛИНИРР \_ инвалаппнаме**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-188"><span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-189">Указано недопустимое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-189">The specified application name is invalid.</span></span> <span data-ttu-id="b7d9e-190">Если имя приложения задано приложением, предполагается, что строка не содержит какие-либо символы, которые не удается воспроизвести, и завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-190">If an application name is specified by the application, it is assumed that the string does not contain any non-displayable characters, and is zero-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**ЛИНИРР \_ инвалбеарермоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-191"><span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR\_INVALBEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-192">Указан недопустимый режим носителя.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-192">The specified bearer mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**ЛИНИРР \_ инвалкаллкомплмоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-193"><span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR\_INVALCALLCOMPLMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-194">Указано недопустимое завершение.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-194">The specified completion is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**ЛИНИРР \_ инвалкаллхандле**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-195"><span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR\_INVALCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-196">Указан недопустимый маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-196">The specified call handle is not valid.</span></span> <span data-ttu-id="b7d9e-197">Например, маркер не равен **null** , но не принадлежит данной строке.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-197">For example, the handle is not **NULL** but does not belong to the given line.</span></span> <span data-ttu-id="b7d9e-198">В некоторых случаях указанный маркер устройства вызова является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-198">In some cases, the specified call device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**ЛИНИРР \_ инвалкаллпарамс**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-199"><span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR\_INVALCALLPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-200">Указаны недопустимые параметры вызова.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-200">The specified call parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**ЛИНИРР \_ инвалкаллпривилеже**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-201"><span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR\_INVALCALLPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-202">Указанный параметр привилегии вызова недопустим.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-202">The specified call privilege parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**ЛИНИРР \_ инвалкаллселект**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-203"><span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR\_INVALCALLSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-204">Указан недопустимый параметр SELECT.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-204">The specified select parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**ЛИНИРР \_ инвалкаллстате**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-205"><span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR\_INVALCALLSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-206">Текущее состояние вызова находится в недопустимом состоянии для запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-206">The current state of a call is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**ЛИНИРР \_ инвалкаллстателист**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-207"><span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR\_INVALCALLSTATELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-208">Указан недопустимый список состояний вызова.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-208">The specified call state list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**ЛИНИРР \_ инвалкард**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-209"><span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR\_INVALCARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-210">Не удалось найти постоянный идентификатор карты, указанный в *двкард* , в любой записи в \[ разделе "карточки" \] в реестре.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-210">The permanent card identifier specified in *dwCard* could not be found in any entry in the \[Cards\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**ЛИНИРР \_ инвалкомплетионид**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-211"><span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR\_INVALCOMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-212">Недопустимый идентификатор завершения.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-212">The completion identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**ЛИНИРР \_ инвалконфкаллхандле**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-213"><span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR\_INVALCONFCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-214">Указанный маркер вызова для вызова конференции является недопустимым или не является обработчиком для вызова конференции.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-214">The specified call handle for the conference call is invalid or is not a handle for a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**ЛИНИРР \_ инвалконсулткаллхандле**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-215"><span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR\_INVALCONSULTCALLHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-216">Указан недопустимый описатель вызова консультации.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-216">The specified consultation call handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**ЛИНИРР \_ инвалкаунтрикоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-217"><span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR\_INVALCOUNTRYCODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-218">Указан недопустимый код страны или региона.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-218">The specified country or region code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**ЛИНИРР \_ инвалдевицекласс**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-219"><span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-220">Устройство линии не имеет связанного устройства для данного класса устройств, или указанная строка не поддерживает указанный класс устройства.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-220">The line device has no associated device for the given device class, or the specified line does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**ЛИНИРР \_ инвалдевицехандле**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-221"><span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR\_INVALDEVICEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-222">Недопустимый маркер устройства линии.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-222">The line device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**ЛИНИРР \_ инвалдиалпарамс**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-223"><span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR\_INVALDIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-224">Недопустимые параметры набора номера.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-224">The dialing parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**ЛИНИРР \_ инвалдигитлист**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-225"><span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR\_INVALDIGITLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-226">Указан недопустимый список цифр.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-226">The specified digit list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**ЛИНИРР \_ инвалдигитмоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-227"><span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR\_INVALDIGITMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-228">Указан недопустимый цифровой режим.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-228">The specified digit mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**ЛИНИРР \_ инвалдигитс**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-229"><span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR\_INVALDIGITS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-230">Указаны недопустимые цифры завершения.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-230">The specified termination digits are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**ЛИНИРР \_ инвалекстверсион**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-231"><span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-232">Недопустимый номер версии расширения поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-232">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**ЛИНИРР \_ инвалфеатуре**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-233"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-234">Недопустимый параметр *двфеатуре* .</span><span class="sxs-lookup"><span data-stu-id="b7d9e-234">The *dwFeature* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**ЛИНИРР \_ инвалфеатуре**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-235"><span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR\_INVALFEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-236">Приложение вызвало функцию, недоступную в этой строке.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-236">The application invoked a feature that is not available on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**ЛИНИРР \_ инвалграупид**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-237"><span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR\_INVALGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-238">Указан недопустимый идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-238">The specified group identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**ЛИНИРР \_ инваллинехандле**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-239"><span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR\_INVALLINEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-240">Указанный вызов, устройство, устройство линии или маркер строки недопустимы.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-240">The specified call, device, line device, or line handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**ЛИНИРР \_ инваллинестате**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-241"><span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR\_INVALLINESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-242">Конфигурация устройства не может быть изменена в текущем состоянии строки.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-242">The device configuration may not be changed in the current line state.</span></span> <span data-ttu-id="b7d9e-243">Строка может использоваться другим приложением, или параметр *двлинестатес* содержит один или несколько битов, которые не являются [ \_ константами линедевстате](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b7d9e-243">The line may be in use by another application or a *dwLineStates* parameter contains one or more bits that are not [LINEDEVSTATE\_ constants](linedevstate--constants.md).</span></span> <span data-ttu-id="b7d9e-244">Значение **линирр \_ инваллинестате** также может указывать на то, что устройство отключено или находится вне обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-244">The **LINEERR\_INVALLINESTATE** value can also indicate that the device is disconnected or out of service.</span></span> <span data-ttu-id="b7d9e-245">Эти состояния обозначаются заданием битов, соответствующих значениям *линедевстатусфлагс \_ Connected* и *линедевстатусфлагсing \_* , равными 0 в элементе **Двдевстатусфлагс** структуры [**линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) , возвращаемой функцией [**линежетлинедевстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="b7d9e-245">These states are indicated by setting the bits corresponding to the *LINEDEVSTATUSFLAGS\_CONNECTED* and *LINEDEVSTATUSFLAGS\_INSERVICE* values to 0 in the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure returned by the [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**ЛИНИРР \_ инваллокатион**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-246"><span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR\_INVALLOCATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-247">Не удалось найти постоянный идентификатор расположения, указанный в *двлокатион* , ни в одной записи в \[ разделе Locations \] в реестре.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-247">The permanent location identifier specified in *dwLocation* could not be found in any entry in the \[Locations\] section in the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**ЛИНИРР \_ инвалмедиалист**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-248"><span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR\_INVALMEDIALIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-249">Указан недопустимый список носителей.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-249">The specified media list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**ЛИНИРР \_ инвалмедиамоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-250"><span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR\_INVALMEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-251">Список типов мультимедиа (режимов) для отслеживания содержит недопустимые данные, указанный параметр типа носителя является недопустимым, или поставщик услуг не поддерживает указанный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-251">The list of media types (modes) to be monitored contains invalid information, the specified media type parameter is invalid, or the service provider does not support the specified media type.</span></span> <span data-ttu-id="b7d9e-252">Типы мультимедиа, поддерживаемые в строке, перечислены в элементе **двмедиамодес** в структуре [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .</span><span class="sxs-lookup"><span data-stu-id="b7d9e-252">The media types supported on the line are listed in the **dwMediaModes** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**ЛИНИРР \_ инвалмессажеид**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-253"><span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR\_INVALMESSAGEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-254">Число, заданное в *двмессажеид* , находится вне диапазона, заданного элементом **Двнумкомплетионмессажес** в структуре [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="b7d9e-254">The number given in *dwMessageID* is outside the range specified by the **dwNumCompletionMessages** member in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**ЛИНИРР \_ инвалпарам**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-255"><span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-256">Параметр или структура, на которые указывает параметр, содержит недопустимые сведения, код страны или региона недопустим, недопустимый указатель окна или указанный параметр прямого списка содержит недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-256">A parameter or structure that a parameter points to contains invalid information, a country or region code is invalid, a window handle is invalid, or the specified forward list parameter contains invalid information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**ЛИНИРР \_ инвалпаркид**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-257"><span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR\_INVALPARKID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-258">Недопустимый идентификатор парковки.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-258">The park identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**ЛИНИРР \_ инвалпаркмоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-259"><span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR\_INVALPARKMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-260">Указан недопустимый режим парковки.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-260">The specified park mode is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**ЛИНИРР \_ инвалпассворд**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-261"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-262">Указан неправильный пароль, запрошенное действие не выполнено.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-262">The specified password is not correct and the requested action has not been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**ЛИНИРР \_ инвалпассворд**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-263"><span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR\_INVALPASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-264">Приложение использовало недопустимый пароль.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-264">The application used an invalid password.</span></span> <span data-ttu-id="b7d9e-265">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-265">This value is exposed only to applications that negotiate a TAPI version of 2.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**ЛИНИРР \_ инвалпоинтер**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-266"><span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-267">Один или несколько указанных параметров указателя (например, *лпкалллист*, *лпдвапиверсион*, *лпекстенсионид*, *лпдвекстверсион*, *лфикон*, *лплинедевкапс* и *Лптонелист*) недопустимы, или необходим указатель на выходной параметр **со значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-267">One or more of the specified pointer parameters (such as *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps*, and *lpToneList*) are invalid, or a required pointer to an output parameter is **NULL**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**ЛИНИРР \_ инвалпривселект**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-268"><span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR\_INVALPRIVSELECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-269">Для параметра *двпривилежес* был задан недопустимый флаг или сочетание флагов.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-269">An invalid flag or combination of flags was set for the *dwPrivileges* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**ЛИНИРР \_ инвалрате**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-270"><span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR\_INVALRATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-271">Указана недопустимая скорость.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-271">The specified rate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**ЛИНИРР \_ инвалрекуестмоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-272"><span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR\_INVALREQUESTMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-273">Недопустимый индикатор [**линерекуестмоде**](linerequestmode--constants.md) .</span><span class="sxs-lookup"><span data-stu-id="b7d9e-273">The [**LINEREQUESTMODE**](linerequestmode--constants.md) indicator is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**ЛИНИРР \_ инвалтерминалид**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-274"><span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR\_INVALTERMINALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-275">Указан недопустимый идентификатор терминала.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-275">The specified terminal identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**ЛИНИРР \_ инвалтерминалмоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-276"><span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR\_INVALTERMINALMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-277">Указан недопустимый параметр режимов терминала.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-277">The specified terminal modes parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**ЛИНИРР \_ инвалтимеаут**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-278"><span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR\_INVALTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-279">Значения времени ожидания не поддерживаются, или значение выходит за пределы допустимого диапазона, указанного в [**линедевкапс**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="b7d9e-279">Timeouts are not supported or a value falls outside the valid range specified in [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**ЛИНИРР \_ инвалтоне**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-280"><span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR\_INVALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-281">Указанный пользовательский тон не представляет допустимый тон или состоит из слишком большого числа частот или если указанная структура тона не описывает допустимый тон.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-281">The specified custom tone does not represent a valid tone or is made up of too many frequencies or the specified tone structure does not describe a valid tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**ЛИНИРР \_ инвалтонелист**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-282"><span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR\_INVALTONELIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-283">Указан недопустимый список тонов.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-283">The specified tone list is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**ЛИНИРР \_ инвалтонемоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-284"><span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR\_INVALTONEMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-285">Указан недопустимый параметр "тоновый режим".</span><span class="sxs-lookup"><span data-stu-id="b7d9e-285">The specified tone mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**ЛИНИРР \_ инвалтрансфермоде**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-286"><span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR\_INVALTRANSFERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-287">Указан недопустимый параметр режима пересылки.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-287">The specified transfer mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**ЛИНИРР \_ линемапперфаилед**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-288"><span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR\_LINEMAPPERFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-289">ЛИНЕМАППЕР было передано значение, переданное в параметре *двдевицеид* , но строки, соответствующие требованиям, указанным в параметре *лпкаллпарамс* , не найдены.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-289">LINEMAPPER was the value passed in the *dwDeviceID* parameter, but no lines were found that match the requirements specified in the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**ЛИНИРРная \_ Конференция**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-290"><span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR\_NOCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-291">Указанный вызов не является обработчиком вызова конференции или вызовом участника.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-291">The specified call is not a conference call handle or a participant call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**\_устройство линирр**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-292"><span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-293">Указанный идентификатор устройства, который ранее был действителен, больше не принимается, так как связанное устройство было удалено из системы с момента последней инициализации TAPI.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-293">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized.</span></span> <span data-ttu-id="b7d9e-294">Кроме того, устройство линии не имеет связанного устройства для данного класса устройств.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-294">Alternately, the line device has no associated device for the given device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**ЛИНИРР \_ Drive**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-295"><span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-296">Не удалось найти Tapiaddr.dll или поставщик телефонной службы для указанного устройства обнаружил, что один из его компонентов отсутствует или поврежден, так как он не был обнаружен во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-296">Either Tapiaddr.dll could not be located or the telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="b7d9e-297">Чтобы устранить проблему, пользователю рекомендуется использовать панель управления телефонии.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-297">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**ЛИНИРР \_ номем**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-298"><span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**LINEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-299">Недостаточно памяти для выполнения операции или не удалось заблокировать память.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-299">Insufficient memory to perform the operation, or unable to lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**ЛИНИРР \_ номултиплеинстанце**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-300"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-301">Поставщик услуг телефонии, который не поддерживает несколько экземпляров, несколько раз указан в \[ \] разделе поставщиков в реестре.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-301">A telephony service provider that does not support multiple instances is listed more than once in the \[Providers\] section in the registry.</span></span> <span data-ttu-id="b7d9e-302">Приложение должно рекомендовать пользователю использовать панель управления телефонии для удаления повторяющегося драйвера.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-302">The application should advise the user to use the Telephony Control Panel to remove the duplicated driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**ЛИНИРР \_ номултиплеинстанце**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-303"><span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR\_NOMULTIPLEINSTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-304">Несколько экземпляров этого поставщика услуг не допускаются.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-304">Multiple instances of this service provider are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**ЛИНИРР, \_ запрос**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-305"><span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR\_NOREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-306">В настоящее время нет запроса, ожидающего указанного режима, или приложение больше не является приложением с наивысшим приоритетом для указанного режима запроса.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-306">There currently is no request pending of the indicated mode, or the application is no longer the highest-priority application for the specified request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**ЛИНИРР \_**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-307"><span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-308">Приложение не имеет прав владельца на указанный вызов.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-308">The application does not have owner privilege to the specified call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**ЛИНИРР \_ зарегистрировано**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-309"><span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR\_NOTREGISTERED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-310">Приложение не зарегистрировано как получатель запроса для указанного режима запроса.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-310">The application is not registered as a request recipient for the indicated request mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**ЛИНИРР \_ оператионфаилед**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-311"><span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-312">Не удалось выполнить операцию по неопределенной или неизвестной причине.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-312">The operation failed for an unspecified or unknown reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**ЛИНИРР \_ оператионунаваил**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-313"><span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-314">Операция недоступна, например для данного устройства или указанной строки.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-314">The operation is not available, such as for the given device or specified line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**ЛИНИРР \_ ратеунаваил**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-315"><span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR\_RATEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-316">В настоящее время поставщик услуг не имеет достаточной пропускной способности, доступной для указанной скорости.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-316">The service provider currently does not have enough bandwidth available for the specified rate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**ЛИНИРР \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-317"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-318">Если была запрошена повторная инициализация TAPI, например, в результате добавления или удаления поставщика услуг телефонии, то запросы [**линеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)или [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) отклоняются с этой ошибкой до тех пор, пока Последнее приложение не завершит использование API (с помощью [**линешутдовн**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), когда новая конфигурация вступит в силу и приложения снова смогут вызвать **линеинитиализе** или **линеинитиализикс**.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-318">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), or [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **lineInitialize** or **lineInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**ЛИНИРР \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-319"><span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**LINEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-320">Приложение попыталось инициализировать TAPI дважды.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-320">The application attempted to initialize TAPI twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**ЛИНИРР \_ рекуестоверрун**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-321"><span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-322">Количество запросов в ожидании, чем устройство может быть обработано.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-322">More requests are pending than the device can handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**ЛИНИРР \_ ресаурцеунаваил**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-323"><span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-324">Недостаточно ресурсов для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-324">Insufficient resources to complete the operation.</span></span> <span data-ttu-id="b7d9e-325">Например, строку нельзя открыть из-за перерасхода динамических ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-325">For example, a line cannot be opened due to a dynamic resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**ЛИНИРР \_ структуретусмалл**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-326"><span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-327">Элемент **двтоталсизе** структуры не указывает достаточно памяти для хранения фиксированной части указанной структуры.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-327">The **dwTotalSize** member of a structure does not specify enough memory to contain the fixed portion of the specified structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**ЛИНИРР \_ таржетнотфаунд**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-328"><span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR\_TARGETNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-329">Не найден целевой объект для перенаправления вызова.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-329">A target for the call handoff was not found.</span></span> <span data-ttu-id="b7d9e-330">Это может произойти, если именованное приложение не открывало бы ту же строку с \_ битом владельца линекаллпривилеже в  параметре двпривилежес [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span><span class="sxs-lookup"><span data-stu-id="b7d9e-330">This can occur if the named application did not open the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span> <span data-ttu-id="b7d9e-331">Или, в случае передачи в режиме мультимедиа, ни одно приложение не открывало в \_ параметре *двпривилежес* [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen) и тип мультимедиа, указанный в *параметре* *ДВМЕДИАМОДЕС* [**линеопен**](/windows/desktop/api/Tapi/nf-tapi-lineopen), ни одна строка с битом линекаллпривилеже Owner.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-331">Or, in the case of media-mode handoff, no application has opened the same line with the LINECALLPRIVILEGE\_OWNER bit in the *dwPrivileges* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) and with the media type specified in the *dwMediaMode* parameter having been specified in the *dwMediaModes* parameter of [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**ЛИНИРР \_ таржетселф**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-332"><span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR\_TARGETSELF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-333">Приложение, вызывающее эту операцию, является целевым объектом косвенной передачи.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-333">The application invoking this operation is the target of the indirect handoff.</span></span> <span data-ttu-id="b7d9e-334">То есть TAPI определил, что вызывающее приложение также является приложением с наивысшим приоритетом для данного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-334">That is, TAPI has determined that the calling application is also the highest priority application for the given media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**ЛИНИРР не \_ инициализирован**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-335"><span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-336">Операция была вызвана до любого приложения с именем [**линеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) или [**линеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="b7d9e-336">The operation was invoked before any application called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**ЛИНИРР \_ усерканцеллед**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-337"><span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR\_USERCANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-338">Пользователь отменил вызов.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-338">The user cancelled the call.</span></span> <span data-ttu-id="b7d9e-339">Это значение предоставляется только для приложений, которые согласовывают TAPI версии 2,2 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-339">This value is exposed only to applications that negotiate a TAPI version of 2.2 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7d9e-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**ЛИНИРР \_ усерусеринфотубиг**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-340"><span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR\_USERUSERINFOTOOBIG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b7d9e-341">Строка, содержащая сведения о пользователе пользователя, превышает максимальное число байтов, указанное в элементе **двууиакцептсизе**, **двууиансверсизе**, **двууидропсизе**, **двууимакекаллсизе** или **двууисендусерусеринфосизе** в [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), либо строка, содержащая сведения о пользователе пользователя, слишком длинная.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-341">The string containing user-user information exceeds the maximum number of bytes specified in the **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize**, or **dwUUISendUserUserInfoSize** member of [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), or the string containing user-user information is too long.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7d9e-342">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7d9e-342">Remarks</span></span>

<span data-ttu-id="b7d9e-343">Значения 0xC0000000 до 0xFFFFFFFF доступны для расширений устройств.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-343">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions.</span></span> <span data-ttu-id="b7d9e-344">Значения от 0x80000000 до 0xBFFFFFFF зарезервированы, а в качестве идентификаторов запросов используется 0x00000000 – 0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-344">The values 0x80000000 through 0xBFFFFFFF are reserved, while 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="b7d9e-345">Если приложение получает сообщение об ошибке, возвращающее, что оно не обрабатывается специально (например, сообщение об ошибке, определенное расширением конкретного устройства), оно должно рассматривать ошибку как ЛИНИРР \_ оператионфаилед (по неизвестной причине).</span><span class="sxs-lookup"><span data-stu-id="b7d9e-345">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a LINEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

<span data-ttu-id="b7d9e-346">При вызове констант ЛИНИРР, которые \_ являются новыми для TAPI 3,0, необходимо обновить файл Tapierr.MC новыми сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b7d9e-346">When invoking the LINEERR\_constants which are new with TAPI 3.0, the Tapierr.mc file must be updated with new messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d9e-347">Требования</span><span class="sxs-lookup"><span data-stu-id="b7d9e-347">Requirements</span></span>



| <span data-ttu-id="b7d9e-348">Требование</span><span class="sxs-lookup"><span data-stu-id="b7d9e-348">Requirement</span></span> | <span data-ttu-id="b7d9e-349">Значение</span><span class="sxs-lookup"><span data-stu-id="b7d9e-349">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b7d9e-350">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="b7d9e-350">TAPI version</span></span><br/> | <span data-ttu-id="b7d9e-351">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b7d9e-351">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b7d9e-352">Header</span><span class="sxs-lookup"><span data-stu-id="b7d9e-352">Header</span></span><br/>       | <dl> <span data-ttu-id="b7d9e-353"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d9e-353"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d9e-354">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7d9e-354">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d9e-355">**линеаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-355">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="b7d9e-356">**линедевкапс**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-356">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="b7d9e-357">**линедевстатус**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-357">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="b7d9e-358">**линежетлинедевстатус**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-358">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="b7d9e-359">**линеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-359">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="b7d9e-360">**линеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-360">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[<span data-ttu-id="b7d9e-361">**линеопен**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-361">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="b7d9e-362">**линешутдовн**</span><span class="sxs-lookup"><span data-stu-id="b7d9e-362">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




