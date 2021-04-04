---
title: Метод Сетколордепс класса Win32_TSClientSetting
description: Метод Сетколордепс задает свойство Clientareawidth для класса.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетколордепс
- Службы удаленных рабочих столов метода Сетколордепс, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетколордепс
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989242"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="5e758-106">Метод Сетколордепс \_ класса Win32 тсклиентсеттинг</span><span class="sxs-lookup"><span data-stu-id="5e758-106">SetColorDepth method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="5e758-107">Метод **сетколордепс** задает свойство **clientareawidth** для класса.</span><span class="sxs-lookup"><span data-stu-id="5e758-107">The **SetColorDepth** method sets the **ColorDepth** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e758-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e758-108">Syntax</span></span>


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a><span data-ttu-id="5e758-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e758-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e758-110">*Clientareawidth* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e758-110">*ColorDepth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e758-111">Новое значение для свойства **clientareawidth** .</span><span class="sxs-lookup"><span data-stu-id="5e758-111">The new value for the **ColorDepth** property.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="5e758-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="5e758-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="5e758-113">8 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="5e758-113">8 bits per pixel</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="5e758-114"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="5e758-114"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="5e758-115">15 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="5e758-115">15 bits per pixel</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="5e758-116"><span id="3"></span>**3-5**</span><span class="sxs-lookup"><span data-stu-id="5e758-116"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="5e758-117">16 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="5e758-117">16 bits per pixel</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="5e758-118"><span id="4"></span>**четырех**</span><span class="sxs-lookup"><span data-stu-id="5e758-118"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="5e758-119">24 бита на пиксель</span><span class="sxs-lookup"><span data-stu-id="5e758-119">24 bits per pixel</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="5e758-120"><span id="5"></span>**5.0**</span><span class="sxs-lookup"><span data-stu-id="5e758-120"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="5e758-121">32 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="5e758-121">32 bits per pixel</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e758-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e758-122">Return value</span></span>

<span data-ttu-id="5e758-123">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="5e758-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5e758-124">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5e758-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="5e758-125">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="5e758-125">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e758-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e758-126">Remarks</span></span>

<span data-ttu-id="5e758-127">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="5e758-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5e758-128">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="5e758-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5e758-129">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="5e758-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5e758-130">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5e758-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e758-131">Требования</span><span class="sxs-lookup"><span data-stu-id="5e758-131">Requirements</span></span>



| <span data-ttu-id="5e758-132">Требование</span><span class="sxs-lookup"><span data-stu-id="5e758-132">Requirement</span></span> | <span data-ttu-id="5e758-133">Значение</span><span class="sxs-lookup"><span data-stu-id="5e758-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e758-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e758-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5e758-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e758-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e758-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e758-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5e758-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e758-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e758-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5e758-138">Namespace</span></span><br/>                | <span data-ttu-id="5e758-139">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="5e758-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5e758-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5e758-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e758-141"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e758-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e758-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5e758-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e758-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e758-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e758-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e758-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e758-145">**\_Тсклиентсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="5e758-145">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

