---
title: Функции SNMP
description: В этом разделе описываются три группы функций SNMP и перечислены функции, которые включены в каждую группу.
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- SNMP-функции
- Функции SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42028e4045d4d0dfeb183dc29a3dc85e7220ed3d5bccf39a3cc9871215188153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143017"
---
# <a name="snmp-functions"></a>Функции SNMP

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. вместо этого используйте [служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

В этом разделе описываются три группы функций SNMP и перечислены функции, которые включены в каждую группу:

-   [Функции API агента расширения SNMP](#snmp-extension-agent-api-functions)
-   [Функции API управления SNMP](#snmp-management-api-functions)
-   [Функции API служебной программы SNMP](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>Функции API агента расширения SNMP

Функции агента расширения SNMP определяют интерфейс между службой SNMP и библиотеками DLL стороннего агента расширения SNMP. В следующей таблице перечислены функции, которые приложения могут использовать для разрешения привязок переменных, заданных входящими единицами данных протокола SNMP.

| Функция API агента расширения SNMP                    | Описание                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**снмпекстенсионклосе**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Запрашивает освобождение ресурсов агентом расширения SNMP и выполнение операций.                                    |
| [**снмпекстенсионинит**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Инициализирует библиотеку DLL агента расширения SNMP.                                                                                |
| [**снмпекстенсионинитекс**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Определяет все дополнительные поддеревья MIB, поддерживаемые агентом расширения SNMP.             |
| [**снмпекстенсионмонитор**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Предоставляет агенту расширения SNMP сведения о внутренних счетчиках и параметрах службы.            |
| [**снмпекстенсионкуери**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Разрешает SNMP-запросы, содержащие переменные, в одном или нескольких зарегистрированных поддеревьях MIB агента расширения SNMP. |
| [**снмпекстенсионкуерекс**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Обрабатывает SNMP-запросы, указывающие переменные в одном или нескольких поддеревьях MIB, зарегистрированных агентами расширения SNMP. |
| [**снмпекстенсионтрап**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Извлекает сведения, необходимые службе для создания ловушек для агента расширения SNMP.                          |



 

## <a name="snmp-management-api-functions"></a>Функции API управления SNMP

Функции управления SNMP определяют интерфейс между сторонними приложениями диспетчера SNMP и библиотекой динамической компоновки (DLL) функции управления Mgmtapi.dll. Библиотека DLL работает совместно со службой ловушек SNMP (Snmptrap.exe) и может взаимодействовать с одним или несколькими приложениями диспетчера SNMP сторонних производителей. В следующей таблице перечислены функции управления, которые приложения сторонних поставщиков используют для выполнения операций SNMP-диспетчера.

| Функция API управления SNMP                   | Описание                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**снмпмгрклосе**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Закрывает коммуникационные сокеты и структуры данных, связанные с указанным сеансом.                                                                                                  |
| [**снмпмгрктл**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Задает рабочий параметр, связанный с сеансом SNMP.                                                                                                                                   |
| [**снмпмгржеттрап**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Возвращает необработанные данные ловушки, которые вызывающий объект не получил, если включен прием ловушек.                                                                                                           |
| [**снмпмгржеттрапекс**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Возвращает необработанные данные ловушки, которые вызывающий объект не получил, если включен прием ловушек. Также возвращает адрес источника транспорта и ловушку сообщества, связанную с этой ловушкой. |
| [**снмпмгроидтостр**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Преобразует внутреннюю структуру идентификатора объекта в строковое представление.                                                                                                                         |
| [**снмпмгропен**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Инициализирует коммуникационные сокеты и структуры данных, необходимые для установления связи с агентом SNMP.                                                                               |
| [**снмпмгррекуест**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Запрашивает выполнение указанной операции указанным агентом.                                                                                                                             |
| [**снмпмгрстртуид**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Преобразует строковое форматирование идентификатора объекта в его внутреннюю структуру идентификатора объекта.                                                                                                        |
| [**снмпмгртраплистен**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Регистрирует способность приложения SNMP Manager принимать SNMP-ловушки из службы ловушек SNMP.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>Функции API служебной программы SNMP

Служебные функции SNMP предоставляют возможности, которые могут быть полезны при разработке приложений SNMP, включая упрощение управления структурами данных SNMP. В следующей таблице перечислены служебные функции SNMP.

| Функция API служебной программы SNMP                                  | Описание                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**снмпсвкжетуптиме**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Возвращает время, в центисекондс, для которого была запущена служба SNMP.                                                                                  |
| [**снмпсвксетлоглевел**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Корректирует уровень детализации выходных данных отладки службы SNMP и агентов расширения SNMP.                                                              |
| [**снмпсвксетлогтипе**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Корректирует назначение для выходных данных отладки службы SNMP и агентов расширения SNMP.                                                                 |
| [**снмпутиласнаникпи**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Копирует исходную структуру [**аснани**](/windows/desktop/api/Snmp/ns-snmp-asnany) в целевую структуру **аснани** .                                                                      |
| [**снмпутиласнанифри**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Освобождает память, выделенную для указанной структуры [**аснани**](/windows/desktop/api/Snmp/ns-snmp-asnany) .                                                                        |
| [**снмпутилдбгпринт**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Задает уровень отладочной информации, которая должна быть получена от службы SNMP или из вызова [**снмпутилдбгпринт**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint).                       |
| [**снмпутилидстоа**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Преобразует идентификатор объекта (OID) в строку, завершающуюся нулем.                                                                                                   |
| [**снмпутилмемаллок**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Выделяет динамическую память из кучи процесса.                                                                                                                    |
| [**снмпутилмемфри**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Освобождает указанный объект памяти.                                                                                                                                 |
| [**снмпутилмемреаллок**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Изменяет размер указанного объекта памяти.                                                                                                                   |
| [**снмпутилоктетскмп**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Сравнивает две строки октета.                                                                                                                                        |
| [**снмпутилоктетскпи**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Копирует исходную структуру [**асноктетстринг**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) в целевую структуру **асноктетстринг** .                                              |
| [**снмпутилоктетсфри**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Освобождает память, выделенную для указанной строки октета.                                                                                                |
| [**снмпутилоктетснкмп**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Выполняет сравнение двух строк октета с указанным числом субидентификаторов.                                                                              |
| [**снмпутилоидаппенд**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Добавляет идентификатор исходного объекта, содержащийся в структуре [**аснобжектидентифиер**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) , к идентификатору целевого объекта.          |
| [**снмпутилоидкмп**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Сравнивает два идентификатора объекта, которые содержатся в структурах [**аснобжектидентифиер**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) .                                           |
| [**снмпутилоидкпи**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Копирует исходную структуру [**аснобжектидентифиер**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) в целевую структуру **аснобжектидентифиер** .                               |
| [**снмпутилоидфри**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Освобождает память, выделенную для указанного идентификатора объекта.                                                                                           |
| [**снмпутилоиднкмп**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Сравнивает два идентификатора объекта, которые содержатся в структурах [**аснобжектидентифиер**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) , с указанным числом субидентификаторов. |
| [**снмпутилоидтоа**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Преобразует идентификатор объекта (OID) в строку, завершающуюся нулем.                                                                                                   |
| [**снмпутилпринтаснани**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Выводит значение, содержащееся в структуре [**аснани**](/windows/desktop/api/Snmp/ns-snmp-asnany) , для целей отладки и разработки.                                              |
| [**снмпутилпринтоид**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Форматирует указанный идентификатор объекта (OID) и выводит результат на стандартное выходное устройство.                                                                 |
| [**снмпутилварбиндкпи**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Копирует исходную структуру [**снмпварбинд**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) в целевую структуру **снмпварбинд** .                                                       |
| [**снмпутилварбиндлисткпи**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Копирует исходную структуру [**снмпварбиндлист**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) в целевую структуру **снмпварбиндлист** .                                           |
| [**снмпутилварбиндфри**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Освобождает память, выделенную для указанной структуры [**снмпварбинд**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) .                                                            |
| [**снмпутилварбиндлистфри**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Освобождает память, выделенную для указанной структуры [**снмпварбиндлист**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) .                                                    |



 

 

 