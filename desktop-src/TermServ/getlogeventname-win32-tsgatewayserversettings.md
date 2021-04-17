---
title: Метод Жетложевентнаме класса Win32_TSGatewayServerSettings
description: Возвращает имя события журнала для указанного индекса событий журнала.
ms.assetid: ca31ef8e-ab84-4132-a6d2-232b1e69230a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетложевентнаме
- Службы удаленных рабочих столов метода Жетложевентнаме, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Жетложевентнаме
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetLogEventName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e9c608b7a12d3de48d75ecd5651df94d0267fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672731"
---
# <a name="getlogeventname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8f0d8-106">Метод Жетложевентнаме \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="8f0d8-106">GetLogEventName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8f0d8-107">Возвращает имя события журнала для указанного индекса событий журнала.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-107">Returns the log event name for the specified log event index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f0d8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f0d8-108">Syntax</span></span>


```mof
uint32 GetLogEventName(
  [in]  uint32 EventIndex,
  [out] string EventName
);
```



## <a name="parameters"></a><span data-ttu-id="8f0d8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f0d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f0d8-110">*Евентиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f0d8-110">*EventIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f0d8-111">Индекс события журнала.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-111">Index of the log event.</span></span> <span data-ttu-id="8f0d8-112">Значение должно быть в диапазоне от нуля до значения свойства **максложевентс** .</span><span class="sxs-lookup"><span data-stu-id="8f0d8-112">The value must be between zero and the value of the **MaxLogEvents** property.</span></span>

</dd> <dt>

<span data-ttu-id="8f0d8-113">*EventName* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8f0d8-113">*EventName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f0d8-114">Имя указанного события.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-114">Name of the specified event.</span></span> <span data-ttu-id="8f0d8-115">В следующем списке приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-115">The following list displays the possible values.</span></span>

<dt>

<span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>

<span data-ttu-id="8f0d8-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**логчаннелдисконнект**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span></span>


</dt> <dd>

<span data-ttu-id="8f0d8-117">Пользователь успешно отключился от ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-117">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>

<span data-ttu-id="8f0d8-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**логфаилуречаннелконнект**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="8f0d8-119">Пользователю не удалось подключиться к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-119">User failed to connect to the resource.</span></span>

</dd> <dt>

<span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="8f0d8-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**логфаилуреконнектионаусоризатиончекк**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="8f0d8-121">Пользователь не прошел авторизацию подключения.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-121">User failed connection authorization.</span></span>

</dd> <dt>

<span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="8f0d8-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**логфаилурересаурцеаусоризатиончекк**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="8f0d8-123">Пользователь не прошел авторизацию ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-123">User failed resource authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>

<span data-ttu-id="8f0d8-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**логсукцессфулчаннелконнект**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="8f0d8-125">Пользователь успешно подключился к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-125">User successfully connected to the resource.</span></span>

</dd> <dt>

<span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="8f0d8-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**логсукцессфулконнектионаусоризатиончекк**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="8f0d8-127">Пользователь успешно прошел авторизацию подключения.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-127">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="8f0d8-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**логсукцессфулресаурцеаусоризатиончекк**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="8f0d8-129">Пользователь успешно прошел авторизацию ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-129">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f0d8-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f0d8-130">Return value</span></span>

<span data-ttu-id="8f0d8-131">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8f0d8-132">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8f0d8-133">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8f0d8-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8f0d8-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f0d8-134">Remarks</span></span>

<span data-ttu-id="8f0d8-135">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8f0d8-136">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8f0d8-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8f0d8-137">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8f0d8-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8f0d8-138">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8f0d8-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8f0d8-139">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8f0d8-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f0d8-140">Требования</span><span class="sxs-lookup"><span data-stu-id="8f0d8-140">Requirements</span></span>



| <span data-ttu-id="8f0d8-141">Требование</span><span class="sxs-lookup"><span data-stu-id="8f0d8-141">Requirement</span></span> | <span data-ttu-id="8f0d8-142">Значение</span><span class="sxs-lookup"><span data-stu-id="8f0d8-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f0d8-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f0d8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8f0d8-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8f0d8-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8f0d8-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f0d8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8f0d8-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f0d8-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8f0d8-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8f0d8-147">Namespace</span></span><br/>                | <span data-ttu-id="8f0d8-148">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="8f0d8-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8f0d8-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8f0d8-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f0d8-150"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f0d8-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f0d8-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8f0d8-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f0d8-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f0d8-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8f0d8-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f0d8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f0d8-154">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-154">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="8f0d8-155">**енаблеложевент**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-155">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="8f0d8-156">**исложевентенаблед**</span><span class="sxs-lookup"><span data-stu-id="8f0d8-156">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)
</dt> </dl>

 

