---
title: Повторное использование существующих указателей на объекты
description: Повторное использование существующих указателей на объекты
ms.assetid: 7e1610c6-89b2-4e7e-aee5-94a6cab87a22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151b8d957fb82718721ad81b452a81a2c71ec84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700496"
---
# <a name="reuse-existing-pointers-to-objects"></a><span data-ttu-id="c21d4-103">Повторное использование существующих указателей на объекты</span><span class="sxs-lookup"><span data-stu-id="c21d4-103">Reuse Existing Pointers to Objects</span></span>

<span data-ttu-id="c21d4-104">В этом сценарии сервер отвечает на запрос [**\_ клиента OBJID**](object-identifiers.md) , используя один и тот же указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) каждый раз.</span><span class="sxs-lookup"><span data-stu-id="c21d4-104">In this scenario, the server responds to an [**OBJID\_CLIENT**](object-identifiers.md) request using the same [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer each time.</span></span>

<span data-ttu-id="c21d4-105">В следующем примере кода объект элемента управления извлекается из дополнительных данных окна, а метод элемента управления вызывается для получения объекта сервера специальных возможностей (определяемого приложением класса Акксервер), если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="c21d4-105">In the following example code, the control object is retrieved from the extra window data, and a method of the control is called to retrieve the accessibility server object (the application-defined AccServer class), if any.</span></span> <span data-ttu-id="c21d4-106">Если сервер специальных возможностей еще не существует, он создается.</span><span class="sxs-lookup"><span data-stu-id="c21d4-106">If the accessibility server does not yet exist, it is created.</span></span>

<span data-ttu-id="c21d4-107">При создании объекта сервера Accessibility он имеет счетчик ссылок, равный 1.</span><span class="sxs-lookup"><span data-stu-id="c21d4-107">When the accessibility server object is created, it has a reference count of 1.</span></span> <span data-ttu-id="c21d4-108">[**Функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) увеличивает счетчик ссылок несколько раз, но эти ссылки будут освобождены, когда клиент завершит работу с объектом.</span><span class="sxs-lookup"><span data-stu-id="c21d4-108">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) increments the reference count several times, but these references will be released when the client is finished with the object.</span></span> <span data-ttu-id="c21d4-109">Сервер освобождает ссылку при уничтожении окна управления.</span><span class="sxs-lookup"><span data-stu-id="c21d4-109">The server releases its reference when the control window is destroyed.</span></span>


```C++
case WM_GETOBJECT:
    {
        // Return the IAccessible object. 
        if ((DWORD)lParam == (DWORD)OBJID_CLIENT)
        {
            // Get the control.  
            CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
            // Create the accessible object. 
            AccServer* pAccServer = pCustomList->GetAccServer();
            if (pAccServer == NULL)
            {
                pAccServer = new AccServer(hwnd, pCustomList);
                pCustomList->SetAccServer(pAccServer);
            }
            if (pAccServer != NULL)  // NULL if out of memory. 
            {
                LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
                return Lresult;
            }
            else return 0;
        }
        break;
    }

    
case WM_DESTROY:
    {
    CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
    AccServer* pAccServer = pCustomList->GetAccServer();
    if (pAccServer!= NULL)
    {
        // Notify the accessibility object that the control no longer exists. 
        pAccServer->SetControlIsAlive(false);
        // Release the reference created in WM_GETOBJECT. 
        pAccServer->Release(); 
    }   
    // Destroy the control. 
    delete pCustomList;
     break;
    }
```



 

 




