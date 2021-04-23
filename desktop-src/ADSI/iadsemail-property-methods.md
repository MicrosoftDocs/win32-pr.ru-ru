---
title: Методы свойств Иадсемаил (iAds. h)
description: Метод свойства интерфейса Иадсемаил задает свойство, описанное в следующей таблице. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадсемаил ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415944"
---
# <a name="iadsemail-property-methods"></a><span data-ttu-id="fbfbb-105">Методы свойств Иадсемаил</span><span class="sxs-lookup"><span data-stu-id="fbfbb-105">IADsEmail Property Methods</span></span>

<span data-ttu-id="fbfbb-106">Метод свойства интерфейса [**иадсемаил**](/windows/desktop/api/Iads/nn-iads-iadsemail) задает свойство, описанное в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fbfbb-106">The property method of the [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) interface sets the property described in the following table.</span></span> <span data-ttu-id="fbfbb-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="fbfbb-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="fbfbb-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="fbfbb-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="fbfbb-109">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="fbfbb-109">**Address**</span></span>
<span data-ttu-id="fbfbb-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fbfbb-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="fbfbb-111">Адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="fbfbb-111">The email address of the user.</span></span>

<dt>

<span data-ttu-id="fbfbb-112">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fbfbb-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fbfbb-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fbfbb-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbfbb-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fbfbb-114">**Type**</span></span>
<span data-ttu-id="fbfbb-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fbfbb-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="fbfbb-116">Тип сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fbfbb-116">The type of the email message.</span></span>

<dt>

<span data-ttu-id="fbfbb-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fbfbb-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fbfbb-118">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="fbfbb-118">Scripting data type: **LONG**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="fbfbb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fbfbb-119">Requirements</span></span>



| <span data-ttu-id="fbfbb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fbfbb-120">Requirement</span></span> | <span data-ttu-id="fbfbb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfbb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbfbb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbfbb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fbfbb-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbfbb-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fbfbb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbfbb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fbfbb-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbfbb-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fbfbb-126">Header</span><span class="sxs-lookup"><span data-stu-id="fbfbb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbfbb-127"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbfbb-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="fbfbb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fbfbb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbfbb-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbfbb-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="fbfbb-130">IID</span><span class="sxs-lookup"><span data-stu-id="fbfbb-130">IID</span></span><br/>                      | <span data-ttu-id="fbfbb-131">IID \_ иадсемаил определен как 97AF011A-478E-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="fbfbb-131">IID\_IADsEmail is defined as 97AF011A-478E-11D1-A3B4-00C04FB950DC</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fbfbb-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbfbb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbfbb-133">**IADsEmail**</span><span class="sxs-lookup"><span data-stu-id="fbfbb-133">**IADsEmail**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[<span data-ttu-id="fbfbb-134">**\_Электронная почта ADS**</span><span class="sxs-lookup"><span data-stu-id="fbfbb-134">**ADS\_EMAIL**</span></span>](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 





