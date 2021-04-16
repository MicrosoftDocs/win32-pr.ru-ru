---
title: Реализация Ксеарч
description: Реализация Ксеарч
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Подключаемые модули проигрывателя Windows Media, класс Ксеарч
- подключаемые модули, класс Ксеарч
- подключаемые модули пользовательского интерфейса, класс Ксеарч
- Подключаемые модули пользовательского интерфейса, класс Ксеарч
- Класс Ксеарч
- инструкции по программированию, подключаемые модули пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531997"
---
# <a name="implementing-csearch"></a><span data-ttu-id="8cfa3-109">Реализация Ксеарч</span><span class="sxs-lookup"><span data-stu-id="8cfa3-109">Implementing CSearch</span></span>

<span data-ttu-id="8cfa3-110">Интерфейс **ивмпплугинуи** имеет несколько методов, которые вызываются проигрывателем Windows Media в разное время в течение жизненного цикла экземпляра подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-110">The **IWMPPluginUI** interface has several methods that are called by Windows Media Player at different times during the life cycle of a plug-in instance.</span></span> <span data-ttu-id="8cfa3-111">Мастер предоставляет основные реализации этих методов, а также конструктор класса и деструктор и другие методы класса.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-111">The wizard provides basic implementations of these methods as well as the class constructor and destructor and other class methods.</span></span> <span data-ttu-id="8cfa3-112">Файл Search. h необходимо изменить, чтобы проигрыватель Windows Media мог взаимодействовать с пользовательским интерфейсом, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="8cfa3-112">The Search.h file must be modified so that Windows Media Player can communicate with the UI, which is described in the next section.</span></span>

<span data-ttu-id="8cfa3-113">Чтобы класс Кплугинвиндов имел доступ к функции ядра m закрытой переменной-члена \_ , объявление дружественного класса должно быть выполнено в определении класса ксеарч, как показано в следующем фрагменте кода:</span><span class="sxs-lookup"><span data-stu-id="8cfa3-113">For the CPluginWindow class to have access to the private member variable m\_spCore, a friend class declaration must be made inside the CSearch class definition as shown in the following code snippet:</span></span>


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a><span data-ttu-id="8cfa3-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8cfa3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cfa3-115">**Программное руководством по программированию подключаемых модулей пользовательского интерфейса**</span><span class="sxs-lookup"><span data-stu-id="8cfa3-115">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




