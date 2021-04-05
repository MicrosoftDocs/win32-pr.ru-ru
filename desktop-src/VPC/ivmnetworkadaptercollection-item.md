---
title: Свойство Item Ивмнетворкадаптерколлектион (Впккоминтерфацес. h)
description: Объект Ивмнетворкадаптер, соответствующий указанному индексу.
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмнетворкадаптерколлектион
- Интерфейс Ивмнетворкадаптерколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d2f7ee389938a44c6608241fb3fb2d48ec1bca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989304"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a><span data-ttu-id="63fda-106">Свойство Ивмнетворкадаптерколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="63fda-106">IVMNetworkAdapterCollection::Item property</span></span>

<span data-ttu-id="63fda-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63fda-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63fda-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63fda-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63fda-109">Извлекает объект [**ивмнетворкадаптер**](ivmnetworkadapter.md) , соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="63fda-109">Retrieves the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="63fda-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="63fda-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63fda-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63fda-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a><span data-ttu-id="63fda-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="63fda-112">Property value</span></span>

<span data-ttu-id="63fda-113">Объект [**ивмнетворкадаптер**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="63fda-113">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63fda-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="63fda-114">Error codes</span></span>



| <span data-ttu-id="63fda-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="63fda-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="63fda-116">Значение</span><span class="sxs-lookup"><span data-stu-id="63fda-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63fda-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63fda-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="63fda-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="63fda-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="63fda-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="63fda-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="63fda-120">Параметр *networkInterface* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="63fda-120">The *networkInterface* parameter is **NULL**.</span></span> <br/>                                      |
| <dl> <span data-ttu-id="63fda-121"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="63fda-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="63fda-122">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="63fda-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="63fda-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="63fda-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="63fda-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="63fda-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="63fda-125">Требования</span><span class="sxs-lookup"><span data-stu-id="63fda-125">Requirements</span></span>



| <span data-ttu-id="63fda-126">Требование</span><span class="sxs-lookup"><span data-stu-id="63fda-126">Requirement</span></span> | <span data-ttu-id="63fda-127">Значение</span><span class="sxs-lookup"><span data-stu-id="63fda-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63fda-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63fda-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63fda-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63fda-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63fda-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63fda-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63fda-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="63fda-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="63fda-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="63fda-132">End of client support</span></span><br/>    | <span data-ttu-id="63fda-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63fda-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="63fda-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="63fda-134">Product</span></span><br/>                  | <span data-ttu-id="63fda-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63fda-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="63fda-136">Header</span><span class="sxs-lookup"><span data-stu-id="63fda-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="63fda-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="63fda-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="63fda-138">IID</span><span class="sxs-lookup"><span data-stu-id="63fda-138">IID</span></span><br/>                      | <span data-ttu-id="63fda-139">IID \_ ивмнетворкадаптерколлектион определен как ebaeafe9-EBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="63fda-139">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63fda-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63fda-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63fda-141">**ивмнетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="63fda-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="63fda-142">**ивмнетворкадаптерколлектион**</span><span class="sxs-lookup"><span data-stu-id="63fda-142">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

