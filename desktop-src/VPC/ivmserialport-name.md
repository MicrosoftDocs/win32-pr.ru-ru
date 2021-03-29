---
title: Свойство имени Ивмсериалпорт (Впккоминтерфацес. h)
description: Имя последовательного порта.
ms.assetid: 4d3fe008-f089-4a1b-9c90-2e0b3ded58fa
keywords:
- Имя свойство Virtual PC
- Имя свойство Virtual PC, интерфейс Ивмсериалпорт
- Ивмсериалпорт интерфейс Virtual PC, свойство Name
topic_type:
- apiref
api_name:
- IVMSerialPort.Name
- IVMSerialPort.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540540e2af91647b9c77735a1c601ed62aecdbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892498"
---
# <a name="ivmserialportname-property"></a><span data-ttu-id="c5b49-106">Свойство Ивмсериалпорт:: Name</span><span class="sxs-lookup"><span data-stu-id="c5b49-106">IVMSerialPort::Name property</span></span>

<span data-ttu-id="c5b49-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c5b49-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c5b49-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c5b49-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c5b49-109">Возвращает имя последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="c5b49-109">Retrieves the name of the serial port.</span></span>

<span data-ttu-id="c5b49-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c5b49-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b49-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5b49-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="c5b49-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c5b49-112">Property value</span></span>

<span data-ttu-id="c5b49-113">Имя последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="c5b49-113">The name of the serial port.</span></span> <span data-ttu-id="c5b49-114">Например, "COM1" для **вмсериалпорт \_ хостпорт**, "C: \\SerialPort.txt" для **вмсериалпорт \_ TextFile** или " \\ \\ *ServerName* \\ pipe \\ *pipeName*" для **вмсериалпорт \_ помощью канала NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="c5b49-114">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c5b49-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c5b49-115">Error codes</span></span>



| <span data-ttu-id="c5b49-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="c5b49-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c5b49-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c5b49-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5b49-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c5b49-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c5b49-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c5b49-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="c5b49-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c5b49-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c5b49-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c5b49-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="c5b49-122"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c5b49-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c5b49-123">Недопустимая конфигурация для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c5b49-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="c5b49-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c5b49-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c5b49-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c5b49-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="c5b49-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c5b49-126">Requirements</span></span>



| <span data-ttu-id="c5b49-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c5b49-127">Requirement</span></span> | <span data-ttu-id="c5b49-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c5b49-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b49-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5b49-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b49-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c5b49-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5b49-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5b49-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b49-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c5b49-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c5b49-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c5b49-133">End of client support</span></span><br/>    | <span data-ttu-id="c5b49-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c5b49-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c5b49-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="c5b49-135">Product</span></span><br/>                  | <span data-ttu-id="c5b49-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c5b49-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c5b49-137">Header</span><span class="sxs-lookup"><span data-stu-id="c5b49-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5b49-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5b49-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c5b49-139">IID</span><span class="sxs-lookup"><span data-stu-id="c5b49-139">IID</span></span><br/>                      | <span data-ttu-id="c5b49-140">IID \_ ивмсериалпорт определен как 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="c5b49-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="c5b49-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5b49-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b49-142">**ивмсериалпорт**</span><span class="sxs-lookup"><span data-stu-id="c5b49-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

