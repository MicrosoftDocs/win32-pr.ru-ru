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
# <a name="speeding-transactions-by-notifying-the-root-object"></a>Ускорение транзакций путем уведомления корневого объекта

Чтобы эффективно использовать автоматические транзакции, каждый компонент транзакции должен указать, что он завершил свою работу. Когда экземпляр объекта успешно завершает свою задачу, он должен установить для флагов consistent и Done значение true, вызвав метод [**иобжектконтекст:: сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) . Когда все внутренние объекты транзакции называются **сеткомплете**, транзакция может быть завершена путем явной деактивации корневого объекта путем вызова его метода **сеткомплете** . Путем явного указания на то, что корневой объект завершил свою работу, можно уменьшить длину транзакции.

При сбое метода объекта транзакции объект должен установить флаг согласованности в значение false, а флаг Done — в значение true, вызвав метод [**иобжектконтекст:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) . Вызывая метод **SetAbort** , объект возвращает управление вызывающему объекту и гарантирует, что транзакция в конечном итоге прерывается.

Однако, если объект, вызывающий [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) , не является корнем транзакции, транзакция продолжит выполняться, даже если она не может сохранить ее в конечном итоге. Чтобы ускорить завершение невыполненной транзакции, можно вызвать ошибку, чтобы создать предупреждение для корневого объекта, чтобы также вызвать **SetAbort**. По завершении корневой объект должен отправить клиенту сообщение об ошибке.

Хотя существует множество различных подходов к обработке ошибок, подход должен четко координировать обмен данными между внутренними объектами и корневым объектом.

В следующих фрагментах кода Visual Basic показан один из подходов к обработке ошибок. В первом фрагменте внутренний объект вызывает [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), вызывает ошибку и выдает сообщение об ошибке следующим образом:

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

Во втором фрагменте корневой объект обрабатывает ошибку и передает сообщение клиенту, как показано ниже.

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление автоматическими транзакциями в COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



