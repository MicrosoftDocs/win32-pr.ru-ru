---
description: Evalcom2.dll можно использовать для реализации операций проверки для пакетов установки и модулей слияния с помощью внутренних оценщиков согласованности — ICEs.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Использование Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809922"
---
# <a name="using-evalcom2"></a>Использование Evalcom2

Evalcom2.dll можно использовать для реализации операций проверки для пакетов установки и модулей слияния с помощью [внутренних оценщиков согласованности — ICEs](internal-consistency-evaluators-ices.md). Основной объект реализует интерфейсы для программ C/C++.

Основной объект также реализует [интерфейсы Evalcom2](evalcom2-interfaces.md) для программ C/C++. CLSID, необходимый для получения интерфейса из [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , — {6E5E1910-8053-4660-B795-6B612E29BC58}. РЕФИИД имеет значение {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.

Для реализации операций проверки можно использовать следующую процедуру.

**Реализация операций проверки**

1.  Инициализируйте COM в вызывающем потоке с помощью [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).
2.  Получите указатель на интерфейс [**ивалидате**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) , используя [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).
3.  Откройте установочный пакет или модуль слияния с помощью метода [**опендатабасе**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) .
4.  Откройте файл оценки с помощью метода [**опенкуб**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) .
5.  Задайте функцию обратного вызова для вывода с помощью метода [**сетдисплай**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) .
6.  Задайте функцию обратного вызова состояния с помощью метода [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) .
7.  Выполните проверку с помощью метода [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) .
8.  Закройте файл. cub с помощью метода [**клосекуб**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) .
9.  Закройте базу данных с помощью метода [**клоседатабасе**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) .
10. Освободите интерфейс [**ивалидате**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) .
11. Отменить инициализацию COM с помощью [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы Evalcom2](evalcom2-interfaces.md)
</dt> <dt>

[Автоматизация проверки](validation-automation.md)
</dt> <dt>

[Функции обратного вызова проверки](validation-callback-functions.md)
</dt> </dl>

 

 
