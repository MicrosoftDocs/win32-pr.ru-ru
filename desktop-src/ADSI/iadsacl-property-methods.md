---
title: Методы свойств Иадсакл (iAds. h)
description: Метод свойства интерфейса Иадсакл задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсакл ADSI
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d8afb1ba3cbf7749ad8e3d14fa970662715909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492018"
---
# <a name="iadsacl-property-methods"></a><span data-ttu-id="e51f7-105">Методы свойств Иадсакл</span><span class="sxs-lookup"><span data-stu-id="e51f7-105">IADsAcl Property Methods</span></span>

<span data-ttu-id="e51f7-106">Метод свойства интерфейса [**иадсакл**](/windows/desktop/api/Iads/nn-iads-iadsacl) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e51f7-106">The property method of the [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) interface sets the property described in the following table.</span></span> <span data-ttu-id="e51f7-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="e51f7-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e51f7-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="e51f7-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="e51f7-109">**Права**</span><span class="sxs-lookup"><span data-stu-id="e51f7-109">**Privileges**</span></span>
<span data-ttu-id="e51f7-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e51f7-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="e51f7-111">Параметры привилегий.</span><span class="sxs-lookup"><span data-stu-id="e51f7-111">Privilege settings.</span></span>

<dt>

<span data-ttu-id="e51f7-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e51f7-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e51f7-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="e51f7-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e51f7-114">**протектедаттрнаме**</span><span class="sxs-lookup"><span data-stu-id="e51f7-114">**ProtectedAttrName**</span></span>
<span data-ttu-id="e51f7-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e51f7-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="e51f7-116">Имя защищенного атрибута.</span><span class="sxs-lookup"><span data-stu-id="e51f7-116">Name of a protected attribute.</span></span>

<dt>

<span data-ttu-id="e51f7-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e51f7-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e51f7-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e51f7-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e51f7-119">**SubjectName**</span><span class="sxs-lookup"><span data-stu-id="e51f7-119">**SubjectName**</span></span>
<span data-ttu-id="e51f7-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e51f7-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="e51f7-121">Имя субъекта.</span><span class="sxs-lookup"><span data-stu-id="e51f7-121">Name of the subject.</span></span>

<dt>

<span data-ttu-id="e51f7-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e51f7-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e51f7-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e51f7-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="e51f7-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e51f7-124">Requirements</span></span>



| <span data-ttu-id="e51f7-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e51f7-125">Requirement</span></span> | <span data-ttu-id="e51f7-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e51f7-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e51f7-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e51f7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e51f7-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e51f7-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e51f7-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e51f7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e51f7-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e51f7-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e51f7-131">Header</span><span class="sxs-lookup"><span data-stu-id="e51f7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e51f7-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="e51f7-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="e51f7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e51f7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e51f7-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e51f7-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="e51f7-135">IID</span><span class="sxs-lookup"><span data-stu-id="e51f7-135">IID</span></span><br/>                      | <span data-ttu-id="e51f7-136">IID \_ иадсакл определен как 8452D3AB-0869-11D1-A377-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="e51f7-136">IID\_IADsAcl is defined as 8452D3AB-0869-11D1-A377-00C04FB950DC</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="e51f7-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e51f7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e51f7-138">**IADsAcl**</span><span class="sxs-lookup"><span data-stu-id="e51f7-138">**IADsAcl**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 





