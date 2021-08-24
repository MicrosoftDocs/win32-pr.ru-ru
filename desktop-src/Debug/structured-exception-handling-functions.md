---
description: В структурированной обработке исключений используются следующие функции.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Функции структурированной обработки исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947cde636051e6d51428b1d75b7d299ce196b0f4335e096f99d6da6a277ae259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815504"
---
# <a name="structured-exception-handling-functions"></a>Функции структурированной обработки исключений

В структурированной обработке исключений используются следующие функции.

-   [**абнормалтерминатион**](abnormaltermination.md)

    Указывает, завершается ли блок **\_ \_ try** обработчика завершения в обычном режиме.

-   [**аддвекторедконтинуехандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    Регистрирует обработчик векторного продолжения.

-   [**аддвекторедексцептионхандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    Регистрирует векторный обработчик исключений.

-   [**GetExceptionCode**](getexceptioncode.md)

    Извлекает код, определяющий тип произошедшего исключения.

-   [**жетексцептионинформатион**](getexceptioninformation.md)

    Извлекает независимое от компьютера описание исключения и сведения о состоянии компьютера, существовавшего для потока при возникновении исключения.

-   [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    Вызывает исключение в вызывающем потоке.

-   [**ремовевекторедконтинуехандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    Отменяет регистрацию обработчика векторного продолжения.

-   [**ремовевекторедексцептионхандлер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    Отменяет регистрацию векторного обработчика исключений.

-   [**ртладдгроваблефунктионтабле**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    Информирует систему о динамической таблице функций, представляющей область памяти, в которой находится код.

-   [**ртлделетегроваблефунктионтабле**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    Информирует систему о том, что ранее указанная таблица динамической функции больше не используется.

-   [**ртлгровфунктионтабле**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    Сообщает о увеличении размера таблицы динамической функции.

-   [**сетунхандледексцептионфилтер**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    Позволяет приложению заменять обработчик исключений верхнего уровня для каждого потока и процесса.

-   [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    Передает необработанные исключения в отладчик, если процесс отлаживается.

-   [**векторедхандлер**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    Определяемая приложением функция, которая служит в качестве векторного обработчика исключений.

Следующие функции используются только для 64-разрядных Windows.

-   [**ртладдфунктионтабле**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    Добавляет таблицу динамической функции в список таблиц динамических функций.

-   [**ртлкаптуреконтекст**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    Извлекает запись контекста в контексте вызывающего объекта.

-   [**ртлделетефунктионтабле**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    Удаляет таблицу динамической функции из списка таблиц динамических функций.

-   [**ртлинсталлфунктионтаблекаллбакк**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    Добавляет таблицу динамической функции в список таблиц динамических функций.

-   [**ртлрестореконтекст**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    Восстанавливает контекст вызывающего объекта в указанную запись контекста.

 

 
