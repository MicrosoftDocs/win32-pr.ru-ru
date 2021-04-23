---
title: Методы свойств Иадсднвисстринг (iAds. h)
description: Метод свойства интерфейса Иадсднвисстринг задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсднвисстринг ADSI
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa63a933a6a41eec9e6e55906a940cee650c87b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654622"
---
# <a name="iadsdnwithstring-property-methods"></a><span data-ttu-id="15672-105">Методы свойств Иадсднвисстринг</span><span class="sxs-lookup"><span data-stu-id="15672-105">IADsDNWithString Property Methods</span></span>

<span data-ttu-id="15672-106">Метод свойства интерфейса [**иадсднвисстринг**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="15672-106">The property method of the [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) interface sets the property described in the following table.</span></span> <span data-ttu-id="15672-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="15672-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="15672-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="15672-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="15672-109">**днстринг**</span><span class="sxs-lookup"><span data-stu-id="15672-109">**DNString**</span></span>
<span data-ttu-id="15672-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="15672-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="15672-111">Строка различающегося имени, связанная со строковым значением.</span><span class="sxs-lookup"><span data-stu-id="15672-111">The DN string associated with a string value.</span></span>

<dt>

<span data-ttu-id="15672-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15672-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15672-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="15672-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="15672-114">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="15672-114">**StringValue**</span></span>
<span data-ttu-id="15672-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="15672-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="15672-116">Строковое значение, связанное с DN объекта.</span><span class="sxs-lookup"><span data-stu-id="15672-116">The string value associated with a DN of an object.</span></span>

<dt>

<span data-ttu-id="15672-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="15672-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="15672-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="15672-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="15672-119">Требования</span><span class="sxs-lookup"><span data-stu-id="15672-119">Requirements</span></span>



| <span data-ttu-id="15672-120">Требование</span><span class="sxs-lookup"><span data-stu-id="15672-120">Requirement</span></span> | <span data-ttu-id="15672-121">Значение</span><span class="sxs-lookup"><span data-stu-id="15672-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15672-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15672-122">Minimum supported client</span></span><br/> | <span data-ttu-id="15672-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15672-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15672-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15672-124">Minimum supported server</span></span><br/> | <span data-ttu-id="15672-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15672-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15672-126">Header</span><span class="sxs-lookup"><span data-stu-id="15672-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="15672-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="15672-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="15672-128">DLL</span><span class="sxs-lookup"><span data-stu-id="15672-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15672-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15672-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="15672-130">IID</span><span class="sxs-lookup"><span data-stu-id="15672-130">IID</span></span><br/>                      | <span data-ttu-id="15672-131">IID \_ иадсднвисстринг определен как 370DF02E-F934-11d2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="15672-131">IID\_IADsDNWithString is defined as 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="15672-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15672-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15672-133">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="15672-133">**IADsDNWithString**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[<span data-ttu-id="15672-134">**\_DN AD \_ со \_ строкой**</span><span class="sxs-lookup"><span data-stu-id="15672-134">**ADS\_DN\_WITH\_STRING**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 





