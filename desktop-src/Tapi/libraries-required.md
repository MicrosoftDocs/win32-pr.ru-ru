---
description: Ниже приведен список LIB-файлов, необходимых для компиляции различных приложений TAPI 3, начиная с 1/22/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Требуются библиотеки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0948599041c466a337d2d6828750a9996dc8d813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673387"
---
# <a name="libraries-required"></a>Требуются библиотеки

Список LIB-файлов, необходимых для компиляции различных приложений TAPI 3, начиная с 1/22/01:

-   Advapi32. lib
-   Амстрмид. lib (идентификаторы GUID ActiveMovie)
-   Kernel32.lib
-   Мдхкпид. lib (многоадресные идентификаторы GUID)
-   Ole32. lib (COM)
-   Oleaut32. lib (модель автоматизации COM)
-   Рендид. lib (встречные идентификаторы GUID)
-   Рпкндр. lib
-   Rpcns4. lib
-   Rpcrt4. lib
-   Сдпблбид. lib (идентификаторы GUID для протокола дескрипторов сеансов (SDP))
-   Стрмиидс. lib
-   User32. lib
-   UUID. lib
-   Wldap32. lib
-   Ws2 \_ 32. lib

Если вы используете Microsoft Visual Studio, может потребоваться обновить версию. В частности, Link.exe должен содержать дату 3/19/98 или более поздней версии.

Определение компилятора должно включать \_ Win32 \_ WinNT, установленный как минимум в 0x500 и \_ Win32 \_ DCOM.

 

 



