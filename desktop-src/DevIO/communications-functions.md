---
description: Для ресурсов связи используются следующие функции.
ms.assetid: ba7d1a9e-6906-4923-a8eb-db58050ba699
title: Функции связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64853bf2b0c42d4e7ca607fbbe624995cfe1a249
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262633"
---
# <a name="communications-functions"></a>Функции связи

Для ресурсов связи используются следующие функции.



| Функция                                                   | Описание                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**буилдкоммдкб**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba)                       | Заполняет указанную структуру [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) значениями, указанными в строке управления устройством.                           |
| [**буилдкоммдкбандтимеаутс**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcbandtimeoutsa) | Преобразует строку определения устройства в соответствующие коды блоков управления устройствами и помещает их в блок управления устройством. |
| [**клеаркоммбреак**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak)                   | Восстанавливает передачу символов для указанного коммуникационного устройства и помещает линию передачи в неразрывный режим.    |
| [**клеаркоммеррор**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror)                   | Извлекает сведения об ошибке связи и сообщает о текущем состоянии коммуникационного устройства.                  |
| [**коммконфигдиалог**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga)               | Отображает диалоговое окно конфигурации, предоставляемое драйвером.                                                                           |
| [**ескапекоммфунктион**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction)           | Направляет указанное коммуникационное устройство для выполнения расширенной функции.                                                     |
| [**жеткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig)                     | Извлекает текущую конфигурацию коммуникационного устройства.                                                                |
| [**жеткомммаск**](/windows/desktop/api/Winbase/nf-winbase-getcommmask)                         | Получает значение маски событий для указанного коммуникационного устройства.                                                   |
| [**жеткомммодемстатус**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)           | Возвращает значения регистров управления модемом.                                                                                       |
| [**жеткоммпропертиес**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties)             | Извлекает сведения о свойствах связи для указанного коммуникационного устройства.                               |
| [**жеткоммстате**](/windows/desktop/api/Winbase/nf-winbase-getcommstate)                       | Извлекает текущие параметры элемента управления для указанного коммуникационного устройства.                                                  |
| [**жеткоммтимеаутс**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts)                 | Возвращает параметры времени ожидания для всех операций чтения и записи на указанном коммуникационном устройстве.                      |
| [**жетдефаулткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga)       | Извлекает конфигурацию по умолчанию для указанного коммуникационного устройства.                                                   |
| [**пуржекомм**](/windows/desktop/api/Winbase/nf-winbase-purgecomm)                             | Отменяет все символы из выходных или входного буфера указанного ресурса связи.                                |
| [**сеткоммбреак**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak)                       | Приостанавливает передачу символов для указанного коммуникационного устройства и помещает линию передачи в состояние Break.       |
| [**сеткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig)                     | Задает текущую конфигурацию коммуникационного устройства.                                                                     |
| [**сеткомммаск**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)                         | Указывает набор событий, отслеживаемых для коммуникационного устройства.                                                         |
| [**сеткоммстате**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)                       | Настраивает коммуникационное устройство в соответствии со спецификациями в блоке управления устройством.                                  |
| [**сеткоммтимеаутс**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)                 | Задает параметры времени ожидания для всех операций чтения и записи на указанном коммуникационном устройстве.                           |
| [**сетдефаулткоммконфиг**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)       | Задает конфигурацию по умолчанию для коммуникационного устройства.                                                                    |
| [**сетупкомм**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)                             | Инициализирует параметры связи для указанного коммуникационного устройства.                                               |
| [**трансмиткоммчар**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar)               | Передает указанный символ впереди всех ожидающих данных в выходном буфере указанного коммуникационного устройства.         |
| [**ваиткоммевент**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)                     | Ожидает возникновения события для указанного коммуникационного устройства.                                                             |



 

 

 



