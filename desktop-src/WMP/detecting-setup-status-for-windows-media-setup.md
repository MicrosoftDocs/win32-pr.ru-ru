---
title: обнаружение состояния установки Windows носителя
description: обнаружение состояния установки Windows носителя
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- проигрыватель Windows Media, обнаружение состояния установки
- проигрыватель Windows Media, состояние установки
- проигрыватель Windows Media, распространение программного обеспечения
- проигрыватель Windows Media, повторное распространение программного обеспечения
- Определение состояния установки
- состояние установки
- распространение программного обеспечения
- повторное распространение программного обеспечения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797c7cb5fe4d34895109777c4da7e15489a0d32acd9cf42660b3346521f6f059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340903"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a>обнаружение состояния установки Windows носителя

следующий код можно использовать с пакетами распространения проигрыватель Windows Media. Состояние установки хранится в записи реестра **инсталлресулт** в следующем подразделе:

**\_Программа hKey текущее \_ пользовательское \\ по \\ Microsoft \\ MediaPlayer \\ Setup**

Запись реестра **инсталлресулт** имеет следующую форму.



| Имя              | Тип           | Значение                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **инсталлресулт** | **REG \_ DWORD** | **значение HRESULT** , указывающее, была ли успешная установка проигрыватель Windows Media и требуется ли перезагрузка. |



 

Ниже приведен пример кода C++, который можно включить в вызывающее приложение настройки. этот код устанавливает `fSuccess` `fRebootNeeded` переменные и равными **true** или **false** в зависимости от значения **HRESULT** , записанного проигрыватель Windows Media установки в пакете перераспределения компонентов.


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
 
if( ERROR_SUCCESS == RegOpenKeyExA( 
                         HKEY_CURRENT_USER, 
                         "Software\\Microsoft\\MediaPlayer\\Setup", 
                         0, KEY_QUERY_VALUE, &hKey ))
    {
        char szResult[64];
        DWORD dwResult = sizeof( szResult );
 
if( ERROR_SUCCESS == RegQueryValueExA( 
                         hKey, "InstallResult", NULL, NULL, 
                         (LPBYTE)szResult, &dwResult ) )
        {
            sscanf_s( szResult, "%x", &dwResult );
            fSuccess = SUCCEEDED( dwResult );
            fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwResult );
        }
 
        RegCloseKey( hKey );
    }
 
    if( fSuccess )
    {
        printf( "Setup Succeeded..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
    else
    {
        printf( "Setup Failed..." );
        if( fRebootNeeded )
            printf( "A restart IS required...\n" );
        else
            printf( "A restart IS NOT required...\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**распространение проигрыватель Windows Media программного обеспечения**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




