---
description: Система сокращает главное окно приложения (перекрывает стиль) в уменьшенное окно, когда пользователь щелкает пункт "минимизировать" в меню "окно" или приложение вызывает функцию ShowWindow и задает значение, например "свести к сведению" \_ .
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Уменьшенные окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811933"
---
# <a name="minimized-windows"></a><span data-ttu-id="60465-103">Уменьшенные окна</span><span class="sxs-lookup"><span data-stu-id="60465-103">Minimized Windows</span></span>

<span data-ttu-id="60465-104">Система сокращает главное окно приложения (перекрывает стиль) в уменьшенное окно, когда пользователь щелкает пункт "минимизировать" в меню "окно" или приложение вызывает функцию [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) и задает значение, например "свести к сведению" \_ .</span><span class="sxs-lookup"><span data-stu-id="60465-104">The system reduces an application's main window (overlapping style) to a minimized window when the user clicks Minimize from the window menu or the application calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function and specifies a value such as SW\_MINIMIZE.</span></span> <span data-ttu-id="60465-105">Свертывание окна ускоряет производительность системы, уменьшая объем работы, которую должно выполнить приложение при обновлении главного окна.</span><span class="sxs-lookup"><span data-stu-id="60465-105">Minimizing a window speeds up system performance by reducing the amount of work an application must do when updating its main window.</span></span>

<span data-ttu-id="60465-106">Для типичного приложения система рисует значок, называемый значком класса, когда окно свернется, помечая значок значком с именем окна.</span><span class="sxs-lookup"><span data-stu-id="60465-106">For a typical application, the system draws an icon, called the class icon, when the window is minimized, labeling the icon with the name of the window.</span></span> <span data-ttu-id="60465-107">Значок класса — статическое изображение, представляющее приложение, задается приложением при регистрации класса окна.</span><span class="sxs-lookup"><span data-stu-id="60465-107">The class icon, a static image that represents the application, is specified by the application when it registers the window class.</span></span> <span data-ttu-id="60465-108">Приложение присваивает обработчику значок класса элементу **Хикон** объекта [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) перед вызовом [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="60465-108">The application assigns a handle to the class icon to the **hIcon** member of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) before calling [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="60465-109">Приложение может использовать функцию [**лоадикон**](/windows/win32/api/winuser/nf-winuser-loadicona) для получения маркера значка.</span><span class="sxs-lookup"><span data-stu-id="60465-109">The application can use the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to retrieve the icon handle.</span></span>

 

 
