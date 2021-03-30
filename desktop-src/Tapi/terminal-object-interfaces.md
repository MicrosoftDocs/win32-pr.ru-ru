---
description: Интерфейсы объектов терминала предоставляют приложению доступ для управления устройствами, используемыми для создания или получения потоков мультимедиа.
ms.assetid: 08320d1c-1400-4746-b526-74b0789c5fc0
title: Интерфейсы объекта терминала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3286d9a2bf3c247f813d3a1f942b0490de0154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819409"
---
# <a name="terminal-object-interfaces"></a>Интерфейсы объекта терминала

Интерфейсы [объектов терминала](terminal-object.md) предоставляют приложению доступ для управления устройствами, используемыми для создания или получения потоков мультимедиа.

Эти интерфейсы реализуются с помощью MSP и не будут доступны, если адрес не поддерживается поставщиком службы мультимедиа. Если существует связанный MSP-объект, интерфейс [**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) предоставляется в [объекте Address](address-object.md).

Интерфейсы [**иенумтерминал**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal) и [**иенумтерминалкласс**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) не предоставляются напрямую в объекте терминала, но тесно связаны с ним и перечислены здесь для удобства.



| Интерфейс                                                                  | Описание                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                           | Базовый интерфейс для объекта терминала. Он предоставляет методы для получения таких сведений, как класс терминала и поддерживаемый мультимедиа. |
| [**итаммедиаформат**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                                 | Задает и получает формат мультимедиа DirectShow.                                                                                            |
| [**итбасикаудиотерминал**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)                       | Предоставляет методы для установки и получения стандартных характеристик звукового терминала, таких как Volume.                                          |
| [**иенумтерминал**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)                                     | Перечисляет [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal).                                                                                      |
| [**иенумтерминалкласс**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)                           | Перечисляет [**класс терминала**](terminal-class.md).                                                                              |
| [**иенумплуггаблесуперклассинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)       | Перечисляет [**итплуггаблетерминалсуперклассинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo).                                        |
| [**иенумплуггаблетерминалклассинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo) | Перечисляет [**итплуггаблетерминалклассинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo).                                                  |
| [**итфилетракк**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack)                                         | Извлекает и задает сведения о дорожках файловых терминалов.                                                                   |
| [**итасртерминалевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent)                           | Извлекает описание событий терминала для автоматического распознавания речи.                                                        |
| [**итфилетерминалевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent)                         | Извлекает описание событий файлового терминала.                                                                                |
| [**итмултитракктерминал**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal)                       | Перечисление, создание или удаление дорожек на терминалах с дорожкой.                                                                   |



 



| Интерфейс                                                                                      | Описание                                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**итплуггаблетерминалклассинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                           | Получает сведения о подключаемом терминале.                                                                       |
| [**итплуггаблетерминалклассрегистратион**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalclassregistration)           | Создает, изменяет или удаляет запись реестра для подключаемого терминала.                                                   |
| [**итплуггаблетерминалинитиализатион**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalinitialization)                 | Выполняет создание основного объекта терминала для подключаемых терминалов, позволяя диспетчеру терминалов инициализировать терминал. |
| [**итплуггаблетерминалсуперклассинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                 | Извлекает имя и идентификатор CLSID подключаемого класса терминала.                                                                  |
| [**итплуггаблетерминалсуперклассрегистратион**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalsuperclassregistration) | Извлекает и устанавливает сведения о суперклассе терминала (имя и CLSID).                                                 |
| [**итплуггаблетерминалевентсинк**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink)                           | Уведомляет клиентские приложения об изменениях в подключаемом терминале.                                                          |
| [**итплуггаблетерминалевентсинкрегистратион**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)   | Регистрирует и отменяет регистрацию клиентского приложения для уведомления о подключаемых событиях терминала.                             |



 



| Интерфейс                                            | Описание                                                        |
|------------------------------------------------------|--------------------------------------------------------------------|
| [**итттстерминалевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent)     | Получает описание событий терминала преобразования текста в речь (TTS). |
| [**иттонедетектионевент**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittonedetectionevent) | Извлекает сведения о событии обнаружения тона.                |
| [**иттонетерминалевент**](/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent)   | Извлекает описание событий сигнала терминала.                 |



 

 

 
