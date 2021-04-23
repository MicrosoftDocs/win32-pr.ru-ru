---
title: Методы свойств Иадспосталаддресс (iAds. h)
description: Метод свойства интерфейса Иадспосталаддресс задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспосталаддресс ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d8eeaac8fa258a2df1452b8aa261ee59b3cc85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654611"
---
# <a name="iadspostaladdress-property-methods"></a><span data-ttu-id="96a56-105">Методы свойств Иадспосталаддресс</span><span class="sxs-lookup"><span data-stu-id="96a56-105">IADsPostalAddress Property Methods</span></span>

<span data-ttu-id="96a56-106">Метод свойства интерфейса [**иадспосталаддресс**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="96a56-106">The property method of the [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) interface sets the property described in the following table.</span></span> <span data-ttu-id="96a56-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="96a56-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="96a56-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="96a56-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="96a56-109">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="96a56-109">**PostalAddress**</span></span>
<span data-ttu-id="96a56-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96a56-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="96a56-111">Массив из шести строк, содержащих почтовый адрес пользователя.</span><span class="sxs-lookup"><span data-stu-id="96a56-111">An array of six strings holding the postal address of the user.</span></span>

<dt>

<span data-ttu-id="96a56-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="96a56-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96a56-113">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="96a56-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="96a56-114">Требования</span><span class="sxs-lookup"><span data-stu-id="96a56-114">Requirements</span></span>



| <span data-ttu-id="96a56-115">Требование</span><span class="sxs-lookup"><span data-stu-id="96a56-115">Requirement</span></span> | <span data-ttu-id="96a56-116">Значение</span><span class="sxs-lookup"><span data-stu-id="96a56-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96a56-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96a56-117">Minimum supported client</span></span><br/> | <span data-ttu-id="96a56-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96a56-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96a56-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96a56-119">Minimum supported server</span></span><br/> | <span data-ttu-id="96a56-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96a56-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96a56-121">Header</span><span class="sxs-lookup"><span data-stu-id="96a56-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="96a56-122"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="96a56-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="96a56-123">DLL</span><span class="sxs-lookup"><span data-stu-id="96a56-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96a56-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96a56-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="96a56-125">IID</span><span class="sxs-lookup"><span data-stu-id="96a56-125">IID</span></span><br/>                      | <span data-ttu-id="96a56-126">IID \_ иадспосталаддресс определен как 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="96a56-126">IID\_IADsPostalAddress is defined as 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="96a56-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96a56-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a56-128">**IADsPostalAddress**</span><span class="sxs-lookup"><span data-stu-id="96a56-128">**IADsPostalAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[<span data-ttu-id="96a56-129">**ADS \_ посталаддресс**</span><span class="sxs-lookup"><span data-stu-id="96a56-129">**ADS\_POSTALADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 





