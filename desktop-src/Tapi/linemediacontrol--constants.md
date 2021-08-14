---
description: '\_Константы побитового флага линемедиаконтрол описывают набор универсальных операций с потоками мультимедиа.'
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Константы LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54c7c83df769eef91afe7c310452c342a855f44391815bbc4429ac07bb6ec92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309974"
---
# <a name="linemediacontrol_-constants"></a>\_Константы линемедиаконтрол

Константы побитового флага **линемедиаконтрол \_** описывают набор универсальных операций с потоками мультимедиа. Интерпретация определяется потоком мультимедиа. Для того чтобы любая операция управления мультимедиа действовала, устройство должно иметь возможность управления мультимедиа.

<dl> <dt>

<span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ None**
</dt> <dd> <dl> <dt>



В поток мультимедиа не вносятся изменения.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**Приостановка ЛИНЕМЕДИАКОНТРОЛ \_**
</dt> <dd> <dl> <dt>



Временная приостановка потока мультимедиа.

Скорость потока мультимедиа возвращается в нормальный режим.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ ратедовн**
</dt> <dd> <dl> <dt>



Скорость потока мультимедиа уменьшается по количеству, определяемому потоком.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ ратенормал**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ ратеуп**
</dt> <dd> <dl> <dt>



Скорость потока мультимедиа увеличивается на определенное потоком количество.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**\_Сброс линемедиаконтрол**
</dt> <dd> <dl> <dt>



Сбросьте поток мультимедиа. Эквивалент конца входных данных. Освобождаются все буферы.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**возобновление ЛИНЕМЕДИАКОНТРОЛ \_**
</dt> <dd> <dl> <dt>



Возобновление приостановленного потока мультимедиа.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**\_Запуск линемедиаконтрол**
</dt> <dd> <dl> <dt>



Запустите поток мультимедиа.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ волумедовн**
</dt> <dd> <dl> <dt>



Амплитуда потока мультимедиа уменьшается на определенное потоком количество.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ волуменормал**
</dt> <dd> <dl> <dt>



Амплитуда потока мультимедиа возвращается в нормальный режим.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ волумеуп**
</dt> <dd> <dl> <dt>



Амплитуда потока мультимедиа увеличивается на определенное потоком количество.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Старшие 16 бит можно назначить для расширений для конкретных устройств. 16 младших разрядов зарезервированы.

Управление носителями обеспечивает повышение производительности действий в потоках мультимедиа в ответ на связанные с телефонами события. Приложение обычно управляет потоком мультимедиа с помощью API-интерфейса для конкретного носителя. Функции управления мультимедиа, предоставляемые здесь, не предназначены для замены собственных API-интерфейсов мультимедиа.

Действия управления мультимедиа могут быть связаны с обнаружением цифр, обнаружением тонов, переходом в состояние вызова и обнаружением типа носителя. Ознакомьтесь с возможностями устройства линии, чтобы определить, доступен ли элемент управления мультимедиа в строке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




