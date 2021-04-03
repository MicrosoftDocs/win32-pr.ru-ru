---
title: Методы свойств Иадсбакклинк (iAds. h)
description: Метод свойства интерфейса Иадсбакклинк задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсбакклинк ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136883"
---
# <a name="iadsbacklink-property-methods"></a><span data-ttu-id="26a0e-105">Методы свойств Иадсбакклинк</span><span class="sxs-lookup"><span data-stu-id="26a0e-105">IADsBackLink Property Methods</span></span>

<span data-ttu-id="26a0e-106">Метод свойства интерфейса [**иадсбакклинк**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="26a0e-106">The property method of the [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) interface sets the property described in the following table.</span></span> <span data-ttu-id="26a0e-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="26a0e-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="26a0e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="26a0e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="26a0e-109">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="26a0e-109">**ObjectName**</span></span>
<span data-ttu-id="26a0e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="26a0e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="26a0e-111">Имя объекта, к которому присоединен атрибут **ссылки назад** .</span><span class="sxs-lookup"><span data-stu-id="26a0e-111">The name of an object the **Back Link** attribute is attached to.</span></span>

<dt>

<span data-ttu-id="26a0e-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26a0e-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26a0e-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="26a0e-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="26a0e-114">**ремотеид**</span><span class="sxs-lookup"><span data-stu-id="26a0e-114">**RemoteID**</span></span>
<span data-ttu-id="26a0e-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="26a0e-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="26a0e-116">Идентификатор удаленного сервера, которому требуется внешняя ссылка на объект, указанный параметром **objectname**.</span><span class="sxs-lookup"><span data-stu-id="26a0e-116">The identifier of the remote server that requires an external reference of the object specified by **ObjectName**.</span></span>

<dt>

<span data-ttu-id="26a0e-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26a0e-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="26a0e-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="26a0e-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="26a0e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="26a0e-119">Requirements</span></span>



| <span data-ttu-id="26a0e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="26a0e-120">Requirement</span></span> | <span data-ttu-id="26a0e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="26a0e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26a0e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26a0e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="26a0e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26a0e-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26a0e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26a0e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="26a0e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26a0e-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26a0e-126">Header</span><span class="sxs-lookup"><span data-stu-id="26a0e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="26a0e-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="26a0e-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="26a0e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="26a0e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26a0e-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26a0e-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="26a0e-130">IID</span><span class="sxs-lookup"><span data-stu-id="26a0e-130">IID</span></span><br/>                      | <span data-ttu-id="26a0e-131">IID \_ иадсбакклинк определен как FD1302BD-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="26a0e-131">IID\_IADsBackLink is defined as FD1302BD-4080-11D1-A3AC-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="26a0e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26a0e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a0e-133">**IADsBackLink**</span><span class="sxs-lookup"><span data-stu-id="26a0e-133">**IADsBackLink**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[<span data-ttu-id="26a0e-134">**ADS \_ посмотрите**</span><span class="sxs-lookup"><span data-stu-id="26a0e-134">**ADS\_BACKLINK**</span></span>](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 





