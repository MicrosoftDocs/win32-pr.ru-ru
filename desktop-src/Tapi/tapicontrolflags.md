---
description: Перечисление Тапиконтролфлагс используется несколькими методами для указания того, управляется ли данное свойство автоматически, или вручную.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Перечисление Тапиконтролфлагс (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689225"
---
# <a name="tapicontrolflags-enumeration"></a><span data-ttu-id="d865c-103">Перечисление Тапиконтролфлагс</span><span class="sxs-lookup"><span data-stu-id="d865c-103">TAPIControlFlags enumeration</span></span>

<span data-ttu-id="d865c-104">\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d865c-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d865c-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="d865c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d865c-106">Перечисление **тапиконтролфлагс** используется несколькими методами для указания того, управляется ли данное свойство автоматически, или вручную.</span><span class="sxs-lookup"><span data-stu-id="d865c-106">The **TAPIControlFlags** enum is used by a number of methods to indicate whether a given property is controlled automatically or manually.</span></span>

## <a name="syntax"></a><span data-ttu-id="d865c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d865c-107">Syntax</span></span>


```C++
} TAPIControlFlags;
```



## <a name="constants"></a><span data-ttu-id="d865c-108">Константы</span><span class="sxs-lookup"><span data-stu-id="d865c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d865c-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**Тапиконтрол \_ без флагов \_**</span><span class="sxs-lookup"><span data-stu-id="d865c-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl\_Flags\_None**</span></span>
</dt> <dd>

<span data-ttu-id="d865c-110">У TAPI нет управляющих флагов для свойства.</span><span class="sxs-lookup"><span data-stu-id="d865c-110">TAPI has no control flags for the property.</span></span>

</dd> <dt>

<span data-ttu-id="d865c-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**\_Auto тапиконтрол flags \_**</span><span class="sxs-lookup"><span data-stu-id="d865c-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl\_Flags\_Auto**</span></span>
</dt> <dd>

<span data-ttu-id="d865c-112">Свойство управляется автоматически.</span><span class="sxs-lookup"><span data-stu-id="d865c-112">The property is controlled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="d865c-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Ручные флаги тапиконтрол \_**</span><span class="sxs-lookup"><span data-stu-id="d865c-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl\_Flags\_Manual**</span></span>
</dt> <dd>

<span data-ttu-id="d865c-114">Свойство управляется вручную.</span><span class="sxs-lookup"><span data-stu-id="d865c-114">The property is controlled manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d865c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d865c-115">Requirements</span></span>



| <span data-ttu-id="d865c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d865c-116">Requirement</span></span> | <span data-ttu-id="d865c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d865c-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d865c-118">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="d865c-118">TAPI version</span></span><br/> | <span data-ttu-id="d865c-119">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="d865c-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="d865c-120">Header</span><span class="sxs-lookup"><span data-stu-id="d865c-120">Header</span></span><br/>       | <dl> <span data-ttu-id="d865c-121"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d865c-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d865c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d865c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d865c-123">**Итаудиодевицеконтрол:: Range**</span><span class="sxs-lookup"><span data-stu-id="d865c-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="d865c-124">**Итаудиодевицеконтрол:: Get**</span><span class="sxs-lookup"><span data-stu-id="d865c-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="d865c-125">**Итаудиодевицеконтрол:: Set**</span><span class="sxs-lookup"><span data-stu-id="d865c-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> <dt>

[<span data-ttu-id="d865c-126">**Итаудиосеттингс:: Range**</span><span class="sxs-lookup"><span data-stu-id="d865c-126">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="d865c-127">**Итаудиосеттингс:: Get**</span><span class="sxs-lookup"><span data-stu-id="d865c-127">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="d865c-128">**Итаудиосеттингс:: Set**</span><span class="sxs-lookup"><span data-stu-id="d865c-128">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> <dt>

[<span data-ttu-id="d865c-129">**Иткаллкуалитиконтрол:: Range**</span><span class="sxs-lookup"><span data-stu-id="d865c-129">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="d865c-130">**Иткаллкуалитиконтрол:: Get**</span><span class="sxs-lookup"><span data-stu-id="d865c-130">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="d865c-131">**Иткаллкуалитиконтрол:: Set**</span><span class="sxs-lookup"><span data-stu-id="d865c-131">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> <dt>

[<span data-ttu-id="d865c-132">**Итстреамкуалитиконтрол:: Range**</span><span class="sxs-lookup"><span data-stu-id="d865c-132">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="d865c-133">**Итстреамкуалитиконтрол:: Get**</span><span class="sxs-lookup"><span data-stu-id="d865c-133">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="d865c-134">**Итстреамкуалитиконтрол:: Set**</span><span class="sxs-lookup"><span data-stu-id="d865c-134">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




