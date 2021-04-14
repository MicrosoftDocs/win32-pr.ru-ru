---
title: Свойство жесткого диска Ивмхарддискконнектион (Впккоминтерфацес. h)
description: Извлекает объект жесткого диска, соответствующий этому соединению.
ms.assetid: dbe369d8-ec05-4039-9494-fc196262f697
keywords:
- Виртуальный ПК свойства жесткого диска
- Свойство жесткого диска Virtual PC, интерфейс Ивмхарддискконнектион
- Интерфейс Ивмхарддискконнектион Virtual PC, свойство жесткого диска
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.HardDisk
- IVMHardDiskConnection.get_HardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9baa365606b71b693dd841471d50a475a42677d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415733"
---
# <a name="ivmharddiskconnectionharddisk-property"></a><span data-ttu-id="8ec64-106">Свойство Ивмхарддискконнектион:: жесткого диска</span><span class="sxs-lookup"><span data-stu-id="8ec64-106">IVMHardDiskConnection::HardDisk property</span></span>

<span data-ttu-id="8ec64-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8ec64-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8ec64-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8ec64-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8ec64-109">Извлекает объект жесткого диска, соответствующий этому соединению.</span><span class="sxs-lookup"><span data-stu-id="8ec64-109">Retrieves a hard disk object corresponding to this connection.</span></span>

<span data-ttu-id="8ec64-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8ec64-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec64-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ec64-111">Syntax</span></span>


```C++
HRESULT get_HardDisk(
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="8ec64-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8ec64-112">Property value</span></span>

<span data-ttu-id="8ec64-113">Объект [**ивмхарддиск**](ivmharddisk.md) , описывающий жесткий диск, связанный с этим соединением.</span><span class="sxs-lookup"><span data-stu-id="8ec64-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8ec64-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="8ec64-114">Error codes</span></span>



| <span data-ttu-id="8ec64-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="8ec64-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="8ec64-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8ec64-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ec64-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8ec64-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="8ec64-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8ec64-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="8ec64-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="8ec64-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="8ec64-120">Параметр имеет **значение NULL** или недопустим.</span><span class="sxs-lookup"><span data-stu-id="8ec64-120">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="8ec64-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8ec64-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="8ec64-122">Текущая конфигурация виртуальной машины недопустима.</span><span class="sxs-lookup"><span data-stu-id="8ec64-122">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="8ec64-123"><dt>Виртуальная машина \_ \_Диск E \_ Недопустимый</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="8ec64-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="8ec64-124">Расположение шины для этого подключения не было правильно инициализировано, или устройство в этом расположении не является допустимым жестким диском.</span><span class="sxs-lookup"><span data-stu-id="8ec64-124">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |
| <dl> <span data-ttu-id="8ec64-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8ec64-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="8ec64-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8ec64-126">An unexpected error has occurred.</span></span><br/>                                                                                                |



## <a name="requirements"></a><span data-ttu-id="8ec64-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8ec64-127">Requirements</span></span>



| <span data-ttu-id="8ec64-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8ec64-128">Requirement</span></span> | <span data-ttu-id="8ec64-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8ec64-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec64-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ec64-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec64-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8ec64-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ec64-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ec64-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec64-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8ec64-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8ec64-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8ec64-134">End of client support</span></span><br/>    | <span data-ttu-id="8ec64-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ec64-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8ec64-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="8ec64-136">Product</span></span><br/>                  | <span data-ttu-id="8ec64-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8ec64-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8ec64-138">Header</span><span class="sxs-lookup"><span data-stu-id="8ec64-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ec64-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec64-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8ec64-140">IID</span><span class="sxs-lookup"><span data-stu-id="8ec64-140">IID</span></span><br/>                      | <span data-ttu-id="8ec64-141">IID \_ ивмхарддискконнектион определен как aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="8ec64-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="8ec64-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ec64-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec64-143">**ивмхарддискконнектион**</span><span class="sxs-lookup"><span data-stu-id="8ec64-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

