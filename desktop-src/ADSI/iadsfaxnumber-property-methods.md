---
title: Методы свойств Иадсфакснумбер (iAds. h)
description: Метод свойства интерфейса Иадсфакснумбер задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: f4d46b9d-8db2-47b3-b489-9ffc363e6ac6
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсфакснумбер ADSI
topic_type:
- apiref
api_name:
- IADsFaxNumber Property Methods
- IADsFaxNumber.TelephoneNumber
- IADsFaxNumber.get_TelephoneNumber
- IADsFaxNumber.put_TelephoneNumber
- IADsFaxNumber.Parameters
- IADsFaxNumber.get_Parameters
- IADsFaxNumber.put_Parameters
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e2d982aee794272f80e58385be34098a92a28e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654619"
---
# <a name="iadsfaxnumber-property-methods"></a><span data-ttu-id="38a54-105">Методы свойств Иадсфакснумбер</span><span class="sxs-lookup"><span data-stu-id="38a54-105">IADsFaxNumber Property Methods</span></span>

<span data-ttu-id="38a54-106">Метод свойства интерфейса [**иадсфакснумбер**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="38a54-106">The property method of the [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) interface sets the property described in the following table.</span></span> <span data-ttu-id="38a54-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="38a54-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="38a54-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="38a54-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="38a54-109">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="38a54-109">**Parameters**</span></span>
<span data-ttu-id="38a54-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="38a54-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="38a54-111">Параметры для факсового компьютера.</span><span class="sxs-lookup"><span data-stu-id="38a54-111">The parameters for the fax machine.</span></span>

<dt>

<span data-ttu-id="38a54-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="38a54-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38a54-113">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="38a54-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parameters(
  [out] VARIANT* retval
);
HRESULT put_Parameters(
  [in] VARIANT vParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="38a54-114">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="38a54-114">**TelephoneNumber**</span></span>
<span data-ttu-id="38a54-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="38a54-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="38a54-116">Номер телефона факсимильного компьютера.</span><span class="sxs-lookup"><span data-stu-id="38a54-116">The telephone number of the fax machine.</span></span>

<dt>

<span data-ttu-id="38a54-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="38a54-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="38a54-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="38a54-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* retVal
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="38a54-119">Требования</span><span class="sxs-lookup"><span data-stu-id="38a54-119">Requirements</span></span>



| <span data-ttu-id="38a54-120">Требование</span><span class="sxs-lookup"><span data-stu-id="38a54-120">Requirement</span></span> | <span data-ttu-id="38a54-121">Значение</span><span class="sxs-lookup"><span data-stu-id="38a54-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38a54-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38a54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="38a54-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38a54-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38a54-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38a54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="38a54-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38a54-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38a54-126">Header</span><span class="sxs-lookup"><span data-stu-id="38a54-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="38a54-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="38a54-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="38a54-128">DLL</span><span class="sxs-lookup"><span data-stu-id="38a54-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38a54-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38a54-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="38a54-130">IID</span><span class="sxs-lookup"><span data-stu-id="38a54-130">IID</span></span><br/>                      | <span data-ttu-id="38a54-131">IID \_ иадсфакснумбер определен как A910DEA9-4680-11D1-0A3B-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="38a54-131">IID\_IADsFaxNumber is defined as A910DEA9-4680-11D1-0A3B-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="38a54-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38a54-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a54-133">**IADsFaxNumber**</span><span class="sxs-lookup"><span data-stu-id="38a54-133">**IADsFaxNumber**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[<span data-ttu-id="38a54-134">**ADS \_ факснумбер**</span><span class="sxs-lookup"><span data-stu-id="38a54-134">**ADS\_FAXNUMBER**</span></span>](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 





