---
title: Свойство Девиценумбер Ивмхарддискконнектион (Впккоминтерфацес. h)
description: Возвращает номер устройства, к которому подключен образ диска.
ms.assetid: fea8bac6-fb25-495a-bc56-1d517b831f33
keywords:
- Девиценумбер свойство Virtual PC
- Девиценумбер свойство Virtual PC, интерфейс Ивмхарддискконнектион
- Ивмхарддискконнектион интерфейс Virtual PC, свойство Девиценумбер
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.DeviceNumber
- IVMHardDiskConnection.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69f7d9d3f9a373c9b8086857af56c7e5da9f5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137318"
---
# <a name="ivmharddiskconnectiondevicenumber-property"></a><span data-ttu-id="2e60b-106">Ивмхарддискконнектион: свойство Евиценумбер:D</span><span class="sxs-lookup"><span data-stu-id="2e60b-106">IVMHardDiskConnection::DeviceNumber property</span></span>

<span data-ttu-id="2e60b-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2e60b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2e60b-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2e60b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2e60b-109">Возвращает номер устройства, к которому подключен образ диска.</span><span class="sxs-lookup"><span data-stu-id="2e60b-109">Retrieves the device number to which the drive image is attached.</span></span>

<span data-ttu-id="2e60b-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2e60b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e60b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e60b-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="2e60b-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2e60b-112">Property value</span></span>

<span data-ttu-id="2e60b-113">Номер устройства, соответствующий этому соединению.</span><span class="sxs-lookup"><span data-stu-id="2e60b-113">The device number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2e60b-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2e60b-114">Error codes</span></span>



| <span data-ttu-id="2e60b-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="2e60b-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="2e60b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2e60b-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e60b-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2e60b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="2e60b-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2e60b-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="2e60b-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2e60b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="2e60b-120">Параметр имеет **значение NULL** или недопустим.</span><span class="sxs-lookup"><span data-stu-id="2e60b-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="2e60b-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2e60b-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="2e60b-122">Текущая конфигурация виртуальной машины недопустима.</span><span class="sxs-lookup"><span data-stu-id="2e60b-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="2e60b-123"><dt>Виртуальная машина \_ \_Диск E \_ Недопустимый</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="2e60b-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="2e60b-124">Расположение шины для этого подключения не инициализировано должным образом.</span><span class="sxs-lookup"><span data-stu-id="2e60b-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="2e60b-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2e60b-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="2e60b-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2e60b-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="2e60b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2e60b-127">Requirements</span></span>



| <span data-ttu-id="2e60b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2e60b-128">Requirement</span></span> | <span data-ttu-id="2e60b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2e60b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e60b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e60b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2e60b-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2e60b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e60b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e60b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2e60b-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2e60b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2e60b-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2e60b-134">End of client support</span></span><br/>    | <span data-ttu-id="2e60b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2e60b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2e60b-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="2e60b-136">Product</span></span><br/>                  | <span data-ttu-id="2e60b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2e60b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2e60b-138">Header</span><span class="sxs-lookup"><span data-stu-id="2e60b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e60b-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e60b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2e60b-140">IID</span><span class="sxs-lookup"><span data-stu-id="2e60b-140">IID</span></span><br/>                      | <span data-ttu-id="2e60b-141">IID \_ ивмхарддискконнектион определен как aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="2e60b-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="2e60b-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e60b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e60b-143">**ивмхарддискконнектион**</span><span class="sxs-lookup"><span data-stu-id="2e60b-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

