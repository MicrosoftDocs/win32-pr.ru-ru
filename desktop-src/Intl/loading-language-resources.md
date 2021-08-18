---
description: Загрузка языковых ресурсов
ms.assetid: 2655b2a3-2926-43f6-aef4-8b756c02a162
title: Загрузка языковых ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eebf027476658872fe392fe60699da1a586f9297f39a191898b1e132439962c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106934"
---
# <a name="loading-language-resources"></a>Загрузка языковых ресурсов

Приложение загружает все языковые ресурсы пользовательского интерфейса, кроме определенных перенаправленных строк реестра, используя вызовы стандартных функций загрузки ресурсов, например [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), [**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa)и [**лоадимаже**](/windows/win32/api/winuser/nf-winuser-loadimagea). Многие функции загрузки ресурсов были изменены для автоматической загрузки ресурсов из файлов ресурсов, зависящих от языка, которые обрабатывают ресурсы так, как если бы они содержались в LN-файле. В следующем примере показано использование **лоадстринг** для загрузки языковых строк для приложения, которое соответствует системным параметрам языка.


```C++
HMODULE hResModule = LoadLibraryEx(TEXT("Mymodule.dll"), 0,
                                   LOAD_LIBRARY_AS_DATAFILE | LOAD_LIBRARY_AS_IMAGE_RESOURCE);
// ...
LoadString(hResModule, myID, lpBuffer, cbBufferSize);
// ...
FreeLibrary(hResModule);
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поиск ресурсов Win32 PE](locating-win32-pe-resources.md)
</dt> </dl>

 

 
