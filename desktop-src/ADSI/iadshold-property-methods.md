---
title: Методы свойств Иадшолд (iAds. h)
description: Метод свойства интерфейса Иадшолд задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадшолд ADSI
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae2499efb461e6c13397fdaef75e515f0a1a21a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136870"
---
# <a name="iadshold-property-methods"></a><span data-ttu-id="1579a-105">Методы свойств Иадшолд</span><span class="sxs-lookup"><span data-stu-id="1579a-105">IADsHold Property Methods</span></span>

<span data-ttu-id="1579a-106">Метод свойства интерфейса [**иадшолд**](/windows/desktop/api/Iads/nn-iads-iadshold) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1579a-106">The property method of the [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) interface sets the property described in the following table.</span></span> <span data-ttu-id="1579a-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1579a-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1579a-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="1579a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="1579a-109">**Сумма**</span><span class="sxs-lookup"><span data-stu-id="1579a-109">**Amount**</span></span>
<span data-ttu-id="1579a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1579a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="1579a-111">Сумма расходов, взимаемых по отношению к пользователю за период удержания, в то время как сервер проверяет баланс учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="1579a-111">The amount of charges levied against the user for the period on hold while the server checks the account balance of the user.</span></span>

<dt>

<span data-ttu-id="1579a-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1579a-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1579a-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="1579a-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1579a-114">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="1579a-114">**ObjectName**</span></span>
<span data-ttu-id="1579a-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1579a-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="1579a-116">Имя объекта, представляющего пользователя при удержании.</span><span class="sxs-lookup"><span data-stu-id="1579a-116">The name of the object representing a user on hold.</span></span>

<dt>

<span data-ttu-id="1579a-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1579a-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1579a-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1579a-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="1579a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1579a-119">Requirements</span></span>



| <span data-ttu-id="1579a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1579a-120">Requirement</span></span> | <span data-ttu-id="1579a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1579a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1579a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1579a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1579a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1579a-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1579a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1579a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1579a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1579a-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1579a-126">Header</span><span class="sxs-lookup"><span data-stu-id="1579a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1579a-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="1579a-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="1579a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1579a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1579a-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1579a-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="1579a-130">IID</span><span class="sxs-lookup"><span data-stu-id="1579a-130">IID</span></span><br/>                      | <span data-ttu-id="1579a-131">IID \_ иадшолд определен как B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="1579a-131">IID\_IADsHold is defined as B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="1579a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1579a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1579a-133">**IADsHold**</span><span class="sxs-lookup"><span data-stu-id="1579a-133">**IADsHold**</span></span>](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





