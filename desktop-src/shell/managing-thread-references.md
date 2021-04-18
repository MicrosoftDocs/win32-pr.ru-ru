---
description: Эта статья содержит сведения об управлении ссылками на потоки с помощью функций из упрощенных служебных функций оболочки.
ms.assetid: d8d479fd-c45a-4dfa-b496-76abc7c09a42
title: Управление ссылками на потоки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b629cd97c99e3b30e66810b5f54720d0dbb1c87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985656"
---
# <a name="managing-thread-references"></a>Управление ссылками на потоки

Эта статья содержит сведения об управлении ссылками на потоки с помощью функций из упрощенных служебных функций оболочки.


Ситуации возникают, когда родительский поток должен оставаться активным в течение времени существования дочернего потока. Например, если объект модели COM создается в родительском потоке и маршалируется в дочерний поток, этот родительский поток не может завершиться перед дочерним потоком. Для этого оболочка предоставляет эти функции.

-   [**шкреатесреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref)
-   [**шсетсреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref)
-   [**шжетсреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref)

Используйте эти функции в родительском потоке, как описано здесь.

1.  Объявите определяемую приложением процедуру потока, следующую за формой функции [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) .

    ``` syntax
    DWORD WINAPI ThreadProc(LPVOID lpParameter);
    ```

2.  В [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))вызовите [**шкреатесреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) , чтобы создать ссылку на поток. Это предоставляет указатель на экземпляр [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Этот **IUnknown** использует значение, на которое указывает *пкреф* , для поддержания счетчика ссылок. Пока значение счетчика больше 0, поток остается активным.
3.  Используя этот указатель на [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), вызовите [**шсетсреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetthreadref) в [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)). Это задает ссылку, чтобы последующие вызовы [**шжетсреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) могли извлекаться.
4.  Если [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) создает другой поток, *среадпрок* этого потока может вызвать [**Шжетсреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetthreadref) с указателем на [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , полученным [**шкреатесреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref). Это увеличивает счетчик ссылок, на который указывает параметр *пкреф* в **шкреатесреадреф**.
5.  Создайте поток. Обычно это делается путем вызова [**шкреатесреад**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread), передавая указатель на [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) в параметре *пфнсреадпрок* . Также передайте \_ \_ флаг ссылки потока КТФ в параметре *dwFlags* . Поток активен при условии, что *среадпрок* исполняется.
6.  При создании дочернего потока передайте флаг **КТФ \_ ref \_ Count** в параметре *DwFlags* в вызове его [**шкреатесреад**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread).
7.  По мере завершения и освобождения дочерних потоков значение, на которое указывает *пкреф* родительский поток, уменьшается. После завершения всех дочерних потоков исходный [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) может завершиться и освободить итоговую ссылку на поток, удалив счетчик ссылок в 0. На этом этапе будет выпущена ссылка на исходный поток, Открытый с помощью [**шкреатесреад**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) , и поток завершился.

Еще одна связанная функция — [**шрелеасесреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreleasethreadref). Эта функция вызывается [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) , если поток был создан с помощью [**шкреатесреад**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread) с флагом **ссылки КТФ \_ Thread \_** . Однако *среадпрок* не требуется делать таким образом. Вызов [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) на указатель на [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , полученный через [**шкреатесреадреф**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadref) , должен быть выполнен.

 

 
