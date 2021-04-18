---
title: Предоставление Owner-Drawn пунктов меню
description: Предоставление Owner-Drawn пунктов меню
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79668115cedd5fb6b8c20b0d4df361d6d1d800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532303"
---
# <a name="exposing-owner-drawn-menu-items"></a><span data-ttu-id="2d4d8-103">Предоставление Owner-Drawn пунктов меню</span><span class="sxs-lookup"><span data-stu-id="2d4d8-103">Exposing Owner-Drawn Menu Items</span></span>

<span data-ttu-id="2d4d8-104">Разработчики приложений могут использовать структуру [**мсааменуинфо**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) для представления названий элементов меню, рисуемых владельцем.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-104">Application developers can use the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure to expose the names of owner-drawn menu items.</span></span> <span data-ttu-id="2d4d8-105">Связав эту структуру с данными элемента меню, рисуемыми владельцем, вам не нужно предоставлять элементы меню с помощью [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="2d4d8-105">By associating this structure with the owner-drawn menu item data, you do not need to expose the menu items with [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>

<span data-ttu-id="2d4d8-106">При создании меню, рисуемого владельцем, определите класс или структуру для данных элемента меню, рисуемых владельцем, и Создайте экземпляры этого класса для каждого пункта меню.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-106">When creating an owner-drawn menu, define a class or structure for the owner-drawn menu item data and create instances of this class for each menu item.</span></span> <span data-ttu-id="2d4d8-107">Передайте указатель на данные элемента при добавлении элементов в меню.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-107">Pass in a pointer to the item data when adding items to the menu.</span></span>

<span data-ttu-id="2d4d8-108">Чтобы предоставить имена пунктов меню, структура [**мсааменуинфо**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) должна быть первым элементом структуры, определяющей данные элемента, зависящего от приложения, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="2d4d8-108">To expose the names of the menu items, the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure must be the first member of the structure that defines the application-specific item data, as shown in the following example:</span></span>


```C++
// Application-specific owner-drawn menu info struct. Owner-drawn data 
// is a pointer to one of these.
struct MenuEntry
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //   separator item 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //   for separator 
};
```



<span data-ttu-id="2d4d8-109">Структура [**мсааменуинфо**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) не может быть членом класса, содержащего виртуальные функции.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-109">The [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure cannot be a member in a class that contains virtual functions.</span></span> <span data-ttu-id="2d4d8-110">При компиляции кода первый член класса всегда создается в компиляторе в виде указателя на таблицу виртуальных функций.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-110">When the code is compiled, the first member of the class is always a compiler-generated pointer to a table of the virtual functions.</span></span> <span data-ttu-id="2d4d8-111">Чтобы обойти эту проблему, создайте структуру данных элемента, содержащую **мсааменуинфо** в качестве первого элемента.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-111">To work around this problem, create an item data structure that contains **MSAAMENUINFO** as the first member.</span></span> <span data-ttu-id="2d4d8-112">Второй элемент — это указатель на экземпляр класса, который определяет рисуемые владельцем данные.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-112">The second member is a pointer to an instance of the class that defines the owner-drawn data.</span></span> <span data-ttu-id="2d4d8-113">Этот метод показан в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-113">The following example demonstrates this technique.</span></span>


```C++
// Application-defined class that contains the owner-drawn data and 
//  virtual functions that operate on that data.  
class MenuEntry
{
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //  separator item. 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //  separator item 
    virtual void m_AnimateIcon();  
    virtual void m_ChangeIconColor();
}

// Application-defined struct that contains MSAAMENUINFO as first 
//  member. Second member points to owner-drawn data. 
struct MenuInfo
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    MenuEntry *pMenuData;      // Points to the owner-drawn data 
}
```



<span data-ttu-id="2d4d8-114">При добавлении элементов в меню передайте указатель на экземпляр структуры, содержащий [**мсааменуинфо**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) , чтобы предоставить имена пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="2d4d8-114">When adding items to the menu, pass a pointer to an instance of the structure that contains [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) to expose the names of the menu items.</span></span>

 

 




