---
description: Шаг 1. Создание транзакционного компонента
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: Шаг 1. Создание транзакционного компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc378d85e628504e8724b765362b3397826f5e5
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350932"
---
# <a name="step-1-creating-a-transactional-component"></a>Шаг 1. Создание транзакционного компонента

## <a name="objectives"></a>Задачи

На этом шаге вы узнаете следующее:

-   Написание транзакционного компонента в Microsoft Visual Basic
-   Параметры по умолчанию для служб COM+
-   Настройка служб COM+

## <a name="description"></a>Описание

Компонент Упдатеаусораддресс, создаваемый в этом разделе, обновляет адрес существующего автора в базе данных Pubs. База данных Pubs — это образец базы данных, который поставляется с Microsoft SQL Server. Он содержит сведения о публикации, такие как имена авторов, адреса и названия книг.

> [!Note]  
> Pubs — это хранилище данных, используемое в рамках этого учебника.

 

Так как Упдатеаусораддресс обновляет хранилище данных, рекомендуется включить работу в транзакцию, как показано на следующем рисунке, чтобы при вызове компонента клиент COM+ автоматически запустил транзакцию и прикрепляет базу данных (Resource Manager) к этой транзакции. (Подробные сведения о транзакциях в COM+ см. в разделе [транзакции COM+](com--transactions.md).)

![Схема, показывающая транзакцию COM+ с Упдатеаусораддресс.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

Чтобы сделать Упдатеаусораддресс транзакционным компонентом, необходимо выполнить следующие шаги.

1.  Компонент должен быть написан. Для дополнительной защиты добавляется подподпрограмма, проверяющая, что COM+ создал объект в транзакции. Кроме того, основная обработка ошибок включена в компонент, чтобы упростить восстановление после ошибок. Проверка транзакций и обработка ошибок повышают надежность компонента. (См. шаг 1. пример кода для получения полного перечня компонента Упдатеаусораддресс.)
2.  После добавления компонента в приложение COM+ и установки приложения атрибут transaction должен иметь значение **Required**, что гарантирует, что com+ создает каждый объект упдатеаусораддресс в транзакции. Инструкции по заданию атрибута транзакции для компонента см. в разделе [Задание атрибута транзакции](setting-the-transaction-attribute.md).
    > [!Note]  
    > Установка атрибута транзакции для компонента определяет, как COM+ создает каждый объект в отношении транзакций. Значения атрибутов транзакций **пропускаются**, **не поддерживаются**, **поддерживаются**, **обязательны** и **требуют новых**. **Требуемое** значение не является одним из значений атрибута по умолчанию компонента.

     

COM+ привязывает службу транзакций с JIT-активацией и параллелизмом. Когда компонент объявляется транзакционным, COM+ также обеспечивает принудительную JIT-активацию и защиту параллелизма (синхронизацию).

## <a name="sample-code"></a>Пример кода

Компонент Упдатеаусораддресс открывает подключение к базе данных pubs, позволяя пользователю изменять имя автора, адрес или состояние контракта. Он также вызывает второй компонент, который рассматривается в разделе [Шаг 2. расширение транзакции для нескольких компонентов](step-2--extending-a-transaction-across-multiple-components.md).

Чтобы использовать следующий код в проекте Microsoft Visual Basic, откройте новый проект ActiveX.dll и добавьте ссылки на библиотеку Microsoft объекты данных ActiveX и библиотеку типов служб COM+.

> [!Note]  
> Пример кода в этом учебнике предназначен для целей иллюстрации и может не быть самым эффективным для фактического промежуточного хранения и рабочей среды.

 


```VB
Option Explicit
'
'  Purpose:   This class is used for updating an author's address.
'
'  Notes:     IMPT:  This component implicitly assumes that it will 
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'

'----------------------------------------------------------
'  VerifyInTxn subroutine
'      Verifies that this component is in a transaction.
'      Throws an error if it is not.
'
Private Sub VerifyInTxn()
  If Not GetObjectContext.IsInTransaction Then
    ' Transactions turned off. 
    Err.Raise 99999, "This component", "I need a transaction!"
  End If
  ' Component is in a transaction.
End Sub

'----------------------------------------------------------
'  UpdateAuthorAddress subroutine
'      Procedure to update an author's address.
'
Public Sub UpdateAuthorAddress( _
                        ByVal strAuthorID As String, _
                        ByVal strPhone As String, _
                       ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String)
  ' Handle any errors.
  On Error GoTo UnexpectedError
  
  ' Verify that component is in a transaction.
  VerifyInTxn
  
  ' Get object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext
  
  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext
  
  ' Validate the new address information.
  ' The ValidateAuthorAddress function is described in Step 2.
  Dim oValidateAuthAddr As Object
  Dim bValidAddr As Boolean
  Set oValidateAuthAddr = _
    CreateObject("ComplusPrimer.ValidateAuthorAddress") 
  bValidAddr = oValidateAuthAddr.ValidateAuthorAddress( _
    strAddress, strCity, strState, strZip)
  If Not bValidAddr Then
    Err.Raise 99999, "The UpdateAuthorAddress component", _
      "The address of the author is incorrect!"
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

  ' Execute the query.
  conn.Execute "update authors set phone= '" & strPhone & "'" & _
               " set address= '" & strAddress & "'" & _
               " set city= '" & strCity & "'" & _
               " set state= '" & strState & "'" & _
               " set zip= '" & strZip & "'" & _
               " where au_id = '" & strAuthorID & "'"
               
  ' Close the connection.
  conn.Close
  
  ' Get rid of the connection.
  Set conn = Nothing
                 
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
End Sub

```



## <a name="summary"></a>Сводка

-   COM+ назначает значения атрибута по умолчанию. Большинство атрибутов службы можно изменить.
-   Установка атрибута транзакции компонента в значение **Required** гарантирует, что COM+ должен создать каждый экземпляр этого компонента в транзакции, но не обязательно запускает новую транзакцию.
-   Проверка наличия транзакции подтверждает, что значение атрибута транзакции компонента не было случайно сброшено на нетранзакционное значение, например **Ignore** или **not supported**.
-   Обработка ошибок делает компонент более надежным и проще в устранении неполадок.
-   COM+ принудительно реализует [JIT-активацию](com--just-in-time-activation.md) и службы [защиты параллелизма](com--synchronization.md) для транзакционных компонентов.
-   Закрытие подключения к базе данных по завершении с ним позволяет другому компоненту в той же транзакции повторно использовать подключение из пула подключений. (Объединение соединений не следует путать с [пулом объектов](com--object-pooling.md).)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Шаг 2. расширение транзакции для нескольких компонентов](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Шаг 3. повторное использование компонентов](step-3--reusing-components.md)
</dt> <dt>

[JIT-активация COM+](com--just-in-time-activation.md)
</dt> <dt>

[Синхронизация COM+](com--synchronization.md)
</dt> <dt>

[Настройка транзакций](configuring-transactions.md)
</dt> <dt>

[Создание приложений COM+](creating-com--applications.md)
</dt> <dt>

[Установка атрибута Transaction](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



