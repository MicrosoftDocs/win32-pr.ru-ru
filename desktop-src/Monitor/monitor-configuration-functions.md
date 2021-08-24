---
title: Мониторинг функций конфигурации
description: Мониторинг функций конфигурации
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- монитор, функции
- мониторинг, функции высокого уровня
- мониторинг, низкоуровневые функции
- мониторинг, функции перечисления
- функции высокого уровня
- низкоуровневые функции
- функции перечисления
- мониторинг конфигурации, функции
- мониторинг конфигурации, функции высокого уровня
- мониторинг конфигурации, низкоуровневые функции
- мониторинг конфигурации, функции перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b4eca3e18b5a5254ef9adc8cd55e123c26a773149d323caf517c5429d972f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013442"
---
# <a name="monitor-configuration-functions"></a>Мониторинг функций конфигурации

Следующие функции используются для получения сведений из монитора и для изменения параметров монитора. Функции конфигурации мониторинга подразделяются на функции высокого уровня, низкоуровневые функции и функции перечисления. Дополнительные сведения см. [в разделе Использование конфигурации монитора](using-monitor-configuration.md).

## <a name="high-level-functions"></a>Функции High-Level



| Функция                                                                         | Описание                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**дегауссмонитор**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | Дегауссес монитор.                                                                 |
| [**жетмониторбригхтнесс**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | Извлекает минимальные, максимальные и текущие настройки яркости монитора.             |
| [**жетмониторкапабилитиес**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | Извлекает возможности конфигурации монитора.                               |
| [**жетмониторколортемпературе**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | Извлекает текущую цветовую температуру монитора.                                     |
| [**жетмониторконтраст**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | Получает параметры минимального, максимального и текущего контраста монитора.               |
| [**жетмонитордисплайареапоситион**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | Извлекает минимальное, максимальное и текущее горизонтальное или вертикальное расположение монитора. |
| [**жетмонитордисплайареасизе**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | Извлекает минимальную, максимальную и текущую ширину и высоту монитора.                 |
| [**жетмониторредгринорблуедриве**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | Извлекает значение красного, зеленого или синего диска монитора.                               |
| [**жетмониторредгринорблуегаин**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | Извлекает значение усиления красного, зеленого или синего цвета монитора.                                |
| [**жетмонитортечнологитипе**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | Возвращает тип технологии, используемой монитором.                                  |
| [**ресторемониторфакториколордефаултс**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | Восстанавливает параметры цвета монитора до заводских значений по умолчанию.                       |
| [**ресторемониторфакторидефаултс**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | Восстанавливает параметры по умолчанию для монитора.                             |
| [**савекуррентмониторсеттингс**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | Сохраняет текущие параметры монитора в неизменяемое хранилище экрана.             |
| [**сетмониторбригхтнесс**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | Задает значение яркости монитора.                                                   |
| [**сетмониторколортемпературе**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | Задает цветовую температуру монитора.                                                  |
| [**сетмониторконтраст**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | Задает значение контраста монитора.                                                     |
| [**сетмонитордисплайареапоситион**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | Задает горизонтальное или вертикальное расположение области отображения монитора.                |
| [**сетмонитордисплайареасизе**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | Задает ширину или высоту области отображения монитора.                                |
| [**сетмониторредгринорблуедриве**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | Задает значение красного, зеленого или синего дисков монитора.                                    |
| [**сетмониторредгринорблуегаин**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | Устанавливает значение усиления красного, зеленого или синего монитора.                                     |



 

## <a name="low-level-functions"></a>Функции Low-Level



| Функция                                                                                   | Описание                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**капабилитиесрекуестандкапабилитиесрепли**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | Извлекает строку, описывающую возможности монитора.                                                        |
| [**жеткапабилитиесстрингленгс**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | Возвращает длину строки возможностей монитора.                                                       |
| [**жеттимингрепорт**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | Извлекает частоту синхронизации по горизонтали и вертикали монитора.                                     |
| [**жетвкпфеатуреандвкпфеатуререпли**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | Извлекает текущее значение, максимальное значение и тип кода для монитора в виртуальной панели управления. |
| [**савекуррентсеттингс**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | Сохраняет текущие параметры монитора в неизменяемое хранилище экрана.                                       |
| [**сетвкпфеатуре**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | Задает значение кода для монитора в виртуальной панели управления.                                            |



 

## <a name="enumeration-functions"></a>Функции перечисления



| Функция                                                                                                   | Описание                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**дестройфисикалмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | Закрывает маркер физического монитора.                                                    |
| [**дестройфисикалмониторс**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | Закрывает массив дескрипторов физического монитора.                                              |
| [**жетнумбероффисикалмониторсфромхмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | Возвращает число физических мониторов, связанных с **хмонитором** монитора. |
| [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | Возвращает число физических мониторов, связанных с устройством Direct3D.              |
| [**жетфисикалмониторсфромхмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | Возвращает физические мониторы, связанные с маркером монитора **хмонитор** .           |
| [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | Возвращает физические мониторы, связанные с устройством Direct3D.                        |



 

## <a name="internal-functions"></a>Внутренние функции

API конфигурации монитора использует следующие функции для доступа к функциональным возможностям драйвера экрана. Приложения не должны вызывать эти функции.

-   [**ддкЦижеткапабилитиесстринг**](ddccigetcapabilitiesstring.md)
-   [**ддкЦижеткапабилитиесстрингленгс**](ddccigetcapabilitiesstringlength.md)
-   [**ддкЦижеттимингрепорт**](ddccigettimingreport.md)
-   [**ддкЦижетвкпфеатуре**](ddccigetvcpfeature.md)
-   [**ддкЦисавекуррентсеттингс**](ddccisavecurrentsettings.md)
-   [**ддкЦисетвкпфеатуре**](ddccisetvcpfeature.md)
-   [**дестройфисикалмониторинтернал**](destroyphysicalmonitorinternal.md)
-   [**жетнумбероффисикалмониторс**](getnumberofphysicalmonitors.md)
-   [**жетфисикалмонитордескриптион**](getphysicalmonitordescription.md)
-   [**жетфисикалмониторс**](getphysicalmonitors.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по конфигурации монитора](monitor-configuration-reference.md)
</dt> </dl>

 

 




