---
description: Шаг 2. Добавление команды меню для захвата афиши
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: Шаг 2. Добавление команды меню для захвата афиши
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d049dc4e79197cfbe0a86b065eaf67a5ea567a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156735"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a><span data-ttu-id="56896-103">Шаг 2. Добавление команды меню для захвата афиши</span><span class="sxs-lookup"><span data-stu-id="56896-103">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>

<span data-ttu-id="56896-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="56896-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="56896-105">В этом разделе приводится шаг 2 по [извлечению кадра афиши](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="56896-105">This topic is Step 2 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="56896-106">Затем добавьте команду для пользователя, чтобы взять афишу из файла.</span><span class="sxs-lookup"><span data-stu-id="56896-106">Next, add a command for the user to grab a poster frame from a file.</span></span> <span data-ttu-id="56896-107">Создайте пункт меню с ИДЕНТИФИКАТОРом ресурса \_ точечного рисунка IDM и добавьте в процедуру окна следующую инструкцию CASE:</span><span class="sxs-lookup"><span data-stu-id="56896-107">Create a menu item with a resource ID of IDM\_BITMAP, and add the following case statement to the window procedure:</span></span>


```C++
case WM_COMMAND:
    switch (LOWORD(wparam))
    {
    case IDM_BITMAP:
        {
            HRESULT hr = DoShowBitmap(hwnd, &pbmi);
            if (SUCCEEDED(hr))
            {
                pBuffer = reinterpret_cast<BYTE*>(pbmi) + 
                    sizeof(BITMAPINFOHEADER);
                InvalidateRect(hwnd, NULL, TRUE);
            }
            else
            {
                MessageBox(hwnd, TEXT("Cannot display the image."),
                    TEXT("Error"), MB_OK | MB_ICONERROR);
            }
        }
        break;  // IDM_BITMAP
    }
    break;  // WM_COMMAND
```



<span data-ttu-id="56896-108">Функция Дошовбитмап вернет выделенный буфер в *пбми*.</span><span class="sxs-lookup"><span data-stu-id="56896-108">The DoShowBitmap function will return the allocated buffer in *pbmi*.</span></span> <span data-ttu-id="56896-109">При условии, что функция выполнена, адрес точечного рисунка (</span><span class="sxs-lookup"><span data-stu-id="56896-109">Assuming the function succeeds, the address of the bitmap (</span></span>


```C++
pBuffer
```



<span data-ttu-id="56896-110">) можно вычислить как смещение от *пбми*.</span><span class="sxs-lookup"><span data-stu-id="56896-110">) can be calculated as an offset from *pbmi*.</span></span> <span data-ttu-id="56896-111">В функции Дошовбитмап выведите диалоговое окно **Открыть файл** , чтобы пользователь выбрал файл, а затем вызовите функцию, определяемую приложением, которая будет извлекать точечный рисунок:</span><span class="sxs-lookup"><span data-stu-id="56896-111">In the DoShowBitmap function, display an **Open File** dialog box for the user to choose a file, and then call the application-defined GetBitmap function, which will retrieve the bitmap:</span></span>


```C++
HRESULT DoShowBitmap(HWND hwnd, BITMAPINFOHEADER** ppbmih)
{
    OPENFILENAME ofn;       // common dialog box structure
    // Initialize OPENFILENAME (not shown).
    // Display the Open File dialog box.  
    if (GetOpenFileName(&ofn) != TRUE) // failed to open file
    {
        return E_FAIL;
    }
    return GetBitmap(ofn.lpstrFile, ppbmih);
}
```



<span data-ttu-id="56896-112">Далее. [Шаг 3. Реализация функции Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)</span><span class="sxs-lookup"><span data-stu-id="56896-112">Next: [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="56896-113">См. также</span><span class="sxs-lookup"><span data-stu-id="56896-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56896-114">Зафрагментировать рамку афиши</span><span class="sxs-lookup"><span data-stu-id="56896-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



