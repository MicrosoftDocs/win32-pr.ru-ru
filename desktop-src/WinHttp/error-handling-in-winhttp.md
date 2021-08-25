---
description: Обработка ошибок в WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Обработка ошибок в WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72dac7775934684afe6cc9c9d54bc36bb8f3295c91deef7449e9a00600bc687e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899193"
---
# <a name="error-handling-in-winhttp"></a>Обработка ошибок в WinHTTP

Не все функции API WinHTTP сообщают об ошибках аналогичным образом.

Некоторые функции, например [**винхттпсеттимеаутс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts), возвращают **логическое** значение, которое указывает на сбой, если **значение равно false**. Если возвращается **значение false** , вызывающие объекты, заинтересованные в ошибке, должны вызывать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). если аргумент **GetLastError** вызывается, когда функция выполнено (возвращает все, кроме **FALSE**), возвращаемое значение становится непредсказуемым и может меняться между Windows версиями, пакетами обновления или даже между вызовами одной и той же функции.

Некоторые функции, такие как [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), возвращают [хинтернет](hinternet-handles-in-winhttp.md) псевдо. Эти функции точно одинаковы, за исключением сбоя, который возвращается **со значением NULL**. Если возвращается **значение NULL** , вызывающие объекты, заинтересованные в ошибке, должны вызывать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). если функция **GetLastError** вызывается при вызове функции выполнено (возвращаемого любого значения, но **значения NULL**), возвращаемое значение становится непредсказуемым и может меняться между Windows версиями, пакетами обновления или даже между вызовами одной и той же функции.

Некоторые функции, такие как [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult), возвращают код ошибки **DWORD** , и нет необходимости вызывать другие функции для получения дополнительных сведений об ошибках. Для этих функций не следует вызывать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) . если вызывается **GetLastError** независимо от успешности или сбоя функции, возвращаемое значение является непредсказуемым и может меняться между версиями Windows, пакетами обновления или даже между вызовами одной и той же функции.

 

 
