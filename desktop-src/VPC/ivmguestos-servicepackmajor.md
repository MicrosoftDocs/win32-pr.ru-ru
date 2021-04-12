---
title: Свойство Сервицепаккмажор Ивмгуестос (Впккоминтерфацес. h)
description: Основной номер версии пакета обновления гостевой операционной системы, работающей на виртуальной машине.
ms.assetid: 87dbc4cc-8a8d-468f-9a29-e5047029b032
keywords:
- Сервицепаккмажор свойство Virtual PC
- Сервицепаккмажор свойство Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, свойство Сервицепаккмажор
topic_type:
- apiref
api_name:
- IVMGuestOS.ServicePackMajor
- IVMGuestOS.get_ServicePackMajor
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1fa89b51e26354ce2983ad42025b1b9a3922d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136186"
---
# <a name="ivmguestosservicepackmajor-property"></a><span data-ttu-id="7da15-106">Свойство Ивмгуестос:: Сервицепаккмажор</span><span class="sxs-lookup"><span data-stu-id="7da15-106">IVMGuestOS::ServicePackMajor property</span></span>

<span data-ttu-id="7da15-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7da15-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7da15-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7da15-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7da15-109">Основной номер версии пакета обновления гостевой операционной системы, работающей на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7da15-109">The major version of the service pack of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="7da15-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7da15-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da15-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7da15-111">Syntax</span></span>


```C++
HRESULT get_ServicePackMajor(
  [out, retval] BSTR *servicePackMajor
);
```



## <a name="property-value"></a><span data-ttu-id="7da15-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7da15-112">Property value</span></span>

<span data-ttu-id="7da15-113">Основной номер версии последнего установленного пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="7da15-113">The major version number of the latest Service Pack installed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7da15-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7da15-114">Error codes</span></span>



| <span data-ttu-id="7da15-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="7da15-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="7da15-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7da15-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7da15-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7da15-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="7da15-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7da15-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="7da15-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="7da15-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="7da15-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7da15-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="7da15-121"><dt>Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="7da15-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="7da15-122">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="7da15-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="7da15-123"><dt>Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_ </dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="7da15-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="7da15-124">Компоненты интеграции не установлены в этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7da15-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="7da15-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7da15-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="7da15-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7da15-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="7da15-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7da15-127">Requirements</span></span>



| <span data-ttu-id="7da15-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7da15-128">Requirement</span></span> | <span data-ttu-id="7da15-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7da15-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da15-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7da15-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7da15-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7da15-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7da15-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7da15-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7da15-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7da15-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7da15-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7da15-134">End of client support</span></span><br/>    | <span data-ttu-id="7da15-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7da15-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7da15-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="7da15-136">Product</span></span><br/>                  | <span data-ttu-id="7da15-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7da15-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7da15-138">Header</span><span class="sxs-lookup"><span data-stu-id="7da15-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7da15-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7da15-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7da15-140">IID</span><span class="sxs-lookup"><span data-stu-id="7da15-140">IID</span></span><br/>                      | <span data-ttu-id="7da15-141">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="7da15-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="7da15-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7da15-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da15-143">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="7da15-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

