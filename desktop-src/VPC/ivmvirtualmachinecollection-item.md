---
title: Свойство Item Ивмвиртуалмачинеколлектион (Впккоминтерфацес. h)
description: Извлекает объект виртуальной машины, соответствующий указанному индексу.
ms.assetid: b3afe211-5d97-4ccf-96b7-e074deb320fb
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмвиртуалмачинеколлектион
- Интерфейс Ивмвиртуалмачинеколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Item
- IVMVirtualMachineCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d70a6e30ff53f234f40803cd02fa16539f09e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071058"
---
# <a name="ivmvirtualmachinecollectionitem-property"></a><span data-ttu-id="4bf57-106">Свойство Ивмвиртуалмачинеколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="4bf57-106">IVMVirtualMachineCollection::Item property</span></span>

<span data-ttu-id="4bf57-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4bf57-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4bf57-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4bf57-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4bf57-109">Извлекает объект виртуальной машины, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="4bf57-109">Retrieves the virtual machine object that corresponds to the specified index.</span></span>

<span data-ttu-id="4bf57-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4bf57-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf57-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bf57-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="4bf57-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4bf57-112">Property value</span></span>

<span data-ttu-id="4bf57-113">Объект [**ивмвиртуалмачине**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="4bf57-113">The [**IVMVirtualMachine**](ivmvirtualmachine.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4bf57-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="4bf57-114">Error codes</span></span>



| <span data-ttu-id="4bf57-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="4bf57-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4bf57-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4bf57-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4bf57-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4bf57-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4bf57-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4bf57-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="4bf57-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="4bf57-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4bf57-120">Параметр *virtualMachine* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4bf57-120">The *virtualMachine* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="4bf57-121"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="4bf57-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="4bf57-122">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="4bf57-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="4bf57-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4bf57-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4bf57-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4bf57-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="4bf57-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4bf57-125">Requirements</span></span>



| <span data-ttu-id="4bf57-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4bf57-126">Requirement</span></span> | <span data-ttu-id="4bf57-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4bf57-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf57-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bf57-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4bf57-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4bf57-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4bf57-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bf57-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4bf57-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4bf57-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4bf57-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4bf57-132">End of client support</span></span><br/>    | <span data-ttu-id="4bf57-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4bf57-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="4bf57-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="4bf57-134">Product</span></span><br/>                  | <span data-ttu-id="4bf57-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4bf57-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="4bf57-136">Header</span><span class="sxs-lookup"><span data-stu-id="4bf57-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bf57-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bf57-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="4bf57-138">IID</span><span class="sxs-lookup"><span data-stu-id="4bf57-138">IID</span></span><br/>                      | <span data-ttu-id="4bf57-139">IID \_ ивмвиртуалмачинеколлектион определен как 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="4bf57-139">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bf57-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bf57-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf57-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="4bf57-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="4bf57-142">**ивмвиртуалмачинеколлектион**</span><span class="sxs-lookup"><span data-stu-id="4bf57-142">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

