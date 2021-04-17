---
title: Метод Сетсинглесессион класса Win32_TerminalServiceSetting
description: Метод Сетсинглесессион задает свойство Синглесессион для класса.
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсинглесессион
- Службы удаленных рабочих столов метода Сетсинглесессион, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сетсинглесессион
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682065"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f425a-106">Метод Сетсинглесессион \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="f425a-106">SetSingleSession method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f425a-107">Метод **сетсинглесессион** задает свойство **синглесессион** для класса.</span><span class="sxs-lookup"><span data-stu-id="f425a-107">The **SetSingleSession** method sets the **SingleSession** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="f425a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f425a-108">Syntax</span></span>


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a><span data-ttu-id="f425a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f425a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f425a-110">*Синглесессион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f425a-110">*SingleSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f425a-111">Флаг отключения или включения свойства **синглесессион** , которое определяет, ограничен ли пользователь одним или несколькими сеансами службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f425a-111">Flag disabling or enabling the **SingleSession** property, which determines whether users are limited to one or more Remote Desktop Services sessions.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="f425a-112"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="f425a-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="f425a-113">Отключите свойство.</span><span class="sxs-lookup"><span data-stu-id="f425a-113">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="f425a-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f425a-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f425a-115">Включите свойство.</span><span class="sxs-lookup"><span data-stu-id="f425a-115">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f425a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f425a-116">Return value</span></span>

<span data-ttu-id="f425a-117">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="f425a-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f425a-118">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f425a-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f425a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f425a-119">Remarks</span></span>

<span data-ttu-id="f425a-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f425a-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f425a-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f425a-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f425a-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f425a-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f425a-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f425a-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f425a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f425a-124">Requirements</span></span>



| <span data-ttu-id="f425a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f425a-125">Requirement</span></span> | <span data-ttu-id="f425a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f425a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f425a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f425a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f425a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f425a-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f425a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f425a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f425a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f425a-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f425a-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f425a-131">Namespace</span></span><br/>                | <span data-ttu-id="f425a-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f425a-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f425a-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f425a-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f425a-134"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f425a-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f425a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f425a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f425a-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f425a-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f425a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f425a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f425a-138">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f425a-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

