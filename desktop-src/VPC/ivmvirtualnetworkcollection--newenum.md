---
title: Свойство _NewEnum Ивмвиртуалнетворкколлектион (Впккоминтерфацес. h)
description: Возвращает перечислитель для коллекции. | Свойство _NewEnum Ивмвиртуалнетворкколлектион (Впккоминтерфацес. h)
ms.assetid: 3ea01a88-72ec-4dc0-901f-e48092cf9251
keywords:
- _NewEnum свойств Virtual PC
- _NewEnum свойств Virtual PC, интерфейс Ивмвиртуалнетворкколлектион
- Ивмвиртуалнетворкколлектион интерфейс Virtual PC, свойство _NewEnum
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection._NewEnum
- IVMVirtualNetworkCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50a279e3f160a79f143a7516e29c0dbc3eccdf4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273654"
---
# <a name="ivmvirtualnetworkcollection_newenum-property"></a><span data-ttu-id="2b825-107">Свойство Ивмвиртуалнетворкколлектион:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="2b825-107">IVMVirtualNetworkCollection::\_NewEnum property</span></span>

<span data-ttu-id="2b825-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2b825-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2b825-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2b825-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2b825-110">Возвращает перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="2b825-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="2b825-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2b825-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b825-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b825-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="2b825-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2b825-113">Property value</span></span>

<span data-ttu-id="2b825-114">Перечислитель [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="2b825-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2b825-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2b825-115">Error codes</span></span>



| <span data-ttu-id="2b825-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="2b825-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2b825-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2b825-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="2b825-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2b825-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2b825-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2b825-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="2b825-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2b825-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2b825-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b825-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="2b825-122"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2b825-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2b825-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2b825-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2b825-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2b825-124">Requirements</span></span>



| <span data-ttu-id="2b825-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2b825-125">Requirement</span></span> | <span data-ttu-id="2b825-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2b825-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b825-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b825-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2b825-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2b825-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b825-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b825-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2b825-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2b825-130">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2b825-131">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2b825-131">End of client support</span></span><br/>    | <span data-ttu-id="2b825-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b825-132">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="2b825-133">Продукт</span><span class="sxs-lookup"><span data-stu-id="2b825-133">Product</span></span><br/>                  | <span data-ttu-id="2b825-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2b825-134">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="2b825-135">Header</span><span class="sxs-lookup"><span data-stu-id="2b825-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b825-136"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b825-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="2b825-137">IID</span><span class="sxs-lookup"><span data-stu-id="2b825-137">IID</span></span><br/>                      | <span data-ttu-id="2b825-138">IID \_ ивмвиртуалнетворкколлектион определен как 8ed680be-4242-4b2a-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="2b825-138">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b825-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b825-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b825-140">**ивмвиртуалнетворкколлектион**</span><span class="sxs-lookup"><span data-stu-id="2b825-140">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

