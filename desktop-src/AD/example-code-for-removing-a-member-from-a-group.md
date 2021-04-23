---
title: Пример кода для удаления члена из группы
description: В следующем примере кода содержится функция, которая удаляет элемент из группы.
ms.assetid: 8a9c65bb-1b61-432b-9ef4-1d257c501026
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, удаление члена из группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bfdebc7cecc0191652a7ef9052a3578ee48cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654193"
---
# <a name="example-code-for-removing-a-member-from-a-group"></a><span data-ttu-id="5b121-104">Пример кода для удаления члена из группы</span><span class="sxs-lookup"><span data-stu-id="5b121-104">Example Code for Removing a Member from a Group</span></span>

<span data-ttu-id="5b121-105">В следующем примере кода содержится функция, которая удаляет элемент из группы.</span><span class="sxs-lookup"><span data-stu-id="5b121-105">The following code example contains a function that removes a member from a group.</span></span>


```C++
////////////////////////////////////////////////////////////////////////////////////////////////////
/*  RemoveMemberFromGroup()   -       Removes the passed directory object from the membership of passed group
 
    Parameters
 
        IADsGroup * pGroup       - Group to remove the member from
        IADs* pIADsNewMember     - Object to remove.
                                   Object can be a user, contact, or group.
*/
HRESULT RemoveMemberFromGroup(IADsGroup * pGroup, IADs* pIADsNewMember)
{
    HRESULT hr = E_INVALIDARG;
    if ((!pGroup)||(!pIADsNewMember))
        return hr;
 
    // Use the IADs::get_ADsPath() member to get the ADsPath
    // When the ADsPath string is returned, all that is required to
    // remove the member from the group, is to call the 
    // IADsGroup::Remove() method, passing in the ADsPath string.
    // Query the member for its AdsPath
    // This is a fully qualified LDAP path to the object to remove.
    BSTR bsNewMemberPath;
    hr = pIADsNewMember->get_ADsPath(&bsNewMemberPath); 
    if (SUCCEEDED(hr))
    {
 
        // Use the IADsGroup interface to remove the member.
        // Pass the LDAP path to the 
        // member to the IADsGroup::Remove() method
        hr = pGroup->Remove(bsNewMemberPath);
 
        // Free the string returned from IADs::get_ADsPath()
        SysFreeString(bsNewMemberPath);
    }
    return hr;
}
```



 

 




