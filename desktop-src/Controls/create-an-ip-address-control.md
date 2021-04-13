---
title: Создание элемента управления "IP-адрес"
description: В этом разделе показано, как создать экземпляр элемента управления IP-адреса.
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8427a5695c0b9c79c19d328f4abc2ab0ffb2e5a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104134803"
---
# <a name="how-to-create-an-ip-address-control"></a><span data-ttu-id="781dc-103">Создание элемента управления "IP-адрес"</span><span class="sxs-lookup"><span data-stu-id="781dc-103">How to Create an IP Address Control</span></span>

<span data-ttu-id="781dc-104">В этом разделе показано, как создать экземпляр элемента управления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="781dc-104">This topic demonstrates how to create an instance of an IP address control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="781dc-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="781dc-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="781dc-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="781dc-106">Technologies</span></span>

-   [<span data-ttu-id="781dc-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="781dc-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="781dc-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="781dc-108">Prerequisites</span></span>

-   <span data-ttu-id="781dc-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="781dc-109">C/C++</span></span>
-   <span data-ttu-id="781dc-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="781dc-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="781dc-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="781dc-111">Instructions</span></span>


<span data-ttu-id="781dc-112">Перед созданием элемента управления IP-адресом загрузите библиотеку DLL общих элементов управления, вызвав [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="781dc-112">Before creating an IP address control, load the common controls DLL by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="781dc-113">Затем используйте [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или функцию [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) для создания элемента управления IP-адреса экземпляра.</span><span class="sxs-lookup"><span data-stu-id="781dc-113">Then use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an instance IP address control.</span></span> <span data-ttu-id="781dc-114">Имя класса для элемента управления — [**WC \_ IPAddress**](common-control-window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="781dc-114">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md).</span></span> <span data-ttu-id="781dc-115">Используйте стиль [**\_ дочерний элемент WS**](/windows/desktop/winmsg/window-styles) , так как нет определенной константы стиля, связанной с элементом управления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="781dc-115">Use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style, because there is no specific style constant associated with the IP address control.</span></span>

<span data-ttu-id="781dc-116">В следующем примере кода C++ функция, определяемая приложением, сначала вызывает [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) и устанавливает для элемента **двикк** структуры [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) значение [**ICC-классов в \_ Интернете \_**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), которое указывает класс IP Address.</span><span class="sxs-lookup"><span data-stu-id="781dc-116">In the following C++ code example, the application-defined function first calls [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) and sets the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure to [**ICC\_INTERNET\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), which specifies the IP address class.</span></span> <span data-ttu-id="781dc-117">Затем он вызывает [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) для создания экземпляра элемента управления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="781dc-117">It then calls [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to create an instance of the IP address control.</span></span>


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a><span data-ttu-id="781dc-118">См. также</span><span class="sxs-lookup"><span data-stu-id="781dc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="781dc-119">Справочник по управлению IP-адресами</span><span class="sxs-lookup"><span data-stu-id="781dc-119">IP Address Control Reference</span></span>](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[<span data-ttu-id="781dc-120">Сведения об элементах управления IP-адресов</span><span class="sxs-lookup"><span data-stu-id="781dc-120">About IP Address Controls</span></span>](ip-address-controls.md)
</dt> <dt>

[<span data-ttu-id="781dc-121">Использование элементов управления IP-адресами</span><span class="sxs-lookup"><span data-stu-id="781dc-121">Using IP Address Controls</span></span>](using-ip-address-controls.md)
</dt> </dl>

 

 