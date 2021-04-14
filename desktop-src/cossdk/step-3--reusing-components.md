---
description: Шаг 3. повторное использование компонентов
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: Шаг 3. повторное использование компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f44446ee20baa6dc8c947ef0650f4478847a1c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104561618"
---
# <a name="step-3-reusing-components"></a>Шаг 3. повторное использование компонентов

## <a name="objectives"></a>Задачи

На этом шаге вы узнаете о следующих возможностях:

-   Многократно используемые компоненты.
-   Планирование повторного использования.

## <a name="description"></a>Описание

Две предыдущие части этого учебника по службам COM+, [Шаг 1. Создание транзакционного компонента](step-1--creating-a-transactional-component.md) и [Шаг 2. расширение транзакции для нескольких компонентов](step-2--extending-a-transaction-across-multiple-components.md) показывает, как написать один компонент, вызывающий второй компонент для выполнения некоторой работы, обновляя сведения об авторе в Microsoft SQL Server базе данных Pubs; Вся работа защищена одной транзакцией. Примеры компонентов зависят от работы по обновлению данных автора и проверке адреса автора, а также от COM+, обеспечивающего обработку транзакций, [JIT-активацию](com--just-in-time-activation.md)и [защиту параллелизма](com--synchronization.md).

На этом шаге демонстрируется повторное использование компонентов, созданных в шагах 1 и 2, и рассматривается структура этих компонентов. Как показано на следующем рисунке, это означает создание нового компонента, `AddNewAuthor` который добавляет новых авторов в базу данных путем вызова `UpdateAuthorAddress` .

![Схема, показывающая последовательность при повторном использовании компонентов.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

В дополнение к повторному использованию существующих функций компонента `AddNewAuthor` вызывается другой новый компонент с именем `ValidateAuthorName` . Как показано на предыдущем рисунке, `ValidateAuthorName` является нетранзакционным. Значение атрибута транзакции для этого компонента оставлено по умолчанию (**не поддерживается**), чтобы исключить свою работу из транзакции. Как показано в примере кода Step 3, `ValidateAuthorName` выполняет запросы только для чтения к базе данных, и сбой этой дополнительной задачи не должен иметь возможности прерывать транзакцию. Однако значение атрибута транзакции `AddNewAuthor` для компонента задается как **Обязательное**.

`AddNewAuthor`Компоненты, `UpdateAuthorAddress` и `ValidateAuthorAddress` проголосуют за транзакцию. В этой транзакции `AddNewAuthor` это корневой объект. COM+ всегда делает первый объект, созданный в транзакции, корневым объектом.

В этом примере повторное использование `UpdateAuthorAddress` компонента — это просто — com + автоматически доставляет ожидаемые службы. Однако результаты будут отличаться, если значение атрибута транзакции `UpdateAuthorAddress` для компонента изначально задается вместо **обязательно**.  На поверхности эти параметры выглядят одинаково. Обе гарантируют транзакцию. **, Однако**, обязательно запускает новую транзакцию, а при **необходимости** запускает новую транзакцию только в том случае, если вызывающий объект не является транзакционным. Вы видите, насколько важно `UpdateAuthorAddress` тщательно и продуманная Настройка. В противном случае COM+ мог интерпретировать запрос на обслуживание по-другому, создавая две несвязанные транзакции, как показано на следующем рисунке, а не на одном.

![Схема, показывающая последовательность при повторном использовании компонентов с "требуется создать".](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> При повторном использовании компонентов убедитесь, что службы настроены для поддержки желаемого результата.

 

## <a name="sample-code"></a>Пример кода

Компонент Аддневаусор выполняет пакетное Добавление новых авторов, позволяя объекту оставаться активным до тех пор, пока клиент не освободит ссылку на объект.


```VB
Option Explicit
'
'   Purpose:   This class is used for adding a new author.
'
'   Notes:    IMPT:  This component implicitly assumes that it will
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'
'  AddNewAuthor
'
Public Sub AddNewAuthor( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String, _
                        ByVal strPhone As String, _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String, _
                        ByVal boolContracted As Boolean)
  ' Handle any errors.
  On Error GoTo UnexpectedError

  ' Verify component is in a transaction.
  ' The VerifyInTxn subroutine is described in Step 1.
  VerifyInTxn

  ' Get our object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext

  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext

  ' Validate that the author is OK.
  ' The ValidateAuthorName function is described after this function.
  Dim oValidateAuthName As Object
  Dim bValidAuthor As Boolean
  Set oValidateAuthName = CreateObject("ComplusPrimer.ValidateAuthorName")
  bValidAuthor = oValidateAuthName.ValidateAuthorName( _
    strAuthorFirstName, strAuthorLastName)
  If Not bValidAuthor Then
    Err.Raise 999999, "The AddNewAuthor component", _
      "You tried to add an author on the banned list!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Tell the database to actually add the author; use empty strings 
  ' for this part and rely on the UpdateAuthorAddress 
  ' component to validate the address/phone/etc data.
  ' Default Contract flag is off.
  Dim strUpdateString As String
  strUpdateString = "insert into authors values(_
                     '789-65-1234'," & _
                     strAuthorLastName & ", " & _
                     strAuthorFirstName & ", " & _
                     "'(555) 555-5555', ', ', ', '98765', "

  If boolContracted Then
    strUpdateString = strUpdateString + "1)"
  Else
    strUpdateString = strUpdateString + "0)"
  End If

  conn.Execute strUpdateString
  
  ' Close the connection; this potentially allows 
  ' another component in the same transaction to
  ' reuse the connection from the connection pool.
  conn.Close
  Set conn = Nothing
  
  ' Create the UpdateAuthorAddress component.
  Dim oUpdateAuthAddr As Object
  Set oUpdateAuthAddr = CreateObject("ComplusPrimer.UpdateAuthorAddress")
  
  ' The component throws an error if anything goes wrong.
  oUpdateAuthAddr.UpdateAuthorAddress "", strPhone, _
    strAddress, strCity, strState, strZip
    
  Set oUpdateAuthAddr = Nothing
  
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  
  '  Design issue:  Allow batch additions of new
  '  authors in one transaction, or should each new author be added
  '  in a single new transaction?
  contextstate.SetDeactivateOnReturn False
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
  
End Sub
```



`ValidateAuthorName`Компонент проверяет имена авторов перед `AddNewAuthor` добавлением имени в базу данных. Этот компонент выдает ошибку обратно вызывающему объекту в случае возникновения непредвиденных событий.


```VB
Option Explicit
'
'   Purpose:   This class is used for validating authors before
'              adding them to the database.
'
'   Notes:   This component doesn't need to be in a transaction because
'            it is performing read-only queries on the database,
'            especially since these queries are not overlapping with
'            any updates of end-user data. If an unexpected error
'            happens, let the error go back to the caller who
'            needs to handle it.
'

Public Function ValidateAuthorName( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String _
                        ) As Boolean
  ValidateAuthorName = False

  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Suppose another hypothetical table has been added to the Pubs 
  ' database, one that contains a list of banned authors.
  Dim rs As ADODB.Recordset
  Set rs = conn.Execute("select * from banned_authors")
  
  ' Loop through the banned-author list looking for the specified
  ' author.
  While Not rs.EOF
    If rs.Fields("FirstName") = strAuthorFirstName And _
      rs.Fields("LastName") = strAuthorLastName Then
        ' This is a banned author.
        conn.Close
        Set conn = Nothing
        Set rs = Nothing
        Exit Function
    End If
    rs.MoveNext
  Wend
  
  ' None of the added authors found in the banned list.
  ValidateAuthorName = True
  conn.Close
  Set conn = Nothing
  Set rs = Nothing
End Function
```



## <a name="summary"></a>Сводка

-   Иногда не нужно, чтобы компонент проголосовать за транзакцию.
-   COM+ не применяет принудительную активацию или защиту параллелизма для нетранзакционных компонентов. Эти службы можно настроить отдельно.
-   Конфигурация вызывающего компонента влияет на то, как COM+ интерпретирует запросы на обслуживание вызванного компонента.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Шаг 1. Создание транзакционного компонента](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Шаг 2. расширение транзакции для нескольких компонентов](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Настройка транзакций](configuring-transactions.md)
</dt> <dt>

[Проектирование для масштабируемости](designing-for-scalability.md)
</dt> </dl>

 

 



