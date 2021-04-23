---
title: Методы свойств Иадснаметранслате (iAds. h)
description: Задает свойство Часереферрал.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадснаметранслате ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989094"
---
# <a name="iadsnametranslate-property-methods"></a><span data-ttu-id="45788-104">Методы свойств Иадснаметранслате</span><span class="sxs-lookup"><span data-stu-id="45788-104">IADsNameTranslate Property Methods</span></span>

<span data-ttu-id="45788-105">Метод property интерфейса [**иадснаметранслате**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) задает свойство **часереферрал** .</span><span class="sxs-lookup"><span data-stu-id="45788-105">The property method of the [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface sets the **ChaseReferral** property.</span></span> <span data-ttu-id="45788-106">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="45788-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="45788-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="45788-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="45788-108">**часереферрал**</span><span class="sxs-lookup"><span data-stu-id="45788-108">**ChaseReferral**</span></span>
<span data-ttu-id="45788-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="45788-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="45788-110">Варианты перенаправления ссылок, как определено в [**баннерах, \_ \_ \_ перечисление ссылок**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span><span class="sxs-lookup"><span data-stu-id="45788-110">Options of referral chasing as defined in [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span></span> <span data-ttu-id="45788-111">Если задано отслеживание ссылок, преобразование имени выполняется для объектов, которые не принадлежат этому каталогу, и являются ссылками, возвращаемыми из прослеживания ссылок.</span><span class="sxs-lookup"><span data-stu-id="45788-111">When referral chasing is set, the name translation is performed on objects that do not belong to this directory and are the referrals returned from referral chasing.</span></span>

<dt>

<span data-ttu-id="45788-112">Тип доступа: только для записи</span><span class="sxs-lookup"><span data-stu-id="45788-112">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="45788-113">Тип данных скрипта: **Long**</span><span class="sxs-lookup"><span data-stu-id="45788-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="45788-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45788-114">Remarks</span></span>

<span data-ttu-id="45788-115">Параметры прослеживания ссылок применяются только при использовании [**иадснаметранслате:: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) и [**Иадснаметранслате:: Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span><span class="sxs-lookup"><span data-stu-id="45788-115">The referral chasing options apply only when you use [**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) and [**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span></span> <span data-ttu-id="45788-116">Эта функция недоступна в [**иадснаметранслате:: сетекс**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) или [**Иадснаметранслате:: жетекс**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span><span class="sxs-lookup"><span data-stu-id="45788-116">The feature is not available with [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) or [**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span></span>

<span data-ttu-id="45788-117">Интерфейс [**иадснаметранслате**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) имеет частичную реализацию объявлений, [**\_ \_ \_ перечисление по ссылкам**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) через свойство **часереферрал** .</span><span class="sxs-lookup"><span data-stu-id="45788-117">The [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface has a partial implementation of [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) through the **ChaseReferral** property.</span></span> <span data-ttu-id="45788-118">Если свойство **часереферрал** имеет нулевое значение (0), то оно аналогично указанию **баннеров \_ \_ \_ никогда** (0).</span><span class="sxs-lookup"><span data-stu-id="45788-118">If the **ChaseReferral** property is set to zero (0), it is the same as specifying **ADS\_CHASE\_REFERRALS\_NEVER** (0).</span></span> <span data-ttu-id="45788-119">Если используется ненулевое значение, то оно аналогично указанию **баннеров \_ \_ \_ всегда** (0x60).</span><span class="sxs-lookup"><span data-stu-id="45788-119">If a nonzero value is used, it is the same as specifying **ADS\_CHASE\_REFERRALS\_ALWAYS** (0x60).</span></span> <span data-ttu-id="45788-120">В **иадснаметранслате** не реализованы **рекламные \_ объявления \_ \_ подчиненные** (0x20) или **баннеры \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="45788-120">**IADsNameTranslate** does not implement the **ADS\_CHASE\_REFERRALS\_SUBORDINATE** (0x20) or **ADS\_CHASE\_REFERRALS\_EXTERNAL** (0x40) options.</span></span>

<span data-ttu-id="45788-121">Включен параметр по умолчанию для прослеживания ссылок (**баннеры \_ \_ \_ всегда отслеживаются по ссылкам**).</span><span class="sxs-lookup"><span data-stu-id="45788-121">The default setting for referral chasing is enabled (**ADS\_CHASE\_REFERRALS\_ALWAYS**).</span></span> <span data-ttu-id="45788-122">Без прослеживания ссылок можно выполнять преобразование имен для объектов, размещенных только на сервере подключенного каталога.</span><span class="sxs-lookup"><span data-stu-id="45788-122">Without referral chasing, you can have name translation performed on those objects residing on the connected directory server only.</span></span> <span data-ttu-id="45788-123">Если вы не уверены, что нужный объект находится на указанном сервере, следует задать это свойство как **баннеры \_ \_ \_ всегда**.</span><span class="sxs-lookup"><span data-stu-id="45788-123">If you are uncertain whether the object of interest is on the specified server, you should set this property to be **ADS\_CHASE\_REFERRALS\_ALWAYS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="45788-124">Требования</span><span class="sxs-lookup"><span data-stu-id="45788-124">Requirements</span></span>



| <span data-ttu-id="45788-125">Требование</span><span class="sxs-lookup"><span data-stu-id="45788-125">Requirement</span></span> | <span data-ttu-id="45788-126">Значение</span><span class="sxs-lookup"><span data-stu-id="45788-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45788-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45788-127">Minimum supported client</span></span><br/> | <span data-ttu-id="45788-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45788-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45788-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45788-129">Minimum supported server</span></span><br/> | <span data-ttu-id="45788-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45788-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45788-131">Header</span><span class="sxs-lookup"><span data-stu-id="45788-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="45788-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="45788-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="45788-133">DLL</span><span class="sxs-lookup"><span data-stu-id="45788-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45788-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45788-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="45788-135">IID</span><span class="sxs-lookup"><span data-stu-id="45788-135">IID</span></span><br/>                      | <span data-ttu-id="45788-136">IID \_ иадснаметранслате определен как B1B272A3-3625-11D1-A3A4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="45788-136">IID\_IADsNameTranslate is defined as B1B272A3-3625-11D1-A3A4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="45788-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45788-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45788-138">**ОБЪЯВЛЕНИЯ \_ о \_ \_ перечислении ссылок**</span><span class="sxs-lookup"><span data-stu-id="45788-138">**ADS\_CHASE\_REFERRALS\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[<span data-ttu-id="45788-139">**IADsNameTranslate**</span><span class="sxs-lookup"><span data-stu-id="45788-139">**IADsNameTranslate**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[<span data-ttu-id="45788-140">**Иадснаметранслате:: Get**</span><span class="sxs-lookup"><span data-stu-id="45788-140">**IADsNameTranslate::Get**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[<span data-ttu-id="45788-141">**Иадснаметранслате:: Жетекс**</span><span class="sxs-lookup"><span data-stu-id="45788-141">**IADsNameTranslate::GetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[<span data-ttu-id="45788-142">**Иадснаметранслате:: Set**</span><span class="sxs-lookup"><span data-stu-id="45788-142">**IADsNameTranslate::Set**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[<span data-ttu-id="45788-143">**Иадснаметранслате:: Сетекс**</span><span class="sxs-lookup"><span data-stu-id="45788-143">**IADsNameTranslate::SetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[<span data-ttu-id="45788-144">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="45788-144">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





