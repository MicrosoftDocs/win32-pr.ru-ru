---
title: Методы свойств Иадскасеигнорелист (iAds. h)
description: Метод свойства интерфейса Иадскасеигнорелист задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадскасеигнорелист ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aabf26508c3e38e117ad25721af8bece5d69b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654624"
---
# <a name="iadscaseignorelist-property-methods"></a><span data-ttu-id="0d51d-105">Методы свойств Иадскасеигнорелист</span><span class="sxs-lookup"><span data-stu-id="0d51d-105">IADsCaseIgnoreList Property Methods</span></span>

<span data-ttu-id="0d51d-106">Метод свойства интерфейса [**иадскасеигнорелист**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0d51d-106">The property method of the [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) interface sets the property described in the following table.</span></span> <span data-ttu-id="0d51d-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="0d51d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0d51d-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="0d51d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="0d51d-109">**касеигнорелист**</span><span class="sxs-lookup"><span data-stu-id="0d51d-109">**CaseIgnoreList**</span></span>
<span data-ttu-id="0d51d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d51d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d51d-111">Упорядоченная последовательность строк без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="0d51d-111">An ordered sequence of case insensitive strings.</span></span>

<dt>

<span data-ttu-id="0d51d-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d51d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d51d-113">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="0d51d-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="0d51d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0d51d-114">Requirements</span></span>



| <span data-ttu-id="0d51d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0d51d-115">Requirement</span></span> | <span data-ttu-id="0d51d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0d51d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d51d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d51d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d51d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d51d-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d51d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d51d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d51d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d51d-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d51d-121">Header</span><span class="sxs-lookup"><span data-stu-id="0d51d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d51d-122"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d51d-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="0d51d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0d51d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d51d-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d51d-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d51d-125">IID</span><span class="sxs-lookup"><span data-stu-id="0d51d-125">IID</span></span><br/>                      | <span data-ttu-id="0d51d-126">IID \_ иадскасеигнорелист определен как 7B66B533-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="0d51d-126">IID\_IADsCaseIgnoreList is defined as 7B66B533-4680-11D1-A3B4-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="0d51d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d51d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d51d-128">**IADsCaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="0d51d-128">**IADsCaseIgnoreList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[<span data-ttu-id="0d51d-129">**\_список ADS касеигноре \_**</span><span class="sxs-lookup"><span data-stu-id="0d51d-129">**ADS\_CASEIGNORE\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





