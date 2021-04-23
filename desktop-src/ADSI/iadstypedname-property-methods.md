---
title: Методы свойств Иадстипеднаме (iAds. h)
description: Метод свойства интерфейса Иадстипеднаме задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 0097c7c0-91f9-4874-93f2-c24900054a49
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадстипеднаме ADSI
topic_type:
- apiref
api_name:
- IADsTypedName Property Methods
- IADsTypedName.ObjectName
- IADsTypedName.get_ObjectName
- IADsTypedName.put_ObjectName
- IADsTypedName.Level
- IADsTypedName.get_Level
- IADsTypedName.put_Level
- IADsTypedName.Interval
- IADsTypedName.get_Interval
- IADsTypedName.put_Interval
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a90e3c3950fb3912e2fe206048053bec6322be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654481"
---
# <a name="iadstypedname-property-methods"></a><span data-ttu-id="c80ed-105">Методы свойств Иадстипеднаме</span><span class="sxs-lookup"><span data-stu-id="c80ed-105">IADsTypedName Property Methods</span></span>

<span data-ttu-id="c80ed-106">Метод свойства интерфейса [**иадстипеднаме**](/windows/desktop/api/Iads/nn-iads-iadstypedname) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c80ed-106">The property method of the [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) interface sets the property described in the following table.</span></span> <span data-ttu-id="c80ed-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c80ed-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c80ed-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="c80ed-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c80ed-109">**Интервал**</span><span class="sxs-lookup"><span data-stu-id="c80ed-109">**Interval**</span></span>
<span data-ttu-id="c80ed-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c80ed-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c80ed-111">Частота ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="c80ed-111">The frequency of reference of the object.</span></span>

<dt>

<span data-ttu-id="c80ed-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c80ed-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c80ed-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="c80ed-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Interval(
  [out] LONG* retval
);
HRESULT put_Interval(
  [in] LONG lnInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c80ed-114">**Уровень**</span><span class="sxs-lookup"><span data-stu-id="c80ed-114">**Level**</span></span>
<span data-ttu-id="c80ed-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c80ed-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="c80ed-116">Уровень приоритета, связанный с объектом.</span><span class="sxs-lookup"><span data-stu-id="c80ed-116">The priority level associated with the object.</span></span>

<dt>

<span data-ttu-id="c80ed-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c80ed-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c80ed-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="c80ed-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Level(
  [out] LONG* retval
);
HRESULT put_Level(
  [in] LONG lnLevel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c80ed-119">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="c80ed-119">**ObjectName**</span></span>
<span data-ttu-id="c80ed-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c80ed-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="c80ed-121">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c80ed-121">The name of an object.</span></span>

<dt>

<span data-ttu-id="c80ed-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c80ed-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c80ed-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c80ed-123">Scripting data type: **BSTR**</span></span>
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

 

## <a name="requirements"></a><span data-ttu-id="c80ed-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c80ed-124">Requirements</span></span>



| <span data-ttu-id="c80ed-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c80ed-125">Requirement</span></span> | <span data-ttu-id="c80ed-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c80ed-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c80ed-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c80ed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c80ed-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c80ed-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c80ed-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c80ed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c80ed-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c80ed-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c80ed-131">Header</span><span class="sxs-lookup"><span data-stu-id="c80ed-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c80ed-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="c80ed-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c80ed-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c80ed-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c80ed-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c80ed-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c80ed-135">IID</span><span class="sxs-lookup"><span data-stu-id="c80ed-135">IID</span></span><br/>                      | <span data-ttu-id="c80ed-136">IID \_ иадстипеднаме определен как B371A349-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="c80ed-136">IID\_IADsTypedName is defined as B371A349-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c80ed-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c80ed-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c80ed-138">**IADsTypedName**</span><span class="sxs-lookup"><span data-stu-id="c80ed-138">**IADsTypedName**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstypedname)
</dt> <dt>

[<span data-ttu-id="c80ed-139">**ADS \_ типеднаме**</span><span class="sxs-lookup"><span data-stu-id="c80ed-139">**ADS\_TYPEDNAME**</span></span>](/windows/win32/api/iads/ns-iads-ads_typedname)
</dt> </dl>

 

 





