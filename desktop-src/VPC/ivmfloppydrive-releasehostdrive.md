---
title: Метод Ивмфлоппидриве Релеасехостдриве (Впккоминтерфацес. h)
description: Освобождает физический диск узла с дисковода гибких дисков.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- Метод Релеасехостдриве Virtual PC
- Метод Релеасехостдриве Virtual PC, интерфейс Ивмфлоппидриве
- Ивмфлоппидриве интерфейс Virtual PC, метод Релеасехостдриве
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ab726ba87dd978a21c4f27b20437926e07c19b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800977"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a><span data-ttu-id="397a5-106">Метод Ивмфлоппидриве:: Релеасехостдриве</span><span class="sxs-lookup"><span data-stu-id="397a5-106">IVMFloppyDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="397a5-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="397a5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="397a5-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="397a5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="397a5-109">Освобождает физический диск узла с дисковода гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="397a5-109">Releases a physical drive on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="397a5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="397a5-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="397a5-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="397a5-111">Parameters</span></span>

<span data-ttu-id="397a5-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="397a5-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="397a5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="397a5-113">Return value</span></span>

<span data-ttu-id="397a5-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="397a5-114">This method can return one of these values.</span></span>



| <span data-ttu-id="397a5-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="397a5-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="397a5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="397a5-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="397a5-117"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="397a5-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="397a5-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="397a5-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="397a5-119"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="397a5-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="397a5-120">Конфигурация этой виртуальной машины недопустима или не найдена.</span><span class="sxs-lookup"><span data-stu-id="397a5-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="397a5-121"><dt>**Виртуальная машина \_ \_ \_ Неверный \_ тип носителя**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="397a5-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="397a5-122">Носитель, подключенный к этому дисководу гибких дисков, не является физическим дисководом гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="397a5-122">The media attached to this floppy drive is not a physical floppy drive.</span></span><br/>     |
| <dl> <span data-ttu-id="397a5-123"><dt>**Виртуальная машина \_ E \_ нет \_ \_**</dt> <dt>0xA00400652ных</dt> носителей</span><span class="sxs-lookup"><span data-stu-id="397a5-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="397a5-124">К этому дисководу гибких дисков не подключен носитель.</span><span class="sxs-lookup"><span data-stu-id="397a5-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="397a5-125"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="397a5-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="397a5-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="397a5-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="397a5-127">Требования</span><span class="sxs-lookup"><span data-stu-id="397a5-127">Requirements</span></span>



| <span data-ttu-id="397a5-128">Требование</span><span class="sxs-lookup"><span data-stu-id="397a5-128">Requirement</span></span> | <span data-ttu-id="397a5-129">Значение</span><span class="sxs-lookup"><span data-stu-id="397a5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="397a5-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="397a5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="397a5-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="397a5-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="397a5-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="397a5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="397a5-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="397a5-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="397a5-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="397a5-134">End of client support</span></span><br/>    | <span data-ttu-id="397a5-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="397a5-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="397a5-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="397a5-136">Product</span></span><br/>                  | <span data-ttu-id="397a5-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="397a5-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="397a5-138">Header</span><span class="sxs-lookup"><span data-stu-id="397a5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="397a5-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="397a5-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="397a5-140">IID</span><span class="sxs-lookup"><span data-stu-id="397a5-140">IID</span></span><br/>                      | <span data-ttu-id="397a5-141">IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="397a5-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="397a5-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="397a5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="397a5-143">**ивмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="397a5-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

