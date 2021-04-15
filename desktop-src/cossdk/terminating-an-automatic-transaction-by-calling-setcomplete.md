---
description: Завершение автоматической транзакции путем вызова Сеткомплете
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Завершение автоматической транзакции путем вызова Сеткомплете
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4bf09e631acf69a9b663d68d7eb82cfaa4490f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662085"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a>Завершение автоматической транзакции путем вызова Сеткомплете

Чтобы эффективно использовать автоматические транзакции, каждый компонент транзакции должен указать, что он завершил свою работу. Когда экземпляр объекта успешно завершает свою задачу, он должен установить для флагов consistent и Done значение true, вызвав метод [**иобжектконтекст:: сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , который предоставляется через интерфейс [**Иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) и объект [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

Самый эффективный способ выполнить автоматическую транзакцию — явно отключить корневой объект с помощью метода [**сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . Путем явного указания на то, что корневой объект завершил свою работу, можно уменьшить длину транзакции.

В следующем Visual Basic примере показано, как указать, что транзакционный объект успешно завершил свою работу:


```VB
Sub MyObjMethod1()
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  objCtx.SetComplete
End Sub
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Флаги consistent и Done](consistent-and-done-flags.md)
</dt> <dt>

[Управление автоматическими транзакциями в COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



