---
description: Показывает, как правильно создать список DACL.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Создание списка DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf8213f6fbb4e2a885655b47437ec464337ea13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912836"
---
# <a name="creating-a-dacl"></a><span data-ttu-id="67e8e-103">Создание списка DACL</span><span class="sxs-lookup"><span data-stu-id="67e8e-103">Creating a DACL</span></span>

<span data-ttu-id="67e8e-104">Создание правильного [*списка управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) — это необходимая и важная часть разработки приложений.</span><span class="sxs-lookup"><span data-stu-id="67e8e-104">Creating a proper [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) is a necessary and important part of application development.</span></span> <span data-ttu-id="67e8e-105">Поскольку **пустой** список DACL разрешает всем типам доступа всем пользователям, не используйте **пустые** списки DACL.</span><span class="sxs-lookup"><span data-stu-id="67e8e-105">Because a **NULL** DACL permits all types of access to all users, do not use **NULL** DACLs.</span></span>

<span data-ttu-id="67e8e-106">В следующем примере показано, как правильно создать список DACL.</span><span class="sxs-lookup"><span data-stu-id="67e8e-106">The following example shows how to properly create a DACL.</span></span> <span data-ttu-id="67e8e-107">Пример содержит функцию Креатемидакл, которая использует [язык определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) для определения предоставленного и запрещенного контроля доступа в списке DACL.</span><span class="sxs-lookup"><span data-stu-id="67e8e-107">The example contains a function, CreateMyDACL, that uses the [security descriptor definition language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) to define the granted and denied access control in a DACL.</span></span> <span data-ttu-id="67e8e-108">Чтобы предоставить другим приложениям доступ к объектам приложения, при необходимости измените функцию Креатемидакл.</span><span class="sxs-lookup"><span data-stu-id="67e8e-108">To provide different access for your application's objects, modify the CreateMyDACL function as needed.</span></span>

<span data-ttu-id="67e8e-109">Ознакомьтесь со следующим примером:</span><span class="sxs-lookup"><span data-stu-id="67e8e-109">In the example:</span></span>

1.  <span data-ttu-id="67e8e-110">Функция Main передает адрес структуры [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) функции креатемидакл.</span><span class="sxs-lookup"><span data-stu-id="67e8e-110">The main function passes an address of a [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to the CreateMyDACL function.</span></span>
2.  <span data-ttu-id="67e8e-111">Функция Креатемидакл использует строки SDDL для:</span><span class="sxs-lookup"><span data-stu-id="67e8e-111">The CreateMyDACL function uses SDDL strings to:</span></span>
    -   <span data-ttu-id="67e8e-112">Запрет доступа к гостям и пользователям с анонимным входом.</span><span class="sxs-lookup"><span data-stu-id="67e8e-112">Deny access to guest and anonymous logon users.</span></span>
    -   <span data-ttu-id="67e8e-113">Разрешить доступ для чтения, записи и выполнения пользователям, прошедшим проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="67e8e-113">Allow read/write/execute access to authenticated users.</span></span>
    -   <span data-ttu-id="67e8e-114">Разрешение полного доступа администраторам.</span><span class="sxs-lookup"><span data-stu-id="67e8e-114">Allow full control to administrators.</span></span>

    <span data-ttu-id="67e8e-115">Дополнительные сведения о форматах строк SDDL см. в разделе [Формат строки дескриптора безопасности](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="67e8e-115">For more information about the SDDL string formats, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>
3.  <span data-ttu-id="67e8e-116">Функция Креатемидакл вызывает функцию [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) для преобразования строк SDDL в [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="67e8e-116">The CreateMyDACL function calls the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL strings to a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="67e8e-117">На дескриптор безопасности указывает член **лпсекуритидескриптор** структуры [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="67e8e-117">The security descriptor is pointed to by the **lpSecurityDescriptor** member of the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="67e8e-118">Креатемидакл отправляет возвращаемое значение из **конвертстрингсекуритидескриптортосекуритидескриптор** в функцию main.</span><span class="sxs-lookup"><span data-stu-id="67e8e-118">CreateMyDACL sends the return value from **ConvertStringSecurityDescriptorToSecurityDescriptor** to the main function.</span></span>
4.  <span data-ttu-id="67e8e-119">Функция Main использует обновленную структуру [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) для указания списка DACL для новой папки, созданной функцией [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="67e8e-119">The main function uses the updated [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure to specify the DACL for a new folder that is created by the [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) function.</span></span>
5.  <span data-ttu-id="67e8e-120">Когда функция Main завершается с использованием структуры [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , функция Main освобождает память, выделенную для члена **лпсекуритидескриптор** , вызывая функцию [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .</span><span class="sxs-lookup"><span data-stu-id="67e8e-120">When the main function is finished using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure, the main function frees the memory allocated for the **lpSecurityDescriptor** member by calling the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function.</span></span>

> [!Note]  
> <span data-ttu-id="67e8e-121">Для успешной компиляции функций SDDL, таких как [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), необходимо определить \_ \_ константу Win32 WinNT как 0x0500 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="67e8e-121">To successfully compile SDDL functions such as [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), you must define the \_WIN32\_WINNT constant as 0x0500 or greater.</span></span>

 


```C++
#define _WIN32_WINNT 0x0500

#include <windows.h>
#include <sddl.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

BOOL CreateMyDACL(SECURITY_ATTRIBUTES *);

void main()
{
     SECURITY_ATTRIBUTES  sa;
      
     sa.nLength = sizeof(SECURITY_ATTRIBUTES);
     sa.bInheritHandle = FALSE;  

     // Call function to set the DACL. The DACL
     // is set in the SECURITY_ATTRIBUTES 
     // lpSecurityDescriptor member.
     if (!CreateMyDACL(&sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateMyDACL\n");
         exit(1);
     }

     // Use the updated SECURITY_ATTRIBUTES to specify
     // security attributes for securable objects.
     // This example uses security attributes during
     // creation of a new directory.
     if (0 == CreateDirectory(TEXT("C:\\MyFolder"), &sa))
     {
         // Error encountered; generate message and exit.
         printf("Failed CreateDirectory\n");
         exit(1);
     }

     // Free the memory allocated for the SECURITY_DESCRIPTOR.
     if (NULL != LocalFree(sa.lpSecurityDescriptor))
     {
         // Error encountered; generate message and exit.
         printf("Failed LocalFree\n");
         exit(1);
     }
}


// CreateMyDACL.
//    Create a security descriptor that contains the DACL 
//    you want.
//    This function uses SDDL to make Deny and Allow ACEs.
//
// Parameter:
//    SECURITY_ATTRIBUTES * pSA
//    Pointer to a SECURITY_ATTRIBUTES structure. It is your
//    responsibility to properly initialize the 
//    structure and to free the structure's 
//    lpSecurityDescriptor member when you have
//    finished using it. To free the structure's 
//    lpSecurityDescriptor member, call the 
//    LocalFree function.
// 
// Return value:
//    FALSE if the address to the structure is NULL. 
//    Otherwise, this function returns the value from the
//    ConvertStringSecurityDescriptorToSecurityDescriptor 
//    function.
BOOL CreateMyDACL(SECURITY_ATTRIBUTES * pSA)
{
     // Define the SDDL for the DACL. This example sets 
     // the following access:
     //     Built-in guests are denied all access.
     //     Anonymous logon is denied all access.
     //     Authenticated users are allowed 
     //     read/write/execute access.
     //     Administrators are allowed full control.
     // Modify these values as needed to generate the proper
     // DACL for your application. 
     TCHAR * szSD = TEXT("D:")       // Discretionary ACL
        TEXT("(D;OICI;GA;;;BG)")     // Deny access to 
                                     // built-in guests
        TEXT("(D;OICI;GA;;;AN)")     // Deny access to 
                                     // anonymous logon
        TEXT("(A;OICI;GRGWGX;;;AU)") // Allow 
                                     // read/write/execute 
                                     // to authenticated 
                                     // users
        TEXT("(A;OICI;GA;;;BA)");    // Allow full control 
                                     // to administrators

    if (NULL == pSA)
        return FALSE;

     return ConvertStringSecurityDescriptorToSecurityDescriptor(
                szSD,
                SDDL_REVISION_1,
                &(pSA->lpSecurityDescriptor),
                NULL);
}
```



 

 
