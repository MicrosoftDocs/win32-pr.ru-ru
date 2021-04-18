---
title: Свойство Ивмдвддривеколлектион Count (Впккоминтерфацес. h)
description: Возвращает число дисководов компакт-и DVD в этой коллекции.
ms.assetid: 22e39c42-1f98-4680-a97e-0d329dc608e2
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмдвддривеколлектион
- Ивмдвддривеколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Count
- IVMDVDDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9ea713810348c0bd78c7de307600fc6ac9adc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691871"
---
# <a name="ivmdvddrivecollectioncount-property"></a><span data-ttu-id="a3f3f-106">Свойство Ивмдвддривеколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="a3f3f-106">IVMDVDDriveCollection::Count property</span></span>

<span data-ttu-id="a3f3f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a3f3f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a3f3f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a3f3f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a3f3f-109">Возвращает число дисководов компакт-и DVD в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="a3f3f-109">Retrieves the number of CD and DVD drives in this collection.</span></span>

<span data-ttu-id="a3f3f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a3f3f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f3f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3f3f-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="a3f3f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a3f3f-112">Property value</span></span>

<span data-ttu-id="a3f3f-113">Число дисководов компакт-дисков и дисков DVD.</span><span class="sxs-lookup"><span data-stu-id="a3f3f-113">The number of CD and DVD drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3f3f-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a3f3f-114">Error codes</span></span>



| <span data-ttu-id="a3f3f-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="a3f3f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a3f3f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a3f3f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a3f3f-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a3f3f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a3f3f-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a3f3f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a3f3f-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="a3f3f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a3f3f-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a3f3f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a3f3f-121"><dt>Д \_ Сбой</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="a3f3f-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="a3f3f-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a3f3f-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="a3f3f-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3f3f-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="a3f3f-124">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="a3f3f-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="a3f3f-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a3f3f-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a3f3f-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a3f3f-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a3f3f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a3f3f-127">Requirements</span></span>



| <span data-ttu-id="a3f3f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a3f3f-128">Requirement</span></span> | <span data-ttu-id="a3f3f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a3f3f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f3f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3f3f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a3f3f-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a3f3f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a3f3f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3f3f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a3f3f-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a3f3f-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a3f3f-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a3f3f-134">End of client support</span></span><br/>    | <span data-ttu-id="a3f3f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3f3f-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a3f3f-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="a3f3f-136">Product</span></span><br/>                  | <span data-ttu-id="a3f3f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a3f3f-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a3f3f-138">Header</span><span class="sxs-lookup"><span data-stu-id="a3f3f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3f3f-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f3f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a3f3f-140">IID</span><span class="sxs-lookup"><span data-stu-id="a3f3f-140">IID</span></span><br/>                      | <span data-ttu-id="a3f3f-141">IID \_ ивмдвддривеколлектион определен как bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="a3f3f-141">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="a3f3f-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3f3f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f3f-143">**ивмдвддривеколлектион**</span><span class="sxs-lookup"><span data-stu-id="a3f3f-143">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

