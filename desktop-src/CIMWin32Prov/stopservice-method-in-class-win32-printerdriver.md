---
description: Помещает службу, представленную \_ объектом Win32 принтердривер, в остановленном состоянии.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Метод «начало» класса Win32_PrinterDriver (Сдоиас. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072457"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="a2e24-103">Метод «начало» \_ класса Принтердривер Win32</span><span class="sxs-lookup"><span data-stu-id="a2e24-103">StopService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="a2e24-104">Метод **"** неработающий [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) " помещает службу, представленную объектом [**Win32 \_ принтердривер**](win32-printerdriver.md) , в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="a2e24-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_PrinterDriver**](win32-printerdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="a2e24-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a2e24-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a2e24-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a2e24-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2e24-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2e24-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="a2e24-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2e24-108">Parameters</span></span>

<span data-ttu-id="a2e24-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a2e24-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2e24-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2e24-110">Return value</span></span>

<span data-ttu-id="a2e24-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="a2e24-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="a2e24-112">Для значений, отличающихся от перечисленных в следующем списке, см. раздел [**константы ошибки WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="a2e24-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="a2e24-113">**0**</span><span class="sxs-lookup"><span data-stu-id="a2e24-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a2e24-114">Служба успешно остановлена.</span><span class="sxs-lookup"><span data-stu-id="a2e24-114">Service successfully stopped.</span></span>

</dd> <dt>

<span data-ttu-id="a2e24-115">**1**</span><span class="sxs-lookup"><span data-stu-id="a2e24-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a2e24-116">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a2e24-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2e24-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a2e24-117">Requirements</span></span>



| <span data-ttu-id="a2e24-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a2e24-118">Requirement</span></span> | <span data-ttu-id="a2e24-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a2e24-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e24-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2e24-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a2e24-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2e24-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a2e24-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2e24-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a2e24-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2e24-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a2e24-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a2e24-124">Namespace</span></span><br/>                | <span data-ttu-id="a2e24-125">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a2e24-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="a2e24-126">Header</span><span class="sxs-lookup"><span data-stu-id="a2e24-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2e24-127"><dt>Сдоиас. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2e24-127"><dt>Sdoias.h</dt></span></span> </dl>           |
| <span data-ttu-id="a2e24-128">MOF</span><span class="sxs-lookup"><span data-stu-id="a2e24-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2e24-129"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2e24-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2e24-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a2e24-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2e24-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2e24-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a2e24-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2e24-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2e24-133">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="a2e24-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a2e24-134">**\_Принтердривер Win32**</span><span class="sxs-lookup"><span data-stu-id="a2e24-134">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

