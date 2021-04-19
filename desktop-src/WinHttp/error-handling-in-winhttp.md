---
description: Обработка ошибок в WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Обработка ошибок в WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf234220d0973e86c830063e4ecc25312fa2d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702757"
---
# <a name="error-handling-in-winhttp"></a>Обработка ошибок в WinHTTP

Не все функции API WinHTTP сообщают об ошибках аналогичным образом.

Некоторые функции, например [**винхттпсеттимеаутс**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts), возвращают **логическое** значение, которое указывает на сбой, если **значение равно false**. Если возвращается **значение false** , вызывающие объекты, заинтересованные в ошибке, должны вызывать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Если аргумент **GetLastError** вызывается, когда функция выполнено (Возвращает все, кроме **false**), возвращаемое значение становится непредсказуемым и может меняться между версиями Windows, пакетами обновления или даже между вызовами одной и той же функции.

Некоторые функции, такие как [**винхттпконнект**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), возвращают [хинтернет](hinternet-handles-in-winhttp.md) псевдо. Эти функции точно одинаковы, за исключением сбоя, который возвращается **со значением NULL**. Если возвращается **значение NULL** , вызывающие объекты, заинтересованные в ошибке, должны вызывать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Если функция **GetLastError** вызывается при вызове функции выполнено (возвращаемого любого значения, но **null**), возвращаемое значение становится непредсказуемым и может меняться между версиями Windows, пакетами обновления или даже между вызовами одной и той же функции.

Некоторые функции, такие как [**винхттпжетпроксиресулт**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult), возвращают код ошибки **DWORD** , и нет необходимости вызывать другие функции для получения дополнительных сведений об ошибках. Для этих функций не следует вызывать [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) . Если вызывается **GetLastError** независимо от успешности или сбоя функции, возвращаемое значение становится непредсказуемым и может меняться между версиями Windows, пакетами обновления или даже между вызовами одной и той же функции.

 

 
