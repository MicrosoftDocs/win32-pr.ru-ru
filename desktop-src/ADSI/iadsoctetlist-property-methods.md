---
title: Методы свойств Иадсоктетлист (iAds. h)
description: Метод свойства интерфейса Иадсоктетлист задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсоктетлист ADSI
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3631adaf00cf599214296e1792ffab8697ba5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989093"
---
# <a name="iadsoctetlist-property-methods"></a><span data-ttu-id="33049-105">Методы свойств Иадсоктетлист</span><span class="sxs-lookup"><span data-stu-id="33049-105">IADsOctetList Property Methods</span></span>

<span data-ttu-id="33049-106">Метод свойства интерфейса [**иадсоктетлист**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="33049-106">The property method of the [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) interface sets the property described in the following table.</span></span> <span data-ttu-id="33049-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="33049-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="33049-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="33049-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="33049-109">**октетлист**</span><span class="sxs-lookup"><span data-stu-id="33049-109">**OctetList**</span></span>
<span data-ttu-id="33049-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="33049-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="33049-111">Упорядоченная последовательность массивов байтов.</span><span class="sxs-lookup"><span data-stu-id="33049-111">An ordered sequence of byte arrays.</span></span>

<dt>

<span data-ttu-id="33049-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="33049-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="33049-113">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="33049-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="33049-114">Требования</span><span class="sxs-lookup"><span data-stu-id="33049-114">Requirements</span></span>



| <span data-ttu-id="33049-115">Требование</span><span class="sxs-lookup"><span data-stu-id="33049-115">Requirement</span></span> | <span data-ttu-id="33049-116">Значение</span><span class="sxs-lookup"><span data-stu-id="33049-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33049-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33049-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33049-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33049-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33049-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33049-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33049-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33049-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33049-121">Header</span><span class="sxs-lookup"><span data-stu-id="33049-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="33049-122"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="33049-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="33049-123">DLL</span><span class="sxs-lookup"><span data-stu-id="33049-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33049-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33049-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="33049-125">IID</span><span class="sxs-lookup"><span data-stu-id="33049-125">IID</span></span><br/>                      | <span data-ttu-id="33049-126">IID \_ иадсоктетлист определен как 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="33049-126">IID\_IADsOctetList is defined as 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="33049-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33049-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33049-128">**IADsOctetList**</span><span class="sxs-lookup"><span data-stu-id="33049-128">**IADsOctetList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[<span data-ttu-id="33049-129">**\_список октетов ADS \_**</span><span class="sxs-lookup"><span data-stu-id="33049-129">**ADS\_OCTET\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 





