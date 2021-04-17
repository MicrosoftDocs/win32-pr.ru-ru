---
description: При возникновении ошибки Инструментарий WMI возвращает код ошибки в виде значения HRESULT. Эти коды могут возвращаться сценариями, приложениями C++ или WMIC.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Константы ошибок WMI (Вбемкли. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711613"
---
# <a name="wmi-error-constants"></a><span data-ttu-id="67da8-104">Константы ошибок WMI</span><span class="sxs-lookup"><span data-stu-id="67da8-104">WMI Error Constants</span></span>

<span data-ttu-id="67da8-105">При возникновении ошибки Инструментарий WMI возвращает код ошибки в виде значения **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67da8-105">If an error occurs, WMI returns an error code as an **HRESULT** value.</span></span> <span data-ttu-id="67da8-106">Эти коды могут возвращаться сценариями, приложениями C++ или [**WMIC**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="67da8-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md).</span></span>

> [!Note]
>
> <span data-ttu-id="67da8-107">Следующая документация предназначена для разработчиков и ИТ-администраторов.</span><span class="sxs-lookup"><span data-stu-id="67da8-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="67da8-108">Если вы являетесь пользователем, имеющим сообщение об ошибке, связанное с WMI, перейдите в [Служба поддержки Майкрософт](https://support.microsoft.com/) и найдите код ошибки, который вы видите в сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="67da8-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="67da8-109">Дополнительные сведения об устранении неполадок со сценариями WMI и службой WMI см. в разделе [инструментарий WMI не работает](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="67da8-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span></span>
>
> <span data-ttu-id="67da8-110">Если инструментарий WMI возвращает сообщения об ошибках, имейте в виду, что они могут не указывать на проблемы в службе WMI или в поставщиках WMI.</span><span class="sxs-lookup"><span data-stu-id="67da8-110">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="67da8-111">Сбои могут исходить из других частей операционной системы и возникать как ошибки через инструментарий WMI.</span><span class="sxs-lookup"><span data-stu-id="67da8-111">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="67da8-112">При любых обстоятельствах не удаляйте репозиторий WMI как первое действие, поскольку удаление репозитория может привести к повреждению системы или установке приложений.</span><span class="sxs-lookup"><span data-stu-id="67da8-112">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="67da8-113">Чтобы получить дополнительные сведения об источнике проблемы, скачайте и запустите программу командной строки для диагностики [служебная программа для диагностики WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="67da8-113">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="67da8-114">Это средство создает отчет, который обычно может изолировать источник проблемы и предоставить инструкции по ее устранению.</span><span class="sxs-lookup"><span data-stu-id="67da8-114">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="67da8-115">Этот отчет также помогает в работе со службой поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="67da8-115">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="67da8-116">Служебная программа для диагностики WMI можно скачать [здесь](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="67da8-116">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

<span data-ttu-id="67da8-117">Некоторые методы в классах WMI могут возвращать системные и сетевые коды ошибок (например, 64).</span><span class="sxs-lookup"><span data-stu-id="67da8-117">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="67da8-118">Определение этих типов кодов ошибок можно проверить с помощью команды **net helpmsg** в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="67da8-118">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="67da8-119">Например, команда **net helpmsg 64** возвращает сообщение: указанное сетевое имя больше недоступно.</span><span class="sxs-lookup"><span data-stu-id="67da8-119">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

<span data-ttu-id="67da8-120">В следующем списке перечислены некоторые распространенные диапазоны ошибок.</span><span class="sxs-lookup"><span data-stu-id="67da8-120">The following list lists some common ranges of errors.</span></span>

<dl> <dt>

<span data-ttu-id="67da8-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span><span class="sxs-lookup"><span data-stu-id="67da8-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span></span>
</dt> <dd>

<span data-ttu-id="67da8-122">Ошибки, возникающие в самом инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="67da8-122">Errors that originate in WMI itself.</span></span>

<span data-ttu-id="67da8-123">Не удалось выполнить определенную операцию WMI из-за</span><span class="sxs-lookup"><span data-stu-id="67da8-123">A specific WMI operation failed because of</span></span>

-   <span data-ttu-id="67da8-124">Ошибка в запросе, например запрос WQL, или учетная запись не имеет нужных разрешений.</span><span class="sxs-lookup"><span data-stu-id="67da8-124">An error in the request, for example, a WQL query fails or the account does not have the correct permissions.</span></span>
-   <span data-ttu-id="67da8-125">Проблема с инфраструктурой WMI, например неправильная регистрация CIM или DCOM.</span><span class="sxs-lookup"><span data-stu-id="67da8-125">A WMI infrastructure problem, such as incorrect CIM or DCOM registration.</span></span>

</dd> <dt>

<span data-ttu-id="67da8-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span><span class="sxs-lookup"><span data-stu-id="67da8-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span></span>
</dt> <dd>

<span data-ttu-id="67da8-127">Ошибки, происходящие в основной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="67da8-127">Errors originating in the core operating system.</span></span> <span data-ttu-id="67da8-128">Инструментарий WMI может вернуть ошибку такого типа из-за внешней ошибки, например ошибки безопасности DCOM.</span><span class="sxs-lookup"><span data-stu-id="67da8-128">WMI may return this type of error because of an external failure, for example, DCOM security failure.</span></span>

</dd> <dt>

<span data-ttu-id="67da8-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span><span class="sxs-lookup"><span data-stu-id="67da8-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span></span>
</dt> <dd>

<span data-ttu-id="67da8-130">Ошибки, происходящие в DCOM.</span><span class="sxs-lookup"><span data-stu-id="67da8-130">Errors originating in DCOM.</span></span> <span data-ttu-id="67da8-131">Например, конфигурация DCOM для операций на удаленном компьютере может быть неверной.</span><span class="sxs-lookup"><span data-stu-id="67da8-131">For example, the DCOM configuration for operations to a remote computer may be incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="67da8-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span><span class="sxs-lookup"><span data-stu-id="67da8-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span></span>
</dt> <dd>

<span data-ttu-id="67da8-133">Ошибка, полученная из ADSI (интерфейсов служб Active Directory) или LDAP (протокол Lightweight Directory Access), например, сбой доступа Active Directory при использовании поставщиков Active Directory WMI.</span><span class="sxs-lookup"><span data-stu-id="67da8-133">Error originating from ADSI (Active Directory Service Interfaces) or LDAP (Lightweight Directory Access Protocol), for example, an Active Directory access failure when using the WMI Active Directory providers.</span></span>

</dd> </dl>

<span data-ttu-id="67da8-134">Некоторые методы в классах WMI могут возвращать системные и сетевые коды ошибок (например, 64).</span><span class="sxs-lookup"><span data-stu-id="67da8-134">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="67da8-135">Определение этих типов кодов ошибок можно проверить с помощью команды **net helpmsg** в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="67da8-135">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="67da8-136">Например, команда **net helpmsg 64** возвращает сообщение: указанное сетевое имя больше недоступно.</span><span class="sxs-lookup"><span data-stu-id="67da8-136">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span> <span data-ttu-id="67da8-137">В C++ можно вызвать [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) и указать **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** в качестве модуля сообщения.</span><span class="sxs-lookup"><span data-stu-id="67da8-137">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="67da8-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**\_сбой WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-139">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="67da8-139">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-140">Сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="67da8-140">Call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="67da8-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-142">2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="67da8-142">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-143">Не удается найти объект.</span><span class="sxs-lookup"><span data-stu-id="67da8-143">Object cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**\_ \_ отказано в доступе к WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-145">2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="67da8-145">2147749891 (0x80041003)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-146">У текущего пользователя нет разрешения на выполнение действия.</span><span class="sxs-lookup"><span data-stu-id="67da8-146">Current user does not have permission to perform the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_ \_ сбой поставщика WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-148">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="67da8-148">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-149">Произошел сбой поставщика в некоторый момент, кроме инициализации.</span><span class="sxs-lookup"><span data-stu-id="67da8-149">Provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**\_несоответствие типов электронной почты WBEM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-151">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="67da8-151">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-152">Обнаружено несоответствие типов.</span><span class="sxs-lookup"><span data-stu-id="67da8-152">Type mismatch occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ \_ \_ , нехваткой \_ памяти**</span><span class="sxs-lookup"><span data-stu-id="67da8-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-154">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="67da8-154">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-155">Недостаточно памяти для операции.</span><span class="sxs-lookup"><span data-stu-id="67da8-155">Not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**\_ \_ Недопустимый контекст для WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM\_E\_INVALID\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-157">2147749895 (0x80041007)</span><span class="sxs-lookup"><span data-stu-id="67da8-157">2147749895 (0x80041007)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-158">Недопустимый объект [**ивбемконтекст**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="67da8-158">The [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_ \_ Недопустимый параметр "WBEM E" \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-160">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="67da8-160">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-161">Один из параметров вызова указан неправильно.</span><span class="sxs-lookup"><span data-stu-id="67da8-161">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="67da8-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-163">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="67da8-163">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-164">Ресурс, обычно удаленный сервер, в настоящее время недоступен.</span><span class="sxs-lookup"><span data-stu-id="67da8-164">Resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**\_ \_ критическая ошибка WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM\_E\_CRITICAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-166">2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="67da8-166">2147749898 (0x8004100A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-167">Произошла внутренняя, критическая и непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="67da8-167">Internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="67da8-168">Сообщите об ошибке службе технической поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="67da8-168">Report the error to Microsoft Technical Support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**\_ \_ Недопустимый \_ поток WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM\_E\_INVALID\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-170">2147749899 (0x8004100B)</span><span class="sxs-lookup"><span data-stu-id="67da8-170">2147749899 (0x8004100B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-171">В течение удаленного сеанса поврежден один или несколько сетевых пакетов.</span><span class="sxs-lookup"><span data-stu-id="67da8-171">One or more network packets were corrupted during a remote session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="67da8-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-173">2147749900 (0x8004100C)</span><span class="sxs-lookup"><span data-stu-id="67da8-173">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-174">Функция или операция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="67da8-174">Feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**\_ \_ Недопустимый \_ суперкласс для WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM\_E\_INVALID\_SUPERCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-176">2147749901 (0x8004100D)</span><span class="sxs-lookup"><span data-stu-id="67da8-176">2147749901 (0x8004100D)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-177">Указан недопустимый родительский класс.</span><span class="sxs-lookup"><span data-stu-id="67da8-177">Parent class specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ недопустимое \_ пространство имен**</span><span class="sxs-lookup"><span data-stu-id="67da8-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-179">2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="67da8-179">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-180">Не удается найти указанное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="67da8-180">Namespace specified cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_ \_ Недопустимый \_ объект для WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-182">2147749903 (0x8004100F)</span><span class="sxs-lookup"><span data-stu-id="67da8-182">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-183">Указан недопустимый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="67da8-183">Specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**\_ \_ Недопустимый \_ класс WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM\_E\_INVALID\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-185">2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="67da8-185">2147749904 (0x80041010)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-186">Указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="67da8-186">Specified class is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_поставщик WBEM \_ E \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="67da8-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**WBEM\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-188">2147749905 (0x80041011)</span><span class="sxs-lookup"><span data-stu-id="67da8-188">2147749905 (0x80041011)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-189">Поставщик, указанный в схеме, не имеет соответствующей регистрации.</span><span class="sxs-lookup"><span data-stu-id="67da8-189">Provider referenced in the schema does not have a corresponding registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**\_ \_ недействительная \_ Регистрация поставщика WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM\_E\_INVALID\_PROVIDER\_REGISTRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-191">2147749906</span><span class="sxs-lookup"><span data-stu-id="67da8-191">2147749906</span></span>
</dt> <dt>



<span data-ttu-id="67da8-192">Поставщик, указанный в схеме, имеет неправильную или неполную регистрацию.</span><span class="sxs-lookup"><span data-stu-id="67da8-192">Provider referenced in the schema has an incorrect or incomplete registration.</span></span>

<span data-ttu-id="67da8-193">Эта ошибка может быть вызвана множеством условий, включая следующие.</span><span class="sxs-lookup"><span data-stu-id="67da8-193">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="67da8-194">Пропущенная команда [ \# пространства имен pragma](pragma-namespace.md) в файле MOF-файл (MOF), используемом для регистрации поставщика.</span><span class="sxs-lookup"><span data-stu-id="67da8-194">A missing [\#pragma namespace](pragma-namespace.md) command in the Managed Object Format (MOF) file used to register the provider.</span></span> <span data-ttu-id="67da8-195">Поставщик может быть зарегистрирован в неправильном пространстве имен WMI.</span><span class="sxs-lookup"><span data-stu-id="67da8-195">The provider may be registered in the wrong WMI namespace.</span></span>
-   <span data-ttu-id="67da8-196">Не удалось получить регистрацию COM.</span><span class="sxs-lookup"><span data-stu-id="67da8-196">Failure to retrieve the COM registration.</span></span>
-   <span data-ttu-id="67da8-197">Недопустимая модель размещения.</span><span class="sxs-lookup"><span data-stu-id="67da8-197">Hosting model is not valid.</span></span> <span data-ttu-id="67da8-198">Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="67da8-198">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="67da8-199">В регистрации указан недопустимый класс.</span><span class="sxs-lookup"><span data-stu-id="67da8-199">An class specified in the registration is not valid.</span></span>
-   <span data-ttu-id="67da8-200">Сбой создания экземпляра или наследования от класса [**\_ \_ Win32Provider**](--win32provider.md) для создания регистрации поставщика в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="67da8-200">Failure to create an instance of or inherit from the [**\_\_Win32Provider**](--win32provider.md) class to create the provider registration in the MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**\_ \_ \_ сбой загрузки поставщика WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM\_E\_PROVIDER\_LOAD\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-202">2147749907 (0x80041013)</span><span class="sxs-lookup"><span data-stu-id="67da8-202">2147749907 (0x80041013)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-203">COM не может найти поставщика, на которого ссылается схема.</span><span class="sxs-lookup"><span data-stu-id="67da8-203">COM cannot locate a provider referenced in the schema.</span></span>

<span data-ttu-id="67da8-204">Эта ошибка может быть вызвана множеством условий, включая следующие.</span><span class="sxs-lookup"><span data-stu-id="67da8-204">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="67da8-205">Поставщик использует библиотеку DLL WMI, которая не соответствует lib-файлу, используемому при построении поставщика.</span><span class="sxs-lookup"><span data-stu-id="67da8-205">Provider is using a WMI DLL that does not match the .lib file used when the provider was built.</span></span>
-   <span data-ttu-id="67da8-206">Библиотека DLL поставщика или любая из библиотек DLL, от которых он зависит, повреждена.</span><span class="sxs-lookup"><span data-stu-id="67da8-206">Provider's DLL, or any of the DLLs on which it depends, is corrupt.</span></span>
-   <span data-ttu-id="67da8-207">Поставщику не удалось экспортировать [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="67da8-207">Provider failed to export [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span>
-   <span data-ttu-id="67da8-208">Внутрипроцессный поставщик не был зарегистрирован с помощью команды **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="67da8-208">In-process provider was not registered using the **regsvr32** command.</span></span>
-   <span data-ttu-id="67da8-209">Внутрипроцессный поставщик не был зарегистрирован с помощью параметра **/regserver** .</span><span class="sxs-lookup"><span data-stu-id="67da8-209">Out-of-process provider was not registered using the **/regserver** switch.</span></span> <span data-ttu-id="67da8-210">Например, **myprog.exe/RegServer**.</span><span class="sxs-lookup"><span data-stu-id="67da8-210">For example, **myprog.exe /regserver**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ Ошибка инициализации WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-212">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="67da8-212">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-213">Не удалось инициализировать компонент, например поставщик, по внутренним причинам.</span><span class="sxs-lookup"><span data-stu-id="67da8-213">Component, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**\_ \_ сбой транспорта с WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM\_E\_TRANSPORT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-215">2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="67da8-215">2147749909 (0x80041015)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-216">Ошибка сети, которая не допустила нормальных операций.</span><span class="sxs-lookup"><span data-stu-id="67da8-216">Networking error that prevents normal operation has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ недействительная \_ Операция WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-218">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="67da8-218">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-219">Запрошенная операция недопустима.</span><span class="sxs-lookup"><span data-stu-id="67da8-219">Requested operation is not valid.</span></span> <span data-ttu-id="67da8-220">Эта ошибка обычно является ответом на недопустимые попытки удалить классы или свойства.</span><span class="sxs-lookup"><span data-stu-id="67da8-220">This error usually applies to invalid attempts to delete classes or properties.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ \_ Недопустимый запрос для WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-222">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="67da8-222">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-223">Синтаксически недопустимый запрос.</span><span class="sxs-lookup"><span data-stu-id="67da8-223">Query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_ \_ Недопустимый \_ тип запроса WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-225">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="67da8-225">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-226">Запрошенный язык запросов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="67da8-226">Requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="67da8-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-228">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="67da8-228">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-229">В операции размещения был указан флаг **вбемчанжефлагкреатеонли** , но экземпляр уже существует.</span><span class="sxs-lookup"><span data-stu-id="67da8-229">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**Переопределение для WBEM \_ E \_ \_ не \_ разрешено**</span><span class="sxs-lookup"><span data-stu-id="67da8-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**WBEM\_E\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-231">2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="67da8-231">2147749914 (0x8004101A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-232">Невозможно выполнить операцию добавления для этого квалификатора, так как объект-владелец не допускает переопределения.</span><span class="sxs-lookup"><span data-stu-id="67da8-232">Not possible to perform the add operation on this qualifier because the owning object does not permit overrides.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**\_ \_ распространяемый квалификатор WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM\_E\_PROPAGATED\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-234">2147749915 (0x8004101B)</span><span class="sxs-lookup"><span data-stu-id="67da8-234">2147749915 (0x8004101B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-235">Пользователь попытался удалить квалификатор, который не является владельцем.</span><span class="sxs-lookup"><span data-stu-id="67da8-235">User attempted to delete a qualifier that was not owned.</span></span> <span data-ttu-id="67da8-236">Квалификатор был унаследован от класса-родителя.</span><span class="sxs-lookup"><span data-stu-id="67da8-236">The qualifier was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**\_ \_ распространяемое свойство WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM\_E\_PROPAGATED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-238">2147749916 (0x8004101C)</span><span class="sxs-lookup"><span data-stu-id="67da8-238">2147749916 (0x8004101C)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-239">Пользователь попытался удалить свойство, владельцем которого он не является.</span><span class="sxs-lookup"><span data-stu-id="67da8-239">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="67da8-240">Свойство было унаследовано от класса-родителя.</span><span class="sxs-lookup"><span data-stu-id="67da8-240">The property was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**\_ \_ непредвиденное непредусмотренное в WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM\_E\_UNEXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-242">2147749917 (0x8004101D)</span><span class="sxs-lookup"><span data-stu-id="67da8-242">2147749917 (0x8004101D)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-243">Клиент сделал непредвиденную и недопустимую последовательность вызовов, например вызов [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) перед вызовом [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span><span class="sxs-lookup"><span data-stu-id="67da8-243">Client made an unexpected and illegal sequence of calls, such as calling [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) before calling [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**\_ \_ Недопустимая операция в WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM\_E\_ILLEGAL\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-245">2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="67da8-245">2147749918 (0x8004101E)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-246">Пользователь запросил недопустимую операцию, например, порождение класса из экземпляра.</span><span class="sxs-lookup"><span data-stu-id="67da8-246">User requested an illegal operation, such as spawning a class from an instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ не может \_ быть \_ ключом**</span><span class="sxs-lookup"><span data-stu-id="67da8-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM\_E\_CANNOT\_BE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-248">2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="67da8-248">2147749919 (0x8004101F)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-249">Недопустимая попытка указать квалификатор ключа для свойства, которое не может быть ключом.</span><span class="sxs-lookup"><span data-stu-id="67da8-249">Illegal attempt to specify a key qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="67da8-250">Ключи указываются в определении класса объекта и не могут быть изменены для каждого отдельного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="67da8-250">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**\_неполный \_ \_ класс WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM\_E\_INCOMPLETE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-252">2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="67da8-252">2147749920 (0x80041020)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-253">Текущий объект не является допустимым определением класса.</span><span class="sxs-lookup"><span data-stu-id="67da8-253">Current object is not a valid class definition.</span></span> <span data-ttu-id="67da8-254">Либо он неполон, либо не зарегистрирован в WMI с помощью [**SWbemObject. постановки \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="67da8-254">Either it is incomplete or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ \_ Недопустимый \_ синтаксис WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-256">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="67da8-256">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-257">Синтаксически недопустимый запрос.</span><span class="sxs-lookup"><span data-stu-id="67da8-257">Query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**\_ \_ недекорированный объект WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM\_E\_NONDECORATED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-259">2147749922 (0x80041022)</span><span class="sxs-lookup"><span data-stu-id="67da8-259">2147749922 (0x80041022)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-260">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="67da8-260">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**\_только для \_ чтения с WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-262">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="67da8-262">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-263">Была предпринята попытка изменить свойство, доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="67da8-263">An attempt was made to modify a read-only property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_поставщик WBEM \_ E \_ не \_ поддерживает**</span><span class="sxs-lookup"><span data-stu-id="67da8-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-265">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="67da8-265">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-266">Поставщик не может выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="67da8-266">Provider cannot perform the requested operation.</span></span> <span data-ttu-id="67da8-267">Это может включать слишком сложный запрос, получение экземпляра, создание или обновление класса, удаление класса или перечисление класса.</span><span class="sxs-lookup"><span data-stu-id="67da8-267">This can include a query that is too complex, retrieving an instance, creating or updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**\_класс WBEM \_ E \_ имеет \_ дочерние элементы**</span><span class="sxs-lookup"><span data-stu-id="67da8-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM\_E\_CLASS\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-269">2147749925 (0x80041025)</span><span class="sxs-lookup"><span data-stu-id="67da8-269">2147749925 (0x80041025)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-270">Предпринята попытка внести изменение, которое сделает подкласс недействительным.</span><span class="sxs-lookup"><span data-stu-id="67da8-270">Attempt was made to make a change that invalidates a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**\_ \_ у класса WBEM E \_ есть \_ экземпляры**</span><span class="sxs-lookup"><span data-stu-id="67da8-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM\_E\_CLASS\_HAS\_INSTANCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-272">2147749926 (0x80041026)</span><span class="sxs-lookup"><span data-stu-id="67da8-272">2147749926 (0x80041026)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-273">Предпринята попытка удалить или изменить класс, имеющий экземпляры.</span><span class="sxs-lookup"><span data-stu-id="67da8-273">Attempt was made to delete or modify a class that has instances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_запрос WBEM \_ E \_ не \_ реализован**</span><span class="sxs-lookup"><span data-stu-id="67da8-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM\_E\_QUERY\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-275">2147749927 (0x80041027)</span><span class="sxs-lookup"><span data-stu-id="67da8-275">2147749927 (0x80041027)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-276">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="67da8-276">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**\_ \_ недопустимое \_ значение NULL для WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-278">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="67da8-278">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-279">Значение Nothing или **null** было указано для свойства, которое должно иметь значение, например, помеченное квалификатором [**Key**](key-qualifier.md), [**индексированным**](optional-qualifiers.md)или **Not \_ null** .</span><span class="sxs-lookup"><span data-stu-id="67da8-279">Value of Nothing/**NULL** was specified for a property that must have a value, such as one that is marked by a [**Key**](key-qualifier.md), [**Indexed**](optional-qualifiers.md), or **Not\_Null** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM \_ E \_ Недопустимый \_ Тип квалификатора \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM\_E\_INVALID\_QUALIFIER\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-281">2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="67da8-281">2147749929 (0x80041029)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-282">Указано значение типа Variant для квалификатора, которое не является допустимым типом квалификатора.</span><span class="sxs-lookup"><span data-stu-id="67da8-282">Variant value for a qualifier was provided that is not a legal qualifier type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**\_ \_ Недопустимый \_ тип свойства WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM\_E\_INVALID\_PROPERTY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-284">2147749930 (0x8004102A)</span><span class="sxs-lookup"><span data-stu-id="67da8-284">2147749930 (0x8004102A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-285">Для свойства указан недопустимый тип CIM.</span><span class="sxs-lookup"><span data-stu-id="67da8-285">CIM type specified for a property is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_значение WBEM E \_ выходит за пределы допустимого \_ \_ \_ диапазона**</span><span class="sxs-lookup"><span data-stu-id="67da8-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-287">2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="67da8-287">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-288">Запрос был выполнен с использованием значения вне допустимого диапазона или несовместим с типом.</span><span class="sxs-lookup"><span data-stu-id="67da8-288">Request was made with an out-of-range value or it is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ не может \_ быть \_ SINGLETON**</span><span class="sxs-lookup"><span data-stu-id="67da8-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM\_E\_CANNOT\_BE\_SINGLETON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-290">2147749932 (0x8004102C)</span><span class="sxs-lookup"><span data-stu-id="67da8-290">2147749932 (0x8004102C)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-291">Предпринята недопустимая попытка создать Singleton класса, например, когда класс является производным от класса, не являющегося Singleton-классом.</span><span class="sxs-lookup"><span data-stu-id="67da8-291">Illegal attempt was made to make a class singleton, such as when the class is derived from a non-singleton class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ Недопустимый \_ \_ тип CIM**</span><span class="sxs-lookup"><span data-stu-id="67da8-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM\_E\_INVALID\_CIM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-293">2147749933 (0x8004102D)</span><span class="sxs-lookup"><span data-stu-id="67da8-293">2147749933 (0x8004102D)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-294">Указан недопустимый тип CIM.</span><span class="sxs-lookup"><span data-stu-id="67da8-294">CIM type specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ \_ Недопустимый \_ метод WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-296">2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="67da8-296">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-297">Запрошенный метод недоступен.</span><span class="sxs-lookup"><span data-stu-id="67da8-297">Requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM \_ E \_ недопустимые \_ \_ Параметры метода**</span><span class="sxs-lookup"><span data-stu-id="67da8-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-299">2147749935 (0x8004102F)</span><span class="sxs-lookup"><span data-stu-id="67da8-299">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-300">Для метода указаны недопустимые параметры.</span><span class="sxs-lookup"><span data-stu-id="67da8-300">Parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**\_ \_ системное свойство WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM\_E\_SYSTEM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-302">2147749936 (0x80041030)</span><span class="sxs-lookup"><span data-stu-id="67da8-302">2147749936 (0x80041030)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-303">Предпринята попытка получить квалификаторы для системного свойства.</span><span class="sxs-lookup"><span data-stu-id="67da8-303">There was an attempt to get qualifiers on a system property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**\_ \_ неправильное \_ свойство WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM\_E\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-305">2147749937 (0x80041031)</span><span class="sxs-lookup"><span data-stu-id="67da8-305">2147749937 (0x80041031)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-306">Тип свойства не распознан.</span><span class="sxs-lookup"><span data-stu-id="67da8-306">Property type is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**\_вызов WBEM \_ E \_ отменен**</span><span class="sxs-lookup"><span data-stu-id="67da8-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM\_E\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-308">2147749938 (0x80041032)</span><span class="sxs-lookup"><span data-stu-id="67da8-308">2147749938 (0x80041032)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-309">Асинхронный процесс был отменен внутренним образом или пользователем.</span><span class="sxs-lookup"><span data-stu-id="67da8-309">Asynchronous process has been canceled internally or by the user.</span></span> <span data-ttu-id="67da8-310">Обратите внимание, что из-за времени и природы асинхронной операции операция может быть недействительно отменена.</span><span class="sxs-lookup"><span data-stu-id="67da8-310">Note that due to the timing and nature of the asynchronous operation, the operation may not have been truly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ , \_ Завершение работы \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM\_E\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-312">2147749939 (0x80041033)</span><span class="sxs-lookup"><span data-stu-id="67da8-312">2147749939 (0x80041033)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-313">Пользователь запросил операцию, пока WMI находится в процессе завершения работы.</span><span class="sxs-lookup"><span data-stu-id="67da8-313">User has requested an operation while WMI is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_ \_ распространенный метод WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM\_E\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-315">2147749940 (0x80041034)</span><span class="sxs-lookup"><span data-stu-id="67da8-315">2147749940 (0x80041034)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-316">Предпринята попытка повторно использовать существующее имя метода из родительского класса, и подписи не совпадают.</span><span class="sxs-lookup"><span data-stu-id="67da8-316">Attempt was made to reuse an existing method name from a parent class and the signatures do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**\_ \_ неподдерживаемый параметр в WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM\_E\_UNSUPPORTED\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-318">2147749941 (0x80041035)</span><span class="sxs-lookup"><span data-stu-id="67da8-318">2147749941 (0x80041035)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-319">Одно или несколько значений параметров, например, текст запроса, являются слишком сложными или не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="67da8-319">One or more parameter values, such as a query text, is too complex or unsupported.</span></span> <span data-ttu-id="67da8-320">Поэтому WMI запрашивает повтор операции с более простыми параметрами.</span><span class="sxs-lookup"><span data-stu-id="67da8-320">WMI is therefore requested to retry the operation with simpler parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM \_ . \_ отсутствует \_ \_ идентификатор параметра**</span><span class="sxs-lookup"><span data-stu-id="67da8-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM\_E\_MISSING\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-322">2147749942 (0x80041036)</span><span class="sxs-lookup"><span data-stu-id="67da8-322">2147749942 (0x80041036)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-323">В вызове метода отсутствовал параметр.</span><span class="sxs-lookup"><span data-stu-id="67da8-323">Parameter was missing from the method call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**\_ \_ Недопустимый \_ идентификатор параметра WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM\_E\_INVALID\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-325">2147749943 (0x80041037)</span><span class="sxs-lookup"><span data-stu-id="67da8-325">2147749943 (0x80041037)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-326">Недопустимый квалификатор [**идентификатора**](standard-wmi-qualifiers.md) параметра метода.</span><span class="sxs-lookup"><span data-stu-id="67da8-326">Method parameter has an [**ID**](standard-wmi-qualifiers.md) qualifier that is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_ \_ непоследовательные \_ \_ идентификаторы параметров в WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM\_E\_NONCONSECUTIVE\_PARAMETER\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-328">2147749944 (0x80041038)</span><span class="sxs-lookup"><span data-stu-id="67da8-328">2147749944 (0x80041038)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-329">Один или несколько параметров метода имеют непоследовательные квалификаторы [**ID**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="67da8-329">One or more of the method parameters have [**ID**](standard-wmi-qualifiers.md) qualifiers that are out of sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ идентификатор параметра WBEM \_ E \_ в \_ RETVAL**</span><span class="sxs-lookup"><span data-stu-id="67da8-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM\_E\_PARAMETER\_ID\_ON\_RETVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-331">2147749945 (0x80041039)</span><span class="sxs-lookup"><span data-stu-id="67da8-331">2147749945 (0x80041039)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-332">Возвращаемое значение метода имеет квалификатор [**идентификатора**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="67da8-332">Return value for a method has an [**ID**](standard-wmi-qualifiers.md) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ Недопустимый \_ \_ путь к объекту**</span><span class="sxs-lookup"><span data-stu-id="67da8-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-334">2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="67da8-334">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-335">Указан недопустимый путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="67da8-335">Specified object path was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM. не \_ \_ хватает \_ \_ места на диске \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM\_E\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-337">2147749947 (0x8004103B)</span><span class="sxs-lookup"><span data-stu-id="67da8-337">2147749947 (0x8004103B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-338">На диске недостаточно места или достигнут предел в 4 ГБ для репозитория WMI (репозиторий CIM).</span><span class="sxs-lookup"><span data-stu-id="67da8-338">Disk is out of space or the 4 GB limit on WMI repository (CIM repository) size is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**\_буфер E \_ WBEM \_ слишком \_ мал**</span><span class="sxs-lookup"><span data-stu-id="67da8-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM\_E\_BUFFER\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-340">2147749948 (0x8004103C)</span><span class="sxs-lookup"><span data-stu-id="67da8-340">2147749948 (0x8004103C)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-341">Указанный буфер слишком мал для размещения всех объектов в перечислителе или для чтения строкового свойства.</span><span class="sxs-lookup"><span data-stu-id="67da8-341">Supplied buffer was too small to hold all of the objects in the enumerator or to read a string property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**\_ \_ неподдерживаемое \_ расширение размещения WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM\_E\_UNSUPPORTED\_PUT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-343">2147749949 (0x8004103D)</span><span class="sxs-lookup"><span data-stu-id="67da8-343">2147749949 (0x8004103D)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-344">Поставщик не поддерживает запрошенную операцию размещения.</span><span class="sxs-lookup"><span data-stu-id="67da8-344">Provider does not support the requested put operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**\_неизвестный \_ \_ тип объекта \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM\_E\_UNKNOWN\_OBJECT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-346">2147749950 (0x8004103E)</span><span class="sxs-lookup"><span data-stu-id="67da8-346">2147749950 (0x8004103E)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-347">При упаковке обнаружен объект с неверным типом или версией.</span><span class="sxs-lookup"><span data-stu-id="67da8-347">Object with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_неизвестный \_ \_ тип пакетов \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM\_E\_UNKNOWN\_PACKET\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-349">2147749951 (0x8004103F)</span><span class="sxs-lookup"><span data-stu-id="67da8-349">2147749951 (0x8004103F)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-350">При упаковке обнаружен пакет с неверным типом или версией.</span><span class="sxs-lookup"><span data-stu-id="67da8-350">Packet with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**\_несоответствие \_ версии модуля WBEM E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM\_E\_MARSHAL\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-352">2147749952 (0x80041040)</span><span class="sxs-lookup"><span data-stu-id="67da8-352">2147749952 (0x80041040)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-353">Пакет имеет неподдерживаемую версию.</span><span class="sxs-lookup"><span data-stu-id="67da8-353">Packet has an unsupported version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**\_ \_ \_ недействительная \_ подпись WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM\_E\_MARSHAL\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-355">2147749953 (0x80041041)</span><span class="sxs-lookup"><span data-stu-id="67da8-355">2147749953 (0x80041041)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-356">Вероятно, пакет поврежден.</span><span class="sxs-lookup"><span data-stu-id="67da8-356">Packet appears to be corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**\_ \_ Недопустимый \_ квалификатор WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM\_E\_INVALID\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-358">2147749954 (0x80041042)</span><span class="sxs-lookup"><span data-stu-id="67da8-358">2147749954 (0x80041042)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-359">Предпринята попытка несовпадения квалификаторов, например помещение \[ ключа \] в объект, а не свойства.</span><span class="sxs-lookup"><span data-stu-id="67da8-359">Attempt was made to mismatch qualifiers, such as putting \[key\] on an object instead of a property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**\_ \_ Недопустимый \_ дублирующийся параметр WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM\_E\_INVALID\_DUPLICATE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-361">2147749955 (0x80041043)</span><span class="sxs-lookup"><span data-stu-id="67da8-361">2147749955 (0x80041043)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-362">В методе CIM объявлен дублирующийся параметр.</span><span class="sxs-lookup"><span data-stu-id="67da8-362">Duplicate parameter was declared in a CIM method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**\_ \_ слишком \_ большой объем \_ данных в WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM\_E\_TOO\_MUCH\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-364">2147749956 (0x80041044)</span><span class="sxs-lookup"><span data-stu-id="67da8-364">2147749956 (0x80041044)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-365">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="67da8-365">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**\_сервер WBEM \_ E \_ \_ занят**</span><span class="sxs-lookup"><span data-stu-id="67da8-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM\_E\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-367">2147749957 (0x80041045)</span><span class="sxs-lookup"><span data-stu-id="67da8-367">2147749957 (0x80041045)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-368">Не удалось вызвать [**ивбемобжектсинк:: обозначение**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="67da8-368">Call to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) has failed.</span></span> <span data-ttu-id="67da8-369">Поставщик может перезапустить событие.</span><span class="sxs-lookup"><span data-stu-id="67da8-369">The provider can refire the event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**\_ \_ Недопустимый \_ флаг WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM\_E\_INVALID\_FLAVOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-371">2147749958 (0x80041046)</span><span class="sxs-lookup"><span data-stu-id="67da8-371">2147749958 (0x80041046)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-372">Указана недопустимая разновидность квалификатора.</span><span class="sxs-lookup"><span data-stu-id="67da8-372">Specified qualifier flavor was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**\_ \_ циклическая \_ ссылка на WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM\_E\_CIRCULAR\_REFERENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-374">2147749959 (0x80041047)</span><span class="sxs-lookup"><span data-stu-id="67da8-374">2147749959 (0x80041047)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-375">Предпринята попытка создать циклическую ссылку (например, производный от себя класс).</span><span class="sxs-lookup"><span data-stu-id="67da8-375">Attempt was made to create a reference that is circular (for example, deriving a class from itself).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**\_ \_ неподдерживаемое \_ обновление класса WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM\_E\_UNSUPPORTED\_CLASS\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-377">2147749960 (0x80041048)</span><span class="sxs-lookup"><span data-stu-id="67da8-377">2147749960 (0x80041048)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-378">Указанный класс не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="67da8-378">Specified class is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ е \_ не \_ может \_ изменить \_ наследование ключа**</span><span class="sxs-lookup"><span data-stu-id="67da8-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_KEY\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-380">2147749961 (0x80041049)</span><span class="sxs-lookup"><span data-stu-id="67da8-380">2147749961 (0x80041049)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-381">Предпринята попытка изменить ключ, когда в экземплярах или подклассах уже используется ключ.</span><span class="sxs-lookup"><span data-stu-id="67da8-381">Attempt was made to change a key when instances or subclasses are already using the key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ не \_ может \_ изменить \_ наследование индекса**</span><span class="sxs-lookup"><span data-stu-id="67da8-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_INDEX\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-383">2147749968 (0x80041050)</span><span class="sxs-lookup"><span data-stu-id="67da8-383">2147749968 (0x80041050)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-384">Предпринята попытка изменить индекс, если в экземплярах или подклассах уже используется индекс.</span><span class="sxs-lookup"><span data-stu-id="67da8-384">An attempt was made to change an index when instances or subclasses are already using the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**\_ \_ слишком \_ много \_ свойств WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM\_E\_TOO\_MANY\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-386">2147749969 (0x80041051)</span><span class="sxs-lookup"><span data-stu-id="67da8-386">2147749969 (0x80041051)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-387">Предпринята попытка создать больше свойств, чем поддерживается текущей версией класса.</span><span class="sxs-lookup"><span data-stu-id="67da8-387">Attempt was made to create more properties than the current version of the class supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**\_несоответствие \_ \_ типа обновления \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM\_E\_UPDATE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-389">2147749970 (0x80041052)</span><span class="sxs-lookup"><span data-stu-id="67da8-389">2147749970 (0x80041052)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-390">Свойство было переопределено с конфликтующим типом в производном классе.</span><span class="sxs-lookup"><span data-stu-id="67da8-390">Property was redefined with a conflicting type in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**\_Переопределение \_ обновления WBEM E \_ \_ не \_ разрешено**</span><span class="sxs-lookup"><span data-stu-id="67da8-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**WBEM\_E\_UPDATE\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-392">2147749971 (0x80041053)</span><span class="sxs-lookup"><span data-stu-id="67da8-392">2147749971 (0x80041053)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-393">Попытка была выполнена в производном классе для переопределения квалификатора, который не может быть переопределен.</span><span class="sxs-lookup"><span data-stu-id="67da8-393">Attempt was made in a derived class to override a qualifier that cannot be overridden.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_ \_ \_ распространяемый метод WBEM E Update \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM\_E\_UPDATE\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-395">2147749972 (0x80041054)</span><span class="sxs-lookup"><span data-stu-id="67da8-395">2147749972 (0x80041054)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-396">Метод был повторно объявлен с конфликтующей сигнатурой в производном классе.</span><span class="sxs-lookup"><span data-stu-id="67da8-396">Method was re-declared with a conflicting signature in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**\_метод WBEM \_ E \_ не \_ реализован**</span><span class="sxs-lookup"><span data-stu-id="67da8-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM\_E\_METHOD\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-398">2147749973 (0x80041055)</span><span class="sxs-lookup"><span data-stu-id="67da8-398">2147749973 (0x80041055)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-399">Предпринята попытка выполнить метод, не помеченный как \[ реализованный \] в каком-либо соответствующем классе.</span><span class="sxs-lookup"><span data-stu-id="67da8-399">Attempt was made to execute a method not marked with \[implemented\] in any relevant class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**\_метод WBEM \_ E \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="67da8-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="67da8-401"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="67da8-401"><dt>


</dt> <dt></span></span>



<span data-ttu-id="67da8-402">Предпринята попытка выполнить метод, помеченный как \[ отключенный \] .</span><span class="sxs-lookup"><span data-stu-id="67da8-402">Attempt was made to execute a method marked with \[disabled\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**Подсистема \_ \_ обновления WBEM \_ занята**</span><span class="sxs-lookup"><span data-stu-id="67da8-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM\_E\_REFRESHER\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-404">2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="67da8-404">2147749975 (0x80041057)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-405">Обновитель занят другой операцией.</span><span class="sxs-lookup"><span data-stu-id="67da8-405">Refresher is busy with another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**\_ \_ неанализируемый запрос WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM\_E\_UNPARSABLE\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-407">2147749976 (0x80041058)</span><span class="sxs-lookup"><span data-stu-id="67da8-407">2147749976 (0x80041058)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-408">Синтаксически недопустимый запрос фильтрации.</span><span class="sxs-lookup"><span data-stu-id="67da8-408">Filtering query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**\_ \_ \_ класс событий WBEM E \_ Not**</span><span class="sxs-lookup"><span data-stu-id="67da8-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM\_E\_NOT\_EVENT\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-410">2147749977 (0x80041059)</span><span class="sxs-lookup"><span data-stu-id="67da8-410">2147749977 (0x80041059)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-411">Предложение FROM запроса фильтрации ссылается на класс, который не является классом событий (производным от [**\_ \_ события**](--event.md)).</span><span class="sxs-lookup"><span data-stu-id="67da8-411">The FROM clause of a filtering query references a class that is not an event class (not derived from [**\_\_Event**](--event.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ . \_ отсутствует \_ Группа \_ в**</span><span class="sxs-lookup"><span data-stu-id="67da8-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM\_E\_MISSING\_GROUP\_WITHIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-413">2147749978 (0x8004105A)</span><span class="sxs-lookup"><span data-stu-id="67da8-413">2147749978 (0x8004105A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-414">Предложение GROUP BY использовано без соответствующего предложения GROUP WITHIN.</span><span class="sxs-lookup"><span data-stu-id="67da8-414">A GROUP BY clause was used without the corresponding GROUP WITHIN clause.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**\_ \_ отсутствует \_ список агрегирования для WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM\_E\_MISSING\_AGGREGATION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-416">2147749979 (0x8004105B)</span><span class="sxs-lookup"><span data-stu-id="67da8-416">2147749979 (0x8004105B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-417">Использовано предложение GROUP BY.</span><span class="sxs-lookup"><span data-stu-id="67da8-417">A GROUP BY clause was used.</span></span> <span data-ttu-id="67da8-418">Статистическая обработка всех свойств не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="67da8-418">Aggregation on all properties is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**\_свойство WBEM \_ E \_ не \_ является \_ объектом**</span><span class="sxs-lookup"><span data-stu-id="67da8-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM\_E\_PROPERTY\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-420">2147749980 (0x8004105C)</span><span class="sxs-lookup"><span data-stu-id="67da8-420">2147749980 (0x8004105C)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-421">Точечная нотация использована для свойства, которое не является внедренным объектом.</span><span class="sxs-lookup"><span data-stu-id="67da8-421">Dot notation was used on a property that is not an embedded object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**\_ \_ вычисление на WBEM E \_ по \_ объектам**</span><span class="sxs-lookup"><span data-stu-id="67da8-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM\_E\_AGGREGATING\_BY\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-423">2147749981 (0x8004105D)</span><span class="sxs-lookup"><span data-stu-id="67da8-423">2147749981 (0x8004105D)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-424">Предложение GROUP BY ссылается на свойство, которое является внедренным объектом, без использования точечной нотации.</span><span class="sxs-lookup"><span data-stu-id="67da8-424">A GROUP BY clause references a property that is an embedded object without using dot notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**\_ \_ неинтерпретируемый \_ запрос поставщика WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM\_E\_UNINTERPRETABLE\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-426">2147749983 (0x8004105F)</span><span class="sxs-lookup"><span data-stu-id="67da8-426">2147749983 (0x8004105F)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-427">В запросе на регистрацию поставщика событий ([**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md)) не указаны классы, для которых были предоставлены события.</span><span class="sxs-lookup"><span data-stu-id="67da8-427">Event provider registration query ([**\_\_EventProviderRegistration**](--eventproviderregistration.md)) did not specify the classes for which events were provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**\_средство WBEM E \_ BACKUP \_ RESTORE \_ \_ работает WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="67da8-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM\_E\_BACKUP\_RESTORE\_WINMGMT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-429">2147749984 (0x80041060)</span><span class="sxs-lookup"><span data-stu-id="67da8-429">2147749984 (0x80041060)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-430">Был сделан запрос на резервное копирование или восстановление репозитория во время его использования WinMgmt.exe или процессом SVCHOST, который содержит службу WMI.</span><span class="sxs-lookup"><span data-stu-id="67da8-430">Request was made to back up or restore the repository while it was in use by WinMgmt.exe, or by the SVCHOST process that contains the WMI service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**\_ \_ переполнение очереди WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM\_E\_QUEUE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-432">2147749985 (0x80041061)</span><span class="sxs-lookup"><span data-stu-id="67da8-432">2147749985 (0x80041061)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-433">Очередь асинхронной доставки переполнена из-за слишком высокой скорости работы потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="67da8-433">Asynchronous delivery queue overflowed from the event consumer being too slow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**\_ \_ отсутствуют права доступа \_ WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM\_E\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-435">2147749986 (0x80041062)</span><span class="sxs-lookup"><span data-stu-id="67da8-435">2147749986 (0x80041062)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-436">Не удалось выполнить операцию, так как клиент не имеет необходимых прав безопасности.</span><span class="sxs-lookup"><span data-stu-id="67da8-436">Operation failed because the client did not have the necessary security privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**\_ \_ Недопустимый \_ оператор WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM\_E\_INVALID\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-438">2147749987 (0x80041063)</span><span class="sxs-lookup"><span data-stu-id="67da8-438">2147749987 (0x80041063)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-439">Недопустимый оператор для этого типа свойства.</span><span class="sxs-lookup"><span data-stu-id="67da8-439">Operator is not valid for this property type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**\_ \_ локальные \_ учетные данные WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM\_E\_LOCAL\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-441">2147749988 (0x80041064)</span><span class="sxs-lookup"><span data-stu-id="67da8-441">2147749988 (0x80041064)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-442">Пользователь указал имя пользователя, пароль или центр в локальном соединении.</span><span class="sxs-lookup"><span data-stu-id="67da8-442">User specified a username/password/authority on a local connection.</span></span> <span data-ttu-id="67da8-443">Пользователь должен использовать пустое имя пользователя и пароль и зависеть от безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="67da8-443">The user must use a blank username/password and rely on default security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ не может \_ быть \_ абстрактным**</span><span class="sxs-lookup"><span data-stu-id="67da8-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM\_E\_CANNOT\_BE\_ABSTRACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-445">2147749989 (0x80041065)</span><span class="sxs-lookup"><span data-stu-id="67da8-445">2147749989 (0x80041065)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-446">Класс был создан абстрактным, если его родительский класс не является абстрактным.</span><span class="sxs-lookup"><span data-stu-id="67da8-446">Class was made abstract when its parent class is not abstract.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**\_ \_ доизмененный объект WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM\_E\_AMENDED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-448">2147749990 (0x80041066)</span><span class="sxs-lookup"><span data-stu-id="67da8-448">2147749990 (0x80041066)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-449">Измененный объект записан без **флага WBEM. указан флаг \_ \_ \_ уточненных \_ квалификаторов** .</span><span class="sxs-lookup"><span data-stu-id="67da8-449">Amended object was written without the **WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS** flag being specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**\_клиент WBEM \_ с \_ слишком \_ высокой скоростью**</span><span class="sxs-lookup"><span data-stu-id="67da8-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM\_E\_CLIENT\_TOO\_SLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-451">2147749991 (0x80041067)</span><span class="sxs-lookup"><span data-stu-id="67da8-451">2147749991 (0x80041067)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-452">Клиент не получал объекты достаточно быстро из перечисления.</span><span class="sxs-lookup"><span data-stu-id="67da8-452">Client did not retrieve objects quickly enough from an enumeration.</span></span> <span data-ttu-id="67da8-453">Эта константа возвращается, когда клиент создает объект перечисления, но не извлекает объекты из перечислителя в течение отведенного времени, что приводит к резервному копированию кэша объектов перечислителя.</span><span class="sxs-lookup"><span data-stu-id="67da8-453">This constant is returned when a client creates an enumeration object, but does not retrieve objects from the enumerator in a timely fashion, causing the enumerator's object caches to back up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**\_ \_ нулевой \_ дескриптор безопасности \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM\_E\_NULL\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-455">2147749992 (0x80041068)</span><span class="sxs-lookup"><span data-stu-id="67da8-455">2147749992 (0x80041068)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-456">Использован дескриптор безопасности со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="67da8-456">Null security descriptor was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**\_ \_ время \_ ожидания WBEM истекло**</span><span class="sxs-lookup"><span data-stu-id="67da8-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM\_E\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-458">2147749993 (0x80041069)</span><span class="sxs-lookup"><span data-stu-id="67da8-458">2147749993 (0x80041069)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-459">Время ожидания операции истекло.</span><span class="sxs-lookup"><span data-stu-id="67da8-459">Operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**\_ \_ недействительная \_ Ассоциация WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM\_E\_INVALID\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-461">2147749994</span><span class="sxs-lookup"><span data-stu-id="67da8-461">2147749994</span></span>
</dt> <dt>



<span data-ttu-id="67da8-462">Недопустимая связь.</span><span class="sxs-lookup"><span data-stu-id="67da8-462">Association is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**\_ \_ неоднозначная \_ операция в WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM\_E\_AMBIGUOUS\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-464">2147749995 (0x8004106B)</span><span class="sxs-lookup"><span data-stu-id="67da8-464">2147749995 (0x8004106B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-465">Операция была неоднозначным.</span><span class="sxs-lookup"><span data-stu-id="67da8-465">Operation was ambiguous.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_ \_ нарушение квоты WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM\_E\_QUOTA\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-467">2147749996 (0x8004106C)</span><span class="sxs-lookup"><span data-stu-id="67da8-467">2147749996 (0x8004106C)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-468">Инструментарий WMI занимает слишком много памяти.</span><span class="sxs-lookup"><span data-stu-id="67da8-468">WMI is taking up too much memory.</span></span> <span data-ttu-id="67da8-469">Это может быть вызвано недостатком доступности памяти или чрезмерным потреблением памяти системой WMI.</span><span class="sxs-lookup"><span data-stu-id="67da8-469">This can be caused by low memory availability or excessive memory consumption by WMI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**\_ \_ конфликт транзакции WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM\_E\_TRANSACTION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-471">2147749997 (0x8004106D)</span><span class="sxs-lookup"><span data-stu-id="67da8-471">2147749997 (0x8004106D)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-472">Операция привела к конфликту транзакций.</span><span class="sxs-lookup"><span data-stu-id="67da8-472">Operation resulted in a transaction conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**\_ \_ принудительный \_ откат от WBEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM\_E\_FORCED\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-474">2147749998 (0x8004106E)</span><span class="sxs-lookup"><span data-stu-id="67da8-474">2147749998 (0x8004106E)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-475">Транзакция вынуждена выполнить откат.</span><span class="sxs-lookup"><span data-stu-id="67da8-475">Transaction forced a rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**\_ \_ неподдерживаемый \_ языковой стандарт WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM\_E\_UNSUPPORTED\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-477">2147749999 (0x8004106F)</span><span class="sxs-lookup"><span data-stu-id="67da8-477">2147749999 (0x8004106F)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-478">Языковой стандарт, используемый в вызове, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="67da8-478">Locale used in the call is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**неактуальный \_ \_ маркер WBEM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM\_E\_HANDLE\_OUT\_OF\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-480">2147750000 (0x80041070)</span><span class="sxs-lookup"><span data-stu-id="67da8-480">2147750000 (0x80041070)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-481">Неактуальный объектный обработчик.</span><span class="sxs-lookup"><span data-stu-id="67da8-481">Object handle is out-of-date.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**\_ \_ не удалось подключиться к WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM\_E\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-483">2147750001 (0x80041071)</span><span class="sxs-lookup"><span data-stu-id="67da8-483">2147750001 (0x80041071)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-484">Не удалось подключиться к базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="67da8-484">Connection to the SQL database failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**\_ \_ Недопустимый \_ запрос маркера WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM\_E\_INVALID\_HANDLE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-486">2147750002 (0x80041072)</span><span class="sxs-lookup"><span data-stu-id="67da8-486">2147750002 (0x80041072)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-487">Запрос на обработку недопустим.</span><span class="sxs-lookup"><span data-stu-id="67da8-487">Handle request was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**\_ \_ \_ \_ слишком длинное имя свойства \_ WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM\_E\_PROPERTY\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-489">2147750003 (0x80041073)</span><span class="sxs-lookup"><span data-stu-id="67da8-489">2147750003 (0x80041073)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-490">Имя свойства содержит более 255 символов.</span><span class="sxs-lookup"><span data-stu-id="67da8-490">Property name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**\_ \_ имя класса WBEM \_ E \_ слишком \_ длинное**</span><span class="sxs-lookup"><span data-stu-id="67da8-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM\_E\_CLASS\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-492">2147750004 (0x80041074)</span><span class="sxs-lookup"><span data-stu-id="67da8-492">2147750004 (0x80041074)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-493">Имя класса содержит более 255 символов.</span><span class="sxs-lookup"><span data-stu-id="67da8-493">Class name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**\_ \_ \_ \_ слишком длинное имя метода \_ WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM\_E\_METHOD\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-495">2147750005 (0x80041075)</span><span class="sxs-lookup"><span data-stu-id="67da8-495">2147750005 (0x80041075)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-496">Имя метода содержит более 255 символов.</span><span class="sxs-lookup"><span data-stu-id="67da8-496">Method name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**\_ \_ \_ \_ слишком длинное имя квалификатора \_ WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM\_E\_QUALIFIER\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-498">2147750006 (0x80041076)</span><span class="sxs-lookup"><span data-stu-id="67da8-498">2147750006 (0x80041076)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-499">Имя квалификатора содержит более 255 символов.</span><span class="sxs-lookup"><span data-stu-id="67da8-499">Qualifier name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**\_команда WBEM E \_ повторного выполнения \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM\_E\_RERUN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-501">2147750007 (0x80041077)</span><span class="sxs-lookup"><span data-stu-id="67da8-501">2147750007 (0x80041077)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-502">Команда SQL должна быть перезапущена, так как в SQL есть взаимоблокировка.</span><span class="sxs-lookup"><span data-stu-id="67da8-502">The SQL command must be rerun because there is a deadlock in SQL.</span></span> <span data-ttu-id="67da8-503">Это может быть возвращено только в том случае, если данные хранятся в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="67da8-503">This can be returned only when data is being stored in an SQL database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**несоответствие версии WBEM \_ E \_ Database \_ ver \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM\_E\_DATABASE\_VER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-505">2147750008 (0x80041078)</span><span class="sxs-lookup"><span data-stu-id="67da8-505">2147750008 (0x80041078)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-506">Версия базы данных не соответствует версии, которая обрабатывается драйвером репозитория.</span><span class="sxs-lookup"><span data-stu-id="67da8-506">The database version does not match the version that the repository driver processes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**\_ \_ Удаление запрета на WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM\_E\_VETO\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-508">2147750009 (0x80041079)</span><span class="sxs-lookup"><span data-stu-id="67da8-508">2147750009 (0x80041079)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-509">Инструментарию WMI не удается выполнить операцию удаления, так как он не разрешен поставщиком.</span><span class="sxs-lookup"><span data-stu-id="67da8-509">WMI cannot execute the delete operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**\_ \_ расстановка ЗАПРЕТов WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM\_E\_VETO\_PUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-511">2147750010 (0x8004107A)</span><span class="sxs-lookup"><span data-stu-id="67da8-511">2147750010 (0x8004107A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-512">Инструментарию WMI не удается выполнить операцию размещения, поскольку он не разрешен поставщиком.</span><span class="sxs-lookup"><span data-stu-id="67da8-512">WMI cannot execute the put operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**\_ \_ Недопустимый \_ языковой стандарт WBEM E**</span><span class="sxs-lookup"><span data-stu-id="67da8-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM\_E\_INVALID\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-514">2147750016 (0x80041080)</span><span class="sxs-lookup"><span data-stu-id="67da8-514">2147750016 (0x80041080)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-515">Указанный идентификатор локали недопустим для операции.</span><span class="sxs-lookup"><span data-stu-id="67da8-515">Specified locale identifier was not valid for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**\_поставщик WBEM \_ E \_ приостановлен**</span><span class="sxs-lookup"><span data-stu-id="67da8-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM\_E\_PROVIDER\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-517">2147750017 (0x80041081)</span><span class="sxs-lookup"><span data-stu-id="67da8-517">2147750017 (0x80041081)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-518">Поставщик приостановлен.</span><span class="sxs-lookup"><span data-stu-id="67da8-518">Provider is suspended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**\_ \_ требуется синхронизация WBEM \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM\_E\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-520">2147750018 (0x80041082)</span><span class="sxs-lookup"><span data-stu-id="67da8-520">2147750018 (0x80041082)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-521">Объект должен быть записан в репозиторий WMI и повторно извлечен до того, как запрошенная операция может быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="67da8-521">Object must be written to the WMI repository and retrieved again before the requested operation can succeed.</span></span> <span data-ttu-id="67da8-522">Эта константа возвращается, когда объект должен быть зафиксирован и получен для просмотра значения свойства.</span><span class="sxs-lookup"><span data-stu-id="67da8-522">This constant is returned when an object must be committed and retrieved to see the property value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ \_ No \_ схема**</span><span class="sxs-lookup"><span data-stu-id="67da8-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM\_E\_NO\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-524">2147750019 (0x80041083)</span><span class="sxs-lookup"><span data-stu-id="67da8-524">2147750019 (0x80041083)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-525">Не удается завершить операцию; нет доступных схем.</span><span class="sxs-lookup"><span data-stu-id="67da8-525">Operation cannot be completed; no schema is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**\_поставщик WBEM \_ E \_ уже \_ зарегистрирован**</span><span class="sxs-lookup"><span data-stu-id="67da8-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**WBEM\_E\_PROVIDER\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-527">02147750020 (0x119FD010)</span><span class="sxs-lookup"><span data-stu-id="67da8-527">02147750020 (0x119FD010)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-528">Поставщик не может быть зарегистрирован, так как он уже зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="67da8-528">Provider cannot be registered because it is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**\_поставщик WBEM \_ E \_ не \_ зарегистрирован**</span><span class="sxs-lookup"><span data-stu-id="67da8-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM\_E\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-530">2147750021 (0x80041085)</span><span class="sxs-lookup"><span data-stu-id="67da8-530">2147750021 (0x80041085)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-531">Поставщик не зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="67da8-531">Provider was not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**\_ \_ Неустранимая \_ ошибка транспорта WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM\_E\_FATAL\_TRANSPORT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-533">2147750022 (0x80041086)</span><span class="sxs-lookup"><span data-stu-id="67da8-533">2147750022 (0x80041086)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-534">Произошла неустранимая ошибка транспорта.</span><span class="sxs-lookup"><span data-stu-id="67da8-534">A fatal transport error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**\_ \_ требуется зашифрованное \_ Подключение WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-536">2147750023 (0x80041087)</span><span class="sxs-lookup"><span data-stu-id="67da8-536">2147750023 (0x80041087)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-537">Пользователь попытался задать имя компьютера или домена без зашифрованного соединения.</span><span class="sxs-lookup"><span data-stu-id="67da8-537">User attempted to set a computer name or domain without an encrypted connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**\_ \_ \_ истекло время ожидания поставщика WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**WBEM\_E\_PROVIDER\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-539">2147750024 (0x80041088)</span><span class="sxs-lookup"><span data-stu-id="67da8-539">2147750024 (0x80041088)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-540">Поставщику не удалось сообщить о результатах в течение указанного времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="67da8-540">A provider failed to report results within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ , \_ без \_ ключа**</span><span class="sxs-lookup"><span data-stu-id="67da8-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM\_E\_NO\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-542">2147750025 (0x80041089)</span><span class="sxs-lookup"><span data-stu-id="67da8-542">2147750025 (0x80041089)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-543">Пользователь попытался разместить экземпляр без определенного ключа.</span><span class="sxs-lookup"><span data-stu-id="67da8-543">User attempted to put an instance with no defined key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_поставщик WBEM \_ E \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="67da8-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM\_E\_PROVIDER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-545">2147750026 (0x8004108A)</span><span class="sxs-lookup"><span data-stu-id="67da8-545">2147750026 (0x8004108A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-546">Пользователь попытался зарегистрировать экземпляр поставщика, но COM-сервер для экземпляра поставщика был выгружен.</span><span class="sxs-lookup"><span data-stu-id="67da8-546">User attempted to register a provider instance but the COM server for the provider instance was unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**\_ \_ \_ слишком \_ широкая вбемессная регистрация**</span><span class="sxs-lookup"><span data-stu-id="67da8-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-548">2147753985 (0x80042001)</span><span class="sxs-lookup"><span data-stu-id="67da8-548">2147753985 (0x80042001)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-549">Регистрация поставщика перекрывается с доменом системных событий.</span><span class="sxs-lookup"><span data-stu-id="67da8-549">Provider registration overlaps with the system event domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**\_ \_ \_ слишком \_ точная регистрация вбемесс E**</span><span class="sxs-lookup"><span data-stu-id="67da8-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_PRECISE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-551">2147753986 (0x80042002)</span><span class="sxs-lookup"><span data-stu-id="67da8-551">2147753986 (0x80042002)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-552">Предложение WITHIN в этом запросе не использовалось.</span><span class="sxs-lookup"><span data-stu-id="67da8-552">A WITHIN clause was not used in this query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**ВБЕМЕСС \_ E \_ \_ не является \_ привилегированным**</span><span class="sxs-lookup"><span data-stu-id="67da8-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS\_E\_AUTHZ\_NOT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-554">2147753987 (0x80042003)</span><span class="sxs-lookup"><span data-stu-id="67da8-554">2147753987 (0x80042003)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-555">У этого компьютера нет необходимых разрешений на доступ к домену для поддержки функций безопасности, связанных с созданным экземпляром подписки.</span><span class="sxs-lookup"><span data-stu-id="67da8-555">This computer does not have the necessary domain permissions to support the security functions that relate to the created subscription instance.</span></span> <span data-ttu-id="67da8-556">Обратитесь к администратору домена, чтобы добавить этот компьютер в группу авторизации доступа Windows.</span><span class="sxs-lookup"><span data-stu-id="67da8-556">Contact the Domain Administrator to get this computer added to the Windows Authorization Access Group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ , \_ Повторная попытка \_ позже**</span><span class="sxs-lookup"><span data-stu-id="67da8-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM\_E\_RETRY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-558">2147758081 (0x80043001)</span><span class="sxs-lookup"><span data-stu-id="67da8-558">2147758081 (0x80043001)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-559">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="67da8-559">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**\_ \_ состязание за ресурсы WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM\_E\_RESOURCE\_CONTENTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-561">2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="67da8-561">2147758082 (0x80043002)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-562">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="67da8-562">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**ВБЕММОФ \_ E \_ ожидаемое \_ имя квалификатора \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF\_E\_EXPECTED\_QUALIFIER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-564">2147762177 (0x80044001)</span><span class="sxs-lookup"><span data-stu-id="67da8-564">2147762177 (0x80044001)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-565">Требуется имя квалификатора.</span><span class="sxs-lookup"><span data-stu-id="67da8-565">Expected a qualifier name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**\_ \_ Ожидаемый вбеммоф \_ E**</span><span class="sxs-lookup"><span data-stu-id="67da8-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF\_E\_EXPECTED\_SEMI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-567">2147762178 (0x80044002)</span><span class="sxs-lookup"><span data-stu-id="67da8-567">2147762178 (0x80044002)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-568">Ожидается точка с запятой или "=".</span><span class="sxs-lookup"><span data-stu-id="67da8-568">Expected semicolon or '='.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**ВБЕММОФ \_ E \_ ожидаемая \_ открывающая \_ фигурная скобка**</span><span class="sxs-lookup"><span data-stu-id="67da8-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-570">2147762179 (0x80044003)</span><span class="sxs-lookup"><span data-stu-id="67da8-570">2147762179 (0x80044003)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-571">Ожидалась открывающая фигурная скобка.</span><span class="sxs-lookup"><span data-stu-id="67da8-571">Expected an opening brace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**ВБЕММОФ \_ E \_ ожидалась \_ закрывающая \_ фигурная скобка**</span><span class="sxs-lookup"><span data-stu-id="67da8-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-573">2147762180 (0x80044004)</span><span class="sxs-lookup"><span data-stu-id="67da8-573">2147762180 (0x80044004)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-574">Отсутствует закрывающая фигурная скобка или недопустимый элемент массива.</span><span class="sxs-lookup"><span data-stu-id="67da8-574">Missing closing brace or an illegal array element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**ВБЕММОФ \_ E \_ ожидаемая \_ закрывающая \_ скобка**</span><span class="sxs-lookup"><span data-stu-id="67da8-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-576">2147762181 (0x80044005)</span><span class="sxs-lookup"><span data-stu-id="67da8-576">2147762181 (0x80044005)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-577">Ожидается закрывающая скобка.</span><span class="sxs-lookup"><span data-stu-id="67da8-577">Expected a closing bracket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**ВБЕММОФ \_ E \_ ожидаемая \_ закрывающая \_ скобка**</span><span class="sxs-lookup"><span data-stu-id="67da8-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-579">2147762182 (0x80044006)</span><span class="sxs-lookup"><span data-stu-id="67da8-579">2147762182 (0x80044006)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-580">Требуется закрывающая круглая скобка.</span><span class="sxs-lookup"><span data-stu-id="67da8-580">Expected closing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**ВБЕММОФ \_ E \_ недопустимое \_ постоянное \_ значение**</span><span class="sxs-lookup"><span data-stu-id="67da8-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF\_E\_ILLEGAL\_CONSTANT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-582">2147762183 (0x80044007)</span><span class="sxs-lookup"><span data-stu-id="67da8-582">2147762183 (0x80044007)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-583">Числовое значение за пределами диапазона или строк без кавычек.</span><span class="sxs-lookup"><span data-stu-id="67da8-583">Numeric value out of range or strings without quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**\_ \_ Ожидаемый \_ идентификатор типа вбеммоф E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF\_E\_EXPECTED\_TYPE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-585">2147762184 (0x80044008)</span><span class="sxs-lookup"><span data-stu-id="67da8-585">2147762184 (0x80044008)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-586">Требуется идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="67da8-586">Expected a type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**\_ \_ ожидаемая \_ открытая \_ скобка вбеммоф E**</span><span class="sxs-lookup"><span data-stu-id="67da8-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-588">2147762185 (0x80044009)</span><span class="sxs-lookup"><span data-stu-id="67da8-588">2147762185 (0x80044009)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-589">Ожидается открывающая скобка.</span><span class="sxs-lookup"><span data-stu-id="67da8-589">Expected an open parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**ВБЕММОФ \_ E \_ нераспознанный \_ токен**</span><span class="sxs-lookup"><span data-stu-id="67da8-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-591">2147762186 (0x8004400A)</span><span class="sxs-lookup"><span data-stu-id="67da8-591">2147762186 (0x8004400A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-592">Непредвиденный токен в файле.</span><span class="sxs-lookup"><span data-stu-id="67da8-592">Unexpected token in the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**ВБЕММОФ \_ E \_ нераспознанный \_ тип**</span><span class="sxs-lookup"><span data-stu-id="67da8-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-594">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="67da8-594">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-595">Нераспознанный или неподдерживаемый идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="67da8-595">Unrecognized or unsupported type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**ВБЕММОФ \_ E \_ ожидаемое \_ \_ имя свойства**</span><span class="sxs-lookup"><span data-stu-id="67da8-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF\_E\_EXPECTED\_PROPERTY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-597">2147762187 (0x8004400B)</span><span class="sxs-lookup"><span data-stu-id="67da8-597">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-598">Требуется имя свойства или метода.</span><span class="sxs-lookup"><span data-stu-id="67da8-598">Expected property or method name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**ВБЕММОФ \_ E \_ TYPEDEF \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="67da8-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF\_E\_TYPEDEF\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-600">2147762189 (0x8004400D)</span><span class="sxs-lookup"><span data-stu-id="67da8-600">2147762189 (0x8004400D)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-601">Определения типов и перечислимые типы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="67da8-601">Typedefs and enumerated types are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**\_ \_ непредвиденный псевдоним вбеммоф E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF\_E\_UNEXPECTED\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-603">2147762190 (0x8004400E)</span><span class="sxs-lookup"><span data-stu-id="67da8-603">2147762190 (0x8004400E)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-604">Только ссылка на объект класса может иметь значение псевдонима.</span><span class="sxs-lookup"><span data-stu-id="67da8-604">Only a reference to a class object can have an alias value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**ВБЕММОФ \_ E \_ непредвиденная \_ \_ Инициализация массива**</span><span class="sxs-lookup"><span data-stu-id="67da8-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF\_E\_UNEXPECTED\_ARRAY\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-606">2147762191 (0x8004400F)</span><span class="sxs-lookup"><span data-stu-id="67da8-606">2147762191 (0x8004400F)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-607">Непредвиденная инициализация массива.</span><span class="sxs-lookup"><span data-stu-id="67da8-607">Unexpected array initialization.</span></span> <span data-ttu-id="67da8-608">Массивы должны быть объявлены с помощью \[ \] .</span><span class="sxs-lookup"><span data-stu-id="67da8-608">Arrays must be declared with \[\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ \_ синтаксис прав**</span><span class="sxs-lookup"><span data-stu-id="67da8-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF\_E\_INVALID\_AMENDMENT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-610">2147762192 (0x80044010)</span><span class="sxs-lookup"><span data-stu-id="67da8-610">2147762192 (0x80044010)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-611">Недопустимый синтаксис пути к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="67da8-611">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ дубликат \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF\_E\_INVALID\_DUPLICATE\_AMENDMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-613">2147762193 (0x80044011)</span><span class="sxs-lookup"><span data-stu-id="67da8-613">2147762193 (0x80044011)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-614">Дублирующиеся описатели прав.</span><span class="sxs-lookup"><span data-stu-id="67da8-614">Duplicate amendment specifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**ВБЕММОФ \_ E \_ Недопустимая \_ директива pragma**</span><span class="sxs-lookup"><span data-stu-id="67da8-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF\_E\_INVALID\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-616">2147762194 (0x80044012)</span><span class="sxs-lookup"><span data-stu-id="67da8-616">2147762194 (0x80044012)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-617">После [ \# директивы pragma](pragma-namespace.md) должно следовать допустимое ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="67da8-617">[\#pragma](pragma-namespace.md) must be followed by a valid keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ синтаксис пространства имен \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-619">2147762195 (0x80044013)</span><span class="sxs-lookup"><span data-stu-id="67da8-619">2147762195 (0x80044013)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-620">Недопустимый синтаксис пути к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="67da8-620">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**ВБЕММОФ \_ E \_ ожидаемое \_ \_ имя класса**</span><span class="sxs-lookup"><span data-stu-id="67da8-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF\_E\_EXPECTED\_CLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-622">2147762196 (0x80044014)</span><span class="sxs-lookup"><span data-stu-id="67da8-622">2147762196 (0x80044014)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-623">Непредвиденный символ в имени класса должен быть идентификатором.</span><span class="sxs-lookup"><span data-stu-id="67da8-623">Unexpected character in class name must be an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**\_несоответствие \_ типов вбеммоф E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-625">2147762197 (0x80044015)</span><span class="sxs-lookup"><span data-stu-id="67da8-625">2147762197 (0x80044015)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-626">Указанное значение не может быть выполнено в соответствующий тип.</span><span class="sxs-lookup"><span data-stu-id="67da8-626">The value specified cannot be made into the appropriate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**ВБЕММОФ \_ E \_ ожидаемое \_ имя псевдонима \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF\_E\_EXPECTED\_ALIAS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-628">2147762198 (0x80044016)</span><span class="sxs-lookup"><span data-stu-id="67da8-628">2147762198 (0x80044016)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-629">За знаком доллара должно следовать имя псевдонима в качестве идентификатора.</span><span class="sxs-lookup"><span data-stu-id="67da8-629">Dollar sign must be followed by an alias name as an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**ВБЕММОФ \_ E \_ недопустимое \_ \_ объявление класса**</span><span class="sxs-lookup"><span data-stu-id="67da8-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF\_E\_INVALID\_CLASS\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-631">2147762199 (0x80044017)</span><span class="sxs-lookup"><span data-stu-id="67da8-631">2147762199 (0x80044017)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-632">Недопустимое объявление класса.</span><span class="sxs-lookup"><span data-stu-id="67da8-632">Class declaration is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**ВБЕММОФ \_ E \_ недопустимое \_ \_ объявление экземпляра**</span><span class="sxs-lookup"><span data-stu-id="67da8-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF\_E\_INVALID\_INSTANCE\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-634">2147762200 (0x80044018)</span><span class="sxs-lookup"><span data-stu-id="67da8-634">2147762200 (0x80044018)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-635">Недопустимое объявление экземпляра.</span><span class="sxs-lookup"><span data-stu-id="67da8-635">The instance declaration is not valid.</span></span> <span data-ttu-id="67da8-636">Оно должно начинаться с "экземпляр"</span><span class="sxs-lookup"><span data-stu-id="67da8-636">It must start with "instance of"</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**\_ \_ Ожидаемый доллар вбеммоф E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF\_E\_EXPECTED\_DOLLAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-638">2147762201 (0x80044019)</span><span class="sxs-lookup"><span data-stu-id="67da8-638">2147762201 (0x80044019)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-639">Ожидаемый знак доллара.</span><span class="sxs-lookup"><span data-stu-id="67da8-639">Expected dollar sign.</span></span> <span data-ttu-id="67da8-640">Псевдоним в формате "$name" должен следовать за ключевым словом "AS".</span><span class="sxs-lookup"><span data-stu-id="67da8-640">An alias in the form "$name" must follow the "as" keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**\_КВАЛИФИКАТОР вбеммоф E \_ Цимтипе \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF\_E\_CIMTYPE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-642">2147762202 (0x8004401A)</span><span class="sxs-lookup"><span data-stu-id="67da8-642">2147762202 (0x8004401A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-643">Квалификатор "ЦИМТИПЕ" не может быть указан непосредственно в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="67da8-643">"CIMTYPE" qualifier cannot be specified directly in a MOF file.</span></span> <span data-ttu-id="67da8-644">Используйте нотацию стандартного типа.</span><span class="sxs-lookup"><span data-stu-id="67da8-644">Use standard type notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**ВБЕММОФ \_ E, \_ повторяющееся \_ свойство**</span><span class="sxs-lookup"><span data-stu-id="67da8-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF\_E\_DUPLICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-646">2147762203 (0x8004401B)</span><span class="sxs-lookup"><span data-stu-id="67da8-646">2147762203 (0x8004401B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-647">В MOF обнаружено повторяющееся имя свойства.</span><span class="sxs-lookup"><span data-stu-id="67da8-647">Duplicate property name was found in the MOF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**ВБЕММОФ \_ E \_ Недопустимая \_ Спецификация пространства имен \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-649">2147762204 (0x8004401C)</span><span class="sxs-lookup"><span data-stu-id="67da8-649">2147762204 (0x8004401C)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-650">Недопустимый синтаксис пространства имен.</span><span class="sxs-lookup"><span data-stu-id="67da8-650">Namespace syntax is not valid.</span></span> <span data-ttu-id="67da8-651">Ссылки на другие серверы не допускаются.</span><span class="sxs-lookup"><span data-stu-id="67da8-651">References to other servers are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**ВБЕММОФ \_ \_ за пределами \_ \_ диапазона**</span><span class="sxs-lookup"><span data-stu-id="67da8-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF\_E\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-653">2147762205 (0x8004401D)</span><span class="sxs-lookup"><span data-stu-id="67da8-653">2147762205 (0x8004401D)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-654">Значение вне допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="67da8-654">Value out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ файл**</span><span class="sxs-lookup"><span data-stu-id="67da8-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF\_E\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-656">2147762206 (0x8004401E)</span><span class="sxs-lookup"><span data-stu-id="67da8-656">2147762206 (0x8004401E)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-657">Файл не является допустимым текстовым MOF-файлом или двоичным MOF-файлом.</span><span class="sxs-lookup"><span data-stu-id="67da8-657">The file is not a valid text MOF file or binary MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**\_ \_ встроенные псевдонимы вбеммоф E \_ \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF\_E\_ALIASES\_IN\_EMBEDDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-659">2147762207 (0x8004401F)</span><span class="sxs-lookup"><span data-stu-id="67da8-659">2147762207 (0x8004401F)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-660">Внедренные объекты не могут быть псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="67da8-660">Embedded objects cannot be aliases.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**ВБЕММОФ \_ \_ массив значений NULL E \_ \_ ELEM**</span><span class="sxs-lookup"><span data-stu-id="67da8-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF\_E\_NULL\_ARRAY\_ELEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-662">2147762208 (0x80044020)</span><span class="sxs-lookup"><span data-stu-id="67da8-662">2147762208 (0x80044020)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-663">Элементы NULL в массиве не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="67da8-663">NULL elements in an array are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**ВБЕММОФный \_ \_ квалификатор дубликата \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF\_E\_DUPLICATE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-665">2147762209 (0x80044021)</span><span class="sxs-lookup"><span data-stu-id="67da8-665">2147762209 (0x80044021)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-666">Квалификатор использовался более одного раза для объекта.</span><span class="sxs-lookup"><span data-stu-id="67da8-666">Qualifier was used more than once on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**\_ \_ Ожидаемый \_ Тип флага вбеммоф E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF\_E\_EXPECTED\_FLAVOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-668">2147762210 (0x80044022)</span><span class="sxs-lookup"><span data-stu-id="67da8-668">2147762210 (0x80044022)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-669">Ожидался тип разновидности, например **тоинстанце**, **ToSubClass**, **енаблеоверриде** или **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="67da8-669">Expected a flavor type such as **ToInstance**, **ToSubClass**, **EnableOverride**, or **DisableOverride**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**\_ \_ несовместимые \_ типы разновидностей вбеммоф E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-671">2147762211 (0x80044023)</span><span class="sxs-lookup"><span data-stu-id="67da8-671">2147762211 (0x80044023)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-672">Объединение **енаблеоверриде** и **DisableOverride** с одним и тем же квалификатором не допускается.</span><span class="sxs-lookup"><span data-stu-id="67da8-672">Combining **EnableOverride** and **DisableOverride** on same qualifier is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**ВБЕММОФ \_ E \_ несколько \_ псевдонимов**</span><span class="sxs-lookup"><span data-stu-id="67da8-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF\_E\_MULTIPLE\_ALIASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-674">2147762212 (0x80044024)</span><span class="sxs-lookup"><span data-stu-id="67da8-674">2147762212 (0x80044024)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-675">Псевдоним нельзя использовать дважды.</span><span class="sxs-lookup"><span data-stu-id="67da8-675">An alias cannot be used twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**ВБЕММОФ \_ E \_ несовместимая \_ разновидность \_ TYPES2**</span><span class="sxs-lookup"><span data-stu-id="67da8-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-677">2147762213 (0x80044025)</span><span class="sxs-lookup"><span data-stu-id="67da8-677">2147762213 (0x80044025)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-678">Сочетание **ограничений Restricted**, **тоинстанце** и **ToSubClass** не допускается.</span><span class="sxs-lookup"><span data-stu-id="67da8-678">Combining **Restricted**, and **ToInstance** or **ToSubClass** is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**ВБЕММОФ \_ е \_ нет \_ \_ возвращенных массивов**</span><span class="sxs-lookup"><span data-stu-id="67da8-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF\_E\_NO\_ARRAYS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-680">2147762214 (0x80044026)</span><span class="sxs-lookup"><span data-stu-id="67da8-680">2147762214 (0x80044026)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-681">Методы не могут возвращать значения массива.</span><span class="sxs-lookup"><span data-stu-id="67da8-681">Methods cannot return array values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**ВБЕММОФ \_ E \_ должен \_ быть \_ in \_ или \_ out**</span><span class="sxs-lookup"><span data-stu-id="67da8-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF\_E\_MUST\_BE\_IN\_OR\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-683">2147762215 (0x80044027)</span><span class="sxs-lookup"><span data-stu-id="67da8-683">2147762215 (0x80044027)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-684">Аргументы должны иметь квалификатор **in** или **out** .</span><span class="sxs-lookup"><span data-stu-id="67da8-684">Arguments must have an **In** or **Out** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**\_ \_ Недопустимый \_ синтаксис флагов вбеммоф E \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF\_E\_INVALID\_FLAGS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-686">2147762216 (0x80044028)</span><span class="sxs-lookup"><span data-stu-id="67da8-686">2147762216 (0x80044028)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-687">Недопустимый синтаксис flags.</span><span class="sxs-lookup"><span data-stu-id="67da8-687">Flags syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**ВБЕММОФ \_ E \_ , ожидаемая \_ скобка \_ или \_ неверный \_ тип**</span><span class="sxs-lookup"><span data-stu-id="67da8-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF\_E\_EXPECTED\_BRACE\_OR\_BAD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-689">2147762217 (0x80044029)</span><span class="sxs-lookup"><span data-stu-id="67da8-689">2147762217 (0x80044029)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-690">Отсутствует последняя фигурная скобка и точка с запятой для класса.</span><span class="sxs-lookup"><span data-stu-id="67da8-690">The final brace and semi-colon for a class are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**ВБЕММОФ \_ E \_ неподдерживаемое \_ \_ значение CIMV22 куал \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_QUAL\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-692">2147762218 (0x8004402A)</span><span class="sxs-lookup"><span data-stu-id="67da8-692">2147762218 (0x8004402A)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-693">Функция CIM версии 2,2 не поддерживается для значения квалификатора.</span><span class="sxs-lookup"><span data-stu-id="67da8-693">A CIM version 2.2 feature is not supported for a qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**ВБЕММОФ \_ E \_ неподдерживаемый \_ \_ тип данных \_ CIMV22**</span><span class="sxs-lookup"><span data-stu-id="67da8-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_DATA\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-695">2147762219 (0x8004402B)</span><span class="sxs-lookup"><span data-stu-id="67da8-695">2147762219 (0x8004402B)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-696">Тип данных CIM версии 2,2 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="67da8-696">The CIM version 2.2 data type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ \_ синтаксис DELETEINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="67da8-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETEINSTANCE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-698">2147762220 (0x8004402C)</span><span class="sxs-lookup"><span data-stu-id="67da8-698">2147762220 (0x8004402C)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-699">Недопустимый синтаксис удаления экземпляра.</span><span class="sxs-lookup"><span data-stu-id="67da8-699">The delete instance syntax is not valid.</span></span> <span data-ttu-id="67da8-700">Оно должно быть `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span><span class="sxs-lookup"><span data-stu-id="67da8-700">It should be `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ синтаксис квалификатора \_**</span><span class="sxs-lookup"><span data-stu-id="67da8-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF\_E\_INVALID\_QUALIFIER\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-702">2147762221 (0x8004402D)</span><span class="sxs-lookup"><span data-stu-id="67da8-702">2147762221 (0x8004402D)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-703">Недопустимый синтаксис квалификатора.</span><span class="sxs-lookup"><span data-stu-id="67da8-703">The qualifier syntax is not valid.</span></span> <span data-ttu-id="67da8-704">Вместо этого она должна иметь вид `qualifiername:type=value,scope(class|instance), flavorname`.</span><span class="sxs-lookup"><span data-stu-id="67da8-704">It should be `qualifiername:type=value,scope(class|instance), flavorname`.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_КВАЛИФИКАТОР вбеммоф E \_ \_ используется \_ вне \_ области видимости**</span><span class="sxs-lookup"><span data-stu-id="67da8-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**WBEMMOF\_E\_QUALIFIER\_USED\_OUTSIDE\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-706">2147762222 (0x8004402E)</span><span class="sxs-lookup"><span data-stu-id="67da8-706">2147762222 (0x8004402E)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-707">Квалификатор используется за пределами области действия.</span><span class="sxs-lookup"><span data-stu-id="67da8-707">The qualifier is used outside of its scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**ВБЕММОФ \_ E \_ Ошибка \_ создания \_ временного \_ файла**</span><span class="sxs-lookup"><span data-stu-id="67da8-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF\_E\_ERROR\_CREATING\_TEMP\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-709">2147762223 (0x8004402F)</span><span class="sxs-lookup"><span data-stu-id="67da8-709">2147762223 (0x8004402F)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-710">Ошибка при создании временного файла.</span><span class="sxs-lookup"><span data-stu-id="67da8-710">Error creating temporary file.</span></span> <span data-ttu-id="67da8-711">Временный файл является промежуточным этапом в компиляции MOF.</span><span class="sxs-lookup"><span data-stu-id="67da8-711">The temporary file is an intermediate stage in the MOF compilation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**\_Ошибка вбеммоф \_ E \_ : недопустимый \_ включаемый \_ файл**</span><span class="sxs-lookup"><span data-stu-id="67da8-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF\_E\_ERROR\_INVALID\_INCLUDE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-713">2147762224 (0x80044030)</span><span class="sxs-lookup"><span data-stu-id="67da8-713">2147762224 (0x80044030)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-714">Файл, включенный в MOF командой препроцессора [ \# , является](-include.md) недопустимым.</span><span class="sxs-lookup"><span data-stu-id="67da8-714">A file included in the MOF by the preprocessor command [\#include](-include.md) is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="67da8-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**ВБЕММОФ \_ E \_ Недопустимый \_ \_ синтаксис делетекласс**</span><span class="sxs-lookup"><span data-stu-id="67da8-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETECLASS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da8-716">2147762225 (0x80044031)</span><span class="sxs-lookup"><span data-stu-id="67da8-716">2147762225 (0x80044031)</span></span>
</dt> <dt>



<span data-ttu-id="67da8-717">Недопустимый синтаксис команд препроцессора: [ \# pragma DeleteInstance](pragma-deleteinstance.md) или [ \# pragma делетекласс](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="67da8-717">The syntax for the preprocessor commands [\#pragma deleteinstance](pragma-deleteinstance.md) or [\#pragma deleteclass](pragma-deleteclass.md) is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67da8-718">Требования</span><span class="sxs-lookup"><span data-stu-id="67da8-718">Requirements</span></span>



| <span data-ttu-id="67da8-719">Требование</span><span class="sxs-lookup"><span data-stu-id="67da8-719">Requirement</span></span> | <span data-ttu-id="67da8-720">Значение</span><span class="sxs-lookup"><span data-stu-id="67da8-720">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67da8-721">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67da8-721">Minimum supported client</span></span><br/> | <span data-ttu-id="67da8-722">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67da8-722">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="67da8-723">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67da8-723">Minimum supported server</span></span><br/> | <span data-ttu-id="67da8-724">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67da8-724">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="67da8-725">Header</span><span class="sxs-lookup"><span data-stu-id="67da8-725">Header</span></span><br/>                   | <dl> <span data-ttu-id="67da8-726"><dt>Вбемкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="67da8-726"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="67da8-727">IDL</span><span class="sxs-lookup"><span data-stu-id="67da8-727">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67da8-728"><dt>Вбемкли. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67da8-728"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67da8-729">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67da8-729">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67da8-730">Коды возврата WMI</span><span class="sxs-lookup"><span data-stu-id="67da8-730">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

