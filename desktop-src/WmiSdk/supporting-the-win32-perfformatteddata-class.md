---
description: При написании высокопроизводительного поставщика, который наследует классы из Win32 \_ перфформаттеддата, необходимо соблюдать определенные соглашения, чтобы инструментарий WMI мог вычислить значения свойств.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Поддержка класса Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702997"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a>Поддержка класса Win32 \_ перфформаттеддата

При написании высокопроизводительного поставщика, который наследует классы из [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), необходимо соблюдать определенные соглашения, чтобы инструментарий WMI мог вычислить значения свойств.

> [!Note]  
> Создание высокопроизводительного поставщика WMI для создания счетчиков производительности не рекомендуется в любой версии операционной системы Windows. Дополнительные сведения см. в разделе [Создание поставщика экземпляров в поставщике High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)и [библиотеках производительности и WMI](performance-libraries-and-wmi.md).

 

В следующей процедуре описывается поддержка \_ класса Win32 перфформаттеддата.

**Поддержка \_ класса Win32 перфформаттеддата**

1.  Создайте класс в том же пространстве имен, что и соответствующий необработанный класс. Класс должен быть производным от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) и иметь квалификатор **HiPerf** со значением **true**. Дополнительные сведения о создании собственного класса для WMI см. в разделе [Разработка классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).
2.  Укажите "Хиперфкукер \_ v1" в квалификаторе [**поставщика**](class-qualifiers-for-performance-counter-classes.md) .
3.  В дополнение к квалификаторам, используемым для необработанных классов, укажите следующие квалификаторы уровня класса:

    -   [**Автокука**](class-qualifiers-for-performance-counter-classes.md)
    -   [**\_Равкласс**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Обработанные**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Требуют**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Динамический**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Языкового стандарта**](class-qualifiers-for-performance-counter-classes.md)
    -   [**перфдефаулт**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Поставщик**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Одноэлементный**](standard-wmi-qualifiers.md)

    > [!Note]  
    > Не устанавливайте значения для **женерикперфктр**, **перфиндекс** или **хелпиндекс** , так как они будут установлены процессом ADAP. Дополнительные сведения см. в разделе [**Квалификаторы класса для классов счетчиков производительности**](class-qualifiers-for-performance-counter-classes.md).

     

4.  Включите в класс ключевое свойство с именем **Name** (это свойство не требуется для одноэлементных классов).

    Значение свойства **Name** должно совпадать с соответствующим необработанным классом. Не следует использовать ключевое свойство, кроме **Name** , в классе.

5.  Создайте данные свойств, которые имеют тип **DWORD** (**UInt32**) или **QWORD** (**UInt64**).

    Свойства должны соответствовать свойству в необработанном классе или свойству в создаваемом классе.

6.  Укажите следующие квалификаторы уровня свойств для всех свойств в классе в дополнение к квалификаторам **перфиндекс** и **перфдетаил** , используемым для свойств необработанного класса:

    -   [**Из**](property-qualifiers-for-performance-counter-classes.md)
    -   [**кукингтипе**](property-qualifiers-for-performance-counter-classes.md)
    -   [**Счетчик**](property-qualifiers-for-performance-counter-classes.md)
    -   [**перфтиместамп**](property-qualifiers-for-performance-counter-classes.md)
    -   [**перфтимефрек**](property-qualifiers-for-performance-counter-classes.md)
    -   [**самплевиндов**](property-qualifiers-for-performance-counter-classes.md)

    Дополнительные сведения см. в разделе [**Квалификаторы свойств для классов счетчиков производительности**](property-qualifiers-for-performance-counter-classes.md). Кроме того, файл заголовка Винперф. h содержит значения, которые можно указать для **перфдетаил** и **CounterType**.

7.  Убедитесь, что поставщик отвечает [требованиям к производительности](#performance-requirements).

## <a name="performance-requirements"></a>Требования к производительности

При создании высокопроизводительного поставщика его производительность должна соответствовать следующим требованиям.

-   Открытие файла DLL высокой производительности может занять не более 100 миллисекунд. В целом, открытие каждого высокопроизводительного поставщика и библиотеки производительности не может превышать 5 секунд.
-   Обновление данных может занимать не более 10 миллисекунд на операцию накопления. При общей операции обновления и получения все высокопроизводительные поставщики вместе не могут занимать более 800 миллисекунд.
-   Общая нагрузка ЦП для всех высокопроизводительных поставщиков не может превышать 6-7% ресурсов ЦП в интерактивном режиме или 5% для ведения журнала.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание поставщика экземпляров в поставщике High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
