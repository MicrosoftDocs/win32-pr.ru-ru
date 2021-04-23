---
title: Свойство Ундохарддиск Ивмхарддискконнектион (Впккоминтерфацес. h)
description: Извлекает объект жесткого диска, соответствующий образу диска отмены этого подключения.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- Ундохарддиск свойство Virtual PC
- Ундохарддиск свойство Virtual PC, интерфейс Ивмхарддискконнектион
- Ивмхарддискконнектион интерфейс Virtual PC, свойство Ундохарддиск
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135054"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a><span data-ttu-id="cd067-106">Свойство Ивмхарддискконнектион:: Ундохарддиск</span><span class="sxs-lookup"><span data-stu-id="cd067-106">IVMHardDiskConnection::UndoHardDisk property</span></span>

<span data-ttu-id="cd067-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cd067-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cd067-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cd067-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cd067-109">Извлекает объект жесткого диска, соответствующий образу диска отмены этого подключения.</span><span class="sxs-lookup"><span data-stu-id="cd067-109">Retrieves a hard disk object corresponding to this connection's undo disk image.</span></span>

<span data-ttu-id="cd067-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cd067-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd067-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd067-111">Syntax</span></span>


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="cd067-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cd067-112">Property value</span></span>

<span data-ttu-id="cd067-113">Объект [**ивмхарддиск**](ivmharddisk.md) , описывающий жесткий диск отмены, связанный с этим соединением.</span><span class="sxs-lookup"><span data-stu-id="cd067-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the undo hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cd067-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="cd067-114">Error codes</span></span>



| <span data-ttu-id="cd067-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="cd067-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="cd067-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cd067-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd067-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cd067-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="cd067-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cd067-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="cd067-119"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cd067-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="cd067-120">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="cd067-120">An unexpected error has occurred.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="cd067-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="cd067-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="cd067-122">Параметр имеет **значение NULL** или недопустим.</span><span class="sxs-lookup"><span data-stu-id="cd067-122">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="cd067-123"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="cd067-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="cd067-124">Диск отмены для этого подключения не найден.</span><span class="sxs-lookup"><span data-stu-id="cd067-124">The undo disk for this connection was not found.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="cd067-125"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cd067-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="cd067-126">Текущая конфигурация виртуальной машины недопустима.</span><span class="sxs-lookup"><span data-stu-id="cd067-126">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="cd067-127"><dt>Виртуальная машина \_ \_Диск E \_ Недопустимый</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="cd067-127"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="cd067-128">Расположение шины для этого подключения не было правильно инициализировано, или устройство в этом расположении не является допустимым жестким диском.</span><span class="sxs-lookup"><span data-stu-id="cd067-128">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cd067-129">Требования</span><span class="sxs-lookup"><span data-stu-id="cd067-129">Requirements</span></span>



| <span data-ttu-id="cd067-130">Требование</span><span class="sxs-lookup"><span data-stu-id="cd067-130">Requirement</span></span> | <span data-ttu-id="cd067-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cd067-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd067-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd067-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cd067-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cd067-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd067-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd067-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cd067-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cd067-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cd067-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cd067-136">End of client support</span></span><br/>    | <span data-ttu-id="cd067-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd067-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cd067-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="cd067-138">Product</span></span><br/>                  | <span data-ttu-id="cd067-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cd067-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cd067-140">Header</span><span class="sxs-lookup"><span data-stu-id="cd067-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd067-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd067-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cd067-142">IID</span><span class="sxs-lookup"><span data-stu-id="cd067-142">IID</span></span><br/>                      | <span data-ttu-id="cd067-143">IID \_ ивмхарддискконнектион определен как aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="cd067-143">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="cd067-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd067-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd067-145">**ивмхарддискконнектион**</span><span class="sxs-lookup"><span data-stu-id="cd067-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

