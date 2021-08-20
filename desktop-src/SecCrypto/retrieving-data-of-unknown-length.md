---
description: Многие функции возвращают потенциально большой объем данных в адрес, предоставленный приложением в качестве одного из параметров.
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: Получение данных неизвестной длины
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a71a30e935dd20bee6cce8f6dbc00a3b61478a90f4ea2139d7daaddc6894da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975018"
---
# <a name="retrieving-data-of-unknown-length"></a>Получение данных неизвестной длины

Многие функции возвращают потенциально большой объем данных в адрес, предоставленный приложением в качестве одного из параметров. Во всех этих случаях операция выполняется аналогичным образом, если оно не идентично. Параметр, указывающий на расположение возвращаемых данных, будет использовать обозначение, где PB или ПС являются первыми двумя символами имени параметра. Другой параметр будет содержать ПКБ в качестве первых трех символов имени параметра. Этот параметр представляет размер (в байтах) данных, которые будут возвращены в расположение PB или PV. Например, рассмотрим следующую спецификацию функции:

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

В этом примере *pbData* — это указатель на расположение, где будут возвращаться данные, а *пкбдата* — размер (в байтах) возвращаемых данных.

> [!Note]  
> В качестве сопутствующего параметра для параметра ПКБ иногда может быть несколько иной префикс, например p или ПС. Кроме того, для сопутствующих параметров, использующих сочетание префиксов пвсз и пкч, параметр пкч — это число в символах ([*Unicode*](../secgloss/u-gly.md) или [*ASCII*](../secgloss/a-gly.md), как применимо) возвращаемых данных.

 

Если буфер, указанный параметром *pbData* , недостаточно велик для хранения возвращаемых данных, функция устанавливает \_ дополнительный \_ код данных (который можно увидеть, вызвав функцию [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) и сохраняет требуемый размер буфера в байтах в переменной, на которую указывает *пкбдата*.

Если **значение NULL** является входным для *pbData* и *пкбдата* не равно **null**, то ошибка не возвращается, а функция возвращает размер (в байтах) требуемого буфера памяти в переменной, на которую указывает *пкбдата*. Это позволяет приложению определить размер и наилучший способ выделения буфера для возвращаемых данных.

> [!Note]  
> Если **значение NULL** является входным для *pbData* , чтобы определить размер, необходимый для обеспечения того, что возвращаемые данные помещаются в указанный буфер, второй вызов функции, которая заполняет буфер требуемыми данными, может не использовать весь буфер. После второго вызова фактический размер возвращаемых данных содержится в *пкбдата*. Используйте этот размер при обработке данных.

 

В следующем примере показано, как можно реализовать входные и выходные параметры для этой цели.


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(char *s);

void main()
{

// Set up SomeFunction variables.
PCCRL_CONTEXT pCrlContext; // Initialized elsewhere.
DWORD dwPropId;            // Initialized elsewhere.
DWORD cbData;
BYTE  *pbData;

// Call SomeFunction to set cbData, the size of 
// the buffer needed for pbData.
if(SomeFunction(
     pCrlContext, 
     dwPropId, 
     NULL, 
     &cbData))
{
       printf("The function succeeded.\n");
}
else
{

// The function call failed. Handle the error.
       MyHandleError("Function call failed.");
}

// The call succeeded; the size for the needed buffer, in bytes, 
// now resides in cbData.

// Malloc memory for the size of the message.
if(pbData = (BYTE*)malloc(cbData))
{
   printf("Memory has been allocated.\n");
}
else
{

   // The allocation failed. Write an error message and exit.
   MyHandleError("Malloc operation failed. ");
}

// The space for the buffer has been allocated.
// Call SomeFunction to fill the buffer with the data.
if(SomeFunction(
      pCrlContext, 
      dwPropId, 
      pbData, 
      &cbData))
{
       printf("The function succeeded.\n");
}
else
{

   // The second function call failed. Handle the error.
   MyHandleError("The second call to the function failed.");
}

// The function succeeded; the data is now in the buffer
// pointed to by pbData. Note that cbData is
// updated with the actual size of the data returned. Use this size 
// to process bytes of pbData.

// When you have finished using the allocated memory, free it.
free(pbData);

} // End of main

//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the 
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.
void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program.\n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr,"Error number %x.\n",GetLastError());
    fprintf(stderr,"Program terminating.\n");
    exit(1);
}
```



 

 
