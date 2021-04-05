---
title: Пример кода для использования в качестве значения для получения членов группы
description: В следующем примере кода для получения членов группы используется диапазон с помощью объектов ActiveX (ADO).
ms.assetid: baebefd5-7ac6-4d36-a5a4-0796d790abee
ms.tgt_platform: multiple
keywords:
- Пример кода использования для получения элементов группы ADSI
- Пример кода C/C++ ADSI с использованием различных способов получения членов группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c596134b8c20bc777c77b65e6fe349884dda25a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986104"
---
# <a name="example-code-for-using-ranging-to-retrieve-members-of-a-group"></a>Пример кода для использования в качестве значения для получения членов группы

В следующем примере кода для получения членов группы используется диапазон с помощью объектов ActiveX (ADO).

В следующем фрагменте кода требуется ссылка на библиотеку Microsoft объекты данных ActiveX 6,0.


```VB
 Private Sub EnumGroupWithADO(ByVal strGroupDN As String, ByVal strUsername As String, ByVal strPassword As String)
        Dim oConn
        Dim oComm
        Dim rangeStep
        Dim lowRange
        Dim highRange
        Dim lastLoop
        Dim commandPrefix
        Dim amp
        Dim commandSuffix
        Dim oRS
        Dim nRetrieved
        oConn = CreateObject("ADODB.Connection")
        oComm = CreateObject("ADODB.Command")

        oConn.Provider = "ADsDSOObject"
        oConn.Properties("ADSI Flag") = 1

        If strUsername <> "" Then
            oConn.Properties("User ID") = strUsername
            oConn.Properties("Password") = strPassword
        End If

        oConn.Open()
        oComm.ActiveConnection = oConn

        ' For compatibility with all operating systems, the number of objects
        ' retrieved by each query should not exceed 999.
        rangeStep = 999

        lastLoop = False
        lowRange = 0
        highRange = lowRange + rangeStep

        commandPrefix = "<LDAP://" & strGroupDN > ">;(objectClass=*);member;range="
        commandSuffix = ";base"

        Do
            If lastLoop Then
                ' Perform this query with the "range=<lowRange>-*" range.
                oComm.CommandText = commandPrefix & lowRange & "-*" & commandSuffix
            Else
                ' Perform this query with the "range=<lowRange>-<highRange>" range.
                oComm.CommandText = commandPrefix & lowRange & "-" & highRange & commandSuffix
            End If
            Debug.Print("Current search command: " & oComm.CommandText)

            ' Execute the query.
            oRS = oComm.Execute

            ' Reset the retrieved members counter.
            nRetrieved = 0

            ' Enumerate the retrieved members.
            While Not oRS.EOF
                For Each oField In oRS.Fields
                    If VarType(oField) = (vbArray + vbVariant) Then
                        For Each oValue In oField.Value
                            Debug.Print(vbTab & oValue)
                            nRetrieved = nRetrieved + 1
                        Next
                    End If
                Next
                oRS.MoveNext()
            End While

            ' If the last query was performed, exit the loop.
            If lastLoop = True Then
                Exit Do
            End If

            If nRetrieved = 0 Then
                ' No objects were retrieved by the last query; perform one last query
                ' with the â€œrange=<lowRange>-*â€ range.
                lastLoop = True
            Else
                ' Increment the high and low ranges to query for the next block of objects.
                lowRange = highRange + 1
                highRange = lowRange + rangeStep
            End If
        Loop While nRetrieved = lowRange
    End Sub
End Module
```



 

 




