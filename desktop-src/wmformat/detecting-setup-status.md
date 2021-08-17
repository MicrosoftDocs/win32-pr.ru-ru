---
title: Определение состояния установки
description: Определение состояния установки
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Пакет SDK для формата мультимедиа, повторное распространение программного обеспечения
- Расширенный формат систем (ASF), повторное распространение программного обеспечения
- ASF (Расширенный системный формат), повторное распространение программного обеспечения
- Windows Пакет SDK для формата мультимедиа, повторное распространение
- Расширенный формат систем (ASF), распространение
- ASF (Расширенный системный формат), повторное распространение
- повторное распространение программного обеспечения, обнаружение состояния установки
- повторное распространение, обнаружение состояния установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250ab87fd81592b868e1dbf13106577f83e680796310aff246f0c1483fa847cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931398"
---
# <a name="detecting-setup-status"></a>Определение состояния установки

Когда исполняемый файл повторного распространения запускается на компьютере, он записывает свое состояние установки в реестре как значение **HRESULT** . Состояние установки хранится в записи реестра **инсталлресулт** в следующем подразделе:

**\_Программа hKey текущее \_ пользовательское \\ по \\ Microsoft \\ MediaPlayer \\ Setup**

Запись реестра **инсталлресулт** имеет следующую форму.



| Имя              | Тип           | Значение                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **инсталлресулт** | **REG \_ DWORD** | **значение HRESULT** , указывающее, была ли успешная установка проигрыватель Windows Media и требуется ли перезагрузка. |



 

следующий код задает для переменных *фсуцесс* и *фребутнидед* значение **True** или **False**(в зависимости от значения **HRESULT** , записанного Windows установки носителя в пакете перераспределения компонентов).


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Повторное распространение программного обеспечения**](software-redistribution.md)
</dt> </dl>

 

 




