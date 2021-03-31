---
title: Метод Ивмфлоппидриве Аттачхостдриве (Впккоминтерфацес. h)
description: Подключает физический диск на узле к дисководу гибких дисков виртуальной машины.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- Метод Аттачхостдриве Virtual PC
- Метод Аттачхостдриве Virtual PC, интерфейс Ивмфлоппидриве
- Ивмфлоппидриве интерфейс Virtual PC, метод Аттачхостдриве
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a21785e3e1e4ec77146f048ab4cce018de9d8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071759"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a><span data-ttu-id="c9f20-106">Метод Ивмфлоппидриве:: Аттачхостдриве</span><span class="sxs-lookup"><span data-stu-id="c9f20-106">IVMFloppyDrive::AttachHostDrive method</span></span>

<span data-ttu-id="c9f20-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c9f20-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c9f20-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c9f20-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c9f20-109">Подключает физический диск на узле к дисководу гибких дисков виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c9f20-109">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f20-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9f20-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="c9f20-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9f20-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9f20-112">*буква_диска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9f20-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f20-113">Буква диска физического дисковода гибких дисков на хост-компьютере, который должен быть подключен.</span><span class="sxs-lookup"><span data-stu-id="c9f20-113">The drive letter of the physical floppy drive on the host machine to is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9f20-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9f20-114">Return value</span></span>

<span data-ttu-id="c9f20-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c9f20-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c9f20-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c9f20-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="c9f20-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c9f20-117">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9f20-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c9f20-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c9f20-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c9f20-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="c9f20-120"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="c9f20-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="c9f20-121">Параметр *буква_диска* имеет **значение NULL**, не является допустимым дисководом гибких дисков, или указанный путь пуст.</span><span class="sxs-lookup"><span data-stu-id="c9f20-121">The *driveLetter* parameter is **NULL**, is not a valid floppy drive, or the given path is empty.</span></span><br/> |
| <dl> <span data-ttu-id="c9f20-122"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c9f20-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c9f20-123">Конфигурация этой виртуальной машины недопустима или не найдена.</span><span class="sxs-lookup"><span data-stu-id="c9f20-123">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                       |
| <dl> <span data-ttu-id="c9f20-124"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c9f20-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c9f20-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c9f20-125">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="c9f20-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c9f20-126">Requirements</span></span>



| <span data-ttu-id="c9f20-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c9f20-127">Requirement</span></span> | <span data-ttu-id="c9f20-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c9f20-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f20-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9f20-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9f20-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c9f20-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9f20-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9f20-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9f20-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c9f20-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c9f20-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c9f20-133">End of client support</span></span><br/>    | <span data-ttu-id="c9f20-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9f20-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c9f20-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="c9f20-135">Product</span></span><br/>                  | <span data-ttu-id="c9f20-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c9f20-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c9f20-137">Header</span><span class="sxs-lookup"><span data-stu-id="c9f20-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9f20-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9f20-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c9f20-139">IID</span><span class="sxs-lookup"><span data-stu-id="c9f20-139">IID</span></span><br/>                      | <span data-ttu-id="c9f20-140">IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="c9f20-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c9f20-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9f20-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f20-142">**ивмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="c9f20-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

