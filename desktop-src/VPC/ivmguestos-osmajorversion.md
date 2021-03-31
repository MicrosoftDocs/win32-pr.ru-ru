---
title: Свойство дочерний osmajorversion Ивмгуестос (Впккоминтерфацес. h)
description: Основной номер версии гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: c9be8b4e-15fe-402d-8396-30be6b065b73
keywords:
- Дочерний osmajorversion свойство Virtual PC
- Дочерний osmajorversion свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство дочерний osmajorversion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMajorVersion
- IVMGuestOS.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f76e3105c4917141c8a5304082d55f383ee947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490449"
---
# <a name="ivmguestososmajorversion-property"></a><span data-ttu-id="5d766-106">Свойство Ивмгуестос:: дочерний osmajorversion</span><span class="sxs-lookup"><span data-stu-id="5d766-106">IVMGuestOS::OSMajorVersion property</span></span>

<span data-ttu-id="5d766-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5d766-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5d766-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5d766-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5d766-109">Извлекает основной номер версии гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5d766-109">Retrieves the major version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="5d766-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5d766-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d766-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d766-111">Syntax</span></span>


```C++
HRESULT get_OSMajorVersion(
  [out, retval] BSTR *majorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="5d766-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5d766-112">Property value</span></span>

<span data-ttu-id="5d766-113">Основная версия.</span><span class="sxs-lookup"><span data-stu-id="5d766-113">The major version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5d766-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="5d766-114">Error codes</span></span>



| <span data-ttu-id="5d766-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="5d766-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="5d766-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5d766-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5d766-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5d766-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="5d766-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5d766-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="5d766-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="5d766-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="5d766-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5d766-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="5d766-121"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="5d766-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="5d766-122">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="5d766-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="5d766-123"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="5d766-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="5d766-124">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5d766-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="5d766-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5d766-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="5d766-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5d766-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="5d766-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5d766-127">Requirements</span></span>



| <span data-ttu-id="5d766-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5d766-128">Requirement</span></span> | <span data-ttu-id="5d766-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5d766-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d766-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d766-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5d766-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5d766-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d766-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d766-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5d766-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5d766-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5d766-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5d766-134">End of client support</span></span><br/>    | <span data-ttu-id="5d766-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5d766-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5d766-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="5d766-136">Product</span></span><br/>                  | <span data-ttu-id="5d766-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5d766-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5d766-138">Header</span><span class="sxs-lookup"><span data-stu-id="5d766-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d766-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d766-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5d766-140">IID</span><span class="sxs-lookup"><span data-stu-id="5d766-140">IID</span></span><br/>                      | <span data-ttu-id="5d766-141">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="5d766-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5d766-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d766-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d766-143">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="5d766-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

