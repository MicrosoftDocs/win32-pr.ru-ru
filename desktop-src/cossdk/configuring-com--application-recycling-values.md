---
description: Для настройки значений перезапуска приложения COM+ можно использовать следующие методы.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Настройка значений перезапуска приложения COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2613fb6f063a49d53baa90fad6f7dac862b848c6abf95fddcc36ace25e3d6b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548646"
---
# <a name="configuring-com-application-recycling-values"></a>Настройка значений перезапуска приложения COM+

Для настройки значений перезапуска приложения COM+ можно использовать следующие методы.

> [!Note]  
> приложение COM+, настроенное для запуска в качестве службы Windows, нельзя перезапустить. Кроме того, библиотечные приложения имеют свойства перезапуска и группирования для своего хостового процесса.

 

## <a name="component-services-administrative-tool"></a>Средство администрирования служб компонентов

Чтобы настроить перезапуск приложения для приложения COM+, выполните следующие действия.

1.  В дереве консоли средства администрирования "службы компонентов" щелкните правой кнопкой мыши серверное приложение COM+, которое необходимо перезапустить, и выберите пункт **Свойства**.

2.  На вкладке **пулы & перезапуск** введите значения для **предельного времени жизни (в минутах)**, **предела памяти (КБ)**, **времени ожидания (в минутах)**, **предельного числа вызовов** и **ограничения активации** в зависимости от критериев, которые вы хотите использовать.

    -   **Ограничение времени существования** указывает максимальное число минут, в течение которых процесс может быть выполнен до его перезапуска. Допустимый диапазон — от 0 до 30 240 минут (21 день). Число минут по умолчанию равно 0.
    -   **Ограничение памяти** указывает максимальный объем использования памяти процесса (в килобайтах) перед повторным запуском процесса. Если объем используемой памяти процесса превышает указанное число в течение более одной минуты, процесс перезапускается. Допустимый диапазон — от 0 до 1 048 576 КБ, а объем используемой памяти по умолчанию — 0 КБ.
    -   **Время ожидания окончания срока действия** указывает количество минут ожидания, прежде чем принудительно завершить работу, для выпуска всех внешних ссылок на объекты в процессе. Допустимый диапазон — от 1 до 1440 минут (24 часа), а время ожидания истечения срока действия по умолчанию — 15 минут. Это значение используется только в том случае, если уже определено, что процесс будет перезапущен на основе других критериев.
    -   **Ограничение вызовов** указывает максимальное число вызовов, которые могут быть приняты объектами приложения перед повторным запуском процесса. Допустимый диапазон — от 0 до 1 048 576 вызовов, а число вызовов по умолчанию — 0.
    -   **Ограничение активации** указывает максимальное число активаций объекта приложения, которое следует принять перед повторным запуском процесса. Допустимый диапазон — от 0 до 1 048 576 активаций, а число активаций по умолчанию — 0.

    > [!Note]  
    > Если **предельное значение времени жизни**, **ограничение памяти**, **число вызовов** или **ограничение активации** задано равным 0 (значение по умолчанию), перезапуск приложения для этого критерия отключается. Если все четыре условия имеют значение 0, повторное использование приложений для выбранного приложения отключается.

     

3.  Нажмите кнопку **ОК**.

## <a name="visual-basic"></a>Visual Basic

в следующей функции Microsoft Visual Basic показано, как можно задать значения для повторного запуска приложения для любого выбранного серверного приложения COM+. чтобы использовать его из Visual Basic, добавьте ссылку на библиотеку типов администрирования COM+.


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



Чтобы использовать функцию, укажите строковое значение для имени приложения и целочисленные значения для нужных параметров повторного запуска приложения. в следующем Visual Basic коде показано, как установить значение **рециклелифетимелимит** равным 5, значение **рециклемеморилимит** — 10, значение **рециклекалллимит** — 9, значение **рециклеактиватионлимит** — 100, а для параметра **RecycleExpirationTimeout** — значение 15.


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Основные понятия перезапуска приложений COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



