---
title: Интерфейсы API диспетчера методов ввода не поддерживаются в упрощенном китайском языке (IME)
description: Интерфейсы API диспетчера методов ввода не поддерживаются в упрощенном китайском языке (IME)
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0454df8df722992e321fd7fc6bd745382ea215116b2fd5a7797f2032a9c7e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935414"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>Интерфейсы API диспетчера методов ввода не поддерживаются в упрощенном китайском языке (IME)

## <a name="platforms"></a>Платформы

<dl> Клиенты — Windows 8.1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>Описание

Следующие API диспетчера методов ввода не поддерживаются упрощенными редакторами IME в Windows 8.1:

-   Интерфейс Ифекоммон
-   Интерфейс Ифедиктионари
-   Интерфейс Ифелангуаже
-   Интерфейс Иимепад
-   Интерфейс Иимепадапплет
-   Интерфейс ИимеспеЦифяпплетс

## <a name="manifestations"></a>Проявлениями

Функции, использующие эти API, не работают с упрощенным IME.

## <a name="solution"></a>Решение

Приложения должны быть спроектированы таким образом, чтобы пользователи могли выполнять нужную задачу без использования указанного API.

## <a name="resources"></a>Ресурсы

-   [Интерфейсы диспетчера методов ввода](../intl/input-method-manager-interfaces.md)
-   [ифекоммон](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Интерфейс Ифекоммон](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Интерфейс Ифедиктионари](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [ифелангуаже](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [иимепад](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [иимепадапплет](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [иимеплугиндиктдиктионарилист](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [иимеспеЦифяпплетс](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 