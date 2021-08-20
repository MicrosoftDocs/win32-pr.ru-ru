---
description: Ниже приведен список LIB-файлов, необходимых для компиляции различных приложений TAPI 3, начиная с 1/22/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Требуются библиотеки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8337042681d84b5f93d5d0218cff18c4bef9259543f60fd13f692ebe5611835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621364"
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

если вы используете Microsoft Visual Studio, может потребоваться обновить версию. В частности, Link.exe должен содержать дату 3/19/98 или более поздней версии.

Определение компилятора должно включать \_ Win32 \_ WinNT, установленный как минимум в 0x500 и \_ Win32 \_ DCOM.

 

 



