---
description: Шаг 2. расширение транзакции для нескольких компонентов
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: Шаг 2. расширение транзакции для нескольких компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350935"
---
# <a name="step-2-extending-a-transaction-across-components"></a>Шаг 2. расширение транзакции между компонентами

## <a name="objectives"></a>Задачи

На этом шаге вы узнаете о следующих возможностях:

-   Поток транзакций
-   Голосование нескольких объектов в транзакции

## <a name="description"></a>Описание

[Шаг 1. Создание транзакционного компонента](step-1--creating-a-transactional-component.md) показывает, как написать простой транзакционный компонент, который обновляет сведения об авторе в базе данных Microsoft SQL Server Pubs. Шаг 2 показывает, что происходит при расширении транзакции по нескольким компонентам.

В соответствии с моделью программирования COM+ `UpdateAuthorAddress` вызывает другой компонент в процессе выполнения своей работы. Второй компонент, `ValidateAuthorAddress` , проверяет адрес автора и возвращает результаты вызывающему объекту, `UpdateAuthorAddress` .

В отличие от вызывающего объекта, `ValidateAuthorAddress` транзакция не требует транзакции, но она по-прежнему может участвовать в ее транзакции вызывающего. На этом шаге для его атрибута транзакции задано значение **Supported**, как показано на следующем рисунке, который расширяет существующую транзакцию до нового объекта.

![Схема, показывающая расширение существующей транзакции до нового объекта.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

**Поддерживаемое** значение атрибута расширяет (или проходит) существующую транзакцию только в том случае, если вызывающий объект является транзакционным. При `UpdateAuthorAddress` вызовах `ValidateAuthorAddress` com+ сначала проверяет контекст вызывающего объекта, чтобы определить, является ли он транзакционным. Затем COM+ просматривает атрибуты службы, заданные в параметре, `ValidateAuthorAddress` и присваивает новому объекту тот же идентификатор транзакции, который назначен вызывающему объекту. Чтобы лучше понять этот процесс, см. раздел [Активация контекста](context-activation.md).

Так как они используют один и тот же идентификатор транзакции, оба объекта должны успешно завершить свою работу, или COM+ отменяет транзакцию (отменяя любые изменения, внесенные в базу данных Pubs).

Все объекты, участвующие в голосовании транзакции, для фиксации или прерывания транзакции. Голосование происходит явно при включении в код инструкций голосования, как показано в следующем примере кода, который создает `UpdateAuthorAddress` компонент:


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



Голосование также происходит неявно, как это делается в `ValidateAuthorAddress` компоненте. Если в объекте не объявлено иначе, COM+ предполагает, что объект завершил свою работу успешно, но не готов к деактивации. COM+ делает следующее допущение:


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



При `ValidateAuthorAddress` возврате вызывающему объекту COM+ читает свой голос в качестве фиксации. COM+ не учитывает голоса до тех пор, пока не будет отключен корневой объект, который является первым объектом в транзакции в данном случае, `UpdateAuthorAddress` объектом.

## <a name="sample-code"></a>Пример кода

`ValidateAuthorAddress`Компонент выполняет простую проверку адреса автора. Так как не продается `UpdateAuthorAddress` явно, com+ использует параметры голосования по умолчанию.


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a>Сводка

-   Установка значения " **поддерживается** " для атрибута транзакции компонента может привести к созданию нового объекта в транзакции вызывающего объекта. COM+ просматривает контекст вызывающего объекта, чтобы определить состояние транзакций для нового экземпляра. Если вызывающий объект является транзакционным, COM+ передает транзакцию в новый объект.
-   Все объекты, участвующие в одной транзакции, совместно используют общий идентификатор транзакции, который COM+ считывает из контекста объекта.
-   Каждый объект в транзакции подвигается независимо от других объектов. COM+ подсчитывает голоса при деактивации корневого объекта.
-   Можно переключить голосование транзакций объекта между фиксацией и прервать до тех пор, пока COM+ не активирует объект или пока COM+ не активирует корневой объект и не завершит транзакцию. Учитывается только последний параметр голосования. Интерфейсы [**иконтекстстате**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) и [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) предоставляют методы и, которые создают аналогичные результаты голосования, как показано в следующей таблице. Для прямого голосования в транзакции можно использовать любой из этих интерфейсов. 

    | Комбинированные методы [**иконтекстстате**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)                                                                                                                                                      | Эквивалентный метод [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте*  =  **ткскоммит**<br/> [**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате*  =  **true**<br/>  | [**сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте*  =  **ткскоммит**<br/> [**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате*  =  **false**<br/> | [**енаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте*  =  **тксаборт**<br/> [**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате*  =  **true**<br/>   | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте*  =  **тксаборт**<br/> [**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате*  =  **false**<br/>  | [**дисаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   COM+ устанавливает голосование объекта в эквивалент [**енаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) , если только голоса компонента не были явно указаны.
-   Явное голосование может сократить общую длительность транзакции и освободить ресурсоемкие блокировки ресурсов.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Шаг 1. Создание транзакционного компонента](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Шаг 3. повторное использование компонентов](step-3--reusing-components.md)
</dt> <dt>

[Активация контекста](context-activation.md)
</dt> <dt>

[Управление автоматическими транзакциями в COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




