---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 223cfe51-8b1d-4965-b7b1-acc3cd5619f0
ms.tgt_platform: multiple
title: S (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48473c58a1c9aae3f3c9e67f7723167b46df0285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684436"
---
# <a name="s-wmi"></a>S (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [р](gloss-h.md) [.](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) S [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_schema"></span><span id="WMI.GLOSS_SCHEMA"></span>**схемы**
</dt> <dd>

Коллекция определений классов, описывающих [*управляемые объекты*](gloss-m.md) в определенной среде.

</dd> <dt>

<span id="wmi.gloss_security_descriptor"></span><span id="WMI.GLOSS_SECURITY_DESCRIPTOR"></span>**Дескриптор безопасности**
</dt> <dd>

Структура данных, содержащая сведения о безопасности защищаемого объекта, например общего ресурса, файла, приемника или фильтра событий.

</dd> <dt>

<span id="wmi.gloss_security_identifier"></span><span id="WMI.GLOSS_SECURITY_IDENTIFIER"></span>**Идентификатор безопасности (SID)**
</dt> <dd>

Структура данных, определяющая учетные записи пользователей, групп и компьютеров.

</dd> <dt>

<span id="wmi.gloss_semi_synchronous"></span><span id="WMI.GLOSS_SEMI_SYNCHRONOUS"></span>**частично синхронный**
</dt> <dd>

См. раздел *метод семисинчронаус*.

</dd> <dt>

<span id="wmi.gloss_semi__synchronous"></span><span id="WMI.GLOSS_SEMI__SYNCHRONOUS"></span>**с частичным синхронным**
</dt> <dd>

См. раздел *метод семисинчронаус*.

</dd> <dt>

<span id="wmi.gloss_semisynchronous"></span><span id="WMI.GLOSS_SEMISYNCHRONOUS"></span>**метод семисинчронаус**
</dt> <dd>

Вызов метода, который возвращает значение немедленно и позволяет приложению или скрипту перечислить возвращенные объекты как коллекцию.

</dd> <dt>

<span id="gloss_servicesid"></span><span id="GLOSS_SERVICESID"></span>**Идентификатор безопасности службы**
</dt> <dd>

Уникальный *идентификатор* безопасности, создаваемый для каждого контекста безопасности; то есть одна для "LocalService" и одна для "NetworkService". Только *идентификатор безопасности службы* имеет разрешения на доступ к ресурсам, таким как потоки и события, создаваемые хост-процессом поставщика WMI (wmiprvse.exe).

</dd> <dt>

<span id="wmi.gloss_sid"></span><span id="WMI.GLOSS_SID"></span>**ТРАНСЛЯЦИЮ**
</dt> <dd>

См. раздел *идентификатор безопасности*.

</dd> <dt>

<span id="wmi.gloss_singleton_class"></span><span id="WMI.GLOSS_SINGLETON_CLASS"></span>**одноэлементный класс**
</dt> <dd>

Класс WMI, поддерживающий один экземпляр.

</dd> <dt>

<span id="wmi.gloss_sink"></span><span id="WMI.GLOSS_SINK"></span>**Радиатор**
</dt> <dd>

COM-объект, который выступает в качестве назначения физической доставки для результатов асинхронной операции или уведомления о событии. Приемник, реализованный [*постоянным потребителем*](gloss-p.md) , поддерживает интерфейс [**ивбемунбаундобжектсинк**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . Приемник, реализованный [*временным потребителем*](gloss-t.md) или приложениями, выполняющими асинхронные вызовы, поддерживает интерфейс [**ивбемобжектсинк**](iwbemobjectsink.md) .

Клиенты скриптов могут использовать объект и события [**свбемсинк**](swbemsink.md) , такие как [**онобжектреади**](swbemsink-onobjectready.md), для получения обратных вызовов, полученных в результате асинхронных вызовов.

</dd> <dt>

<span id="wmi.gloss_standard_consumer"></span><span id="WMI.GLOSS_STANDARD_CONSUMER"></span>**Стандартный потребитель**
</dt> <dd>

Предустановленные [*постоянные потребители*](gloss-p.md) , которые выполняют такие действия, как отправка сообщения электронной почты или запись в журнал при настройке с помощью файла [*MOF-файл (MOF)*](gloss-m.md) или скрипта.

</dd> <dt>

<span id="wmi.gloss_standard_provider"></span><span id="WMI.GLOSS_STANDARD_PROVIDER"></span>**Стандартный поставщик**
</dt> <dd>

[*Поставщик*](gloss-p.md) , встроенный в WMI, который отличается от стороннего или пользовательского поставщика.

</dd> <dt>

<span id="wmi.gloss_standard_qualifier"></span><span id="WMI.GLOSS_STANDARD_QUALIFIER"></span>**Стандартный квалификатор**
</dt> <dd>

[*Квалификатор*](gloss-q.md) , который [*Диспетчер объектов CIM*](gloss-c.md) автоматически присоединяется к классу, экземпляру, свойству, методу или параметру метода.

</dd> <dt>

<span id="wmi.gloss_standard_schema"></span><span id="WMI.GLOSS_STANDARD_SCHEMA"></span>**Стандартная схема**
</dt> <dd>

Общая концептуальная платформа, которая организует и связывает классы, представляющие текущее рабочее состояние системы, сети или приложения. [*Распределенное управление задачей Force (DMTF)*](gloss-d.md) определяет стандартную схему в [*модель CIM (CIM)*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_static_class"></span><span id="WMI.GLOSS_STATIC_CLASS"></span>**Статический класс**
</dt> <dd>

Определение класса CIM, которое редко изменяется и хранится в [*репозитории CIM*](gloss-c.md) до тех пор, пока он не будет явно удален. [*Диспетчер объектов CIM*](gloss-c.md) может предоставить определение статического класса без [*поставщика*](gloss-p.md). Статический класс может поддерживать как *статические* , так и [*динамические экземпляры*](gloss-d.md).

</dd> <dt>

<span id="wmi.gloss_static_instance"></span><span id="WMI.GLOSS_STATIC_INSTANCE"></span>**статический экземпляр**
</dt> <dd>

Экземпляр класса CIM, который постоянно хранится в [*репозитории CIM*](gloss-c.md) и остается действительным до тех пор, пока не будет явно удален, даже при перезапуске системы.

</dd> <dt>

<span id="wmi.gloss_static_method"></span><span id="WMI.GLOSS_STATIC_METHOD"></span>**статический метод**
</dt> <dd>

Метод, определенный в классе CIM, который выполняется путем извлечения определения класса вместо получения экземпляра класса.

</dd> <dt>

<span id="wmi.gloss_subschema"></span><span id="WMI.GLOSS_SUBSCHEMA"></span>**подсхема**
</dt> <dd>

Часть *схемы* , принадлежащая определенной организации. [*Win32schema*](gloss-w.md) является примером подсхемы.

</dd> <dt>

<span id="wmi.gloss_system_class"></span><span id="WMI.GLOSS_SYSTEM_CLASS"></span>**системный класс**
</dt> <dd>

Класс, определяемый [*Диспетчер объектов CIM*](gloss-c.md) для поддержки основных функций, таких как уведомления о событиях, безопасность и локализация. Системный класс определяется автоматически в каждом [*пространстве имен*](gloss-n.md). Системный класс является производным от абстрактного базового класса [**\_ \_ системкласс**](--systemclass.md).

</dd> <dt>

<span id="wmi.gloss_system_monitor"></span><span id="WMI.GLOSS_SYSTEM_MONITOR"></span>**Системный монитор**
</dt> <dd>

Служебная программа (CIM), которая является графическим интерфейсом для мониторинга производительности.

</dd> <dt>

<span id="wmi.gloss_system_property"></span><span id="WMI.GLOSS_SYSTEM_PROPERTY"></span>**системное свойство**
</dt> <dd>

Свойство, которое определяет [*Диспетчер объектов CIM*](gloss-c.md) , чтобы предоставить сведения, относящиеся к каждому классу, например имя, производные и [*пространство имен*](gloss-n.md).

</dd> </dl>

 

 



