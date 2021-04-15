---
title: Свойство OSName Ивмгуестос (Впккоминтерфацес. h)
description: Имя гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: 6381fc15-a6ab-429b-809d-7f89e7ec666d
keywords:
- OSName свойство Virtual PC
- OSName свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство OSName
topic_type:
- apiref
api_name:
- IVMGuestOS.OSName
- IVMGuestOS.get_OSName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672c7b2c852bcbb1ec39b61889b03738e3a2df23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490446"
---
# <a name="ivmguestososname-property"></a><span data-ttu-id="fd329-106">Свойство Ивмгуестос:: OSName</span><span class="sxs-lookup"><span data-stu-id="fd329-106">IVMGuestOS::OSName property</span></span>

<span data-ttu-id="fd329-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd329-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fd329-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fd329-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fd329-109">Извлекает имя гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fd329-109">Retrieves the name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="fd329-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fd329-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd329-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd329-111">Syntax</span></span>


```C++
HRESULT get_OSName(
  [out, retval] BSTR *guestOSName
);
```



## <a name="property-value"></a><span data-ttu-id="fd329-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fd329-112">Property value</span></span>

<span data-ttu-id="fd329-113">Полное имя операционной системы на виртуальной машине (включая имя набора).</span><span class="sxs-lookup"><span data-stu-id="fd329-113">The full name (including suite name) of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fd329-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="fd329-114">Error codes</span></span>



| <span data-ttu-id="fd329-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="fd329-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="fd329-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fd329-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fd329-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fd329-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="fd329-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fd329-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="fd329-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="fd329-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="fd329-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fd329-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="fd329-121"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="fd329-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="fd329-122">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="fd329-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="fd329-123"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="fd329-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="fd329-124">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fd329-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="fd329-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="fd329-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="fd329-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="fd329-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="fd329-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd329-127">Remarks</span></span>

<span data-ttu-id="fd329-128">Виртуальная машина должна быть запущена (то есть полностью загружена и не завершается), а компоненты интеграции должны быть установлены при вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="fd329-128">The VM must be running (that is, fully booted and not shutting down) and integration components must be installed when this method is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd329-129">Требования</span><span class="sxs-lookup"><span data-stu-id="fd329-129">Requirements</span></span>



| <span data-ttu-id="fd329-130">Требование</span><span class="sxs-lookup"><span data-stu-id="fd329-130">Requirement</span></span> | <span data-ttu-id="fd329-131">Значение</span><span class="sxs-lookup"><span data-stu-id="fd329-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd329-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd329-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fd329-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd329-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd329-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd329-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fd329-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd329-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fd329-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fd329-136">End of client support</span></span><br/>    | <span data-ttu-id="fd329-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd329-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fd329-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="fd329-138">Product</span></span><br/>                  | <span data-ttu-id="fd329-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fd329-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fd329-140">Header</span><span class="sxs-lookup"><span data-stu-id="fd329-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd329-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd329-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fd329-142">IID</span><span class="sxs-lookup"><span data-stu-id="fd329-142">IID</span></span><br/>                      | <span data-ttu-id="fd329-143">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="fd329-143">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fd329-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd329-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd329-145">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="fd329-145">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

