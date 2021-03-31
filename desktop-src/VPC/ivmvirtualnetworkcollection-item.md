---
title: Свойство Item Ивмвиртуалнетворкколлектион (Впккоминтерфацес. h)
description: Объект Ивмвиртуалнетворк, соответствующий указанному индексу.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмвиртуалнетворкколлектион
- Интерфейс Ивмвиртуалнетворкколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac5a7648db4708fbc1b445029419ee794809abcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071716"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a><span data-ttu-id="88da0-106">Свойство Ивмвиртуалнетворкколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="88da0-106">IVMVirtualNetworkCollection::Item property</span></span>

<span data-ttu-id="88da0-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="88da0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="88da0-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="88da0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="88da0-109">Извлекает объект [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) , соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="88da0-109">Retrieves the [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="88da0-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="88da0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88da0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88da0-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="88da0-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="88da0-112">Property value</span></span>

<span data-ttu-id="88da0-113">Объект [**ивмвиртуалнетворк**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="88da0-113">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88da0-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="88da0-114">Error codes</span></span>



| <span data-ttu-id="88da0-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="88da0-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="88da0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="88da0-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="88da0-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="88da0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="88da0-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="88da0-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="88da0-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="88da0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="88da0-120">Параметр *virtualNetwork* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="88da0-120">The *virtualNetwork* parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="88da0-121"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="88da0-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="88da0-122">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="88da0-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="88da0-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="88da0-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="88da0-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="88da0-124">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="88da0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="88da0-125">Requirements</span></span>



| <span data-ttu-id="88da0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="88da0-126">Requirement</span></span> | <span data-ttu-id="88da0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="88da0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88da0-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88da0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="88da0-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="88da0-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="88da0-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88da0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="88da0-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="88da0-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="88da0-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="88da0-132">End of client support</span></span><br/>    | <span data-ttu-id="88da0-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88da0-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="88da0-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="88da0-134">Product</span></span><br/>                  | <span data-ttu-id="88da0-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="88da0-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="88da0-136">Header</span><span class="sxs-lookup"><span data-stu-id="88da0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="88da0-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="88da0-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="88da0-138">IID</span><span class="sxs-lookup"><span data-stu-id="88da0-138">IID</span></span><br/>                      | <span data-ttu-id="88da0-139">IID \_ ивмвиртуалнетворкколлектион определен как 8ed680be-4242-4b2a-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="88da0-139">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88da0-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88da0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88da0-141">**ивмвиртуалнетворк**</span><span class="sxs-lookup"><span data-stu-id="88da0-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> <dt>

[<span data-ttu-id="88da0-142">**ивмвиртуалнетворкколлектион**</span><span class="sxs-lookup"><span data-stu-id="88da0-142">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

