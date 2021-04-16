---
title: Метод Сетклиентпроперти класса Win32_TSClientSetting
description: Метод Сетклиентпроперти задает свойство Лптпортмаппинг, Компортмаппинг, Аудиомаппинг, Клипбоардмаппинг, Дривемаппинг или WindowsPrinterMapping для класса.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетклиентпроперти
- Службы удаленных рабочих столов метода Сетклиентпроперти, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетклиентпроперти
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672629"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="0ac1a-106">Метод Сетклиентпроперти \_ класса Win32 тсклиентсеттинг</span><span class="sxs-lookup"><span data-stu-id="0ac1a-106">SetClientProperty method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="0ac1a-107">Метод **сетклиентпроперти** задает свойство **лптпортмаппинг**, **компортмаппинг**, **аудиомаппинг**, **клипбоардмаппинг**, **дривемаппинг** или **WindowsPrinterMapping** для класса.</span><span class="sxs-lookup"><span data-stu-id="0ac1a-107">The **SetClientProperty** method sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac1a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ac1a-108">Syntax</span></span>


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="0ac1a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ac1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac1a-110">*PropertyName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ac1a-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac1a-111">Указывает свойство клиента, для которого настраивается метод.</span><span class="sxs-lookup"><span data-stu-id="0ac1a-111">Specifies the client property that the method is setting.</span></span>

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span data-ttu-id="0ac1a-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**аудиомаппинг**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span></span>


</dt> <dd>

<span data-ttu-id="0ac1a-113">Метод устанавливает свойство **аудиомаппинг** .</span><span class="sxs-lookup"><span data-stu-id="0ac1a-113">The method is setting the **AudioMapping** property.</span></span>

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span data-ttu-id="0ac1a-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**клипбоардмаппинг**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span></span>


</dt> <dd>

<span data-ttu-id="0ac1a-115">Метод устанавливает свойство **клипбоардмаппинг** .</span><span class="sxs-lookup"><span data-stu-id="0ac1a-115">The method is setting the **ClipboardMapping** property.</span></span>

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span data-ttu-id="0ac1a-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**компортмаппинг**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="0ac1a-117">Метод устанавливает свойство **компортмаппинг** .</span><span class="sxs-lookup"><span data-stu-id="0ac1a-117">The method is setting the **COMPortMapping** property.</span></span>

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span data-ttu-id="0ac1a-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**дривемаппинг**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span></span>


</dt> <dd>

<span data-ttu-id="0ac1a-119">Метод устанавливает свойство **дривемаппинг** .</span><span class="sxs-lookup"><span data-stu-id="0ac1a-119">The method is setting the **DriveMapping** property.</span></span>

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span data-ttu-id="0ac1a-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**лптпортмаппинг**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="0ac1a-121">Метод устанавливает свойство **лптпортмаппинг** .</span><span class="sxs-lookup"><span data-stu-id="0ac1a-121">The method is setting the **LPTPortMapping** property.</span></span>

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span data-ttu-id="0ac1a-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**пнпредиректион**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span></span>


</dt> <dd>

<span data-ttu-id="0ac1a-123">Метод устанавливает свойство **пнпредиректион** .</span><span class="sxs-lookup"><span data-stu-id="0ac1a-123">The method is setting the **PNPRedirection** property.</span></span>

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span data-ttu-id="0ac1a-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**виндовспринтермаппинг**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span></span>


</dt> <dd>

<span data-ttu-id="0ac1a-125">Метод устанавливает свойство **виндовспринтермаппинг** .</span><span class="sxs-lookup"><span data-stu-id="0ac1a-125">The method is setting the **WindowsPrinterMapping** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0ac1a-126">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ac1a-126">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac1a-127">Значение, указывающее, следует ли включать или отключать свойство, заданное параметром *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="0ac1a-127">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="0ac1a-128"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-128"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="0ac1a-129">Отключите свойство.</span><span class="sxs-lookup"><span data-stu-id="0ac1a-129">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="0ac1a-130"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-130"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="0ac1a-131">Включите свойство.</span><span class="sxs-lookup"><span data-stu-id="0ac1a-131">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac1a-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ac1a-132">Return value</span></span>

<span data-ttu-id="0ac1a-133">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="0ac1a-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0ac1a-134">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac1a-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="0ac1a-135">Метод возвращает ошибку, если указанное свойство клиента не находится в элементе управления групповой политики или если параметр свойства не может переопределяться сервером.</span><span class="sxs-lookup"><span data-stu-id="0ac1a-135">The method returns an error if the specified client property is not under group policy control or if the property setting is not eligible for override by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac1a-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ac1a-136">Remarks</span></span>

<span data-ttu-id="0ac1a-137">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0ac1a-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0ac1a-138">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="0ac1a-138">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0ac1a-139">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0ac1a-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0ac1a-140">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0ac1a-140">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac1a-141">Требования</span><span class="sxs-lookup"><span data-stu-id="0ac1a-141">Requirements</span></span>



| <span data-ttu-id="0ac1a-142">Требование</span><span class="sxs-lookup"><span data-stu-id="0ac1a-142">Requirement</span></span> | <span data-ttu-id="0ac1a-143">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac1a-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac1a-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ac1a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac1a-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ac1a-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0ac1a-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ac1a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac1a-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ac1a-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ac1a-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0ac1a-148">Namespace</span></span><br/>                | <span data-ttu-id="0ac1a-149">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0ac1a-149">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0ac1a-150">MOF</span><span class="sxs-lookup"><span data-stu-id="0ac1a-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ac1a-151"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ac1a-151"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ac1a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="0ac1a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ac1a-153"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ac1a-153"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac1a-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ac1a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac1a-155">**\_Тсклиентсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="0ac1a-155">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

