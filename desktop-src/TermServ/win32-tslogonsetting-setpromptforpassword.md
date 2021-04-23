---
title: Метод Сетпромптфорпассворд класса Win32_TSLogonSetting
description: Метод Сетпромптфорпассворд задает свойство Промптфорпассворд.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетпромптфорпассворд
- Службы удаленных рабочих столов метода Сетпромптфорпассворд, класс Win32_TSLogonSetting
- Класс Win32_TSLogonSetting службы удаленных рабочих столов, метод Сетпромптфорпассворд
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672743"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="2de8f-106">Метод Сетпромптфорпассворд \_ класса Win32 тслогонсеттинг</span><span class="sxs-lookup"><span data-stu-id="2de8f-106">SetPromptForPassword method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="2de8f-107">Метод **сетпромптфорпассворд** задает свойство **промптфорпассворд** .</span><span class="sxs-lookup"><span data-stu-id="2de8f-107">The **SetPromptForPassword** method sets the **PromptForPassword** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de8f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2de8f-108">Syntax</span></span>


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a><span data-ttu-id="2de8f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2de8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de8f-110">*Промптфорпассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2de8f-110">*PromptForPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2de8f-111">Флаг отключения или включения свойства **промптфорпассворд** .</span><span class="sxs-lookup"><span data-stu-id="2de8f-111">Flag disabling or enabling the **PromptForPassword** property.</span></span>

<dt>

<span data-ttu-id="2de8f-112">0</span><span class="sxs-lookup"><span data-stu-id="2de8f-112">0</span></span>
</dt> <dd>

<span data-ttu-id="2de8f-113">Отключает запрос пароля.</span><span class="sxs-lookup"><span data-stu-id="2de8f-113">Disables password-prompting.</span></span>

</dd> <dt>

<span data-ttu-id="2de8f-114">1</span><span class="sxs-lookup"><span data-stu-id="2de8f-114">1</span></span>
</dt> <dd>

<span data-ttu-id="2de8f-115">Включает запрос пароля.</span><span class="sxs-lookup"><span data-stu-id="2de8f-115">Enables password-prompting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de8f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2de8f-116">Return value</span></span>

<span data-ttu-id="2de8f-117">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="2de8f-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2de8f-118">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2de8f-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="2de8f-119">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="2de8f-119">The method returns an error if the setting is under group policy control.</span></span>

<dl> <dt>

<span data-ttu-id="2de8f-120">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="2de8f-120">**FALSE** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2de8f-121">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="2de8f-121">**TRUE** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2de8f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2de8f-122">Remarks</span></span>

<span data-ttu-id="2de8f-123">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="2de8f-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2de8f-124">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="2de8f-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2de8f-125">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="2de8f-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2de8f-126">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2de8f-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2de8f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2de8f-127">Requirements</span></span>



| <span data-ttu-id="2de8f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2de8f-128">Requirement</span></span> | <span data-ttu-id="2de8f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2de8f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2de8f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2de8f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2de8f-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2de8f-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2de8f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2de8f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2de8f-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2de8f-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2de8f-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2de8f-134">Namespace</span></span><br/>                | <span data-ttu-id="2de8f-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="2de8f-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2de8f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2de8f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2de8f-137"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2de8f-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2de8f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2de8f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2de8f-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2de8f-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de8f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2de8f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de8f-141">**\_Тслогонсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="2de8f-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

