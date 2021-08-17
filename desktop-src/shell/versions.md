---
description: В этом разделе описывается, как определить версию библиотек DLL оболочки, на котором работает приложение, и как выбрать целевое приложение для конкретной версии.
title: 'Версии оболочки и Shlwapi DLL '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6d74371478b30037e75b1c168dc235735ba6bd219fa461245262ff55a508ae5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967843"
---
# <a name="shell-and-shlwapi-dll-versions"></a>Версии оболочки и Shlwapi DLL 

В этом разделе описывается, как определить версию библиотек DLL оболочки, на котором работает приложение, и как выбрать целевое приложение для конкретной версии.

-   [Номера версий DLL](#dll-version-numbers)
-   [Определение номера версии с помощью Дллжетверсион](#using-dllgetversion-to-determine-the-version-number)
    -   [Использование Дллжетверсион](#using-dllgetversion)
-   [Project Операционных](#project-versions)

## <a name="dll-version-numbers"></a>Номера версий DLL

Все элементы программирования, описанные в документации по оболочке, содержатся в двух библиотеках DLL: Shell32.dll и Shlwapi.dll. Из-за текущих улучшений различные версии этих библиотек DLL реализуют различные функции. В справочной документации по оболочке каждый программный элемент указывает минимальный поддерживаемый номер версии DLL. Этот номер версии указывает, что программный элемент реализован в этой версии и последующих версиях библиотеки DLL, если не указано иное. Если номер версии не указан, программный элемент реализуется во всех существующих версиях библиотеки DLL.

до Windows XP в новых версиях Windows Internet Explorer иногда появились новые версии Shell32.dll и Shlwapi.dll. начиная с Windows XP эти библиотеки dll больше не были предоставлены как распространяемые файлы за пределами новых версий Windows. в следующей таблице приведены различные версии DLL и способы их распространения датировано обратно в microsoft Internet Explorer 3,0, Windows 95 и microsoft Windows NT 4,0.

Shell32.dll версии 4,0 находятся в исходных версиях Windows 95 и Microsoft Windows NT 4,0. Оболочка не была обновлена с выпуском Internet Explorer 3,0, поэтому Shell32.dll не имеет версии 4,70. Shell32.dll версии 4,71 и 4,72 были поставляются с соответствующими выпусками Internet Explorer, но они не обязательно были установлены (см. Примечание 1). для выпусков, походящих в Microsoft Internet Explorer 4,01 и Windows 98, номера версий для Shell32.dll и Shlwapi.dll расходятся. В общем случае следует предположить, что библиотеки DLL имеют разные номера версий и проверяют каждый из них отдельно.

#### <a name="shell32dll"></a>Shell32.dll

| Версия | Платформа распространения                                                       |
|---------|-----------------------------------------------------------------------------|
| 4,0     | Windows 95 и Microsoft Windows NT 4,0                                     |
| 4,71    | Microsoft Internet Explorer 4,0. См. примечание 1.                                |
| 4,72    | Internet Explorer 4,01 и Windows 98. См. примечание 1.                          |
| 5.0     | Windows 2000 и Windows Millennium Edition (Windows Me). См. Примечание 2.       |
| 6,0     | Windows XP                                                                  |
| 6.0.1   | Windows Vista                                                               |
| 6.1     | Windows 7                                                                   |

#### <a name="shlwapidll"></a>Shlwapi.dll

| Версия | Платформа распространения                                                       |
|---------|-----------------------------------------------------------------------------|
| 4,0     | Windows 95 и Microsoft Windows NT 4,0                                     |
| 4,71    | Internet Explorer 4,0. См. примечание 1.                                          |
| 4,72    | Internet Explorer 4,01 и Windows 98. См. примечание 1.                          |
| 4,7     | Internet Explorer 3. x                                                       |
| 5.0     | Microsoft Internet Explorer 5 и Windows 98 SE. См. Примечание 2.                |
| 5.5     | Microsoft Internet Explorer 5,5 и Windows Millennium Edition (Windows Me) |
| 6,0     | Windows XP и Windows Vista                                                |



**Примечание 1.** Все системы с Internet Explorer 4,0 или 4,01 имеют связанную версию Shlwapi.dll (4,71 или 4,72 соответственно). однако для систем, выпущенных до Windows 98, Internet Explorer 4,0 и 4,01 можно установить с помощью среды или без нее, известной как *интегрированная оболочка*. Если Internet Explorer был установлен с интегрированной оболочкой, также была установлена соответствующая версия Shell32.dll (4,71 или 4,72). Если Internet Explorer был установлен без интегрированной оболочки, Shell32.dll остается версией 4,0. Иными словами, наличие версии 4,71 или 4,72 Shlwapi.dll в системе не гарантирует, что Shell32.dll имеет тот же номер версии. все системы Windows 98 имеют версию 4,72 Shell32.dll.

**Примечание 2.** версия 5,0 Shlwapi.dll была распространена с Internet explorer 5 и обнаружена во всех системах, где был установлен internet explorer 5, за исключением Windows 2000. версия 5,0 Shell32.dll была изначально распространена с Windows 2000 и Windows Millennium Edition (Windows Me) вместе с версией 5,0 Shlwapi.dll.

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Определение номера версии с помощью Дллжетверсион

Начиная с версии 4,71 библиотеки DLL оболочки, в других случаях, начали экспортировать [**дллжетверсион**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Эта функция может быть вызвана приложением для определения версии библиотеки DLL, имеющейся в системе.

> [!Note]  
> Библиотеки DLL не обязательно экспортируют [**дллжетверсион**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Прежде чем пытаться использовать его, всегда проверяйте его.

для Windows версий более ранних, чем Windows 2000, [**дллжетверсион**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) возвращает структуру [**дллверсионинфо**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) , содержащую основной и дополнительный номера версии, номер сборки и идентификатор платформы. для Windows 2000 и более поздних систем **дллжетверсион** может возвращать структуру [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) . Помимо информации, предоставляемой через **дллверсионинфо**, **DLLVERSIONINFO2** также предоставляет номер исправления, который определяет последний установленный пакет обновления, что обеспечивает более надежный способ сравнения номеров версий. Поскольку первый элемент **DLLVERSIONINFO2** является структурой **дллверсионинфо** , более поздняя структура является обратно совместимой.

### <a name="using-dllgetversion"></a>Использование Дллжетверсион

Следующий пример функции `GetVersion` загружает указанную библиотеку DLL и пытается вызвать ее функцию [**дллжетверсион**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) . В случае успеха он использует макрос для упаковки основного и дополнительного номеров версий из структуры [**дллверсионинфо**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) в **DWORD** , возвращаемый вызывающему приложению. Если библиотека DLL не экспортирует **дллжетверсион**, функция возвращает ноль. при использовании Windows 2000 и более поздних версий можно изменить функцию, чтобы решить, что **дллжетверсион** возвращает структуру [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) . Если это так, используйте сведения в элементе **уллверсион** структуры **DLLVERSIONINFO2** для сравнения версий, номеров сборки и выпусков пакетов обновления. Макрос [**македллверулл**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) упрощает задачу сравнения этих значений с ними в **уллверсион**.

> [!Note]  
> Неправильное использование [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) может представлять угрозу безопасности. Сведения о правильной загрузке библиотек DLL с разными версиями Windows см. в документации по **LoadLibrary** .


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


В следующем примере кода показано, как можно использовать `GetVersion` , чтобы проверить, имеет ли Shell32.dll версию 6,0 или более позднюю.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a>Project Операционных

Чтобы обеспечить совместимость приложения с различными целевыми версиями файла .dll, в файлах заголовков содержатся макросы версии. Эти макросы используются для определения, исключения или переопределения определенных определений для различных версий библиотеки DLL. подробное описание этих макросов см. в разделе [использование Windows заголовков](../winprog/using-the-windows-headers.md) .

Например, имя макроса **\_ Win32 \_ IE** обычно находится в более старых заголовках. Вы несете ответственность за определение макроса в виде шестнадцатеричного числа. Этот номер версии определяет целевую версию приложения, использующего библиотеку DLL. В следующей таблице показаны доступные номера версий и их воздействие на приложение.


| Версия | Описание                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0200  | Приложение совместимо с Shell32.dll версии 4,00 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 4,00.                                              |
| 0x0300  | Приложение совместимо с Shell32.dll версии 4,70 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 4,70.                                              |
| 0x0400  | Приложение совместимо с Shell32.dll версии 4,71 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 4,71.                                              |
| 0x0401  | Приложение совместимо с Shell32.dll версии 4,72 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 4,72.                                              |
| 0x0500  | Приложение совместимо с Shell32.dll и Shlwapi.dll версии 5,0 и более поздних версий. Приложение не может реализовывать функции, добавленные после Shell32.dll и Shlwapi.dll версии 5,0. |
| 0x0501  | Приложение совместимо с Shell32.dll и Shlwapi.dll версии 5,0 и более поздних версий. Приложение не может реализовывать функции, добавленные после Shell32.dll и Shlwapi.dll версии 5,0. |
| 0x0600  | Приложение совместимо с Shell32.dll и Shlwapi.dll версии 6,0 и более поздних версий. Приложение не может реализовывать функции, добавленные после Shell32.dll и Shlwapi.dll версии 6,0. |


Если в проекте не определен макрос **\_ Win32 \_ IE** , он автоматически определяется как 0x0500. Чтобы определить другое значение, можно добавить следующий объект в директивы компилятора в файле make. Замените требуемый номер версии для 0x0400.

```
/D _WIN32_IE=0x0400
```

Другой способ — добавить строку, аналогичную приведенной ниже, в исходный код перед включением файлов заголовков оболочки. Замените требуемый номер версии для 0x0400.

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
