---
title: Метод Форцерефреш класса MicrosoftDNS_Zone
description: Метод Форцерефреш вызывает принудительное обновление дополнительного DNS-сервера с главного сервера.
ms.assetid: 8dde1703-53c3-4d1e-bfb3-f6d5d1666740
keywords:
- DNS-метод Форцерефреш
- Форцерефреш метода DNS, класс MicrosoftDNS_Zone
- DNS класса MicrosoftDNS_Zone, метод Форцерефреш
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ForceRefresh
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85390230b0a0852ee479bc8b7e396972f6e69080
ms.sourcegitcommit: 03fb201e1ea36e353c335ff063ed993fb5993e61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655569"
---
# <a name="forcerefresh-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="abb71-106">Метод Форцерефреш \_ класса зоны микрософтднс</span><span class="sxs-lookup"><span data-stu-id="abb71-106">ForceRefresh method of the MicrosoftDNS\_Zone class</span></span>

> [!NOTE]
> <span data-ttu-id="abb71-107">Эта статья содержит ссылки на термин «главный сервер», термин, который корпорация Майкрософт больше не использует.</span><span class="sxs-lookup"><span data-stu-id="abb71-107">This article contains references to the term master server, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="abb71-108">Когда этот термин будет удален из программного обеспечения, мы удалим его из статьи.</span><span class="sxs-lookup"><span data-stu-id="abb71-108">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="abb71-109">Метод **форцерефреш** вызывает принудительное обновление дополнительного DNS-сервера с главного сервера.</span><span class="sxs-lookup"><span data-stu-id="abb71-109">The **ForceRefresh** method forces an update of the secondary DNS Server from the master server.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb71-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abb71-110">Syntax</span></span>


```mof
void ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="abb71-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="abb71-111">Parameters</span></span>

<span data-ttu-id="abb71-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="abb71-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="abb71-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abb71-113">Return value</span></span>

<span data-ttu-id="abb71-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="abb71-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="abb71-115">Требования</span><span class="sxs-lookup"><span data-stu-id="abb71-115">Requirements</span></span>



| <span data-ttu-id="abb71-116">Требование</span><span class="sxs-lookup"><span data-stu-id="abb71-116">Requirement</span></span> | <span data-ttu-id="abb71-117">Значение</span><span class="sxs-lookup"><span data-stu-id="abb71-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abb71-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abb71-118">Minimum supported client</span></span><br/> | <span data-ttu-id="abb71-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="abb71-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="abb71-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abb71-120">Minimum supported server</span></span><br/> | <span data-ttu-id="abb71-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="abb71-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="abb71-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="abb71-122">Namespace</span></span><br/>                | <span data-ttu-id="abb71-123">Корневой \\ микрософтднс</span><span class="sxs-lookup"><span data-stu-id="abb71-123">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="abb71-124">MOF</span><span class="sxs-lookup"><span data-stu-id="abb71-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abb71-125"><dt>Днспров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abb71-125"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abb71-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abb71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb71-127">**\_Зона микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-127">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="abb71-128">**Метод Ажеаллрекордс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-128">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="abb71-129">**Метод Чанжезонетипе \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-129">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="abb71-130">**Метод Креатезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-130">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="abb71-131">**Метод Жетдистингуишеднаме \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-131">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="abb71-132">**Метод Паусезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-132">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="abb71-133">**Метод Релоадзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-133">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="abb71-134">**Метод Ресетсекондариес \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-134">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="abb71-135">**Метод Ресумезоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-135">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="abb71-136">**Метод Упдатефромдс \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-136">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="abb71-137">**Метод Вритебаккзоне \_ класса зоны микрософтднс**</span><span class="sxs-lookup"><span data-stu-id="abb71-137">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





