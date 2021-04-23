---
title: Метод Енаблеложевент класса Win32_TSGatewayServerSettings
description: Включает или отключает ведение журнала для указанного типа событий.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблеложевент
- Службы удаленных рабочих столов метода Енаблеложевент, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Енаблеложевент
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72f7cb8567c7f2d5c3ca79d241013e2bd64a5e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493209"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="6fd6a-106">Метод Енаблеложевент \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="6fd6a-106">EnableLogEvent method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="6fd6a-107">Включает или отключает ведение журнала для указанного типа событий.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-107">Enables or disables logging of the specified event type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd6a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fd6a-108">Syntax</span></span>


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="6fd6a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fd6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fd6a-110">*EventName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6fd6a-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fd6a-111">Имя события.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-111">Name of the event.</span></span> <span data-ttu-id="6fd6a-112">Это значение должно быть получено с помощью метода [**жетложевентнаме**](getlogeventname-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="6fd6a-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="6fd6a-113">логчаннелдисконнект</span><span class="sxs-lookup"><span data-stu-id="6fd6a-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="6fd6a-114">Пользователь успешно отключился от ресурса.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="6fd6a-115">логфаиледчаннелконнект</span><span class="sxs-lookup"><span data-stu-id="6fd6a-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="6fd6a-116">Пользователю не удалось подключиться к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="6fd6a-117">логфаилуренетворкакцессчекк</span><span class="sxs-lookup"><span data-stu-id="6fd6a-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="6fd6a-118">Пользователь не прошел авторизацию подключения.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="6fd6a-119">логфаилурересаурцеакцессчекк</span><span class="sxs-lookup"><span data-stu-id="6fd6a-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="6fd6a-120">Пользователь не прошел авторизацию ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="6fd6a-121">логсукцессчаннелконнект</span><span class="sxs-lookup"><span data-stu-id="6fd6a-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="6fd6a-122">Пользователь успешно подключился к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="6fd6a-123">логсукцессфулнетворкакцессчекк</span><span class="sxs-lookup"><span data-stu-id="6fd6a-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="6fd6a-124">Пользователь успешно прошел авторизацию подключения.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="6fd6a-125">логсукцессфулресаурцеакцессчекк</span><span class="sxs-lookup"><span data-stu-id="6fd6a-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="6fd6a-126">Пользователь успешно прошел авторизацию ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6fd6a-127">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6fd6a-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fd6a-128">Указывает, должно ли событие быть включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-128">Specifies whether the event should be enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fd6a-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fd6a-129">Return value</span></span>

<span data-ttu-id="6fd6a-130">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6fd6a-131">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6fd6a-132">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6fd6a-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6fd6a-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6fd6a-133">Remarks</span></span>

<span data-ttu-id="6fd6a-134">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6fd6a-135">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6fd6a-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6fd6a-136">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="6fd6a-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6fd6a-137">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="6fd6a-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6fd6a-138">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6fd6a-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd6a-139">Требования</span><span class="sxs-lookup"><span data-stu-id="6fd6a-139">Requirements</span></span>



| <span data-ttu-id="6fd6a-140">Требование</span><span class="sxs-lookup"><span data-stu-id="6fd6a-140">Requirement</span></span> | <span data-ttu-id="6fd6a-141">Значение</span><span class="sxs-lookup"><span data-stu-id="6fd6a-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd6a-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fd6a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd6a-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6fd6a-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6fd6a-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fd6a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd6a-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fd6a-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6fd6a-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6fd6a-146">Namespace</span></span><br/>                | <span data-ttu-id="6fd6a-147">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="6fd6a-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6fd6a-148">MOF</span><span class="sxs-lookup"><span data-stu-id="6fd6a-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fd6a-149"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fd6a-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fd6a-150">DLL</span><span class="sxs-lookup"><span data-stu-id="6fd6a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fd6a-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fd6a-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6fd6a-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fd6a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd6a-153">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="6fd6a-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="6fd6a-154">**жетложевентнаме**</span><span class="sxs-lookup"><span data-stu-id="6fd6a-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

