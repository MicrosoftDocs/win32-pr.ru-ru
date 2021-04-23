---
title: Создание новых объектов со специальными возможностями
description: Создание новых объектов со специальными возможностями
ms.assetid: d34a52d1-1eb2-4bb4-989c-a1ca4b5d815f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efa85e44d6d51105e6363d276ecb7e5f33d8378
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776628"
---
# <a name="create-new-accessible-objects"></a><span data-ttu-id="f003e-103">Создание новых объектов со специальными возможностями</span><span class="sxs-lookup"><span data-stu-id="f003e-103">Create New Accessible Objects</span></span>

<span data-ttu-id="f003e-104">В этом сценарии сервер создает новый доступный объект в ответ на каждый запрос [**\_ клиента OBJID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="f003e-104">In this scenario, the server creates a new accessible object in response to each [**OBJID\_CLIENT**](object-identifiers.md) request.</span></span>

<span data-ttu-id="f003e-105">В следующем примере кода указатель на элемент управления извлекается из дополнительных данных окна.</span><span class="sxs-lookup"><span data-stu-id="f003e-105">In the following example code, a pointer to the control is retrieved from the extra window data.</span></span> <span data-ttu-id="f003e-106">Этот и обработчик окна передаются конструктору объекта пользовательского сервера специальных возможностей (Акксервер).</span><span class="sxs-lookup"><span data-stu-id="f003e-106">This and the window handle are passed to the constructor of the custom accessibility server (AccServer) object.</span></span> <span data-ttu-id="f003e-107">Этот объект создается всякий раз, когда получен [**\_ клиент OBJID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="f003e-107">This object is created whenever [**OBJID\_CLIENT**](object-identifiers.md) is received.</span></span>

<span data-ttu-id="f003e-108">При создании объекта сервер получает ссылку, которая должна быть освобождена после вызова [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), чтобы объект был уничтожен сразу после завершения работы клиента.</span><span class="sxs-lookup"><span data-stu-id="f003e-108">When the object is created, the server obtains a reference, which must be released after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), so that the object is destroyed as soon as the client is finished with it.</span></span> <span data-ttu-id="f003e-109">Обратите внимание, что **функции lresultfromobject** увеличивает число ссылок несколько раз, но для освобождения этих ссылок отвечает клиентские приложения и среда выполнения Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="f003e-109">Note that **LresultFromObject** increments the reference count several times, but it is the responsibility of client applications, and the Microsoft Active Accessibility runtime, to release these references.</span></span>


```C++
case WM_GETOBJECT:
{
    // Return the IAccessible object. 
    if ((DWORD)lParam == OBJID_CLIENT)
    {
        // Get the control.  
        CustomListControl* pCustomList = (CustomListControl*)(LONG_PTR)GetWindowLongPtr(hwnd, 0);
        AccServer* pAccServer = new AccServer(hwnd, pCustomList);
        if (pAccServer != NULL)  // NULL if out of memory. 
        {
            LRESULT Lresult = LresultFromObject(IID_IAccessible, wParam, pAccServer);
            pAccServer->Release();
            return Lresult;
        }
        else return 0;
    }
    break;
}
```



 

 




