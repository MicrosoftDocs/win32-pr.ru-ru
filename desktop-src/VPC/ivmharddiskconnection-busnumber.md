---
title: Свойство Буснумбер Ивмхарддискконнектион (Впккоминтерфацес. h)
description: Возвращает номер шины, к которой подключен образ диска.
ms.assetid: 2a792930-d8c9-419d-88eb-ddec7c43c5bc
keywords:
- Буснумбер свойство Virtual PC
- Буснумбер свойство Virtual PC, интерфейс Ивмхарддискконнектион
- Ивмхарддискконнектион интерфейс Virtual PC, свойство Буснумбер
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.BusNumber
- IVMHardDiskConnection.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc49a0d4cb284ecd1e2a1340d3b0bf8d9ed43ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491883"
---
# <a name="ivmharddiskconnectionbusnumber-property"></a><span data-ttu-id="dd111-106">Свойство Ивмхарддискконнектион:: Буснумбер</span><span class="sxs-lookup"><span data-stu-id="dd111-106">IVMHardDiskConnection::BusNumber property</span></span>

<span data-ttu-id="dd111-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dd111-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dd111-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dd111-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dd111-109">Возвращает номер шины, к которой подключен образ диска.</span><span class="sxs-lookup"><span data-stu-id="dd111-109">Retrieves the bus number to which the drive image is attached.</span></span>

<span data-ttu-id="dd111-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dd111-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd111-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd111-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="dd111-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dd111-112">Property value</span></span>

<span data-ttu-id="dd111-113">Номер шины, соответствующий этому соединению.</span><span class="sxs-lookup"><span data-stu-id="dd111-113">The bus number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dd111-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dd111-114">Error codes</span></span>



| <span data-ttu-id="dd111-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="dd111-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="dd111-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dd111-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dd111-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dd111-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="dd111-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dd111-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="dd111-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="dd111-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="dd111-120">Параметр имеет **значение NULL** или недопустим.</span><span class="sxs-lookup"><span data-stu-id="dd111-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="dd111-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dd111-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="dd111-122">Текущая конфигурация виртуальной машины недопустима.</span><span class="sxs-lookup"><span data-stu-id="dd111-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="dd111-123"><dt>Виртуальная машина \_ \_Диск E \_ Недопустимый</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="dd111-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="dd111-124">Расположение шины для этого подключения не инициализировано должным образом.</span><span class="sxs-lookup"><span data-stu-id="dd111-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="dd111-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dd111-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="dd111-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="dd111-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="dd111-127">Требования</span><span class="sxs-lookup"><span data-stu-id="dd111-127">Requirements</span></span>



| <span data-ttu-id="dd111-128">Требование</span><span class="sxs-lookup"><span data-stu-id="dd111-128">Requirement</span></span> | <span data-ttu-id="dd111-129">Значение</span><span class="sxs-lookup"><span data-stu-id="dd111-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd111-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd111-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dd111-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dd111-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd111-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd111-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dd111-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd111-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dd111-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dd111-134">End of client support</span></span><br/>    | <span data-ttu-id="dd111-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dd111-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dd111-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="dd111-136">Product</span></span><br/>                  | <span data-ttu-id="dd111-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dd111-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dd111-138">Header</span><span class="sxs-lookup"><span data-stu-id="dd111-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd111-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd111-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dd111-140">IID</span><span class="sxs-lookup"><span data-stu-id="dd111-140">IID</span></span><br/>                      | <span data-ttu-id="dd111-141">IID \_ ивмхарддискконнектион определен как aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="dd111-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="dd111-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd111-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd111-143">**ивмхарддискконнектион**</span><span class="sxs-lookup"><span data-stu-id="dd111-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

