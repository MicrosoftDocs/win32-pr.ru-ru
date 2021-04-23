---
title: Пример кода для удаления пользователей на рядовом сервере или в Windows 2000 Professional
description: В этом разделе содержится пример кода, показывающий, как удалить пользователя на рядовом сервере или рабочей станции.
ms.assetid: 04469061-f95c-4810-99d0-03d98b70d3d3
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, удаление пользователей на рядовом сервере или в Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4831fb1276f71245e6de46f61c9428267491d05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067378"
---
# <a name="example-code-for-deleting-users-on-a-member-server-or-windows-2000-professional"></a><span data-ttu-id="f2f1f-104">Пример кода для удаления пользователей на рядовом сервере или в Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f2f1f-104">Example Code for Deleting Users on a Member Server or Windows 2000 Professional</span></span>

<span data-ttu-id="f2f1f-105">Следующий Visual Basic код удаляет пользователя на рядовом сервере или рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="f2f1f-105">The following Visual Basic code deletes a user on a member server or workstation.</span></span>


```VB
Dim cont As IADsContainer
Dim oGroup As IADsGroup

'Example: Deleting a user on a member server or workstation
 
''''''''''''''''''''
'Parse the arguments
''''''''''''''''''''
On Error Resume Next
sComputer = InputBox("This script deletes a user from a member " _
                     & "server or workstation." _
                     & vbCrLf & vbCrLf _
                     & "Specify the computer name:")
If sComputer = "" Then
    Exit Sub
End If

sUser = InputBox("Specify the user name:")
If sUser = "" Then
    Exit Sub
End If
 
''''''''''''''''''''
'Bind to the computer
''''''''''''''''''''
Set cont = GetObject("WinNT://" & sComputer & ",computer")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
''''''''''''''''''''
'Delete the user
''''''''''''''''''''
cont.Delete "user", sUser

If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADsContainer::Delete method"
End If
 
strText = "The user " & sUser & " was deleted on computer " _
          & sComputer & "."
 
Call show_users(strText, sComputer) 
''''''''''''''''''''
'Display subroutines
''''''''''''''''''''
Sub show_users(strText, strName)
    MsgBox strText, vbInformation, "Delete user on " & strName
End Sub
```



 

 




