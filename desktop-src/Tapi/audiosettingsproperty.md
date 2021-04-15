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
# <a name="audiosettingsproperty-enumeration"></a>Перечисление Аудиосеттингспроперти

\[ Это перечисление недоступно для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Перечисление **аудиосеттингспроперти** используется методами [**итаудиосеттингс::**](itaudiosettings-getrange.md), [**Итаудиосеттингс:: Get**](itaudiosettings-get.md)и [**итаудиосеттингс:: Set**](itaudiosettings-set.md) для указания на обрабатываемое свойство настройки звука.

## <a name="syntax"></a>Синтаксис


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**Аудиосеттингс \_ сигналлевел**
</dt> <dd>

Свойство параметров сигнала.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**Аудиосеттингс \_ силенцесрешолд**
</dt> <dd>

Свойство порога бездействия.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Том аудиосеттингс**
</dt> <dd>

Свойство тома.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**\_Баланс аудиосеттингс**
</dt> <dd>

Свойство Balance.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**\_Громкость аудиосеттингс**
</dt> <dd>

Свойство громкости.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**Аудиосеттингс \_ высоких частот**
</dt> <dd>

Свойство высоких частот.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**Аудиосеттингс \_ НЧ**
</dt> <dd>

Свойство басов.

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**Аудиосеттингс \_ Mono**
</dt> <dd>

Свойство монаурал.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ипмсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Итаудиосеттингс:: Range**](itaudiosettings-getrange.md)
</dt> <dt>

[**Итаудиосеттингс:: Get**](itaudiosettings-get.md)
</dt> <dt>

[**Итаудиосеттингс:: Set**](itaudiosettings-set.md)
</dt> </dl>

 

 




