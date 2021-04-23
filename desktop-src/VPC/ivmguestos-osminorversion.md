---
title: Свойство дочерний osminorversion Ивмгуестос (Впккоминтерфацес. h)
description: Дополнительный номер версии гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: fa71e215-8633-4f53-ab71-bc9bfdb56cc8
keywords:
- Дочерний osminorversion свойство Virtual PC
- Дочерний osminorversion свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство дочерний osminorversion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMinorVersion
- IVMGuestOS.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c068ee6d8112561f57d0644f6bc7bc4844096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691838"
---
# <a name="ivmguestososminorversion-property"></a><span data-ttu-id="bb998-106">Свойство Ивмгуестос:: дочерний osminorversion</span><span class="sxs-lookup"><span data-stu-id="bb998-106">IVMGuestOS::OSMinorVersion property</span></span>

<span data-ttu-id="bb998-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bb998-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bb998-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bb998-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bb998-109">Извлекает дополнительный номер версии гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bb998-109">Retrieves the minor version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="bb998-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bb998-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb998-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb998-111">Syntax</span></span>


```C++
HRESULT get_OSMinorVersion(
  [out, retval] BSTR *minorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="bb998-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bb998-112">Property value</span></span>

<span data-ttu-id="bb998-113">Дополнительная версия.</span><span class="sxs-lookup"><span data-stu-id="bb998-113">The minor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bb998-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="bb998-114">Error codes</span></span>



| <span data-ttu-id="bb998-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="bb998-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="bb998-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bb998-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bb998-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bb998-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="bb998-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bb998-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="bb998-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="bb998-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="bb998-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bb998-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="bb998-121"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="bb998-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="bb998-122">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="bb998-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="bb998-123"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="bb998-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="bb998-124">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bb998-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="bb998-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bb998-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="bb998-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="bb998-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="bb998-127">Требования</span><span class="sxs-lookup"><span data-stu-id="bb998-127">Requirements</span></span>



| <span data-ttu-id="bb998-128">Требование</span><span class="sxs-lookup"><span data-stu-id="bb998-128">Requirement</span></span> | <span data-ttu-id="bb998-129">Значение</span><span class="sxs-lookup"><span data-stu-id="bb998-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb998-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb998-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bb998-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bb998-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb998-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb998-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bb998-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bb998-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bb998-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="bb998-134">End of client support</span></span><br/>    | <span data-ttu-id="bb998-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb998-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bb998-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="bb998-136">Product</span></span><br/>                  | <span data-ttu-id="bb998-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bb998-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bb998-138">Header</span><span class="sxs-lookup"><span data-stu-id="bb998-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb998-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb998-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bb998-140">IID</span><span class="sxs-lookup"><span data-stu-id="bb998-140">IID</span></span><br/>                      | <span data-ttu-id="bb998-141">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="bb998-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="bb998-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb998-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb998-143">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="bb998-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

