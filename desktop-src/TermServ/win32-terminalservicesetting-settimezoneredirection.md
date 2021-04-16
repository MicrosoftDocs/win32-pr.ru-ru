---
title: Метод Сеттимезонередиректион класса Win32_TerminalServiceSetting
description: Метод Сеттимезонередиректион задает свойство Тимезонередиректион, которое позволяет клиентскому компьютеру перенаправлять параметры часового пояса в сеанс службы удаленных рабочих столов.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сеттимезонередиректион
- Службы удаленных рабочих столов метода Сеттимезонередиректион, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сеттимезонередиректион
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672631"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="415b7-106">Метод Сеттимезонередиректион \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="415b7-106">SetTimeZoneRedirection method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="415b7-107">Метод **сеттимезонередиректион** задает свойство **тимезонередиректион** , которое позволяет клиентскому компьютеру перенаправлять параметры часового пояса в сеанс службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="415b7-107">The **SetTimeZoneRedirection** method sets the **TimeZoneRedirection** property, which allows the client computer to redirect its time zone settings to the Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="415b7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="415b7-108">Syntax</span></span>


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a><span data-ttu-id="415b7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="415b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="415b7-110">*Тимезонередиректион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="415b7-110">*TimeZoneRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="415b7-111">Новое значение для свойства **тимезонередиректион** .</span><span class="sxs-lookup"><span data-stu-id="415b7-111">The new value for the **TimeZoneRedirection** property.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="415b7-112"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="415b7-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="415b7-113">Отключает свойство **тимезонередиректион** .</span><span class="sxs-lookup"><span data-stu-id="415b7-113">Disables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="415b7-114">Перенаправление часового пояса не выполняется.</span><span class="sxs-lookup"><span data-stu-id="415b7-114">No time zone redirection occurs.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="415b7-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="415b7-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="415b7-116">Включает свойство **тимезонередиректион** .</span><span class="sxs-lookup"><span data-stu-id="415b7-116">Enables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="415b7-117">Часовой пояс клиента перенаправляется в часовой пояс сеанса.</span><span class="sxs-lookup"><span data-stu-id="415b7-117">The client's time zone is redirected to the session's time zone.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="415b7-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="415b7-118">Return value</span></span>

<span data-ttu-id="415b7-119">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="415b7-119">Returns 0 on success; otherwise returns a WMI error code.</span></span> <span data-ttu-id="415b7-120">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="415b7-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="415b7-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="415b7-121">Remarks</span></span>

<span data-ttu-id="415b7-122">По умолчанию часовой пояс для сеанса службы удаленных рабочих столов совпадает с часовым поясом для сервера узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="415b7-122">By default, the time zone for the Remote Desktop Services session is the same as the time zone for the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="415b7-123">Клиентские компьютеры не могут перенаправить сведения о часовом поясе.</span><span class="sxs-lookup"><span data-stu-id="415b7-123">Client computers cannot redirect time zone information.</span></span>

<span data-ttu-id="415b7-124">Если перенаправление часового пояса отключено, новые сеансы наследуют часовой пояс сервера.</span><span class="sxs-lookup"><span data-stu-id="415b7-124">If time zone redirection is disabled, new sessions inherit the server time zone.</span></span> <span data-ttu-id="415b7-125">При повторном подключении сеанса сеанс удерживает часовой пояс, который он имел до отключения.</span><span class="sxs-lookup"><span data-stu-id="415b7-125">When a session reconnects, the session retains the time zone it had prior to disconnecting.</span></span>

<span data-ttu-id="415b7-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="415b7-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="415b7-127">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="415b7-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="415b7-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="415b7-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="415b7-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="415b7-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="415b7-130">Требования</span><span class="sxs-lookup"><span data-stu-id="415b7-130">Requirements</span></span>



| <span data-ttu-id="415b7-131">Требование</span><span class="sxs-lookup"><span data-stu-id="415b7-131">Requirement</span></span> | <span data-ttu-id="415b7-132">Значение</span><span class="sxs-lookup"><span data-stu-id="415b7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="415b7-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="415b7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="415b7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="415b7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="415b7-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="415b7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="415b7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="415b7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="415b7-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="415b7-137">Namespace</span></span><br/>                | <span data-ttu-id="415b7-138">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="415b7-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="415b7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="415b7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="415b7-140"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="415b7-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="415b7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="415b7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="415b7-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="415b7-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="415b7-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="415b7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="415b7-144">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="415b7-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

