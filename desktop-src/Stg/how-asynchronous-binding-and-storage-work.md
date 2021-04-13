---
title: Как работает асинхронная привязка и хранилище
description: Асинхронное хранилище расширяет спецификацию структурированного хранилища COM для поддержки загрузки объектов хранилища в сетях с высокой задержкой, например в Интернете.
ms.assetid: 891152c3-5abd-45e4-a7bb-0aac23262b03
keywords:
- Как работает асинхронная привязка и хранилище
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626e8c7a55b667e158de42b3c88a17315b5e41ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413132"
---
# <a name="how-asynchronous-binding-and-storage-work"></a>Как работает асинхронная привязка и хранилище

Асинхронное хранилище расширяет спецификацию структурированного хранилища COM для поддержки загрузки объектов хранилища в сетях с высокой задержкой, например в Интернете. Асинхронное хранилище работает совместно с асинхронными моникерами для обеспечения полного асинхронного поведения привязки.

## <a name="document-object-embedded-in-a-web-page"></a>Объект Document, внедренный в веб-страницу

Когда пользователь щелкает ссылку, представляющую документ, внедренный в веб-страницу, происходят следующие события.

1.  Браузер вызывает функцию [**мкпарседисплайнаме**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) , передавая URL-адрес ссылки.
2.  [**Мкпарседисплайнаме**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) анализирует URL-адрес, создает соответствующее асинхронное моникерное имя и возвращает указатель на интерфейс [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) моникера.
3.  Браузер вызывает [**исасинкмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) , чтобы определить, является ли моникер асинхронным, создает контекст привязки, регистрирует интерфейс [**метода интерфейса IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) в контексте привязки, только если моникер является асинхронным, и вызывает [**IMoniker:: биндтубжект**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject), передавая контекст привязки.
4.  Моникер привязывается к объекту и запрашивает его для интерфейса [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , который указывает, поддерживает ли объект асинхронную привязку и хранилище. Если объект возвращает указатель на **иперсистмоникер**:

    1.  Моникер URL вызывает [**иперсистмоникер:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)), передавая ему собственный указатель [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) на объект.
    2.  Объект изменяет контекст привязки, выбирает, требуется ли блокировка или неблокировка хранилища, регистрирует собственный [**метода интерфейса IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) и вызывает [**IMoniker:: биндтостораже**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) в указателе, полученном через [**иперсистмоникер:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)).
    3.  Моникер создает асинхронное хранилище, сохраняет ссылку на интерфейс [**ифилллоккбитес**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) объекта-оболочки, регистрирует интерфейс [**ипрогресснотифи**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) в корневом хранилище и вызывает [**иперсистстораже:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), передавая указатель [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) асинхронного хранилища. По мере поступления данных (в фоновом потоке) моникер вызывает **ифилллоккбитес** для заполнения [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) во временном файле.
    4.  Объект считывает данные из хранилища и возвращает из [**иперсистмоникер:: Load**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775044(v=vs.85)) , когда он получает достаточно данных для самостоятельной инициализации. Если объект пытается прочитать данные, которые еще не скачаны, загрузчик получает уведомление на [**ипрогресснотифи**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Внутри метода [**ипрогресснотифи:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) поток загрузки либо блокируется в модальном цикле обработки сообщений, либо приводит к тому, что асинхронное хранилище возвращает «е \_ » в ожидании, в зависимости от того, запрашивал ли объект блокирование или неблокировку хранилища.

5.  Если объект не реализует [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)), моникер запрашивает [**иперсистстораже**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), который указывает, что устойчивое состояние объекта хранится в объекте хранилища. Если объект возвращает указатель на **иперсистстораже**:

    1.  Моникер вызывает [**IMoniker:: биндтостораже**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) на самом себе, запрашивая блокировку [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) (поскольку объект не поддерживает асинхронную передачу), создает асинхронное хранилище, сохраняет ссылку на интерфейс [**ифилллоккбитес**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) объекта-оболочки, регистрирует интерфейс [**Ипрогресснотифи**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) в корневом хранилище и вызывает [**иперсистстораже:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load), передавая указатель **IStorage** асинхронного хранилища. По мере поступления данных (в фоновом потоке) моникер вызывает [**ифилллоккбитес**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) для заполнения [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) во временном файле.
    2.  Объект считывает данные из хранилища и возвращает из [**иперсистстораже:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) , если он получил достаточно данных для самостоятельной инициализации. Если объект пытается прочитать данные, которые еще не были загружены, он получает уведомление о [**ипрогресснотифи**](/windows/win32/api/objidl/nn-objidl-iprogressnotify). Внутри метода [**ипрогресснотифи:: OnProgress**](/windows/win32/api/objidl/nf-objidl-iprogressnotify-onprogress) поток загрузки всегда блокируется в модальном цикле обработки сообщений.

6.  Независимо от того, является ли загрузка синхронной или асинхронной, моникер возвращает из [**IMoniker:: биндтубжект**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject), и браузер получает инициализированный запрошенный объект.
7.  Браузер запрашивает [**иолеобжект**](/windows/win32/api/oleidl/nn-oleidl-ioleobject) и размещает объект как объект документа. (На этом этапе объект может быть инициализирован не полностью, но достаточно для того, чтобы он отображал что-нибудь полезное, в этом случае скачивание продолжится в фоновом режиме.)

 

 