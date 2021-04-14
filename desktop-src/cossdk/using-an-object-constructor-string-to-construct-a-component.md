---
description: Использование строки конструктора объекта для создания компонента
ms.assetid: 57d66988-2a65-4309-957a-36a5972233b5
title: Использование строки конструктора объекта для создания компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8cbbb1c156fd7ee675b6c21c8ae097494da59ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496311"
---
# <a name="using-an-object-constructor-string-to-construct-a-component"></a><span data-ttu-id="f725a-103">Использование строки конструктора объекта для создания компонента</span><span class="sxs-lookup"><span data-stu-id="f725a-103">Using an Object Constructor String to Construct a Component</span></span>

<span data-ttu-id="f725a-104">В следующем примере показано, как программным способом получить и использовать строку конструктора объекта при создании экземпляра компонента.</span><span class="sxs-lookup"><span data-stu-id="f725a-104">The following example illustrates how to programmatically retrieve and use an object constructor string when a component is instantiated.</span></span> <span data-ttu-id="f725a-105">В нем показана реализация интерфейса [**интерфейс IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) , который получает строку конструктора объекта.</span><span class="sxs-lookup"><span data-stu-id="f725a-105">It shows an implementation of the [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) interface that retrieves an object constructor string.</span></span> <span data-ttu-id="f725a-106">Затем строку можно проанализировать, чтобы задать начальные значения или повлиять на поведение компонента.</span><span class="sxs-lookup"><span data-stu-id="f725a-106">The string can then be parsed to set initial values or influence the behavior of the component.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="f725a-107">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f725a-107">Visual Basic</span></span>


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="f725a-108">См. также</span><span class="sxs-lookup"><span data-stu-id="f725a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f725a-109">Основные понятия о строках конструктора объектов COM+</span><span class="sxs-lookup"><span data-stu-id="f725a-109">COM+ Object Constructor Strings Concepts</span></span>](com--object-constructor-strings-concepts.md)
</dt> <dt>

[<span data-ttu-id="f725a-110">Указание строки конструктора объекта для компонента</span><span class="sxs-lookup"><span data-stu-id="f725a-110">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



