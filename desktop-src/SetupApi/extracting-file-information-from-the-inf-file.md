---
description: После открытия файла INF можно собирать сведения из него для создания пользовательского интерфейса или для направления процесса установки. Функции установки предоставляют несколько уровней функциональности для сбора информации из INF-файла.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Извлечение сведений о файлах из INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897766"
---
# <a name="extracting-file-information-from-the-inf-file"></a>Извлечение сведений о файлах из INF-файла

После открытия файла INF можно собирать сведения из него для создания пользовательского интерфейса или для направления процесса установки. Функции установки предоставляют несколько уровней функциональности для сбора информации из INF-файла.



| Для сбора информации...                | Использовать эти функции...                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| Сведения о INF-файле                    | [**сетупжетинфинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [**сетупкуеринффилеинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | [**Сетупкуеринфверсионинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa). |
| Сведения об исходном и целевом файлах         | [**сетупжетсаурцефилелокатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [**сетупжетсаурцефилесизе**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [**сетупжеттаржетпас**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [**сетупжетсаурцеинфо**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| Из строки INF-файла            | [**сетупжетлинетекст**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [**сетупфинднекстлине**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [**сетупфинднекстматчлине**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [**сетупжетлинебиндекс**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [**сетупфиндфирстлине**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| Из поля строки в INF-файле | [**сетупжетстрингфиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [**сетупжетинтфиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [**сетупжетбинарифиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [**сетупжетмултисзфиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

В следующем примере функция [**сетупжетсаурцеинфо**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) используется для получения понятного пользователю описания исходного носителя из INF-файла.


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



В этом примере Минф — это маркер открытого INF-файла. SourceId — это идентификатор указанного исходного носителя. Описание value СРЦИНФО \_ указывает, что функция [**сетупжетсаурцеинфо**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) должна извлекать описание исходного носителя. Буфер указывает на строку, которая получит описание, Максбуфсизе указывает ресурсы, выделенные буферу, а Буфсизе — ресурсы, необходимые для хранения буфера.

Если Буфсизе больше Максбуфсизе, функция возвратит **значение false**, а последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) вернет ошибку \_ недостаточный \_ Размер буфера.

 

 
