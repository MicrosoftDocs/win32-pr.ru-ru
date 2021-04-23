---
description: Метод StartService помещает службу в запущенное состояние.
ms.assetid: 0f221db1-29ad-4071-98d3-6d06e4f5e026
ms.tgt_platform: multiple
title: Метод StartService класса Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44e6fedb9e1d0edd9f355c654c7fe2cd25760ec7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655883"
---
# <a name="startservice-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="76c74-103">Метод StartService \_ класса Win32 принтердривер</span><span class="sxs-lookup"><span data-stu-id="76c74-103">StartService method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="76c74-104">Метод **StartService** помещает службу в запущенное состояние.</span><span class="sxs-lookup"><span data-stu-id="76c74-104">The **StartService** method places the service in the started state.</span></span>

<span data-ttu-id="76c74-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="76c74-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="76c74-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="76c74-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="76c74-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76c74-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="76c74-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="76c74-108">Parameters</span></span>

<span data-ttu-id="76c74-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="76c74-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76c74-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76c74-110">Return value</span></span>

<span data-ttu-id="76c74-111">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="76c74-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="76c74-112">Для значений, отличающихся от перечисленных в следующем списке, см. раздел [**константы ошибки WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="76c74-112">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="76c74-113">**0**</span><span class="sxs-lookup"><span data-stu-id="76c74-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="76c74-114">Служба успешно запущена.</span><span class="sxs-lookup"><span data-stu-id="76c74-114">Service successfully started.</span></span>

</dd> <dt>

<span data-ttu-id="76c74-115">**1**</span><span class="sxs-lookup"><span data-stu-id="76c74-115">**1**</span></span>
</dt> <dd>

<span data-ttu-id="76c74-116">Запрос не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="76c74-116">Request not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76c74-117">Требования</span><span class="sxs-lookup"><span data-stu-id="76c74-117">Requirements</span></span>



| <span data-ttu-id="76c74-118">Требование</span><span class="sxs-lookup"><span data-stu-id="76c74-118">Requirement</span></span> | <span data-ttu-id="76c74-119">Значение</span><span class="sxs-lookup"><span data-stu-id="76c74-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76c74-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76c74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76c74-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76c74-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="76c74-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76c74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76c74-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76c74-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="76c74-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="76c74-124">Namespace</span></span><br/>                | <span data-ttu-id="76c74-125">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="76c74-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="76c74-126">MOF</span><span class="sxs-lookup"><span data-stu-id="76c74-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76c74-127"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76c74-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="76c74-128">DLL</span><span class="sxs-lookup"><span data-stu-id="76c74-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76c74-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76c74-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="76c74-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76c74-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76c74-131">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="76c74-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="76c74-132">**\_Принтердривер Win32**</span><span class="sxs-lookup"><span data-stu-id="76c74-132">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

