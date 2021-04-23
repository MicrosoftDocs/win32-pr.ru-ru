---
description: Создает новый драйвер принтера.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Метод Аддпринтердривер класса Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423234"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="e1d83-103">Метод Аддпринтердривер \_ класса Win32 принтердривер</span><span class="sxs-lookup"><span data-stu-id="e1d83-103">AddPrinterDriver method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="e1d83-104">Метод класса **аддпринтердривер** создает новый драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="e1d83-104">The **AddPrinterDriver** class method creates a new printer driver.</span></span>

<span data-ttu-id="e1d83-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="e1d83-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e1d83-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e1d83-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d83-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1d83-107">Syntax</span></span>


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e1d83-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1d83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d83-109">*Дриверинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1d83-109">*DriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d83-110">Экземпляр класса [**Win32 \_ принтердривер**](win32-printerdriver.md) , представляющий драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="e1d83-110">An instance of the [**Win32\_PrinterDriver**](win32-printerdriver.md) class that represents the printer driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d83-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1d83-111">Return value</span></span>

<span data-ttu-id="e1d83-112">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="e1d83-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="e1d83-113">Для значений, отличающихся от перечисленных в следующем списке, см. раздел [**константы ошибки WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="e1d83-113">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="e1d83-114">**0**</span><span class="sxs-lookup"><span data-stu-id="e1d83-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e1d83-115">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e1d83-115">Success.</span></span>

</dd> <dt>

<span data-ttu-id="e1d83-116">**5**</span><span class="sxs-lookup"><span data-stu-id="e1d83-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="e1d83-117">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="e1d83-117">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="e1d83-118">**87**</span><span class="sxs-lookup"><span data-stu-id="e1d83-118">**87**</span></span>
</dt> <dd>

<span data-ttu-id="e1d83-119">Неправильный параметр".</span><span class="sxs-lookup"><span data-stu-id="e1d83-119">The parameter is incorrect.</span></span> <span data-ttu-id="e1d83-120">Может возникнуть, когда объект неверно заполнен или не удается найти драйвер в системе.</span><span class="sxs-lookup"><span data-stu-id="e1d83-120">May occur when the object is not correctly filled or when driver can not be found in the system.</span></span> <span data-ttu-id="e1d83-121">Кроме того, атрибут Name может отличаться от модели, указанной в INF-файле.</span><span class="sxs-lookup"><span data-stu-id="e1d83-121">Alternately, the name attribute may be different than the model specified in the .inf file.</span></span> <span data-ttu-id="e1d83-122">Или в атрибуте Пасфиле может отсутствовать обратная косая черта (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="e1d83-122">Or, there may be a missing backslash ("\\") on a PathFile attribute.</span></span>

</dd> <dt>

<span data-ttu-id="e1d83-123">**1797**</span><span class="sxs-lookup"><span data-stu-id="e1d83-123">**1797**</span></span>
</dt> <dd>

<span data-ttu-id="e1d83-124">Неизвестный драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="e1d83-124">The printer driver is unknown.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1d83-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1d83-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e1d83-126">При использовании метода **аддпринтердривер** необходимо использовать **селоаддриверпривилеже** для загрузки или выгрузки драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="e1d83-126">When using the **AddPrinterDriver** method you must use **SeLoadDriverPrivilege** to load or unload a device driver.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e1d83-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="e1d83-127">Examples</span></span>

<span data-ttu-id="e1d83-128">[Установка драйвера принтера, не найденного в файле Drivers CAB](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) , пример кода VBScript устанавливает гипотетический принтер с помощью драйвера печати, не найденного в Drivers.cab.</span><span class="sxs-lookup"><span data-stu-id="e1d83-128">The[Install a Printer Driver not Found in Drivers Cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript code example installs a hypothetical printer using a print driver not found in Drivers.cab.</span></span>

<span data-ttu-id="e1d83-129">Следующий пример сценария VBScript устанавливает драйвер принтера для принтера Apple LaserWriter 8500.</span><span class="sxs-lookup"><span data-stu-id="e1d83-129">The following VBScript sample installs the printer driver for an Apple LaserWriter 8500 printer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a><span data-ttu-id="e1d83-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e1d83-130">Requirements</span></span>



| <span data-ttu-id="e1d83-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e1d83-131">Requirement</span></span> | <span data-ttu-id="e1d83-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e1d83-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d83-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1d83-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e1d83-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1d83-134">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e1d83-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1d83-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e1d83-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1d83-136">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e1d83-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e1d83-137">Namespace</span></span><br/>                | <span data-ttu-id="e1d83-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e1d83-138">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="e1d83-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e1d83-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1d83-140"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1d83-140"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1d83-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e1d83-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1d83-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1d83-142"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e1d83-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1d83-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d83-144">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="e1d83-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e1d83-145">**\_Принтердривер Win32**</span><span class="sxs-lookup"><span data-stu-id="e1d83-145">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

