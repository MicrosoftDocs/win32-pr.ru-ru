---
description: В этом разделе описаны различные способы создания экземпляра элемента управления InkEdit.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Создание экземпляра InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497649"
---
# <a name="instantiating-inkedit"></a>Создание экземпляра InkEdit

В этом разделе описаны различные способы создания экземпляра элемента управления [InkEdit](inkedit-control.md) .

## <a name="visual-basic-net-and-c"></a>Visual Basic .NET и C\#

Если вы работаете с Microsoft Visual Basic .NET или C \# , перетащите элемент управления [InkEdit](./inkedit-control.md) с панели элементов в Visual Studio на форму или страницу, где должен отображаться элемент управления.

## <a name="win32c"></a>Win32/C++

Элемент управления [InkEdit](inkedit-control-reference.md) является суперклассом для встраиваемого элемента управления с широкими возможностями редактирования 4,5 Win32 OLE.

Приложения Win32 создают экземпляр элемента управления [InkEdit](inkedit-control-reference.md) путем вызова [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) и передачи InkEdit в качестве класса окна. INKEDIT определяется в соответствии с. h. После создания элемента управления можно «поговорить» с элементом управления с сообщениями. Сообщения с расширенными возможностями редактирования (EM \_ \* ) передаются из InkEdit в форматируемый редактор без изменений; доступны все существующие функции расширенного редактирования.

Чтобы создать элемент управления [InkEdit](inkedit-control-reference.md) , вызовите функцию [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) , указав класс окна InkEdit. Используйте [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) для регистрации InkEd.dll. Укажите \_ константу класса INKEDIT, определенную для параметра класса Window, и используйте стили окна, как указано в следующих примерах.

### <a name="instantiating-a-multiline-inkedit-control"></a>Создание экземпляра элемента управления "многострочный InkEdit"


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER|ES_MULTILINE,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



### <a name="instantiating-a-single-line-inkedit-control"></a>Создание экземпляра элемента управления InkEdit Single-Line


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



> [!Note]  
> В отличие от функции RichEdit, перед созданием элемента управления [InkEdit](inkedit-control-reference.md) необходимо вызвать функцию [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) . Вызовите метод [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) при завершении работы приложения. После вызова метода CoUninitialize () необходимо вызвать [FreeLibrary (s \_ Хлиб)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) , чтобы уменьшить число ссылок на файл InkEdit.dll.

 

При использовании стиля окна [ES \_ ноиме](../controls/rich-edit-control-styles.md) встроенная поддержка исправлений недоступна. Если не указать родительское окно, элемент управления создается как окно верхнего уровня и \_ добавляется стиль WS сисмену. Это также отключает встроенную поддержку исправления.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Добавление элементов управления рукописного ввода в проект](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
