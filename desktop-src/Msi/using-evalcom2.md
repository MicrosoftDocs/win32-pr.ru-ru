---
description: Evalcom2.dll можно использовать для реализации операций проверки для пакетов установки и модулей слияния с помощью внутренних оценщиков согласованности — ICEs.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Использование Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f89ba0215e697cb03111daa80510e6ba6c677c2e74f31e74b5640340d2d0d9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527128"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейсы Evalcom2](evalcom2-interfaces.md)
</dt> <dt>

[Автоматизация проверки](validation-automation.md)
</dt> <dt>

[Функции обратного вызова проверки](validation-callback-functions.md)
</dt> </dl>

 

 
