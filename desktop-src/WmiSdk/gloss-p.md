---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dd72fca871352f8a31652eb72f693da43d1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999493"
---
# <a name="p-wmi"></a>P (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [р](gloss-h.md) [.](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**Счетчик производительности**
</dt> <dd>

Свойство в классе производительности, производное от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) , в котором хранятся данные производительности.

</dd> <dt>

<span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**Объект производительности**
</dt> <dd>

Объект в библиотеке производительности, хранящий данные в счетчиках. Эти объекты отображаются в программе [*системного монитора*](gloss-s.md) . Примерами являются объекты кэша и логические диски. При передаче в WMI процессом [*ADAP*](gloss-a.md) каждый объект превращается в два класса производительности WMI. Один класс, содержащий необработанные данные, является производным от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). Другой класс является производным от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) и содержит те же данные, которые отображаются в системном мониторе, как рассчитывается поставщиком счетчика обработанные.

</dd> <dt>

<span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**Постоянный потребитель**
</dt> <dd>

[*Потребитель событий*](gloss-e.md) , регистрация которого продолжается до тех пор, пока она не будет явно отменена. См. также [*временный потребитель*](gloss-t.md).

</dd> <dt>

<span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**физический потребитель**
</dt> <dd>

COM-объект, реализованный [*поставщиком потребителей событий*](gloss-e.md) , который содержит [*приемник*](gloss-s.md) для получения уведомлений о событиях.

</dd> <dt>

<span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**свойства**
</dt> <dd>

Пара имя/значение, описывающая единицу данных для класса. Значения свойств должны иметь допустимый [*MOF-файл типа данных (MOF)*](gloss-m.md) . См. также [*свойство Reference*](gloss-r.md).

</dd> <dt>

<span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**поставщик свойств**
</dt> <dd>

COM-сервер, который поддерживает извлечение и изменение свойств WMI. Поставщики свойств реализуют интерфейсы [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и [**ивбемпропертипровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) .

</dd> <dt>

<span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**поставщики**
</dt> <dd>

COM-сервер, который обменивается данными с управляемыми объектами для доступа к данным и уведомлениям о событиях, таким как реестр или SNMP-устройство. Поставщики перенаправляют эти данные в [*Диспетчер объектов CIM*](gloss-c.md) для интеграции и интерпретации.

</dd> <dt>

<span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**метод поставщика**
</dt> <dd>

Метод, реализуемый *поставщиком* WMI.

</dd> </dl>

 

 
