---
title: Определение состояния установки
description: Определение состояния установки
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Media Format SDK, повторное распространение программного обеспечения
- Расширенный формат систем (ASF), повторное распространение программного обеспечения
- ASF (Расширенный системный формат), повторное распространение программного обеспечения
- Пакет SDK для Windows Media Format, повторное распространение
- Расширенный формат систем (ASF), распространение
- ASF (Расширенный системный формат), повторное распространение
- повторное распространение программного обеспечения, обнаружение состояния установки
- повторное распространение, обнаружение состояния установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6add696f2b2989de1e77d48504a1d540634213d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779754"
---
# <a name="detecting-setup-status"></a>Определение состояния установки

Когда исполняемый файл повторного распространения запускается на компьютере, он записывает свое состояние установки в реестре как значение **HRESULT** . Состояние установки хранится в записи реестра **инсталлресулт** в следующем подразделе:

**\_Программа hKey текущее \_ пользовательское \\ по \\ Microsoft \\ MediaPlayer \\ Setup**

Запись реестра **инсталлресулт** имеет следующую форму.



| Имя              | Тип           | Значение                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **инсталлресулт** | **REG \_ DWORD** | **Значение HRESULT** , указывающее, была ли установка проигрывателя Windows Media выполнена успешно и требуется ли перезагрузка. |



 

Следующий код задает для переменных *фсуцесс* и *фребутнидед* значение **true** или **false**(в зависимости от значения **HRESULT** , записанного программой установки Windows Media в пакете перераспределения компонентов).


```C++
#include <windows.h>
#include <stdio.h>

// If NS_S_REBOOT_REQUIRED is undefined, use 0xD2AF9.
#ifndef NS_S_REBOOT_REQUIRED
#define NS_S_REBOOT_REQUIRED       0xd2af9
#endif
  
int main( void )
{
    HKEY hKey = NULL;
    BOOL fSuccess = FALSE;
    BOOL fRebootNeeded = FALSE;

    LONG lResult = RegOpenKeyEx( 
        HKEY_CURRENT_USER, 
        TEXT("Software\\Microsoft\\MediaPlayer\\Setup"), 
        0, 
        KEY_QUERY_VALUE, 
        &hKey 
        );

    if ( lResult == ERROR_SUCCESS )
    {
        DWORD dwRegType = 0;   // Registry value type.
        DWORD dwValue = 0;     // Registry value.
        DWORD cbValue = sizeof( dwValue );  // Size of the value in bytes.

        lResult = RegQueryValueEx( 
            hKey, 
            TEXT("InstallResult"), 
            NULL, 
            &dwRegType, 
            (LPBYTE)&dwValue, 
            &cbValue
            );

        if( lResult == ERROR_SUCCESS )
        {
            if (dwRegType == REG_DWORD)
            {
                fSuccess = SUCCEEDED( dwValue );
                fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwValue );
            }
        }

        RegCloseKey( hKey );
    }

    if( fSuccess )
    {
        printf( "Setup succeeded." );
    }
    else
    {
        printf( "Setup failed." );
    }

    if( fRebootNeeded )
    {
        printf( "A reboot IS required.\n" );
    }
    else
    {
        printf( "A reboot IS NOT required.\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Повторное распространение программного обеспечения**](software-redistribution.md)
</dt> </dl>

 

 




