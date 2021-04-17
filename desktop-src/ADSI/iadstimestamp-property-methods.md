---
title: Методы свойств Иадстиместамп (iAds. h)
description: Метод свойства интерфейса Иадстиместамп задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадстиместамп ADSI
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77db7a6a3b3814cd10beca5da5e3166ab1b61a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490239"
---
# <a name="iadstimestamp-property-methods"></a><span data-ttu-id="c5f53-105">Методы свойств Иадстиместамп</span><span class="sxs-lookup"><span data-stu-id="c5f53-105">IADsTimestamp Property Methods</span></span>

<span data-ttu-id="c5f53-106">Метод свойства интерфейса [**иадстиместамп**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c5f53-106">The property method of the [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) interface sets the property described in the following table.</span></span> <span data-ttu-id="c5f53-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c5f53-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c5f53-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="c5f53-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c5f53-109">**EventID**</span><span class="sxs-lookup"><span data-stu-id="c5f53-109">**EventID**</span></span>
<span data-ttu-id="c5f53-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c5f53-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c5f53-111">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="c5f53-111">An event identifier.</span></span>

<dt>

<span data-ttu-id="c5f53-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c5f53-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c5f53-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="c5f53-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c5f53-114">**вхолесекондс**</span><span class="sxs-lookup"><span data-stu-id="c5f53-114">**WholeSeconds**</span></span>
<span data-ttu-id="c5f53-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c5f53-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="c5f53-116">Количество секунд с нулевым значением 12:00 AM, 1970 января, UTC.</span><span class="sxs-lookup"><span data-stu-id="c5f53-116">Number of seconds with zero value being 12:00 AM, January 1970, UTC.</span></span>

<dt>

<span data-ttu-id="c5f53-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c5f53-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c5f53-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="c5f53-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="c5f53-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c5f53-119">Requirements</span></span>



| <span data-ttu-id="c5f53-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c5f53-120">Requirement</span></span> | <span data-ttu-id="c5f53-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c5f53-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f53-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5f53-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c5f53-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5f53-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5f53-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5f53-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c5f53-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5f53-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5f53-126">Header</span><span class="sxs-lookup"><span data-stu-id="c5f53-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5f53-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5f53-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c5f53-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c5f53-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5f53-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5f53-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5f53-130">IID</span><span class="sxs-lookup"><span data-stu-id="c5f53-130">IID</span></span><br/>                      | <span data-ttu-id="c5f53-131">IID \_ иадстиместамп определен как B2F5A901-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="c5f53-131">IID\_IADsTimestamp is defined as B2F5A901-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c5f53-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5f53-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f53-133">**IADsTimestamp**</span><span class="sxs-lookup"><span data-stu-id="c5f53-133">**IADsTimestamp**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[<span data-ttu-id="c5f53-134">**\_Метка времени ADS**</span><span class="sxs-lookup"><span data-stu-id="c5f53-134">**ADS\_TIMESTAMP**</span></span>](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





