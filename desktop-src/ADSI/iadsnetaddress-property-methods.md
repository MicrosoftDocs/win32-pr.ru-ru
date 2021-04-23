---
title: Методы свойств Иадснетаддресс (iAds. h)
description: Метод свойства интерфейса Иадснетаддресс задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадснетаддресс ADSI
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073033c703db8eaa55b05058d6d2bbc3d3167f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803167"
---
# <a name="iadsnetaddress-property-methods"></a><span data-ttu-id="6a78e-105">Методы свойств Иадснетаддресс</span><span class="sxs-lookup"><span data-stu-id="6a78e-105">IADsNetAddress Property Methods</span></span>

<span data-ttu-id="6a78e-106">Метод свойства интерфейса [**иадснетаддресс**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6a78e-106">The property method of the [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) interface sets the property described in the following table.</span></span> <span data-ttu-id="6a78e-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6a78e-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6a78e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="6a78e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6a78e-109">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="6a78e-109">**Address**</span></span>
<span data-ttu-id="6a78e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6a78e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6a78e-111">Сетевой адрес.</span><span class="sxs-lookup"><span data-stu-id="6a78e-111">A network address.</span></span>

<dt>

<span data-ttu-id="6a78e-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6a78e-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a78e-113">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="6a78e-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a78e-114">**AddressType**</span><span class="sxs-lookup"><span data-stu-id="6a78e-114">**AddressType**</span></span>
<span data-ttu-id="6a78e-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6a78e-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="6a78e-116">Тип протоколов связи.</span><span class="sxs-lookup"><span data-stu-id="6a78e-116">A type of communication protocols.</span></span>

<dt>

<span data-ttu-id="6a78e-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6a78e-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6a78e-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="6a78e-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="6a78e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6a78e-119">Requirements</span></span>



| <span data-ttu-id="6a78e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6a78e-120">Requirement</span></span> | <span data-ttu-id="6a78e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6a78e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a78e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a78e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6a78e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a78e-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a78e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a78e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6a78e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a78e-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a78e-126">Header</span><span class="sxs-lookup"><span data-stu-id="6a78e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a78e-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a78e-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="6a78e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6a78e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a78e-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a78e-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="6a78e-130">IID</span><span class="sxs-lookup"><span data-stu-id="6a78e-130">IID</span></span><br/>                      | <span data-ttu-id="6a78e-131">IID \_ иадснетаддресс определен как B21A50A9-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="6a78e-131">IID\_IADsNetAddress is defined as B21A50A9-4080-11D1-A3AC-00C04FB950DC</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6a78e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a78e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a78e-133">**IADsNetAddress**</span><span class="sxs-lookup"><span data-stu-id="6a78e-133">**IADsNetAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[<span data-ttu-id="6a78e-134">**ADS \_ нетаддресс**</span><span class="sxs-lookup"><span data-stu-id="6a78e-134">**ADS\_NETADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 





