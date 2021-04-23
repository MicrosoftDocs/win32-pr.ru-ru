---
title: Метод ЕксплиЦитлогон класса Win32_TSLogonSetting
description: Метод ЕксплиЦитлогон задает учетные данные, используемые для проверки подлинности.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ЕксплиЦитлогон
- Службы удаленных рабочих столов метода ЕксплиЦитлогон, класс Win32_TSLogonSetting
- Класс Win32_TSLogonSetting службы удаленных рабочих столов, метод ЕксплиЦитлогон
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415833"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="eba70-106">Метод ЕксплиЦитлогон \_ класса Win32 тслогонсеттинг</span><span class="sxs-lookup"><span data-stu-id="eba70-106">ExplicitLogon method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="eba70-107">Метод **експлиЦитлогон** задает учетные данные, используемые для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="eba70-107">The **ExplicitLogon** method sets the credentials to use for authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="eba70-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eba70-108">Syntax</span></span>


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a><span data-ttu-id="eba70-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eba70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eba70-110">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eba70-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba70-111">Учетные данные имени пользователя для входа.</span><span class="sxs-lookup"><span data-stu-id="eba70-111">The user name logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="eba70-112">*Домен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eba70-112">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba70-113">Учетные данные для входа в домен.</span><span class="sxs-lookup"><span data-stu-id="eba70-113">The domain logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="eba70-114">*Пароль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eba70-114">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eba70-115">Учетные данные для входа на пароль.</span><span class="sxs-lookup"><span data-stu-id="eba70-115">The password logon credential.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eba70-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eba70-116">Return value</span></span>

<span data-ttu-id="eba70-117">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="eba70-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="eba70-118">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="eba70-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="eba70-119">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="eba70-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="eba70-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eba70-120">Remarks</span></span>

<span data-ttu-id="eba70-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="eba70-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eba70-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="eba70-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eba70-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="eba70-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eba70-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eba70-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eba70-125">Требования</span><span class="sxs-lookup"><span data-stu-id="eba70-125">Requirements</span></span>



| <span data-ttu-id="eba70-126">Требование</span><span class="sxs-lookup"><span data-stu-id="eba70-126">Requirement</span></span> | <span data-ttu-id="eba70-127">Значение</span><span class="sxs-lookup"><span data-stu-id="eba70-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eba70-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eba70-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eba70-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eba70-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eba70-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eba70-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eba70-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eba70-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eba70-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eba70-132">Namespace</span></span><br/>                | <span data-ttu-id="eba70-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="eba70-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="eba70-134">MOF</span><span class="sxs-lookup"><span data-stu-id="eba70-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eba70-135"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eba70-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="eba70-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eba70-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eba70-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eba70-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eba70-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eba70-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba70-139">**\_Тслогонсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="eba70-139">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

