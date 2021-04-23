---
title: Метод Сесомедиректори класса Win32_TerminalServiceSetting
description: Задает свойство Терминалсервицешомедиректори для класса.
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сесомедиректори
- Службы удаленных рабочих столов метода Сесомедиректори, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сесомедиректори
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534064"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="dc583-106">Метод Сесомедиректори \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="dc583-106">SetHomeDirectory method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="dc583-107">Метод **сесомедиректори** задает свойство **терминалсервицешомедиректори** для класса.</span><span class="sxs-lookup"><span data-stu-id="dc583-107">The **SetHomeDirectory** method sets the **TerminalServicesHomeDirectory** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc583-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc583-108">Syntax</span></span>


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="dc583-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc583-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc583-110">*Хомедиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc583-110">*HomeDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc583-111">Новое значение свойства **терминалсервицешомедиректори** , которое указывает корневой каталог компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc583-111">The new value for the **TerminalServicesHomeDirectory** property, which specifies the computer's root directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc583-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc583-112">Return value</span></span>

<span data-ttu-id="dc583-113">Возвращает успешное завершение; в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="dc583-113">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="dc583-114">Список кодов ошибок WMI см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dc583-114">For a list of WMI error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dc583-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc583-115">Remarks</span></span>

<span data-ttu-id="dc583-116">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="dc583-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dc583-117">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="dc583-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dc583-118">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="dc583-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dc583-119">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="dc583-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc583-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dc583-120">Requirements</span></span>



| <span data-ttu-id="dc583-121">Требование</span><span class="sxs-lookup"><span data-stu-id="dc583-121">Requirement</span></span> | <span data-ttu-id="dc583-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dc583-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc583-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc583-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dc583-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc583-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc583-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc583-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dc583-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc583-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc583-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dc583-127">Namespace</span></span><br/>                | <span data-ttu-id="dc583-128">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="dc583-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="dc583-129">MOF</span><span class="sxs-lookup"><span data-stu-id="dc583-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc583-130"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc583-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc583-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dc583-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc583-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc583-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc583-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc583-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc583-134">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="dc583-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

