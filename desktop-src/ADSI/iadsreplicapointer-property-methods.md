---
title: Методы свойств Иадсрепликапоинтер (iAds. h)
description: Метод свойства интерфейса Иадсрепликапоинтер задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: fc520ea4-b2c2-44c0-8bec-25f8d4a77074
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсрепликапоинтер ADSI
topic_type:
- apiref
api_name:
- IADsReplicaPointer Property Methods
- IADsReplicaPointer.ServerName
- IADsReplicaPointer.get_ServerName
- IADsReplicaPointer.put_ServerName
- IADsReplicaPointer.ReplicaType
- IADsReplicaPointer.get_ReplicaType
- IADsReplicaPointer.put_ReplicaType
- IADsReplicaPointer.ReplicaNumber
- IADsReplicaPointer.get_ReplicaNumber
- IADsReplicaPointer.put_ReplicaNumber
- IADsReplicaPointer.Count
- IADsReplicaPointer.get_Count
- IADsReplicaPointer.put_Count
- IADsReplicaPointer.ReplicaAddressHints
- IADsReplicaPointer.get_ReplicaAddressHints
- IADsReplicaPointer.put_ReplicaAddressHints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044d5a5f1b87d42accb7e8e6e6c83eeda69eb5e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534049"
---
# <a name="iadsreplicapointer-property-methods"></a><span data-ttu-id="af9cd-105">Методы свойств Иадсрепликапоинтер</span><span class="sxs-lookup"><span data-stu-id="af9cd-105">IADsReplicaPointer Property Methods</span></span>

<span data-ttu-id="af9cd-106">Метод свойства интерфейса [**иадсрепликапоинтер**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="af9cd-106">The property method of the [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) interface sets the property described in the following table.</span></span> <span data-ttu-id="af9cd-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="af9cd-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="af9cd-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="af9cd-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="af9cd-109">**Количество**</span><span class="sxs-lookup"><span data-stu-id="af9cd-109">**Count**</span></span>
<span data-ttu-id="af9cd-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="af9cd-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="af9cd-111">Количество существующих реплик.</span><span class="sxs-lookup"><span data-stu-id="af9cd-111">The number of existing replicas.</span></span>

<dt>

<span data-ttu-id="af9cd-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="af9cd-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="af9cd-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="af9cd-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* retval
);
HRESULT put_Count(
  [in] LONG lnCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="af9cd-114">**репликааддресшинтс**</span><span class="sxs-lookup"><span data-stu-id="af9cd-114">**ReplicaAddressHints**</span></span>
<span data-ttu-id="af9cd-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="af9cd-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="af9cd-116">Сетевой адрес, предлагаемый как вероятная ссылка на узел, ведущий к серверу имен.</span><span class="sxs-lookup"><span data-stu-id="af9cd-116">A network address suggested as a likely reference to a node leading to the name server.</span></span>

<dt>

<span data-ttu-id="af9cd-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="af9cd-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="af9cd-118">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="af9cd-118">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaAddressHints(
  [out] VARIANT* retval
);
HRESULT put_ReplicaAddressHints(
  [in] VARIANT vReplicaAddressHints
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="af9cd-119">**репликанумбер**</span><span class="sxs-lookup"><span data-stu-id="af9cd-119">**ReplicaNumber**</span></span>
<span data-ttu-id="af9cd-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="af9cd-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="af9cd-121">Идентификационный номер реплики.</span><span class="sxs-lookup"><span data-stu-id="af9cd-121">Identification number of the replica.</span></span>

<dt>

<span data-ttu-id="af9cd-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="af9cd-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="af9cd-123">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="af9cd-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaNumber(
  [out] LONG* retval
);
HRESULT put_ReplicaNumber(
  [in] LONG lnReplicaNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="af9cd-124">**репликатипе**</span><span class="sxs-lookup"><span data-stu-id="af9cd-124">**ReplicaType**</span></span>
<span data-ttu-id="af9cd-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="af9cd-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="af9cd-126">Тип реплики (главный, вторичный или только для чтения).</span><span class="sxs-lookup"><span data-stu-id="af9cd-126">Type of replica (master, secondary, or read-only.)</span></span>

<dt>

<span data-ttu-id="af9cd-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="af9cd-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="af9cd-128">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="af9cd-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaType(
  [out] LONG* retval
);
HRESULT put_ReplicaType(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="af9cd-129">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="af9cd-129">**ServerName**</span></span>
<span data-ttu-id="af9cd-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="af9cd-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="af9cd-131">Имя сервера имен, на котором находится реплика.</span><span class="sxs-lookup"><span data-stu-id="af9cd-131">Name of the name server holding the replica.</span></span>

<dt>

<span data-ttu-id="af9cd-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="af9cd-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="af9cd-133">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="af9cd-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServerName(
  [out] BSTR* retVal
);
HRESULT put_ServerName(
  [in] BSTR bstrServerName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="af9cd-134">Требования</span><span class="sxs-lookup"><span data-stu-id="af9cd-134">Requirements</span></span>



| <span data-ttu-id="af9cd-135">Требование</span><span class="sxs-lookup"><span data-stu-id="af9cd-135">Requirement</span></span> | <span data-ttu-id="af9cd-136">Значение</span><span class="sxs-lookup"><span data-stu-id="af9cd-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af9cd-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af9cd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="af9cd-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af9cd-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af9cd-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af9cd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="af9cd-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af9cd-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af9cd-141">Header</span><span class="sxs-lookup"><span data-stu-id="af9cd-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="af9cd-142"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="af9cd-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="af9cd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="af9cd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af9cd-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af9cd-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="af9cd-145">IID</span><span class="sxs-lookup"><span data-stu-id="af9cd-145">IID</span></span><br/>                      | <span data-ttu-id="af9cd-146">IID \_ иадсрепликапоинтер определен как F60FB803-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="af9cd-146">IID\_IADsReplicaPointer is defined as F60FB803-4080-11D1-A3AC-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="af9cd-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af9cd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9cd-148">**IADsReplicaPointer**</span><span class="sxs-lookup"><span data-stu-id="af9cd-148">**IADsReplicaPointer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)
</dt> <dt>

[<span data-ttu-id="af9cd-149">**ADS \_ репликапоинтер**</span><span class="sxs-lookup"><span data-stu-id="af9cd-149">**ADS\_REPLICAPOINTER**</span></span>](/windows/win32/api/iads/ns-iads-ads_replicapointer)
</dt> </dl>

 

 





