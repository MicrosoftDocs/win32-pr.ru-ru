---
description: Ускорение транзакций путем уведомления корневого объекта
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: Ускорение транзакций путем уведомления корневого объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262596"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a><span data-ttu-id="e85be-103">Ускорение транзакций путем уведомления корневого объекта</span><span class="sxs-lookup"><span data-stu-id="e85be-103">Speeding Transactions by Notifying the Root Object</span></span>

<span data-ttu-id="e85be-104">Чтобы эффективно использовать автоматические транзакции, каждый компонент транзакции должен указать, что он завершил свою работу.</span><span class="sxs-lookup"><span data-stu-id="e85be-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="e85be-105">Когда экземпляр объекта успешно завершает свою задачу, он должен установить для флагов consistent и Done значение true, вызвав метод [**иобжектконтекст:: сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) .</span><span class="sxs-lookup"><span data-stu-id="e85be-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="e85be-106">Когда все внутренние объекты транзакции называются **сеткомплете**, транзакция может быть завершена путем явной деактивации корневого объекта путем вызова его метода **сеткомплете** .</span><span class="sxs-lookup"><span data-stu-id="e85be-106">When all of the interior objects of the transaction have called **SetComplete**, the transaction can be terminated by explicitly deactivating the root object by calling its **SetComplete** method.</span></span> <span data-ttu-id="e85be-107">Путем явного указания на то, что корневой объект завершил свою работу, можно уменьшить длину транзакции.</span><span class="sxs-lookup"><span data-stu-id="e85be-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="e85be-108">При сбое метода объекта транзакции объект должен установить флаг согласованности в значение false, а флаг Done — в значение true, вызвав метод [**иобжектконтекст:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) .</span><span class="sxs-lookup"><span data-stu-id="e85be-108">When a transactional object method fails, the object should set its consistent flag to False and its done flag to True by calling the [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) method.</span></span> <span data-ttu-id="e85be-109">Вызывая метод **SetAbort** , объект возвращает управление вызывающему объекту и гарантирует, что транзакция в конечном итоге прерывается.</span><span class="sxs-lookup"><span data-stu-id="e85be-109">By calling the **SetAbort** method, an object returns control to its caller and ensures that the transaction is ultimately aborted.</span></span>

<span data-ttu-id="e85be-110">Однако, если объект, вызывающий [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) , не является корнем транзакции, транзакция продолжит выполняться, даже если она не может сохранить ее в конечном итоге.</span><span class="sxs-lookup"><span data-stu-id="e85be-110">However, unless the object calling [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) is the root of the transaction, the transaction continues to run even though nothing can save it from eventually aborting.</span></span> <span data-ttu-id="e85be-111">Чтобы ускорить завершение невыполненной транзакции, можно вызвать ошибку, чтобы создать предупреждение для корневого объекта, чтобы также вызвать **SetAbort**.</span><span class="sxs-lookup"><span data-stu-id="e85be-111">To speed up the termination of a failed transaction, you can raise an error to alert the root object to also call **SetAbort**.</span></span> <span data-ttu-id="e85be-112">По завершении корневой объект должен отправить клиенту сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e85be-112">For completion, the root object should then send an error message to its client.</span></span>

<span data-ttu-id="e85be-113">Хотя существует множество различных подходов к обработке ошибок, подход должен четко координировать обмен данными между внутренними объектами и корневым объектом.</span><span class="sxs-lookup"><span data-stu-id="e85be-113">While there are many different approaches you can take to handle errors, your approach should clearly coordinate the communications between interior objects and the root object.</span></span>

<span data-ttu-id="e85be-114">В следующих фрагментах кода Visual Basic показан один из подходов к обработке ошибок.</span><span class="sxs-lookup"><span data-stu-id="e85be-114">The following Visual Basic code fragments show one approach to error handling.</span></span> <span data-ttu-id="e85be-115">В первом фрагменте внутренний объект вызывает [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), вызывает ошибку и выдает сообщение об ошибке следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e85be-115">In the first fragment, an interior object calls [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), raises an error, and generates an error message, as follows:</span></span>

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

<span data-ttu-id="e85be-116">Во втором фрагменте корневой объект обрабатывает ошибку и передает сообщение клиенту, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e85be-116">In the second fragment, the root object handles the error and passes the message to its client, as follows:</span></span>

``` syntax
Sub MyObjMethod1()
  On Error GoTo MyObjMethod1_err
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  ObjCtx.SetComplete
Exit Sub
  MyObjMethod1_err:
  ' Doom the transaction and exit.
  ObjCtx.SetAbort
  ' Pass the message back to client.
  Err.Raise Err.Number, , Err.Description
End Sub
```

## <a name="related-topics"></a><span data-ttu-id="e85be-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e85be-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e85be-118">Управление автоматическими транзакциями в COM+</span><span class="sxs-lookup"><span data-stu-id="e85be-118">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



