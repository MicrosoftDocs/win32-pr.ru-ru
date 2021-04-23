---
title: Методы свойств Иадспас (iAds. h)
description: Метод свойства интерфейса Иадспас задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 6fc7ce1a-575b-48c4-9f66-3ea22d60c96b
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадспас ADSI
topic_type:
- apiref
api_name:
- IADsPath Property Methods
- IADsPath.Type
- IADsPath.get_Type
- IADsPath.put_Type
- IADsPath.VolumeName
- IADsPath.get_VolumeName
- IADsPath.put_VolumeName
- IADsPath.Path
- IADsPath.get_Path
- IADsPath.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5adcc1c60a9b678e99074ae3547d35c7ac8c7356
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803161"
---
# <a name="iadspath-property-methods"></a><span data-ttu-id="6ae53-105">Методы свойств Иадспас</span><span class="sxs-lookup"><span data-stu-id="6ae53-105">IADsPath Property Methods</span></span>

<span data-ttu-id="6ae53-106">Метод свойства интерфейса [**иадспас**](/windows/desktop/api/Iads/nn-iads-iadspath) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6ae53-106">The property method of the [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath) interface sets the property described in the following table.</span></span> <span data-ttu-id="6ae53-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6ae53-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6ae53-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="6ae53-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6ae53-109">**Путь**</span><span class="sxs-lookup"><span data-stu-id="6ae53-109">**Path**</span></span>
<span data-ttu-id="6ae53-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6ae53-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6ae53-111">Путь к каталогу файловой системы.</span><span class="sxs-lookup"><span data-stu-id="6ae53-111">Path of a directory of the file system.</span></span>

<dt>

<span data-ttu-id="6ae53-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6ae53-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6ae53-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6ae53-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* retval
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ae53-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6ae53-114">**Type**</span></span>
<span data-ttu-id="6ae53-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6ae53-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="6ae53-116">Тип файла файловой системы.</span><span class="sxs-lookup"><span data-stu-id="6ae53-116">File type of the file system.</span></span>

<dt>

<span data-ttu-id="6ae53-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6ae53-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6ae53-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="6ae53-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ae53-119">**Тома**</span><span class="sxs-lookup"><span data-stu-id="6ae53-119">**VolumeName**</span></span>
<span data-ttu-id="6ae53-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6ae53-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="6ae53-121">Имя существующего тома файловой системы.</span><span class="sxs-lookup"><span data-stu-id="6ae53-121">Name of an existing volume of the file system.</span></span>

<dt>

<span data-ttu-id="6ae53-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6ae53-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6ae53-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6ae53-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_VolumeName(
  [out] BSTR* retval
);
HRESULT put_VolumeName(
  [in] BSTR bstrVolumeName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="6ae53-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6ae53-124">Requirements</span></span>



| <span data-ttu-id="6ae53-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6ae53-125">Requirement</span></span> | <span data-ttu-id="6ae53-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6ae53-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae53-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ae53-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae53-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ae53-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ae53-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ae53-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae53-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ae53-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ae53-131">Header</span><span class="sxs-lookup"><span data-stu-id="6ae53-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ae53-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae53-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="6ae53-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6ae53-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ae53-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ae53-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ae53-135">IID</span><span class="sxs-lookup"><span data-stu-id="6ae53-135">IID</span></span><br/>                      | <span data-ttu-id="6ae53-136">IID \_ иадспас определен как B287FCD5-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="6ae53-136">IID\_IADsPath is defined as B287FCD5-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6ae53-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ae53-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae53-138">**IADsPath**</span><span class="sxs-lookup"><span data-stu-id="6ae53-138">**IADsPath**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspath)
</dt> <dt>

[<span data-ttu-id="6ae53-139">**\_путь AD**</span><span class="sxs-lookup"><span data-stu-id="6ae53-139">**ADS\_PATH**</span></span>](/windows/win32/api/iads/ns-iads-ads_path)
</dt> </dl>

 

 





