---
title: Стандартные версии элементов управления
description: В этом разделе перечислены доступные версии библиотеки общих элементов управления (ComCtl32.dll), описаны способы определения версии, используемой приложением, и объясняется, как выбрать целевое приложение для конкретной версии.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc51fe027e6169ab1c28904c3145be2f5042d9a0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488592"
---
# <a name="common-control-versions"></a>Стандартные версии элементов управления

В этом разделе перечислены доступные версии библиотеки общих элементов управления (ComCtl32.dll), описаны способы определения версии, используемой приложением, и объясняется, как выбрать целевое приложение для конкретной версии.

В этом разделе содержатся следующие подразделы.

-   [Номера версий библиотеки общих элементов управления](#common-control-dll-versions-numbers)
-   [Размеры структуры для различных стандартных версий элементов управления](#structure-sizes-for-different-common-control-versions)
-   [Определение номера версии с помощью Дллжетверсион](#using-dllgetversion-to-determine-the-version-number)
-   [Версии проекта](#project-versions)
-   [См. также](#related-topics)

## <a name="common-control-dll-versions-numbers"></a>Номера версий библиотеки общих элементов управления

Поддержка стандартных элементов управления обеспечивается ComCtl32.dll, которые включают в себя все 32-разрядные и 64-разрядные версии Windows. Каждая последовательная версия библиотеки DLL поддерживает функции и API более ранних версий и добавляет новые функции.

Поскольку различные версии ComCtl32.dll были распространены с помощью Internet Explorer, активная версия иногда отличается от версии, поставляемой с операционной системой. Поэтому приложение должно напрямую определить, какая версия ComCtl32.dll установлена.

В справочной документации по общим элементам управления во многих программных элементах указывается минимальный поддерживаемый номер версии DLL. Этот номер версии указывает, что программный элемент реализован в этой версии и последующих версиях библиотеки DLL, если не указано иное. Если номер версии не указан, программный элемент реализуется во всех существующих версиях библиотеки DLL.

В следующей таблице приведены различные версии библиотек DLL и их распределение по поддерживаемым ОС.



ComCtl32.dll

Версия

Платформа распространения

5,81

Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 и Microsoft Internet Explorer 6

5,82

Windows Server 2003, Windows Vista, Windows Server 2008 и Windows 7

6.0

Windows Server 2003

6.10

Windows Vista, Windows Server 2008 и Windows 7



 

## <a name="structure-sizes-for-different-common-control-versions"></a>Размеры структуры для различных стандартных версий элементов управления

Текущие усовершенствования стандартных элементов управления приводят к необходимости расширения многих структур. По этой причине размер структур изменился между различными версиями Коммктрл. h. Так как большая часть общих структур управления принимает размер структуры как один из параметров, сообщение или функция может завершиться ошибкой, если размер не распознан. Чтобы устранить эту проблему, были определены константы размера структуры, чтобы помочь в нацеливании на другую версию ComCtl32.dll. В следующем списке определяются константы размера структуры.



|                               |                                                                                              |
|-------------------------------|----------------------------------------------------------------------------------------------|
| \_Размер хдитем v1 \_              | Размер структуры [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) в версии 4,0.                           |
| \_Размер имажелистдравпарамс v3 \_ | Размер структуры [**имажелистдравпарамс**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) в версии 5,9. |
| \_Размер LVCOLUMN v1 \_            | Размер структуры [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) в версии 4,0.                       |
| \_Размер лвграуп V5 \_             | Размер структуры [**лвграуп**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) в версии 6,0.                         |
| \_Размер лвхиттестинфо v1 \_       | Размер структуры [**лвхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) в версии 4,0.             |
| \_Размер лвитем v1 \_              | Размер структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) в версии 4,0.                           |
| \_Размер лвитем V5 \_              | Размер структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) в версии 6,0.                           |
| \_Размер лвтилеинфо V5 \_          | Размер структуры [**лвтилеинфо**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) в версии 6,0.                   |
| \_Размер мчиттестинфо v1 \_       | Размер структуры [**мчиттестинфо**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) в версии 4,0.             |
| \_Размер нмлвкустомдрав v3 \_      | Размер структуры [**нмлвкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) в версии 4,7.           |
| \_Размер нмттдиспинфо v1 \_        | Размер структуры [**нмттдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) в версии 4,0.               |
| \_Размер нмтвкустомдрав v3 \_      | Размер структуры [**нмтвкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) в версии 4,7.           |
| \_Размер пропшисеадер v1 \_     | Размер структуры [**пропшисеадер**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) в версии 4,0.         |
| \_Размер пропшитпаже v1 \_       | Размер структуры [**пропшитпаже**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) в версии 4,0.             |
| \_Размер ребарбандинфо v3 \_       | Размер структуры [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) в версии 4,7.             |
| \_Размер ребарбандинфо V6 \_       | Размер структуры [**ребарбандинфо**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) в версии 6,0.             |
| \_Размер тттулинфо v1 \_          | Размер структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) в версии 4,0.                       |
| \_Размер тттулинфо v2 \_          | Размер структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) в версии 4,7.                       |
| \_Размер тттулинфо v3 \_          | Размер структуры [**тулинфо**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) в версии 6,0.                       |
| \_Размер твинсертструкт v1 \_      | Размер структуры [**твинсертструкт**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) в версии 4,0.           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Определение номера версии с помощью Дллжетверсион

Функция [**дллжетверсион**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) может быть вызвана приложением для определения версии библиотеки DLL, имеющейся в системе.

[**Дллжетверсион**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) возвращает структуру [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . Помимо информации, предоставляемой через [**дллверсионинфо**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** также предоставляет номер исправления, который определяет последний установленный пакет обновления, что обеспечивает более надежный способ сравнения номеров версий. Поскольку первый элемент **DLLVERSIONINFO2** является структурой **дллверсионинфо** , более поздняя структура является обратно совместимой.


Следующий пример функции `GetVersion` загружает указанную библиотеку DLL и пытается вызвать ее функцию [**дллжетверсион**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) . В случае успеха он использует макрос для упаковки основного и дополнительного номеров версий из структуры [**дллверсионинфо**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) в **DWORD** , возвращаемый вызывающему приложению. Если библиотека DLL не экспортирует **дллжетверсион**, функция возвращает ноль. Вы можете изменить функцию, чтобы она обрабатывала вероятность того, что **дллжетверсион** возвращает структуру [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . Если это так, используйте сведения в элементе **уллверсион** структуры **DLLVERSIONINFO2** для сравнения версий, номеров сборки и выпусков пакетов обновления. Макрос [**македллверулл**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) упрощает задачу сравнения этих значений с ними в **уллверсион**.

> [!Note]  
> Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может представлять угрозу безопасности. Сведения о правильной загрузке библиотек DLL с разными версиями Windows см. в документации по **LoadLibrary** .

 


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

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

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



В следующем примере кода показано, как можно использовать `GetVersion` , чтобы проверить, имеет ли ComCtl32.dll версию 6,0 или более позднюю.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a>Версии проекта

Чтобы обеспечить совместимость приложения с различными целевыми версиями DLL-файла, в файлах заголовков есть макросы версии. Эти макросы используются для определения, исключения или переопределения определенных определений для различных версий библиотеки DLL. Подробное описание этих макросов см. в разделе [Использование заголовков Windows](/windows/desktop/WinProg/using-the-windows-headers) .

Например, имя макроса **\_ Win32 \_ IE** обычно находится в более старых заголовках. Вы несете ответственность за определение макроса в виде шестнадцатеричного числа. Этот номер версии определяет целевую версию приложения, использующего библиотеку DLL. В следующей таблице показаны доступные номера версий и их воздействие на приложение.



| Версия | Описание                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0300  | Приложение совместимо с ComCtl32.dll версии 4,70 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 4,70. |
| 0x0400  | Приложение совместимо с ComCtl32.dll версии 4,71 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 4,71. |
| 0x0401  | Приложение совместимо с ComCtl32.dll версии 4,72 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 4,72. |
| 0x0500  | Приложение совместимо с ComCtl32.dll версии 5,80 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 5,80. |
| 0x0501  | Приложение совместимо с ComCtl32.dll версии 5,81 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 5,81. |
| 0x0600  | Приложение совместимо с ComCtl32.dll версии 6,0 и более поздних версий. Приложение не может реализовывать функции, которые были добавлены после версии 6,0.   |



 

Если в проекте не определен макрос **\_ Win32 \_ IE** , он автоматически определяется как 0x0500. Чтобы определить другое значение, можно добавить следующий объект в директивы компилятора в файле make. Замените требуемый номер версии для 0x0400.


```C++
/D _WIN32_IE=0x0400
```



Другой способ — добавить строку, аналогичную приведенной ниже, в исходный код перед включением файлов заголовков оболочки. Замените требуемый номер версии для 0x0400.


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения об элементах управления](common-controls-intro.md)
</dt> </dl>

 

 