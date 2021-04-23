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
# <a name="detecting-setup-status-for-windows-media-setup"></a><span data-ttu-id="0eec2-111">Обнаружение состояния установки для программы установки Windows Media</span><span class="sxs-lookup"><span data-stu-id="0eec2-111">Detecting Setup Status for Windows Media Setup</span></span>

<span data-ttu-id="0eec2-112">Следующий код можно использовать с пакетами распространения проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0eec2-112">The following code can be used with the Windows Media Player redistribution packages.</span></span> <span data-ttu-id="0eec2-113">Состояние установки хранится в записи реестра **инсталлресулт** в следующем подразделе:</span><span class="sxs-lookup"><span data-stu-id="0eec2-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="0eec2-114">**\_Программа hKey текущее \_ пользовательское \\ по \\ Microsoft \\ MediaPlayer \\ Setup**</span><span class="sxs-lookup"><span data-stu-id="0eec2-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="0eec2-115">Запись реестра **инсталлресулт** имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="0eec2-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="0eec2-116">Имя</span><span class="sxs-lookup"><span data-stu-id="0eec2-116">Name</span></span>              | <span data-ttu-id="0eec2-117">Тип</span><span class="sxs-lookup"><span data-stu-id="0eec2-117">Type</span></span>           | <span data-ttu-id="0eec2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0eec2-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eec2-119">**инсталлресулт**</span><span class="sxs-lookup"><span data-stu-id="0eec2-119">**InstallResult**</span></span> | <span data-ttu-id="0eec2-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0eec2-120">**REG\_DWORD**</span></span> | <span data-ttu-id="0eec2-121">**Значение HRESULT** , указывающее, была ли установка проигрывателя Windows Media выполнена успешно и требуется ли перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="0eec2-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="0eec2-122">Ниже приведен пример кода C++, который можно включить в вызывающее приложение настройки.</span><span class="sxs-lookup"><span data-stu-id="0eec2-122">Here is example C++ code that could be incorporated into a calling setup application.</span></span> <span data-ttu-id="0eec2-123">Этот код присвойте `fSuccess` `fRebootNeeded` переменным и значение **true** или **false** в зависимости от значения **HRESULT** , записанного программой установки проигрывателя Windows Media в пакет распространения компонента.</span><span class="sxs-lookup"><span data-stu-id="0eec2-123">This code will set the `fSuccess` and `fRebootNeeded` variables to **true** or **false**, as appropriate, based on the **HRESULT** value written by Windows Media Player Setup in the component redistribution package.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0eec2-124">См. также</span><span class="sxs-lookup"><span data-stu-id="0eec2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eec2-125">**Распространение программного обеспечения проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0eec2-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




