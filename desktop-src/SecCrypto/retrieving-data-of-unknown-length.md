---
description: Многие функции возвращают потенциально большой объем данных в адрес, предоставленный приложением в качестве одного из параметров.
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: Получение данных неизвестной длины
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30620018f3c4871bd27299c3dd21ae42936c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898630"
---
# <a name="retrieving-data-of-unknown-length"></a><span data-ttu-id="13eb2-103">Получение данных неизвестной длины</span><span class="sxs-lookup"><span data-stu-id="13eb2-103">Retrieving Data of Unknown Length</span></span>

<span data-ttu-id="13eb2-104">Многие функции возвращают потенциально большой объем данных в адрес, предоставленный приложением в качестве одного из параметров.</span><span class="sxs-lookup"><span data-stu-id="13eb2-104">Many functions return a potentially large amount of data to an address provided as one of the parameters by the application.</span></span> <span data-ttu-id="13eb2-105">Во всех этих случаях операция выполняется аналогичным образом, если оно не идентично.</span><span class="sxs-lookup"><span data-stu-id="13eb2-105">In all these cases, the operation is performed in a similar, if not identical, fashion.</span></span> <span data-ttu-id="13eb2-106">Параметр, указывающий на расположение возвращаемых данных, будет использовать обозначение, где PB или ПС являются первыми двумя символами имени параметра.</span><span class="sxs-lookup"><span data-stu-id="13eb2-106">The parameter that points to the location of the returned data will use the notation convention where pb or pv are the first two characters of the parameter name.</span></span> <span data-ttu-id="13eb2-107">Другой параметр будет содержать ПКБ в качестве первых трех символов имени параметра.</span><span class="sxs-lookup"><span data-stu-id="13eb2-107">Another parameter will have pcb as the first three characters of the parameter name.</span></span> <span data-ttu-id="13eb2-108">Этот параметр представляет размер (в байтах) данных, которые будут возвращены в расположение PB или PV.</span><span class="sxs-lookup"><span data-stu-id="13eb2-108">This parameter represents the size, in bytes, of the data that will be returned to the pb or pv location.</span></span> <span data-ttu-id="13eb2-109">Например, рассмотрим следующую спецификацию функции:</span><span class="sxs-lookup"><span data-stu-id="13eb2-109">For example, consider the following function specification:</span></span>

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

<span data-ttu-id="13eb2-110">В этом примере *pbData* — это указатель на расположение, где будут возвращаться данные, а *пкбдата* — размер (в байтах) возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="13eb2-110">In this example, *pbData* is a pointer to the location where the data will be returned, and *pcbData* is the size, in bytes, of the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="13eb2-111">В качестве сопутствующего параметра для параметра ПКБ иногда может быть несколько иной префикс, например p или ПС.</span><span class="sxs-lookup"><span data-stu-id="13eb2-111">The companion parameter to the pcb parameter may sometimes carry a slightly different prefix, such as p or pv.</span></span> <span data-ttu-id="13eb2-112">Кроме того, для сопутствующих параметров, использующих сочетание префиксов пвсз и пкч, параметр пкч — это число в символах ([*Unicode*](../secgloss/u-gly.md) или [*ASCII*](../secgloss/a-gly.md), как применимо) возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="13eb2-112">Also, for companion parameters using the combination of prefixes pwsz and pcch, the pcch parameter is the count, in characters ([*Unicode*](../secgloss/u-gly.md) or [*ASCII*](../secgloss/a-gly.md), as applicable), of the returned data.</span></span>

 

<span data-ttu-id="13eb2-113">Если буфер, указанный параметром *pbData* , недостаточно велик для хранения возвращаемых данных, функция устанавливает \_ дополнительный \_ код данных (который можно увидеть, вызвав функцию [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) и сохраняет требуемый размер буфера в байтах в переменной, на которую указывает *пкбдата*.</span><span class="sxs-lookup"><span data-stu-id="13eb2-113">If the buffer specified by the *pbData* parameter is not large enough to hold the returned data, the function sets the ERROR\_MORE\_DATA code (which can be seen by calling the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function) and stores the required buffer size, in bytes, in the variable pointed to by *pcbData*.</span></span>

<span data-ttu-id="13eb2-114">Если **значение NULL** является входным для *pbData* и *пкбдата* не равно **null**, то ошибка не возвращается, а функция возвращает размер (в байтах) требуемого буфера памяти в переменной, на которую указывает *пкбдата*.</span><span class="sxs-lookup"><span data-stu-id="13eb2-114">If **NULL** is input for *pbData* and *pcbData* is not **NULL**, no error is returned, and the function returns the size, in bytes, of the needed memory buffer in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="13eb2-115">Это позволяет приложению определить размер и наилучший способ выделения буфера для возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="13eb2-115">This lets an application determine the size of, and the best way to allocate, a buffer for the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="13eb2-116">Если **значение NULL** является входным для *pbData* , чтобы определить размер, необходимый для обеспечения того, что возвращаемые данные помещаются в указанный буфер, второй вызов функции, которая заполняет буфер требуемыми данными, может не использовать весь буфер.</span><span class="sxs-lookup"><span data-stu-id="13eb2-116">When **NULL** is input for *pbData* to determine the size needed to ensure that the returned data fits in the specified buffer, the second call to the function which populates the buffer with the desired data may not use the whole buffer.</span></span> <span data-ttu-id="13eb2-117">После второго вызова фактический размер возвращаемых данных содержится в *пкбдата*.</span><span class="sxs-lookup"><span data-stu-id="13eb2-117">After the second call, the actual size of the data returned is contained in *pcbData*.</span></span> <span data-ttu-id="13eb2-118">Используйте этот размер при обработке данных.</span><span class="sxs-lookup"><span data-stu-id="13eb2-118">Use this size when processing the data.</span></span>

 

<span data-ttu-id="13eb2-119">В следующем примере показано, как можно реализовать входные и выходные параметры для этой цели.</span><span class="sxs-lookup"><span data-stu-id="13eb2-119">The following example shows how input and output parameters might be implemented for this purpose.</span></span>


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



 

 
