---
description: Показывает, как правильно создать список DACL.
ms.assetid: f8ec202f-4f34-4123-8f3c-cfc5960b4dc2
title: Создание списка DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af1c7c43c24c07d3d301642b93db41496f2ff70742ce8e2e95fd3f7364ad765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516054"
---
# <a name="creating-a-dacl"></a>Создание списка DACL

Создание правильного [*списка управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) — это необходимая и важная часть разработки приложений. Поскольку **пустой** список DACL разрешает всем типам доступа всем пользователям, не используйте **пустые** списки DACL.

В следующем примере показано, как правильно создать список DACL. Пример содержит функцию Креатемидакл, которая использует [язык определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL) для определения предоставленного и запрещенного контроля доступа в списке DACL. Чтобы предоставить другим приложениям доступ к объектам приложения, при необходимости измените функцию Креатемидакл.

Ознакомьтесь со следующим примером:

1.  Функция Main передает адрес структуры [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) функции креатемидакл.
2.  Функция Креатемидакл использует строки SDDL для:
    -   Запрет доступа к гостям и пользователям с анонимным входом.
    -   Разрешить доступ для чтения, записи и выполнения пользователям, прошедшим проверку подлинности.
    -   Разрешение полного доступа администраторам.

    Дополнительные сведения о форматах строк SDDL см. в разделе [Формат строки дескриптора безопасности](/windows/desktop/SecAuthZ/security-descriptor-string-format).
3.  Функция Креатемидакл вызывает функцию [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) для преобразования строк SDDL в [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly). На дескриптор безопасности указывает член **лпсекуритидескриптор** структуры [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . Креатемидакл отправляет возвращаемое значение из **конвертстрингсекуритидескриптортосекуритидескриптор** в функцию main.
4.  Функция Main использует обновленную структуру [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) для указания списка DACL для новой папки, созданной функцией [**CreateDirectory**](/windows/desktop/api/fileapi/nf-fileapi-createdirectorya) .
5.  Когда функция Main завершается с использованием структуры [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , функция Main освобождает память, выделенную для члена **лпсекуритидескриптор** , вызывая функцию [**функции LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .

> [!Note]  
> Для успешной компиляции функций SDDL, таких как [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora), необходимо определить \_ \_ константу Win32 WinNT как 0x0500 или более позднюю.

 


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



 

 
