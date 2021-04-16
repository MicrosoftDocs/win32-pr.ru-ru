---
description: Укажите сведения об объекте производительности, с которым сопоставлен класс счетчика производительности WMI.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Квалификаторы классов для классов счетчиков производительности
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712476"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a>Квалификаторы классов для классов счетчиков производительности

Квалификаторы класса указывают сведения об объекте производительности, с которым сопоставлен [класс счетчика производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI. Дополнительные сведения см. в разделе [наблюдение за данными производительности](monitoring-performance-data.md).

-   [Квалификаторы для необработанных и форматированных Перформанцеклассес](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [Квалификаторы для необработанных классов производительности](#)
-   [Квалификаторы для отформатированных классов производительности](#)
-   [См. также](#related-topics)


Счетчик производительности — конкретные квалификаторы автоматически присоединяются поставщиком "Вбемперфкласс" к классам и свойствам [**Win32 \_ Перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) в корневом \\ CIMv2.

Эти сведения применяются ко всем экземплярам класса. Некоторые квалификаторы с **логическими** значениями, которые всегда имеют **значение false** , могут отсутствовать в определенных классах.

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a>Квалификаторы для необработанных и форматированных Перформанцеклассес

Следующие квалификаторы применяются ко всем классам, производным от [**Win32 \_ Перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Обработанные**
</dt> <dd>

**boolean**

Указывает, содержит ли класс данные обработанные.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**
</dt> <dd>

**string**

Имя объекта производительности. Дополнительные сведения см. в статье [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**детаиллевел**
</dt> <dd>

**sint32**

Не предоставляет подробные данные. Всегда содержит значение 100.

</dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Платформе**
</dt> <dd>

**boolean**

Всегда имеет значение **true** , так как экземпляры всегда являются динамическими.

</dd> <dt>

<span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**женерикперфктр**
</dt> <dd>

**boolean**

Указывает, поступает ли класс из устаревшей библиотеки производительности. Всегда имеет значение **true**.

</dd> <dt>

<span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**хелпиндекс**
</dt> <dd>

**sint32**

Индексы больше не действительны. Этот квалификатор всегда равен нулю.

</dd> <dt>

<span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf** 
</dt> <dd>

**boolean**

Указывает, что класс является классом высокой производительности. Всегда имеет значение **true**.

</dd> <dt>

<span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Языкового стандарта**
</dt> <dd>

**sint32**

Идентификатор языкового стандарта. Значение всегда равно 1033 (Английский (США)).

</dd> <dt>

<span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**перфиндекс**
</dt> <dd>

**int32**

Индексы больше не действительны. Этот квалификатор всегда равен нулю.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Поставщики**
</dt> <dd>

**string**

Имя поставщика экземпляра. Значение — "WbemPerfV2".

</dd> <dt>

<span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**
</dt> <dd>

**string**

Имя драйвера в разделе **hKey \_ Local \_ Machine \\ CurrentControlSet \\ Services** , в котором можно найти ключ производительности. Это имя также является именем службы, предоставляющей счетчик производительности.

</dd> <dt>

<span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Единый**
</dt> <dd>

**boolean**

Если **значение — true**, указывает, что существует только один экземпляр класса.

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a>Квалификаторы для необработанных классов производительности

Следующие квалификаторы применяются ко всем классам, производным от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).

<dl> <dt>

<span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Требуют**
</dt> <dd>

**boolean**

Указывает, является ли получение экземпляров этого класса дорогостоящей операцией. Всегда имеет значение **true** для классов с \_ добавлением "дорогостоящих" к концу имени класса.

</dd> <dt>

<span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**детаиллевел**
</dt> <dd>

**uint32**

Не предоставляет подробные данные. Всегда содержит значение 100.

</dd> <dt>

<span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**перфдефаулт**
</dt> <dd>

**boolean**

Значение всегда равно **false**.

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a>Квалификаторы для отформатированных классов производительности

Следующие квалификаторы применяются ко всем классам, производным от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

<dl> <dt>

<span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Автокука**
</dt> <dd>

**int32**

Указывает, что значения в экземплярах класса автоматически вычисляются на основе соответствующего класса необработанных данных. Значение всегда равно 1.

</dd> <dt>

<span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**\_Равкласс**
</dt> <dd>

**string**

Имя необработанного класса, используемое для вычисления для форматированного класса. Этот квалификатор является обязательным.

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Мониторинг данных производительности](monitoring-performance-data.md)
</dt> <dt>

[Квалификаторы, относящиеся к классам производительности WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Доступ к предустановленным классам производительности WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Задачи WMI: Мониторинг производительности](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
