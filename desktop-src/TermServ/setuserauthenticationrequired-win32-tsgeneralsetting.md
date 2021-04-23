---
title: Метод Сетусераусентикатионрекуиред класса Win32_TSGeneralSetting
description: Включает или отключает требование, которое пользователи должны пройти проверку подлинности во время соединения, задав значение свойства Усераусентикатионрекуиред.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетусераусентикатионрекуиред
- Службы удаленных рабочих столов метода Сетусераусентикатионрекуиред, класс Win32_TSGeneralSetting
- Класс Win32_TSGeneralSetting службы удаленных рабочих столов, метод Сетусераусентикатионрекуиред
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341130"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="5559b-106">Метод Сетусераусентикатионрекуиред \_ класса Win32 тсженералсеттинг</span><span class="sxs-lookup"><span data-stu-id="5559b-106">SetUserAuthenticationRequired method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="5559b-107">Включает или отключает требование, которое пользователи должны пройти проверку подлинности во время соединения, задав значение свойства **усераусентикатионрекуиред** в классе [**Win32 \_ тсженералсеттинг**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="5559b-107">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property in the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span> <span data-ttu-id="5559b-108">Если **значение равно true**, то при подключении **усераусентикатионрекуиред** требуется проверка подлинности пользователя во время подключения, чтобы повысить защиту сервера от сетевых атак.</span><span class="sxs-lookup"><span data-stu-id="5559b-108">If **True**, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="5559b-109">Подключаться могут только клиенты протокол удаленного рабочего стола (RDP), поддерживающие RDP версии 6,0 или выше.</span><span class="sxs-lookup"><span data-stu-id="5559b-109">Only Remote Desktop Protocol (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="5559b-110">Чтобы избежать нарушений работы удаленных пользователей, перед включением свойства рекомендуется развернуть клиенты RDP, поддерживающие соответствующую версию протокола.</span><span class="sxs-lookup"><span data-stu-id="5559b-110">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5559b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5559b-111">Syntax</span></span>


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a><span data-ttu-id="5559b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5559b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5559b-113">*Усераусентикатионрекуиред* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5559b-113">*UserAuthenticationRequired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5559b-114">Указывает, требуется ли проверка подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="5559b-114">Indicates whether user authentication is required.</span></span>

<dt>

<span data-ttu-id="5559b-115">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="5559b-115">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="5559b-116">Отключить требование, когда пользователь должен пройти проверку подлинности</span><span class="sxs-lookup"><span data-stu-id="5559b-116">Disable requirement that user must be authenticated</span></span>

</dd> <dt>

<span data-ttu-id="5559b-117">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5559b-117">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="5559b-118">Включает требование, которое пользователь должен пройти проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="5559b-118">Enables requirement that user must be authenticated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5559b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5559b-119">Return value</span></span>

<span data-ttu-id="5559b-120">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="5559b-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5559b-121">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5559b-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5559b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5559b-122">Remarks</span></span>

<span data-ttu-id="5559b-123">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="5559b-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5559b-124">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="5559b-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5559b-125">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="5559b-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5559b-126">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5559b-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5559b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5559b-127">Requirements</span></span>



| <span data-ttu-id="5559b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5559b-128">Requirement</span></span> | <span data-ttu-id="5559b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5559b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5559b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5559b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5559b-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5559b-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5559b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5559b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5559b-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5559b-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5559b-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5559b-134">Namespace</span></span><br/>                | <span data-ttu-id="5559b-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="5559b-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5559b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5559b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5559b-137"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5559b-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5559b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5559b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5559b-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5559b-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5559b-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5559b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5559b-141">**\_Тсженералсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="5559b-141">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

