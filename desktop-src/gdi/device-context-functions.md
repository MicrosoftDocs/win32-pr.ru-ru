---
description: В контекстах устройств используются следующие функции.
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: Функции контекста устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33eda03ce65a5873c4420f6675128243e30493dc75fa3055c8718f6826f4a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966054"
---
# <a name="device-context-functions"></a>Функции контекста устройства

В контекстах устройств используются следующие функции.



| Функция                                                   | Описание                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**канцелдк**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | Отменяет все ожидающие операции в указанном контексте устройства.                                                                            |
| [**чанжедисплайсеттингс**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | Изменяет параметры устройства вывода по умолчанию на указанный графический режим.                                                        |
| [**чанжедисплайсеттингсекс**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | Изменяет параметры указанного устройства вывода на указанный графический режим.                                                      |
| [**креатекомпатибледк**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | Создает контекст устройства памяти, совместимый с указанным устройством.                                                                     |
| [**креатедк**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | Создает контекст устройства для устройства, используя указанное имя.                                                                           |
| [**Создать**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | Создает информационный контекст для указанного устройства.                                                                                  |
| [**делетедк**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | Удаляет указанный контекст устройства.                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | Удаляет логическое перо, кисть, шрифт, точечный рисунок, область или палитру, освобождая все системные ресурсы, связанные с объектом.                  |
| [**девицекапабилитиес**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | Получает возможности драйвера печатающего устройства.                                                                                    |
| [**дравескапе**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | Предоставляет возможности рисования указанного экрана видео, которые недоступны напрямую через интерфейс графических устройств.       |
| [**енумдисплайдевицес**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | Извлекает сведения об устройствах вывода в системе.                                                                              |
| [**енумдисплайсеттингс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | Извлекает сведения о одном из графических режимов для устройства вывода.                                                               |
| [**енумдисплайсеттингсекс**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | Извлекает сведения о одном из графических режимов для устройства вывода.                                                               |
| [**енумобжектс**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | Перечисляет перья или кисти, доступные для указанного контекста устройства.                                                                |
| [**енумобжектспрок**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | Определяемая приложением функция обратного вызова, используемая с функцией [**енумобжектс**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) .                                       |
| [**жеткуррентобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | Извлекает маркер объекта указанного типа, выбранного в заданном контексте устройства.                           |
| [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | Извлекает маркер контекста устройства отображения для клиентской области указанного окна или для всего экрана.                        |
| [**жетдкбрушколор**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | Извлекает текущий цвет кисти для указанного контекста устройства.                                                                       |
| [**жетдцекс**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | Извлекает маркер контекста устройства отображения для клиентской области указанного окна или для всего экрана.                        |
| [**жетдкоржекс**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | Извлекает конечный источник преобразования для указанного контекста устройства.                                                                    |
| [**жетдкпенколор**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | Извлекает текущий цвет пера для указанного контекста устройства.                                                                         |
| [**жетдевицекапс**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | Извлекает сведения о конкретном устройстве для указанного устройства.                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | Извлекает макет контекста устройства.                                                                                                 |
| [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | Извлекает сведения для указанного объекта Graphics.                                                                                  |
| [**жетобжекттипе**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | Извлекает тип указанного объекта.                                                                                               |
| [**жетстоккобжект**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | Извлекает маркер одного из перьев, кистей, шрифтов или палитр.                                                                 |
| [**релеаседк**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | Освобождает контекст устройства, освобождая его для использования другими приложениями.                                                                      |
| [**ресетдк**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | Обновляет указанный контекст устройства принтера или плоттера, используя указанные сведения.                                                  |
| [**ресторедк**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | Восстанавливает контекст устройства в указанном состоянии.                                                                                         |
| [**саведк**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | Сохраняет текущее состояние указанного контекста устройства путем копирования данных, описывающих выбранные объекты и графические режимы, в стек контекста. |
| [**Функцию**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | Выбирает объект в указанном контексте устройства.                                                                                      |
| [**сетдкбрушколор**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Устанавливает цвет кисти контекста текущего устройства в указанное значение цвета.                                                                 |
| [**сетдкпенколор**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | Устанавливает цвет пера контекста текущего устройства в указанное значение цвета.                                                                   |
| [**сетлайаут**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | Задает макет для контекста устройства.                                                                                                     |
| [**виндовфромдк**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | Возвращает маркер окна, связанного с контекстом устройства.                                                                          |



 

 

 
