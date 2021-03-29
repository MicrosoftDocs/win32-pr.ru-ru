---
description: В следующем примере выполняется шифрование и расшифровка большого двоичного объекта данных с помощью CryptProtectData и CryptUnprotectData.
ms.assetid: 51607aad-9fa8-4db6-bd2a-3821dce619e7
title: 'Пример программы C: использование CryptProtectData'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87359bf6e4d90c4e46140aa9e114ffabf0a5ad80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913040"
---
# <a name="example-c-program-using-cryptprotectdata"></a>Пример программы C: использование CryptProtectData

В следующем примере выполняется шифрование и расшифровка [*большого двоичного объекта*](../secgloss/b-gly.md) данных с помощью [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata).

В этом примере показаны следующие задачи и функции CryptoAPI:

-   Инициализация структуры данных [**криптпротект \_ промптструкт**](/windows/desktop/api/Dpapi/ns-dpapi-cryptprotect_promptstruct) .
-   Использование [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) для шифрования большого двоичного объекта данных.
-   Использование [**CryptUnprotectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata) для расшифровки данных.
-   Использование [**функции LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) для высвобождения выделенной памяти.

В этом примере используется функция [**михандлиррор**](myhandleerror.md) . Код для этой функции включен в пример. Код для этой и других вспомогательных функций также указан в разделе [общего назначения функции](general-purpose-functions.md).

В следующем примере показана защита данных.


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main()
{

// Copyright (C) Microsoft.  All rights reserved.
// Encrypt data from DATA_BLOB DataIn to DATA_BLOB DataOut.
// Then decrypt to DATA_BLOB DataVerify.

//-------------------------------------------------------------------
// Declare and initialize variables.

DATA_BLOB DataIn;
DATA_BLOB DataOut;
DATA_BLOB DataVerify;
BYTE *pbDataInput =(BYTE *)"Hello world of data protection.";
DWORD cbDataInput = strlen((char *)pbDataInput)+1;
DataIn.pbData = pbDataInput;    
DataIn.cbData = cbDataInput;
CRYPTPROTECT_PROMPTSTRUCT PromptStruct;
LPWSTR pDescrOut = NULL;

//-------------------------------------------------------------------
//  Begin processing.

printf("The data to be encrypted is: %s\n",pbDataInput);

//-------------------------------------------------------------------
//  Initialize PromptStruct.

ZeroMemory(&PromptStruct, sizeof(PromptStruct));
PromptStruct.cbSize = sizeof(PromptStruct);
PromptStruct.dwPromptFlags = CRYPTPROTECT_PROMPT_ON_PROTECT;
PromptStruct.szPrompt = L"This is a user prompt.";

//-------------------------------------------------------------------
//  Begin protect phase.

if(CryptProtectData(
     &DataIn,
     L"This is the description string.", // A description string. 
     NULL,                               // Optional entropy
                                         // not used.
     NULL,                               // Reserved.
     &PromptStruct,                      // Pass a PromptStruct.
     0,
     &DataOut))
{
     printf("The encryption phase worked. \n");
}
else
{
    MyHandleError("Encryption error!");
}
//-------------------------------------------------------------------
//   Begin unprotect phase.

if (CryptUnprotectData(
        &DataOut,
        &pDescrOut,
        NULL,                 // Optional entropy
        NULL,                 // Reserved
        &PromptStruct,        // Optional PromptStruct
        0,
        &DataVerify))
{
     printf("The decrypted data is: %s\n", DataVerify.pbData);
     printf("The description of the data was: %S\n",pDescrOut);
}
else
{
    MyHandleError("Decryption error!");
}
//-------------------------------------------------------------------
// At this point, memcmp could be used to compare DataIn.pbData and 
// DataVerify.pbDate for equality. If the two functions worked
// correctly, the two byte strings are identical. 

//-------------------------------------------------------------------
//  Clean up.

LocalFree(pDescrOut);
LocalFree(DataOut.pbData);
LocalFree(DataVerify.pbData);
} // End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the  
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // End of MyHandleError
```



 

 
