---
description: Шаг 1. Создание платформы Windows
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: Шаг 1. Создание платформы Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff1712f631db520ff30065e8943d13b280f3d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673996"
---
# <a name="step-1-create-the-windows-framework"></a><span data-ttu-id="a0554-103">Шаг 1. Создание платформы Windows</span><span class="sxs-lookup"><span data-stu-id="a0554-103">Step 1: Create the Windows Framework</span></span>

<span data-ttu-id="a0554-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="a0554-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="a0554-105">Начните с создания базовой платформы приложения Windows, включая WinMain и процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="a0554-105">Start by creating the basic framework of a Windows application, including WinMain and a window procedure.</span></span> <span data-ttu-id="a0554-106">Функция WinMain не показана здесь; Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) перед циклом обработки сообщений, чтобы инициализировать библиотеку COM, и [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) после завершения цикла обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="a0554-106">The WinMain function is not shown here; call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before the message loop to initialize the COM library, and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) after the message loop exits.</span></span> <span data-ttu-id="a0554-107">Начните со следующей минимальной процедуры окна:</span><span class="sxs-lookup"><span data-stu-id="a0554-107">Start with the following minimal window procedure:</span></span>


```C++
LRESULT CALLBACK MainWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    static BITMAPINFOHEADER *pbmi = NULL;
    static BYTE *pBuffer = NULL;
    switch (msg)
    {
    case WM_CLOSE:
        DestroyWindow(hwnd);
        break;
    case WM_DESTROY:
        if (pbmi) delete [] pbmi;
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hwnd, msg, wparam, lparam);
    }
    return 0;
}
```



<span data-ttu-id="a0554-108">При извлечении кадра афиши из детектора мультимедиа он возвращает буфер, содержащий структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , за которой следуют биты изображения.</span><span class="sxs-lookup"><span data-stu-id="a0554-108">When you retrieve a poster frame from the Media Detector, it returns a buffer that contains a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the image bits.</span></span> <span data-ttu-id="a0554-109">Поэтому определите две статические переменные в окне процедуры: *пбми* будет содержать указатель на структуру **Битмапинфохеадер** , а *pBuffer* будет содержать указатель на точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="a0554-109">Therefore, define two static variables in the window procedure: *pbmi* will hold a pointer to the **BITMAPINFOHEADER** structure, and *pBuffer* will hold a pointer to the bitmap.</span></span> <span data-ttu-id="a0554-110">Приложение будет распределять буфер в *пбми* с помощью `new` , поэтому перед уничтожением окна необходимо удалить буфер.</span><span class="sxs-lookup"><span data-stu-id="a0554-110">The application will allocate the buffer in *pbmi* using `new`, so it must delete the buffer before the window is destroyed.</span></span> <span data-ttu-id="a0554-111">Указатель *pBuffer* вычисляется как смещение от *пбми*, поэтому нет необходимости удалять его.</span><span class="sxs-lookup"><span data-stu-id="a0554-111">The *pBuffer* pointer is calculated as an offset from *pbmi*, so there is no need to delete it.</span></span>

<span data-ttu-id="a0554-112">Далее. [Шаг 2. Добавление команды меню для захвата афиши](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span><span class="sxs-lookup"><span data-stu-id="a0554-112">Next: [Step 2: Add a Menu Command to Grab a Poster Frame](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0554-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a0554-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0554-114">Зафрагментировать рамку афиши</span><span class="sxs-lookup"><span data-stu-id="a0554-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
