---
title: Свойство Хостдривелеттер Ивмфлоппидриве (Впккоминтерфацес. h)
description: Буква диска узла, к которому подключен дисковод гибких дисков.
ms.assetid: 16d11e06-e3bc-4a4a-850d-f7b4122e6af9
keywords:
- Хостдривелеттер свойство Virtual PC
- Хостдривелеттер свойство Virtual PC, интерфейс Ивмфлоппидриве
- Ивмфлоппидриве интерфейс Virtual PC, свойство Хостдривелеттер
topic_type:
- apiref
api_name:
- IVMFloppyDrive.HostDriveLetter
- IVMFloppyDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4896699dd3547eb3488e2fc085b5b2c54de827b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534289"
---
# <a name="ivmfloppydrivehostdriveletter-property"></a><span data-ttu-id="43bc3-106">Свойство Ивмфлоппидриве:: Хостдривелеттер</span><span class="sxs-lookup"><span data-stu-id="43bc3-106">IVMFloppyDrive::HostDriveLetter property</span></span>

<span data-ttu-id="43bc3-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="43bc3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="43bc3-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="43bc3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="43bc3-109">Извлекает букву диска узла, к которому подключен дисковод гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="43bc3-109">Retrieves the letter of the host drive to which the floppy drive is attached.</span></span>

<span data-ttu-id="43bc3-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="43bc3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="43bc3-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43bc3-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="43bc3-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="43bc3-112">Property value</span></span>

<span data-ttu-id="43bc3-113">Буква физического дисковода гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="43bc3-113">The letter of the physical floppy drive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="43bc3-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="43bc3-114">Error codes</span></span>



| <span data-ttu-id="43bc3-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="43bc3-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="43bc3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="43bc3-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43bc3-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="43bc3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="43bc3-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="43bc3-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="43bc3-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="43bc3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="43bc3-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="43bc3-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="43bc3-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="43bc3-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="43bc3-122">Конфигурация этой виртуальной машины недопустима или не найдена.</span><span class="sxs-lookup"><span data-stu-id="43bc3-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="43bc3-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="43bc3-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="43bc3-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="43bc3-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="43bc3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="43bc3-125">Requirements</span></span>



| <span data-ttu-id="43bc3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="43bc3-126">Requirement</span></span> | <span data-ttu-id="43bc3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="43bc3-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="43bc3-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43bc3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="43bc3-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="43bc3-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43bc3-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43bc3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="43bc3-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="43bc3-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="43bc3-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="43bc3-132">End of client support</span></span><br/>    | <span data-ttu-id="43bc3-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43bc3-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="43bc3-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="43bc3-134">Product</span></span><br/>                  | <span data-ttu-id="43bc3-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="43bc3-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="43bc3-136">Header</span><span class="sxs-lookup"><span data-stu-id="43bc3-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="43bc3-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="43bc3-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="43bc3-138">IID</span><span class="sxs-lookup"><span data-stu-id="43bc3-138">IID</span></span><br/>                      | <span data-ttu-id="43bc3-139">IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="43bc3-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="43bc3-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43bc3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43bc3-141">**ивмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="43bc3-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

