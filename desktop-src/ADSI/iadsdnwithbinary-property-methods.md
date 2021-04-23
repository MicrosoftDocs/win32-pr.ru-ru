---
title: Методы свойств Иадсднвисбинари (iAds. h)
description: Метод свойства интерфейса Иадсднвисбинари задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсднвисбинари ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf0398a141596de677d7d1739e84ff7525da9a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136878"
---
# <a name="iadsdnwithbinary-property-methods"></a><span data-ttu-id="6fddd-105">Методы свойств Иадсднвисбинари</span><span class="sxs-lookup"><span data-stu-id="6fddd-105">IADsDNWithBinary Property Methods</span></span>

<span data-ttu-id="6fddd-106">Метод свойства интерфейса [**иадсднвисбинари**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6fddd-106">The property method of the [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) interface sets the property described in the following table.</span></span> <span data-ttu-id="6fddd-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6fddd-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6fddd-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="6fddd-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6fddd-109">**бинаривалуе**</span><span class="sxs-lookup"><span data-stu-id="6fddd-109">**BinaryValue**</span></span>
<span data-ttu-id="6fddd-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6fddd-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6fddd-111">Идентификатор GUID объекта, связанного с различающимся именем.</span><span class="sxs-lookup"><span data-stu-id="6fddd-111">The GUID of an object associated with a DN.</span></span>

<dt>

<span data-ttu-id="6fddd-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6fddd-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6fddd-113">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="6fddd-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6fddd-114">**днстринг**</span><span class="sxs-lookup"><span data-stu-id="6fddd-114">**DNString**</span></span>
<span data-ttu-id="6fddd-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6fddd-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="6fddd-116">Строка различающегося имени, связанная с идентификатором GUID объекта.</span><span class="sxs-lookup"><span data-stu-id="6fddd-116">The DN string associated with the GUID of an object.</span></span>

<dt>

<span data-ttu-id="6fddd-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6fddd-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6fddd-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6fddd-118">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="6fddd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6fddd-119">Requirements</span></span>



| <span data-ttu-id="6fddd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6fddd-120">Requirement</span></span> | <span data-ttu-id="6fddd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6fddd-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fddd-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fddd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6fddd-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fddd-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6fddd-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fddd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6fddd-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fddd-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6fddd-126">Header</span><span class="sxs-lookup"><span data-stu-id="6fddd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fddd-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fddd-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="6fddd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6fddd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fddd-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fddd-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="6fddd-130">IID</span><span class="sxs-lookup"><span data-stu-id="6fddd-130">IID</span></span><br/>                      | <span data-ttu-id="6fddd-131">IID \_ иадсднвисбинари определен как 7E99C0A2-F935-11d2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="6fddd-131">IID\_IADsDNWithBinary is defined as 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="6fddd-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fddd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fddd-133">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="6fddd-133">**IADsDNWithBinary**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[<span data-ttu-id="6fddd-134">**\_DN AD \_ с \_ двоичными данными**</span><span class="sxs-lookup"><span data-stu-id="6fddd-134">**ADS\_DN\_WITH\_BINARY**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 





