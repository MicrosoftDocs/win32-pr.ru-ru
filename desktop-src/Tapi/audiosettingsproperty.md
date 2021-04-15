---
description: 'Перечисление Аудиосеттингспроперти используется методами Итаудиосеттингс::, Итаудиосеттингс:: Get и Итаудиосеттингс:: Set для указания на обрабатываемое свойство настройки звука.'
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Перечисление Аудиосеттингспроперти (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688914"
---
# <a name="audiosettingsproperty-enumeration"></a><span data-ttu-id="f7d8b-103">Перечисление Аудиосеттингспроперти</span><span class="sxs-lookup"><span data-stu-id="f7d8b-103">AudioSettingsProperty enumeration</span></span>

<span data-ttu-id="f7d8b-104">\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f7d8b-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f7d8b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f7d8b-106">Перечисление **аудиосеттингспроперти** используется методами [**итаудиосеттингс::**](itaudiosettings-getrange.md), [**Итаудиосеттингс:: Get**](itaudiosettings-get.md)и [**итаудиосеттингс:: Set**](itaudiosettings-set.md) для указания на обрабатываемое свойство настройки звука.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-106">The **AudioSettingsProperty** enum is used by the [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md), and [**ITAudioSettings::Set**](itaudiosettings-set.md) methods to indicate the audio setting property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d8b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7d8b-107">Syntax</span></span>


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a><span data-ttu-id="f7d8b-108">Константы</span><span class="sxs-lookup"><span data-stu-id="f7d8b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f7d8b-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**Аудиосеттингс \_ сигналлевел**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings\_SignalLevel**</span></span>
</dt> <dd>

<span data-ttu-id="f7d8b-110">Свойство параметров сигнала.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-110">Signal settings property.</span></span>

</dd> <dt>

<span data-ttu-id="f7d8b-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**Аудиосеттингс \_ силенцесрешолд**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings\_SilenceThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="f7d8b-112">Свойство порога бездействия.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-112">Silence threshold property.</span></span>

</dd> <dt>

<span data-ttu-id="f7d8b-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Том аудиосеттингс**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings\_Volume**</span></span>
</dt> <dd>

<span data-ttu-id="f7d8b-114">Свойство тома.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-114">Volume property.</span></span>

</dd> <dt>

<span data-ttu-id="f7d8b-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**\_Баланс аудиосеттингс**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings\_Balance**</span></span>
</dt> <dd>

<span data-ttu-id="f7d8b-116">Свойство Balance.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-116">Balance property.</span></span>

</dd> <dt>

<span data-ttu-id="f7d8b-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**\_Громкость аудиосеттингс**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings\_Loudness**</span></span>
</dt> <dd>

<span data-ttu-id="f7d8b-118">Свойство громкости.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-118">Loudness property.</span></span>

</dd> <dt>

<span data-ttu-id="f7d8b-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**Аудиосеттингс \_ высоких частот**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings\_Treble**</span></span>
</dt> <dd>

<span data-ttu-id="f7d8b-120">Свойство высоких частот.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-120">Treble property.</span></span>

</dd> <dt>

<span data-ttu-id="f7d8b-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**Аудиосеттингс \_ НЧ**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings\_Bass**</span></span>
</dt> <dd>

<span data-ttu-id="f7d8b-122">Свойство басов.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-122">Bass property.</span></span>

</dd> <dt>

<span data-ttu-id="f7d8b-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**Аудиосеттингс \_ Mono**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings\_Mono**</span></span>
</dt> <dd>

<span data-ttu-id="f7d8b-124">Свойство монаурал.</span><span class="sxs-lookup"><span data-stu-id="f7d8b-124">Monaural property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7d8b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f7d8b-125">Requirements</span></span>



| <span data-ttu-id="f7d8b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f7d8b-126">Requirement</span></span> | <span data-ttu-id="f7d8b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f7d8b-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d8b-128">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f7d8b-128">TAPI version</span></span><br/> | <span data-ttu-id="f7d8b-129">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f7d8b-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="f7d8b-130">Header</span><span class="sxs-lookup"><span data-stu-id="f7d8b-130">Header</span></span><br/>       | <dl> <span data-ttu-id="f7d8b-131"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d8b-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d8b-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7d8b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d8b-133">**Итаудиосеттингс:: Range**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-133">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="f7d8b-134">**Итаудиосеттингс:: Get**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-134">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="f7d8b-135">**Итаудиосеттингс:: Set**</span><span class="sxs-lookup"><span data-stu-id="f7d8b-135">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> </dl>

 

 




