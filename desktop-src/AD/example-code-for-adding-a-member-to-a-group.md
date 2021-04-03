---
title: Пример кода для добавления члена в группу
description: В этом разделе содержатся примеры кода, которые добавляют элемент в группу.
ms.assetid: 306fcadb-a492-41e5-bfb3-8beaaec24fb5
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, Добавление члена в группу
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a64a41fac871c6793ee4d0db1f4be79c9fbd0d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "103987991"
---
# <a name="example-code-for-adding-a-member-to-a-group"></a><span data-ttu-id="0065f-104">Пример кода для добавления члена в группу</span><span class="sxs-lookup"><span data-stu-id="0065f-104">Example Code for Adding a Member to a Group</span></span>

<span data-ttu-id="0065f-105">В этом разделе содержатся примеры кода, которые добавляют элемент в группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-105">This topic contains code examples that add a member to a group.</span></span> <span data-ttu-id="0065f-106">В сценариях Visual Basic Scripting Edition (VBScript) и C++ добавляется член путем добавления объекта [**iAds**](/windows/desktop/api/iads/nn-iads-iads) , представляющего элемент, в объект [**иадсграуп**](/windows/desktop/api/iads/nn-iads-iadsgroup) , представляющий группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-106">The Visual Basic Scripting Edition (VBScript) and C++ examples add a member by adding the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) object that represents the member to the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) object that represents the group.</span></span> <span data-ttu-id="0065f-107">В Visual Basic .NET и C# примеры изменяют свойство Member объекта [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) , представляющего группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-107">The Visual Basic .NET and C# examples modify the member property of the [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) object that represents the group.</span></span>


<span data-ttu-id="0065f-108">В следующих примерах кода C# добавляется существующий элемент в группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-108">The following C# code examples add an existing member to a group.</span></span> <span data-ttu-id="0065f-109">Функция принимает путь ADsPath контейнера группы и различающееся имя члена, добавляемого в группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-109">The function takes the ADsPath of the group container and the distinguished name of the member to be added to the group.</span></span> <span data-ttu-id="0065f-110">Путь ADsPath используется для создания объекта [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) , представляющего группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-110">The ADsPath is used to create a [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) object that represents the group.</span></span> <span data-ttu-id="0065f-111">Метод [пропертивалуеколлектион. Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) добавляет в группу член, различающееся имя которого было передано в функцию.</span><span class="sxs-lookup"><span data-stu-id="0065f-111">The [PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) method adds to the group the member whose distinguished name was passed to the function.</span></span> <span data-ttu-id="0065f-112">Затем функция использует метод [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) для записи новых сведений о членах в базу данных.</span><span class="sxs-lookup"><span data-stu-id="0065f-112">The function then uses the [DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) method to write the new member information to the database.</span></span>

<span data-ttu-id="0065f-113">Вызовите функцию со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="0065f-113">Call the function with the following parameters:</span></span>

-   <span data-ttu-id="0065f-114">*биндстринг*: допустимый путь ADsPath для контейнера группы, например "LDAP://fabrikam.com/CN=TestGroup,OU=testOU,DC=Fabrikam,DC=com"</span><span class="sxs-lookup"><span data-stu-id="0065f-114">*bindString*: a valid ADsPath for a group container, such as "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"</span></span>
-   <span data-ttu-id="0065f-115">*newMember*: различающееся имя члена, добавляемого в группу, например "CN = ЖЕФФСМИС, OU = ТЕСТАУ, DC = Fabrikam, DC = com"</span><span class="sxs-lookup"><span data-stu-id="0065f-115">*newMember*: the distinguished name of the member to be added to the group, such as "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"</span></span>


```CSharp
private void AddMemberToGroup(

                                string bindString,

                                string newMember

                                )

{

    try
    {

        DirectoryEntry ent = new DirectoryEntry( bindString );

        ent.Properties["member"].Add(newMember);

        ent.CommitChanges();

    }

    catch (Exception e)
    {

        Console.WriteLine( "An error occurred.");

        Console.WriteLine( "{0}", e.Message);

        return;

    }

}
```




<span data-ttu-id="0065f-116">В следующем Visual Basic примеров кода .NET добавляется существующий элемент в группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-116">The following Visual Basic .NET code examples add an existing member to a group.</span></span> <span data-ttu-id="0065f-117">Функция принимает путь ADsPath контейнера группы и различающееся имя члена, добавляемого в группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-117">The function takes the ADsPath of the group container and the distinguished name of the member to be added to the group.</span></span> <span data-ttu-id="0065f-118">Путь ADsPath используется для создания объекта [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) , представляющего группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-118">The ADsPath is used to create a [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry) object that represents the group.</span></span> <span data-ttu-id="0065f-119">Метод [пропертивалуеколлектион. Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) добавляет в группу член, различающееся имя которого было передано в функцию.</span><span class="sxs-lookup"><span data-stu-id="0065f-119">The [PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) method adds to the group the member whose distinguished name was passed to the function.</span></span> <span data-ttu-id="0065f-120">Затем функция использует метод [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) для записи новых сведений о членах в базу данных.</span><span class="sxs-lookup"><span data-stu-id="0065f-120">The function then uses the [DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) method to write the new member information to the database.</span></span>

<span data-ttu-id="0065f-121">Вызовите функцию со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="0065f-121">Call the function with the following parameters:</span></span>

-   <span data-ttu-id="0065f-122">*биндстринг*: допустимый путь ADsPath для контейнера группы, например "LDAP://fabrikam.com/CN=TestGroup,OU=testOU,DC=Fabrikam,DC=com"</span><span class="sxs-lookup"><span data-stu-id="0065f-122">*bindString*: a valid ADsPath for a group container, such as "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"</span></span>
-   <span data-ttu-id="0065f-123">*newMember*: различающееся имя члена, добавляемого в группу, например "CN = ЖЕФФСМИС, OU = ТЕСТАУ, DC = Fabrikam, DC = com"</span><span class="sxs-lookup"><span data-stu-id="0065f-123">*newMember*: the distinguished name of the member to be added to the group, such as "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"</span></span>


```VB
Private Sub AddMemberToGroup(ByVal bindString As String, 
                                      ByVal newMember As String)

    Try

        Dim ent As New DirectoryEntry(bindString)

        ent.Properties("member").Add(newMember)

        ent.CommitChanges()

    Catch e As Exception

        Console.WriteLine("An error occurred.")

        Console.WriteLine("{0}", e.Message)

        Return

    End Try

End Sub
```




<span data-ttu-id="0065f-124">В следующем примере на языке VBScript добавляется существующий элемент в группу.</span><span class="sxs-lookup"><span data-stu-id="0065f-124">The following VBScript example adds an existing member to a group.</span></span> <span data-ttu-id="0065f-125">Сценарий добавляет пользователя, Джефф Смит, в группу TestGroup.</span><span class="sxs-lookup"><span data-stu-id="0065f-125">The script adds the user, Jeff Smith, to the TestGroup group.</span></span>


```VB
Option Explicit

On Error Resume Next

Dim scriptResult        ' Script success or failure

Dim groupPath           ' ADsPath to the group container

Dim group               ' Group object

Dim memberPath          ' ADsPath to the member

Dim member              ' Member object

Dim groupMemberList     ' Used to display group members

Dim errorText           ' Error handing text

scriptResult = False

groupPath = "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"

memberPath = "LDAP://CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"

WScript.Echo("Retrieving group object")

Set group = GetObject(groupPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not create group object.")

End If

Call ShowMembers(groupPath)     'Optional function call

WScript.Echo("Retrieving new member object")

Set member = GetObject(memberPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not get new member object.")

End If

WScript.Echo("Adding member to group.")

group.Add(member.ADsPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not add member to group.")

End If

Call ShowMembers(groupPath)     ' Optional function call

scriptResult = True

Call FinalResult(scriptResult)

'****************************************************************
' This function displays the members of a group. The function
' takes the ADsPath of the group.
'****************************************************************

Sub ShowMembers(groupPath)

    Dim groupMember

    Dim groupMemberList

    Dim groupObject

    Set groupObject = GetObject(groupPath)

    Set groupMemberList = groupObject.Members

    Select Case groupMemberList.Count

        Case 1 

            WScript.Echo vbcrlf & "The group has one member."

        Case 0

            WScript.Echo vbcrlf & "The group has no members."

        Case Else

            WScript.Echo vbcrlf & "The group has " & groupMemberList.Count & " members."

    End Select

    If groupMemberList.Count > 0 then

        WScript.Echo vbcrlf & "Here is a member list."

        For Each groupMember in groupMemberList

            WScript.Echo groupMember.Name

        Next

        WScript.Echo vbcrlf

    End If

    Set groupObject = Nothing

    Set groupMemberList = Nothing

End Sub

'****************************************************************
' This function shows if the script succeeded or failed. The 
' function processed the scriptResult variable.
'****************************************************************

Sub FinalResult(scriptResult)

    WScript.Echo vbcrlf

    If scriptResult = False then

        WScript.Echo "Script failed."

    Else

        WScript.Echo("Script successfully completed.")

    End If

    WScript.Quit

End Sub

'****************************************************************
' This function handles errors that occur in the script.
'****************************************************************

Sub ErrorHandler( errorText )

    WScript.Echo(vbcrlf & errorText)

    WScript.Echo("Error number: " & Err.number)

    WScript.Echo("Error Description: " & Err.Description)

    Err.Clear 

    Call FinalResult(scriptResult)

End Sub

```




<span data-ttu-id="0065f-126">В следующем примере кода C++ в группу добавляется существующий элемент.</span><span class="sxs-lookup"><span data-stu-id="0065f-126">The following C++ code example adds an existing member to a group.</span></span>


```C++
/////////////////////////////////////////////////////////////
/*  AddMemberToGroup() - Adds the passed directory object as a member 
                         of passed group
 
    Parameters
 
        IADsGroup * pGroup   - Group to hold the new IDirectoryObject.
        IADs* pIADsNewMember - Object which will become a member 
                               of the group. Object can be a user, 
                               contact, or group.
*/
HRESULT AddMemberToGroup(IADsGroup * pGroup, IADs* pIADsNewMember)
{
    HRESULT hr = E_INVALIDARG;
    if ((!pGroup)||(!pIADsNewMember))
        return hr;
 
    // Use the IADs::get_ADsPath() member to get the ADsPath.
    // When the ADsPath string is returned, to add the new
    // member to the group, call the IADsGroup::Add() member,
    // passing in the ADsPath string.
    // Query the new member for its AdsPath.
    // This is a fully qualified LDAP path to the object to add.
    BSTR bsNewMemberPath;
    hr = pIADsNewMember->get_ADsPath(&bsNewMemberPath); 
    if (SUCCEEDED(hr))
    {
 
        // Use the IADsGroup interface to add the new member.
        // Pass the LDAP path to the 
        // new member to the IADsGroup::Add() member
        hr = pGroup->Add(bsNewMemberPath);
 
        // Free the string returned from IADs::get_ADsPath()
        SysFreeString(bsNewMemberPath);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0065f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="0065f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0065f-128">Добавление членов в группы в домене</span><span class="sxs-lookup"><span data-stu-id="0065f-128">Adding Members to Groups in a Domain</span></span>](adding-members-to-groups-in-a-domain.md)
</dt> <dt>

[<span data-ttu-id="0065f-129">DirectoryEntry</span><span class="sxs-lookup"><span data-stu-id="0065f-129">DirectoryEntry</span></span>](/dotnet/api/system.directoryservices.directoryentry)
</dt> <dt>

[<span data-ttu-id="0065f-130">DirectoryEntry. CommitChanges</span><span class="sxs-lookup"><span data-stu-id="0065f-130">DirectoryEntry.CommitChanges</span></span>](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges)
</dt> <dt>

[<span data-ttu-id="0065f-131">**IADs**</span><span class="sxs-lookup"><span data-stu-id="0065f-131">**IADs**</span></span>](/windows/desktop/api/iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="0065f-132">**иадсграуп**</span><span class="sxs-lookup"><span data-stu-id="0065f-132">**IADsGroup**</span></span>](/windows/desktop/api/iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="0065f-133">Пропертивалуеколлектион. Add</span><span class="sxs-lookup"><span data-stu-id="0065f-133">PropertyValueCollection.Add</span></span>](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_)
</dt> </dl>

 

 