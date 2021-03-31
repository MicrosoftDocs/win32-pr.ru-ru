---
title: Обнаружение состояния установки для программы установки Windows Media
description: Обнаружение состояния установки для программы установки Windows Media
ms.assetid: c3acc268-934b-4a10-aab5-4b1764cb4c87
keywords:
- Проигрыватель Windows Media, определение состояния установки
- Проигрыватель Windows Media, состояние установки
- Проигрыватель Windows Media, распространение программного обеспечения
- Проигрыватель Windows Media, повторное распространение программного обеспечения
- Определение состояния установки
- состояние установки
- распространение программного обеспечения
- повторное распространение программного обеспечения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28a4df9b842a1b6491a0ec98ca0a3182630c389
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411318"
---
# <a name="detecting-setup-status-for-windows-media-setup"></a>Обнаружение состояния установки для программы установки Windows Media

Следующий код можно использовать с пакетами распространения проигрывателя Windows Media. Состояние установки хранится в записи реестра **инсталлресулт** в следующем подразделе:

**\_Программа hKey текущее \_ пользовательское \\ по \\ Microsoft \\ MediaPlayer \\ Setup**

Запись реестра **инсталлресулт** имеет следующую форму.



| Имя              | Тип           | Значение                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| **инсталлресулт** | **REG \_ DWORD** | **Значение HRESULT** , указывающее, была ли установка проигрывателя Windows Media выполнена успешно и требуется ли перезагрузка. |



 

Ниже приведен пример кода C++, который можно включить в вызывающее приложение настройки. Этот код присвойте `fSuccess` `fRebootNeeded` переменным и значение **true** или **false** в зависимости от значения **HRESULT** , записанного программой установки проигрывателя Windows Media в пакет распространения компонента.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Распространение программного обеспечения проигрывателя Windows Media**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




