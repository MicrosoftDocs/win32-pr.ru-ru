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
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a><span data-ttu-id="148c1-103">Завершение автоматической транзакции путем вызова Сеткомплете</span><span class="sxs-lookup"><span data-stu-id="148c1-103">Terminating an Automatic Transaction by Calling SetComplete</span></span>

<span data-ttu-id="148c1-104">Чтобы эффективно использовать автоматические транзакции, каждый компонент транзакции должен указать, что он завершил свою работу.</span><span class="sxs-lookup"><span data-stu-id="148c1-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="148c1-105">Когда экземпляр объекта успешно завершает свою задачу, он должен установить для флагов consistent и Done значение true, вызвав метод [**иобжектконтекст:: сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) , который предоставляется через интерфейс [**Иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) и объект [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .</span><span class="sxs-lookup"><span data-stu-id="148c1-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method, which is exposed through both the [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interface and the [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) object.</span></span>

<span data-ttu-id="148c1-106">Самый эффективный способ выполнить автоматическую транзакцию — явно отключить корневой объект с помощью метода [**сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="148c1-106">The most efficient way to complete an automatic transaction is to explicitly deactivate the root object by using the [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="148c1-107">Путем явного указания на то, что корневой объект завершил свою работу, можно уменьшить длину транзакции.</span><span class="sxs-lookup"><span data-stu-id="148c1-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="148c1-108">В следующем Visual Basic примере показано, как указать, что транзакционный объект успешно завершил свою работу:</span><span class="sxs-lookup"><span data-stu-id="148c1-108">The following Visual Basic example shows how to indicate that a transactional object has completed its work successfully:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="148c1-109">См. также</span><span class="sxs-lookup"><span data-stu-id="148c1-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="148c1-110">Флаги consistent и Done</span><span class="sxs-lookup"><span data-stu-id="148c1-110">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="148c1-111">Управление автоматическими транзакциями в COM+</span><span class="sxs-lookup"><span data-stu-id="148c1-111">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



