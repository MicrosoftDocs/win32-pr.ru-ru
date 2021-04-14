---
title: Enable, метод класса Win32_Terminal
description: Метод Enable отключает или включает терминал.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Включить метод службы удаленных рабочих столов
- Включение метода службы удаленных рабочих столов, Win32_Terminal класса
- Класс Win32_Terminal службы удаленных рабочих столов, метод Enable
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415021"
---
# <a name="enable-method-of-the-win32_terminal-class"></a><span data-ttu-id="85565-106">Enable, метод \_ класса терминала Win32</span><span class="sxs-lookup"><span data-stu-id="85565-106">Enable method of the Win32\_Terminal class</span></span>

<span data-ttu-id="85565-107">Метод **Enable** отключает или включает терминал.</span><span class="sxs-lookup"><span data-stu-id="85565-107">The **Enable** method disables or enables the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="85565-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85565-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="85565-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="85565-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85565-110">*фенаблетерминал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85565-110">*fEnableTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85565-111">Флаг, который отключает или включает терминал.</span><span class="sxs-lookup"><span data-stu-id="85565-111">Flag that disables or enables the terminal.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="85565-112"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="85565-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="85565-113">Терминал отключен.</span><span class="sxs-lookup"><span data-stu-id="85565-113">The terminal is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="85565-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="85565-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="85565-115">Терминал включен.</span><span class="sxs-lookup"><span data-stu-id="85565-115">The terminal is enabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85565-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85565-116">Return value</span></span>

<span data-ttu-id="85565-117">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="85565-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="85565-118">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="85565-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="85565-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85565-119">Remarks</span></span>

<span data-ttu-id="85565-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="85565-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="85565-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="85565-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="85565-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="85565-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="85565-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="85565-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="85565-124">Требования</span><span class="sxs-lookup"><span data-stu-id="85565-124">Requirements</span></span>



| <span data-ttu-id="85565-125">Требование</span><span class="sxs-lookup"><span data-stu-id="85565-125">Requirement</span></span> | <span data-ttu-id="85565-126">Значение</span><span class="sxs-lookup"><span data-stu-id="85565-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85565-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85565-127">Minimum supported client</span></span><br/> | <span data-ttu-id="85565-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85565-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85565-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85565-129">Minimum supported server</span></span><br/> | <span data-ttu-id="85565-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85565-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85565-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="85565-131">Namespace</span></span><br/>                | <span data-ttu-id="85565-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="85565-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="85565-133">MOF</span><span class="sxs-lookup"><span data-stu-id="85565-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85565-134"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85565-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="85565-135">DLL</span><span class="sxs-lookup"><span data-stu-id="85565-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85565-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85565-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85565-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85565-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85565-138">**\_Терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="85565-138">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

