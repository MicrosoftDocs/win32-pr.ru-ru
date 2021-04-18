---
title: Методы свойств Иадсларжеинтежер (iAds. h)
description: Методы свойств интерфейса Иадсларжеинтежер получают и задают свойства, описанные в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсларжеинтежер ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 097e9ae7387658f983c691e56e4f90ba40dea407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654616"
---
# <a name="iadslargeinteger-property-methods"></a><span data-ttu-id="b15ce-105">Методы свойств Иадсларжеинтежер</span><span class="sxs-lookup"><span data-stu-id="b15ce-105">IADsLargeInteger Property Methods</span></span>

<span data-ttu-id="b15ce-106">Методы свойств интерфейса [**иадсларжеинтежер**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) получают и задают свойства, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b15ce-106">The property methods of the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface get and set the properties described in the following table.</span></span> <span data-ttu-id="b15ce-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b15ce-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b15ce-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="b15ce-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b15ce-109">**хигхпарт**</span><span class="sxs-lookup"><span data-stu-id="b15ce-109">**HighPart**</span></span>
<span data-ttu-id="b15ce-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b15ce-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="b15ce-111">Верхняя часть целого числа.</span><span class="sxs-lookup"><span data-stu-id="b15ce-111">The high part of the integer.</span></span>

<dt>

<span data-ttu-id="b15ce-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b15ce-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b15ce-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="b15ce-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b15ce-114">**ловпарт**</span><span class="sxs-lookup"><span data-stu-id="b15ce-114">**LowPart**</span></span>
<span data-ttu-id="b15ce-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b15ce-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="b15ce-116">Нижняя часть целого числа.</span><span class="sxs-lookup"><span data-stu-id="b15ce-116">The low part of the integer.</span></span>

<dt>

<span data-ttu-id="b15ce-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b15ce-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b15ce-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="b15ce-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="b15ce-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b15ce-119">Remarks</span></span>

<span data-ttu-id="b15ce-120">Если Ларжеинт имеет тип **ларжеинтежер** , его значение задается параметрами **хигхпарт** и **ловпарт** в соответствии со следующей формулой.</span><span class="sxs-lookup"><span data-stu-id="b15ce-120">If largeInt is of the **LargeInteger** type, its value is specified by those of **HighPart** and **LowPart** according to the following formula.</span></span>


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a><span data-ttu-id="b15ce-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="b15ce-121">Examples</span></span>

<span data-ttu-id="b15ce-122">В следующем примере кода Visual Basic для большого целого числа устанавливается значение 43937327281.</span><span class="sxs-lookup"><span data-stu-id="b15ce-122">The following Visual Basic code example sets a large integer to 43937327281.</span></span>


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a><span data-ttu-id="b15ce-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b15ce-123">Requirements</span></span>



| <span data-ttu-id="b15ce-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b15ce-124">Requirement</span></span> | <span data-ttu-id="b15ce-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b15ce-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b15ce-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b15ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b15ce-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b15ce-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b15ce-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b15ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b15ce-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b15ce-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b15ce-130">Header</span><span class="sxs-lookup"><span data-stu-id="b15ce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b15ce-131"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="b15ce-131"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b15ce-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b15ce-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b15ce-133"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b15ce-133"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b15ce-134">IID</span><span class="sxs-lookup"><span data-stu-id="b15ce-134">IID</span></span><br/>                      | <span data-ttu-id="b15ce-135">IID \_ иадсларжеинтежер определен как 9068270B-0939-11D1-8BE1-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="b15ce-135">IID\_IADsLargeInteger is defined as 9068270B-0939-11D1-8BE1-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="b15ce-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b15ce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15ce-137">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="b15ce-137">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





