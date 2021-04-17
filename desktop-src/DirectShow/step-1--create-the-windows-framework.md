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
# <a name="step-1-create-the-windows-framework"></a>Шаг 1. Создание платформы Windows

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

Начните с создания базовой платформы приложения Windows, включая WinMain и процедуру окна. Функция WinMain не показана здесь; Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) перед циклом обработки сообщений, чтобы инициализировать библиотеку COM, и [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) после завершения цикла обработки сообщений. Начните со следующей минимальной процедуры окна:


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



При извлечении кадра афиши из детектора мультимедиа он возвращает буфер, содержащий структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , за которой следуют биты изображения. Поэтому определите две статические переменные в окне процедуры: *пбми* будет содержать указатель на структуру **Битмапинфохеадер** , а *pBuffer* будет содержать указатель на точечный рисунок. Приложение будет распределять буфер в *пбми* с помощью `new` , поэтому перед уничтожением окна необходимо удалить буфер. Указатель *pBuffer* вычисляется как смещение от *пбми*, поэтому нет необходимости удалять его.

Далее. [Шаг 2. Добавление команды меню для захвата афиши](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Зафрагментировать рамку афиши](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
