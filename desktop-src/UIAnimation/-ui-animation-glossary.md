---
title: Windows Глоссарий анимации
description: в этом глоссарии содержатся термины и акронимы, представляющие интерес для разработчиков, использующих Windowsный диспетчер анимации.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 66e9cfb4-b9ae-4c21-9b1f-532c7d750903
keywords:
- Windows анимация Windows анимации, глоссарий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb477edcaa49aa8baff1bc628ca5d94c13dacc0e552137275ff1e92d8e4cfae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137397"
---
# <a name="windows-animation-glossary"></a>Windows Глоссарий анимации

в этом глоссарии содержатся термины и акронимы, представляющие интерес для разработчиков, использующих Windowsный диспетчер анимации.

<dl> <dt>

<span id="uianimation.term.animation"></span><span id="UIANIMATION.TERM.ANIMATION"></span>**анимация** 
</dt> <dd>

Последовательность искусственных, последовательных изображений, которые создают иллюзию движения при воспроизведении.

</dd> <dt>

<span id="uianimation.term.animation_manager"></span><span id="UIANIMATION.TERM.ANIMATION_MANAGER"></span>**диспетчер анимации** 
</dt> <dd>

основной компонент анимации Windows и центрального программного интерфейса для управления анимациями (создания, планирования и управления).

</dd> <dt>

<span id="uianimation.term.animation_timer"></span><span id="UIANIMATION.TERM.ANIMATION_TIMER"></span>**таймер анимации**
</dt> <dd>

Компонент для предоставления служб времени, которые можно использовать совместно с диспетчером анимации. Он динамически регулирует частоту кадров в зависимости от загрузки приложения и системы или в режиме низкого энергопотребления. См. также: регулирование.

</dd> <dt>

<span id="uianimation.term.animation_variable"></span><span id="UIANIMATION.TERM.ANIMATION_VARIABLE"></span>**переменная анимации** 
</dt> <dd>

Значение, которое может быть анимировано. Переменные анимации могут использоваться для представления расположения, размера, вращения, прозрачности и других качеств видимых объектов.

</dd> <dt>

<span id="uianimation.term.cancellation"></span><span id="UIANIMATION.TERM.CANCELLATION"></span>**уведомление**
</dt> <dd>

Процесс удаления раскадровки из расписания до начала воспроизведения.

</dd> <dt>

<span id="uianimation.term.compression"></span><span id="UIANIMATION.TERM.COMPRESSION"></span>**компакт**
</dt> <dd>

Деформацию восприятия времени раскадровки. Система увеличивает скорость, с которой раскадровка проходит, передавая значения времени ввода, которые увеличиваются быстрее системных часов.

</dd> <dt>

<span id="uianimation.term.conclusion"></span><span id="UIANIMATION.TERM.CONCLUSION"></span>**завершен**
</dt> <dd>

Процесс направления раскадровки для выхода из неопределенного цикла. Если цикл начался, текущая итерация будет завершена, а оставшаяся часть раскадровки будет воспроизводиться. В противном случае Циклическая часть раскадровки будет полностью пропущена.

</dd> <dt>

<span id="uianimation.term.frame"></span><span id="UIANIMATION.TERM.FRAME"></span>**кадр** 
</dt> <dd>

Одно изображение в фильме или в анимации.

</dd> <dt>

<span id="uianimation.term.frame_rate"></span><span id="UIANIMATION.TERM.FRAME_RATE"></span>**Частота кадров** 
</dt> <dd>

Число кадров, отображаемых в секунду. Более высокие частоты кадров обычно создают более плавные движения на изображении.

</dd> <dt>

<span id="uianimation.term.interpolator"></span><span id="UIANIMATION.TERM.INTERPOLATOR"></span>**интерполятора**
</dt> <dd>

Объект программирования, который выполняет математическую интерполяцию значения и скорости переменной для перехода.

</dd> <dt>

<span id="uianimation.term.keyframe"></span><span id="UIANIMATION.TERM.KEYFRAME"></span>**кадр**
</dt> <dd>

Момент времени в раскадровке, который может быть указан относительно начала раскадровки, относительно другого опорного кадра или времени окончания перехода и используется для указания времени начала и окончания других переходов или цикла в раскадровке.

</dd> <dt>

<span id="uianimation.term.loop"></span><span id="UIANIMATION.TERM.LOOP"></span>**повторить**
</dt> <dd>

Раздел раскадровки между двумя опорными кадрами, которые воспроизводятся повторно. Цикл может играть конечное число раз или бесконечно.

</dd> <dt>

<span id="uianimation.term.priority_comparison"></span><span id="UIANIMATION.TERM.PRIORITY_COMPARISON"></span>**Сравнение приоритетов** 
</dt> <dd>

Определяемый клиентом код, сравнивающий две раскадровки, один из которых уже запланирован, и другое расписание для определения их относительного приоритета. Запланированная раскадровка может быть обрезана, сжата, отменена или закончена, чтобы включить планирование раскадровки с более высоким приоритетом.

</dd> <dt>

<span id="uianimation.term.storyboard"></span><span id="UIANIMATION.TERM.STORYBOARD"></span>**раскадровка** 
</dt> <dd>

Группа переходов анимации, синхронизированная относительно друг с другом.

</dd> <dt>

<span id="uianimation.term.tag"></span><span id="UIANIMATION.TERM.TAG"></span>**тег** 
</dt> <dd>

Пара, состоящая из целочисленного идентификатора и COM-объекта, используемого приложением для определения переменных анимации и раскадровок в области конкретного диспетчера анимации.

</dd> <dt>

<span id="uianimation.term.throttling"></span><span id="UIANIMATION.TERM.THROTTLING"></span>**регулирование** 
</dt> <dd>

Динамическое изменение частоты кадров анимации в соответствии с определенными требованиями. Регулирование позволяет обеспечить визуализацию анимации с одинаковой частотой кадров, одновременно минимизируя использование системных ресурсов для отрисовки с частотой, превышающей необходимый или полезный уровень.

</dd> <dt>

<span id="uianimation.term.tick"></span><span id="UIANIMATION.TERM.TICK"></span>**тактовая шкала** 
</dt> <dd>

Событие таймера, которое обычно запускает отрисовку одного кадра.

</dd> <dt>

<span id="uianimation.term.transition"></span><span id="UIANIMATION.TERM.TRANSITION"></span>**Переход** на 
</dt> <dd>

Конструкция, определяющая последовательные обновления для переменной анимации в течение определенного периода времени.

</dd> <dt>

<span id="uianimation.term.trimming"></span><span id="UIANIMATION.TERM.TRIMMING"></span>**обрезки**
</dt> <dd>

Приоритетное управление раскадровкой для переменной анимации с помощью раскадровки с более высоким приоритетом. Если обрезка раскадровки на одной или нескольких переменных приводит к преждевременному завершению раскадровки, оно считается усеченным. См. также: усечение.

</dd> <dt>

<span id="uianimation.term.truncation"></span><span id="UIANIMATION.TERM.TRUNCATION"></span>**усечение**
</dt> <dd>

Преждевременное завершение раскадровки с помощью приоритетного управления одной или несколькими переменными, которые она анимируется, с одной или несколькими раскадровкой с более высоким приоритетом. См. также: усечение.

</dd> </dl>

 

 




