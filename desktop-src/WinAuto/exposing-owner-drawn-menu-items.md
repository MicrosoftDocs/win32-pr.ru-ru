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
# <a name="exposing-owner-drawn-menu-items"></a>Предоставление Owner-Drawn пунктов меню

Разработчики приложений могут использовать структуру [**мсааменуинфо**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) для представления названий элементов меню, рисуемых владельцем. Связав эту структуру с данными элемента меню, рисуемыми владельцем, вам не нужно предоставлять элементы меню с помощью [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

При создании меню, рисуемого владельцем, определите класс или структуру для данных элемента меню, рисуемых владельцем, и Создайте экземпляры этого класса для каждого пункта меню. Передайте указатель на данные элемента при добавлении элементов в меню.

Чтобы предоставить имена пунктов меню, структура [**мсааменуинфо**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) должна быть первым элементом структуры, определяющей данные элемента, зависящего от приложения, как показано в следующем примере:


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



Структура [**мсааменуинфо**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) не может быть членом класса, содержащего виртуальные функции. При компиляции кода первый член класса всегда создается в компиляторе в виде указателя на таблицу виртуальных функций. Чтобы обойти эту проблему, создайте структуру данных элемента, содержащую **мсааменуинфо** в качестве первого элемента. Второй элемент — это указатель на экземпляр класса, который определяет рисуемые владельцем данные. Этот метод показан в следующем примере.


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



При добавлении элементов в меню передайте указатель на экземпляр структуры, содержащий [**мсааменуинфо**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) , чтобы предоставить имена пунктов меню.

 

 




