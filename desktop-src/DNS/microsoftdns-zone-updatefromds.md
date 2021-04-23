---
title: Метод Упдатефромдс класса MicrosoftDNS_Zone
description: Метод Упдатефромдс принудительно обновляет зону из службы каталогов (DS).
ms.assetid: 471f0754-1221-4d1d-8ffd-36c1ab54b7e5
keywords:
- DNS-метод Упдатефромдс
- Упдатефромдс метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Упдатефромдс
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.UpdateFromDS
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8fd0ba4db9b182379ce2ec93508c7a3bab354a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137826"
---
# <a name="updatefromds-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="cc8e0-106">Метод Упдатефромдс \_ класса зоны микрософтднс</span><span class="sxs-lookup"><span data-stu-id="cc8e0-106">UpdateFromDS method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="cc8e0-107">Метод **упдатефромдс** принудительно обновляет зону из службы каталогов (DS).</span><span class="sxs-lookup"><span data-stu-id="cc8e0-107">The **UpdateFromDS** method forces an update of the zone from the Directory Service (DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc8e0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc8e0-108">Syntax</span></span>


```mof
void UpdateFromDS();
```



## <a name="parameters"></a><span data-ttu-id="cc8e0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc8e0-109">Parameters</span></span>

<span data-ttu-id="cc8e0-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cc8e0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc8e0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc8e0-111">Return value</span></span>

<span data-ttu-id="cc8e0-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cc8e0-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc8e0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc8e0-113">Remarks</span></span>

<span data-ttu-id="cc8e0-114">Для успешного выполнения этого метода ZoneType должен быть равен нулю, а зона должна храниться в DS.</span><span class="sxs-lookup"><span data-stu-id="cc8e0-114">In order to successfully execute this method, the ZoneType must be zero, and the zone must be stored on the DS.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc8e0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cc8e0-115">Requirements</span></span>



| <span data-ttu-id="cc8e0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cc8e0-116">Requirement</span></span> | <span data-ttu-id="cc8e0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cc8e0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8e0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc8e0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cc8e0-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cc8e0-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cc8e0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc8e0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cc8e0-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cc8e0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cc8e0-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cc8e0-122">Namespace</span></span><br/>                | <span data-ttu-id="cc8e0-123">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="cc8e0-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="cc8e0-124">MOF</span><span class="sxs-lookup"><span data-stu-id="cc8e0-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc8e0-125"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e0-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc8e0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc8e0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc8e0-127">**\_Зона микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-128">**Метод Ажеаллрекордс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-129">**Метод Чанжезонетипе \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-130">**Метод Креатезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-131">**Метод Форцерефреш \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-131">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-132">**Метод Жетдистингуишеднаме \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-132">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-133">**Метод Паусезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-133">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-134">**Метод Релоадзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-134">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-135">**Метод Ресетсекондариес \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-135">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-136">**Метод Ресумезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-136">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="cc8e0-137">**Метод Вритебаккзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="cc8e0-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





