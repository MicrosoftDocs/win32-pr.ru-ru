---
title: Метод Сетфаллбаккпринтдривертипе класса Win32_TerminalServiceSetting
description: Метод Сетфаллбаккпринтдривертипе задает свойство Фаллбаккпринтдривертипе для класса.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетфаллбаккпринтдривертипе
- Службы удаленных рабочих столов метода Сетфаллбаккпринтдривертипе, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сетфаллбаккпринтдривертипе
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071946"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="0afd3-106">Метод Сетфаллбаккпринтдривертипе \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="0afd3-106">SetFallbackPrintDriverType method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="0afd3-107">Метод **сетфаллбаккпринтдривертипе** задает свойство **фаллбаккпринтдривертипе** для класса.</span><span class="sxs-lookup"><span data-stu-id="0afd3-107">The **SetFallbackPrintDriverType** method sets the **FallbackPrintDriverType** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="0afd3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0afd3-108">Syntax</span></span>


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a><span data-ttu-id="0afd3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0afd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0afd3-110">*Фаллбаккпринтдривертипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0afd3-110">*FallbackPrintDriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0afd3-111">Задает свойство **фаллбаккпринтдривертипе** , которое разрешает или запрещает новые подключения службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0afd3-111">Sets the **FallbackPrintDriverType** property which allows or denies new Remote Desktop Services connections.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="0afd3-112"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="0afd3-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="0afd3-113">Нет резервных драйверов.</span><span class="sxs-lookup"><span data-stu-id="0afd3-113">No fallback drivers.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="0afd3-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="0afd3-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="0afd3-115">Лучшее предположение.</span><span class="sxs-lookup"><span data-stu-id="0afd3-115">Best guess.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="0afd3-116"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="0afd3-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="0afd3-117">Лучшее предположение.</span><span class="sxs-lookup"><span data-stu-id="0afd3-117">Best guess.</span></span> <span data-ttu-id="0afd3-118">Если совпадений не найдено, откат к Hewlett-Packard языку управления принтера (PCL).</span><span class="sxs-lookup"><span data-stu-id="0afd3-118">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="0afd3-119"><span id="3"></span>**3-5**</span><span class="sxs-lookup"><span data-stu-id="0afd3-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="0afd3-120">Лучшее предположение.</span><span class="sxs-lookup"><span data-stu-id="0afd3-120">Best guess.</span></span> <span data-ttu-id="0afd3-121">Если совпадений не найдено, возвращается резервный вариант в PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="0afd3-121">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="0afd3-122"><span id="4"></span>**четырех**</span><span class="sxs-lookup"><span data-stu-id="0afd3-122"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="0afd3-123">Лучшее предположение.</span><span class="sxs-lookup"><span data-stu-id="0afd3-123">Best guess.</span></span> <span data-ttu-id="0afd3-124">Если совпадений не найдено, отобразите драйверы PS и PCL.</span><span class="sxs-lookup"><span data-stu-id="0afd3-124">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0afd3-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0afd3-125">Return value</span></span>

<span data-ttu-id="0afd3-126">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="0afd3-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0afd3-127">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0afd3-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="0afd3-128">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="0afd3-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0afd3-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0afd3-129">Remarks</span></span>

<span data-ttu-id="0afd3-130">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0afd3-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0afd3-131">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="0afd3-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0afd3-132">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0afd3-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0afd3-133">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0afd3-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0afd3-134">Требования</span><span class="sxs-lookup"><span data-stu-id="0afd3-134">Requirements</span></span>



| <span data-ttu-id="0afd3-135">Требование</span><span class="sxs-lookup"><span data-stu-id="0afd3-135">Requirement</span></span> | <span data-ttu-id="0afd3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="0afd3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0afd3-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0afd3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0afd3-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0afd3-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0afd3-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0afd3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0afd3-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0afd3-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0afd3-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0afd3-141">Namespace</span></span><br/>                | <span data-ttu-id="0afd3-142">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0afd3-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0afd3-143">MOF</span><span class="sxs-lookup"><span data-stu-id="0afd3-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0afd3-144"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0afd3-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0afd3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0afd3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0afd3-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0afd3-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0afd3-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0afd3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0afd3-148">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="0afd3-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

