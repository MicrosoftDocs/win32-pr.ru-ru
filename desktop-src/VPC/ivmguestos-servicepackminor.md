---
title: Свойство Сервицепаккминор Ивмгуестос (Впккоминтерфацес. h)
description: Дополнительный номер версии пакета обновления гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: f1413b5a-6a74-42a6-9671-b00b7c8912fa
keywords:
- Сервицепаккминор свойство Virtual PC
- Сервицепаккминор свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Сервицепаккминор
topic_type:
- apiref
api_name:
- IVMGuestOS.ServicePackMinor
- IVMGuestOS.get_ServicePackMinor
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e7a94c5ed8de42cc2455160424246e899014cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491085"
---
# <a name="ivmguestosservicepackminor-property"></a><span data-ttu-id="d22d1-106">Свойство Ивмгуестос:: Сервицепаккминор</span><span class="sxs-lookup"><span data-stu-id="d22d1-106">IVMGuestOS::ServicePackMinor property</span></span>

<span data-ttu-id="d22d1-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d22d1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d22d1-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d22d1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d22d1-109">Дополнительный номер версии пакета обновления гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d22d1-109">The minor version of the service pack of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="d22d1-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d22d1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d22d1-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d22d1-111">Syntax</span></span>


```C++
HRESULT get_ServicePackMinor(
  [out, retval] BSTR *servicePackMinor
);
```



## <a name="property-value"></a><span data-ttu-id="d22d1-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d22d1-112">Property value</span></span>

<span data-ttu-id="d22d1-113">Дополнительный номер версии последнего установленного пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="d22d1-113">The minor version number of the latest Service Pack installed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d22d1-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d22d1-114">Error codes</span></span>



| <span data-ttu-id="d22d1-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="d22d1-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="d22d1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d22d1-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d22d1-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d22d1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="d22d1-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d22d1-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="d22d1-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d22d1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="d22d1-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d22d1-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="d22d1-121"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d22d1-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="d22d1-122">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="d22d1-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="d22d1-123"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="d22d1-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="d22d1-124">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d22d1-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d22d1-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d22d1-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="d22d1-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d22d1-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="d22d1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d22d1-127">Requirements</span></span>



| <span data-ttu-id="d22d1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d22d1-128">Requirement</span></span> | <span data-ttu-id="d22d1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d22d1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d22d1-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d22d1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d22d1-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d22d1-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d22d1-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d22d1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d22d1-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d22d1-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d22d1-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d22d1-134">End of client support</span></span><br/>    | <span data-ttu-id="d22d1-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d22d1-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d22d1-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="d22d1-136">Product</span></span><br/>                  | <span data-ttu-id="d22d1-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d22d1-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d22d1-138">Header</span><span class="sxs-lookup"><span data-stu-id="d22d1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d22d1-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d22d1-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d22d1-140">IID</span><span class="sxs-lookup"><span data-stu-id="d22d1-140">IID</span></span><br/>                      | <span data-ttu-id="d22d1-141">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="d22d1-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d22d1-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d22d1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22d1-143">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="d22d1-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

