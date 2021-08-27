---
title: Использование значков
description: В этом разделе приводятся примеры кода, демонстрирующие выполнение задач, связанных со значками.
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- ресурсы, значки
- значки, создание
- значки, отображение
- значки, совместное использование ресурсов
- Создание значков
- отображение значков
- Общий доступ к ресурсам значков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40db7a5828c80dc27780ac54e4110e37a80f44938c9475904ce32089be50d84f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472602"
---
# <a name="using-icons"></a>Использование значков

В следующих разделах описывается выполнение определенных задач, связанных со значками.

-   [Создание значка](#creating-an-icon)
-   [Отображение значка](#displaying-an-icon)
-   [Общий доступ к ресурсам значков](#sharing-icon-resources)

## <a name="creating-an-icon"></a>Создание значка

Чтобы использовать значок, приложение должно получить маркер для значка. В следующем примере показано, как создать два разных маркера значков: один для стандартного значка вопроса, а другой — для пользовательского значка, включаемого в качестве ресурса в файл определения ресурса приложения.


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



Приложение должно реализовывать пользовательские значки как ресурсы и использовать функцию [**лоадикон**](/windows/desktop/api/Winuser/nf-winuser-loadicona) или [**лоадимаже**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) вместо того, чтобы создавать значки во время выполнения. Такой подход позволяет избежать зависимости устройства, упрощает локализацию и позволяет приложениям совместно использовать точечные рисунки значков. Однако в следующем примере используется [**креатеикон**](/windows/desktop/api/Winuser/nf-winuser-createicon) для создания пользовательского значка во время выполнения на основе битовых масок битов. он включен, чтобы продемонстрировать, как система интерпретирует битовые маски битовой карты.


```
HICON hIcon3;      // icon handle 
 
// Yang icon AND bitmask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,   // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,   // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,   // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,   // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,   // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 7 
                      0xFF, 0xF0, 0x00, 0x07,   // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,   // line 9 
                      0xFF, 0xE0, 0x00, 0x03,   // line 10 
                      0xFF, 0xE0, 0x00, 0x01,   // line 11 
                      0xFF, 0xE0, 0x00, 0x01,   // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,   // line 13 
                      0xFF, 0xF0, 0x00, 0x00,   // line 14 
                      0xFF, 0xF8, 0x00, 0x00,   // line 15 
                      0xFF, 0xFC, 0x00, 0x00,   // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,   // line 17 
                      0xFF, 0xFF, 0x80, 0x00,   // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,   // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,   // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,   // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,   // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,   // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,   // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,   // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,   // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,   // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF};  // line 32 
 
// Yang icon XOR bitmask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,   // line 1 
                      0x00, 0x00, 0x00, 0x00,   // line 2 
                      0x00, 0x00, 0x00, 0x00,   // line 3 
                      0x00, 0x00, 0x00, 0x00,   // line 4 
 
                      0x00, 0x00, 0x00, 0x00,   // line 5 
                      0x00, 0x00, 0x00, 0x00,   // line 6 
                      0x00, 0x00, 0x00, 0x00,   // line 7 
                      0x00, 0x00, 0x38, 0x00,   // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,   // line 9 
                      0x00, 0x00, 0x7C, 0x00,   // line 10 
                      0x00, 0x00, 0x7C, 0x00,   // line 11 
                      0x00, 0x00, 0x38, 0x00,   // line 12 
 
                      0x00, 0x00, 0x00, 0x00,   // line 13 
                      0x00, 0x00, 0x00, 0x00,   // line 14 
                      0x00, 0x00, 0x00, 0x00,   // line 15 
                      0x00, 0x00, 0x00, 0x00,   // line 16 
 
                      0x00, 0x00, 0x00, 0x00,   // line 17 
                      0x00, 0x00, 0x00, 0x00,   // line 18 
                      0x00, 0x00, 0x00, 0x00,   // line 19 
                      0x00, 0x00, 0x00, 0x00,   // line 20 
 
                      0x00, 0x00, 0x00, 0x00,   // line 21 
                      0x00, 0x00, 0x00, 0x00,   // line 22 
                      0x00, 0x00, 0x00, 0x00,   // line 23 
                      0x00, 0x00, 0x00, 0x00,   // line 24 
 
                      0x00, 0x00, 0x00, 0x00,   // line 25 
                      0x00, 0x00, 0x00, 0x00,   // line 26 
                      0x00, 0x00, 0x00, 0x00,   // line 27 
                      0x00, 0x00, 0x00, 0x00,   // line 28 
 
                      0x00, 0x00, 0x00, 0x00,   // line 29 
                      0x00, 0x00, 0x00, 0x00,   // line 30 
                      0x00, 0x00, 0x00, 0x00,   // line 31 
                      0x00, 0x00, 0x00, 0x00};  // line 32 
 
hIcon3 = CreateIcon(hinst,    // application instance  
             32,              // icon width 
             32,              // icon height 
             1,               // number of XOR planes 
             1,               // number of bits per pixel 
             ANDmaskIcon,     // AND bitmask  
             XORmaskIcon);    // XOR bitmask 
              
```



Чтобы создать значок, [**креатеикон**](/windows/desktop/api/Winuser/nf-winuser-createicon) применяет следующую таблицу истинности к битовым маскам and и XOR.



| И битовая маска | Битовая маска XOR | Отображение        |
|-------------|-------------|----------------|
| 0           | 0           | Черный          |
| 0           | 1           | Белый          |
| 1           | 0           | Screen         |
| 1           | 1           | Обратный экран |



 

Перед закрытием приложение должно использовать [**дестройикон**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) для уничтожения любого значка, созданного с помощью [**креатеикониндирект**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect). Удалять значки, созданные другими функциями, необязательно.

## <a name="displaying-an-icon"></a>Отображение значка

Приложение может загружать и создавать значки, отображаемые в клиентской области приложения или дочерних окнах. В следующем примере показано, как нарисовать значок в клиентской области окна, контекст устройства (DC) которого определяется параметром *HDC* .


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



Система автоматически отображает значки классов для окна. Приложение может назначать значки классов при регистрации класса окна. Приложение может заменить значок класса с помощью функции [**сеткласслонг**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) . Эта функция изменяет параметры окна по умолчанию для всех окон данного класса. В следующем примере значок класса заменяется значком, идентификатором ресурса которого является 480.


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLongPtr(hwnd,          // window handle 
    GCLP_HICON,              // changes icon 
    (LONG_PTR) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



Дополнительные сведения о классах окон см. в разделе [классы окон](/windows/desktop/winmsg/window-classes).

## <a name="sharing-icon-resources"></a>Общий доступ к ресурсам значков

В следующем коде используются функции [**креатеиконфромресаурцеекс**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**дравикон**](/windows/desktop/api/Winuser/nf-winuser-drawicon)и [**лукупиконидфромдиректорекс**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), а также несколько функций ресурсов для создания маркера значка на основе данных значков из другого исполняемого файла. Затем он отображает значок в окне.

**Предупреждение системы безопасности:** Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL. Сведения о правильной загрузке библиотек DLL с разными версиями Windows см. в документации по **LoadLibrary** .


```
HICON hIcon1;       // icon handle 
HINSTANCE hExe;     // handle to loaded .EXE file 
HRSRC hResource;    // handle to FindResource  
HRSRC hMem;         // handle to LoadResource 
BYTE *lpResource;   // pointer to resource data  
int nID;            // ID of resource that best fits current screen 
 
HDC hdc;        // handle to display context 
 
// Load the file from which to copy the icon. 
// Note: LoadLibrary should have a fully explicit path.
//
hExe = LoadLibrary("myapp.exe");
if (hExe == NULL)
{
    //Error loading module -- fail as securely as possible
    return;
}
 
 
// Find the icon directory whose identifier is 440. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(440), 
    RT_GROUP_ICON); 
 
// Load and lock the icon directory. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Get the identifier of the icon that is most appropriate 
// for the video display. 
 
nID = LookupIconIdFromDirectoryEx((PBYTE) lpResource, TRUE, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Find the bits for the nID icon. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(nID), 
    MAKEINTRESOURCE(RT_ICON)); 
 
// Load and lock the icon. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Create a handle to the icon. 
 
hIcon1 = CreateIconFromResourceEx((PBYTE) lpResource, 
    SizeofResource(hExe, hResource), TRUE, 0x00030000, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Draw the icon in the client area. 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



 

 
