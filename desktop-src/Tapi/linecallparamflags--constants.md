---
description: '\_Константы линекаллпарамфлагс описывают различные флаги состояния вызова.'
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Константы LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674896"
---
# <a name="linecallparamflags_-constants"></a>\_Константы линекаллпарамфлагс

Константы **линекаллпарамфлагс \_** описывают различные флаги состояния вызова.

<dl> <dt>

<span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ ИД блока**
</dt> <dd> <dl> <dt>



Удостоверение инициатора следует скрыть (блокировать вызывающий код).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ дестоффхук**
</dt> <dd> <dl> <dt>



Телефонный номер вызываемой стороны должен быть автоматически сделан оффхук.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ бездействие**
</dt> <dd> <dl> <dt>



Вызов должен быть создан на внешнем представлении вызова, но не присоединяться к выполняемому вызову. Если при использовании функции [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) \_ значение неактивности линекаллпарамфлагс не задано и в строке уже существует вызов, функция переключается на существующий вызов, если это необходимо для создания нового вызова. Если нет существующего вызова, функция создает новый вызов, как указано.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ нохолдконференце**
</dt> <dd> <dl> <dt>



Этот бит используется только совместно с [**линесетупконференце**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) и [**линепрепареаддтоконференце**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference). Адрес для Конференции с текущим вызовом указывается в элементе **targetAddress** в [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). Вызов консультации не является физическим выдачей сигнала от коммутатора, но будет проходить по различным состояниям набора вызовов (например, по набору номера, по продолжению работы). Когда вызов консультации достигнет состояния Connected, Конференция устанавливается автоматически. Исходный вызов, который оставался в состоянии Connected (подключен), переходит в состояние conferenceed. вызов консультации переходит в состояние conferenceed (конференция). Хконфкалл переходит в состояние Connected. Если вызов консультации завершается неудачей (переходит в состояние DISCONNECTED, а затем в режиме простоя), Хконфкалл также переходит в состояние простоя, а исходный вызов (который мог быть уже существующей конференции в случае **линепрепареаддтоконференце**) остается в подключенном состоянии. Исходная сторона (или стороны) никогда не воспринимает вызов. Эта функция часто используется для добавления супервизора в вызов ACD-агента, когда это необходимо для отслеживания взаимодействия с вызывающим объектом ирате.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ онестептрансфер**
</dt> <dd> <dl> <dt>



Этот бит используется только совместно с [**линесетуптрансфер**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). Он сочетает в себе операцию **линесетуптрансфер** , за которой следует [**линедиал**](/windows/desktop/api/Tapi/nf-tapi-linedial) на вызов консультации в один шаг. Адрес, который необходимо набрать, указывается в элементе **targetAddress** в [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). Исходный вызов помещается в состояние *онхолдпендингтрансфер* , как если бы **линесетуптрансфер** вызывался обычным образом, а вызов консультации устанавливается обычным образом. Приложение по-прежнему должно вызывать [**линекомплететрансфер**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) , чтобы влиять на перемещение. Эта функция часто используется при вызове передачи с сервера по ссылке на управление вызовами стороннего производителя, так как такие ссылки часто не поддерживают стандартный двухэтапный процесс.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ оригоффхук**
</dt> <dd> <dl> <dt>



Телефон инициатора должен автоматически принимать оффхук.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ предиктиведиал**
</dt> <dd> <dl> <dt>



Этот бит используется только при помещении вызова на адрес с возможностью прогнозного набора (ЛИНЕАДДРКАПФЛАГС \_ предиктиведиалер включен в член **Дваддркапфлагс** в [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)). Чтобы включить расширенный ход вызова и (или) возможности мониторинга устройства мультимедиа, бит должен быть включен. Если этот бит не включен, вызов будет помещен без улучшенного хода выполнения вызова или наблюдения за типами мультимедиа, а автоматическое перемещение не будет инициировано на основе состояния вызова.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**ЛИНЕКАЛЛПАРАМФЛАГС \_ безопасность**
</dt> <dd> <dl> <dt>



Вызов должен быть настроен как безопасный.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**линекомплететрансфер**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**линедиал**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**линепрепареаддтоконференце**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**линесетупконференце**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**линесетуптрансфер**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




