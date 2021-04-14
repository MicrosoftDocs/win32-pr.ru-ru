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
# <a name="using-an-object-constructor-string-to-construct-a-component"></a>Использование строки конструктора объекта для создания компонента

В следующем примере показано, как программным способом получить и использовать строку конструктора объекта при создании экземпляра компонента. В нем показана реализация интерфейса [**интерфейс IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct) , который получает строку конструктора объекта. Затем строку можно проанализировать, чтобы задать начальные значения или повлиять на поведение компонента.

## <a name="visual-basic"></a>Visual Basic


```VB
Implements IObjectConstruct
Private Sub IObjectConstruct_Construct( ByVal pCtorObj As Object )
    Dim strConstructorString As String
    strConstructorString = pCtorObj.ConstructString
     Parse and use strConstructorString here. 
End Sub
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные понятия о строках конструктора объектов COM+](com--object-constructor-strings-concepts.md)
</dt> <dt>

[Указание строки конструктора объекта для компонента](specifying-an-object-constructor-string-for-a-component.md)
</dt> </dl>

 

 



