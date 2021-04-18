---
description: Вызывает функцию Аттачпропертиес для отображения свойств, которые существуют в части распознанных данных.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Реализация Аттачпропертиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673423"
---
# <a name="implementing-attachproperties"></a><span data-ttu-id="62f30-103">Реализация Аттачпропертиес</span><span class="sxs-lookup"><span data-stu-id="62f30-103">Implementing AttachProperties</span></span>

<span data-ttu-id="62f30-104">Сетевой монитор вызывает функцию [**аттачпропертиес**](attachproperties.md) для отображения свойств, которые существуют в части распознанных данных.</span><span class="sxs-lookup"><span data-stu-id="62f30-104">Network Monitor calls the [**AttachProperties**](attachproperties.md) function to map the properties that exist in a piece of recognized data.</span></span> <span data-ttu-id="62f30-105">Функция [**аттачпропертиес**](attachproperties.md) сопоставляет свойства с конкретным расположением.</span><span class="sxs-lookup"><span data-stu-id="62f30-105">The [**AttachProperties**](attachproperties.md) function maps the properties to a specific location.</span></span>

<span data-ttu-id="62f30-106">Для анализа данных в кадре сетевой монитор используется следующий процесс.</span><span class="sxs-lookup"><span data-stu-id="62f30-106">Network Monitor uses the following process to parse the data in a frame.</span></span>

-   <span data-ttu-id="62f30-107">Во-первых, сетевой монитор вызывает [рекогнизефраме](recognizeframe.md) для распознавания всех протоколов, имеющихся в кадре.</span><span class="sxs-lookup"><span data-stu-id="62f30-107">First, Network Monitor calls [RecognizeFrame](recognizeframe.md) to recognize all the protocols that exist in a frame.</span></span>
-   <span data-ttu-id="62f30-108">Затем сетевой монитор вызывает [**аттачпропертиес**](attachproperties.md) для каждого средства синтаксического анализа, распознающего фрагмент данных.</span><span class="sxs-lookup"><span data-stu-id="62f30-108">Then, Network Monitor calls [**AttachProperties**](attachproperties.md) for each parser that recognizes a piece of data.</span></span>

<span data-ttu-id="62f30-109">Когда сетевой монитор вызывает функцию [аттачпропертиес](attachproperties.md) для распознаваемых данных, средство синтаксического анализа, которое вызывается, должно анализировать данные, а затем сопоставлять каждое существующее свойство с расположением в распознанных данных.</span><span class="sxs-lookup"><span data-stu-id="62f30-109">When Network Monitor calls the [AttachProperties](attachproperties.md) function for the recognized data, the parser that is called must parse the data, and then map each existing property to a location in the recognized data.</span></span> <span data-ttu-id="62f30-110">Средство синтаксического анализа определяет, какие свойства существуют, и где каждое свойство находится в данных.</span><span class="sxs-lookup"><span data-stu-id="62f30-110">The parser determines which properties exist, and where each property is located in the data.</span></span> <span data-ttu-id="62f30-111">На следующем рисунке показаны распознаваемые синтаксическим анализатором данные.</span><span class="sxs-lookup"><span data-stu-id="62f30-111">The following figure shows parser-recognized data.</span></span>

![данные, распознаваемые синтаксическим анализатором](images/attachproperties1.png)

<span data-ttu-id="62f30-113">Во время реализации [**аттачпропертиес**](attachproperties.md)необходимо вызвать одну из следующих функций для каждого свойства, существующего в кадре данных.</span><span class="sxs-lookup"><span data-stu-id="62f30-113">During the implementation of [**AttachProperties**](attachproperties.md), you must call one of the following functions for each property that exists in a data frame.</span></span>

-   <span data-ttu-id="62f30-114">Вызовите функцию [**аттачпропертинстанцеекс**](attachpropertyinstanceex.md) , если требуется изменить данные свойства в кадре.</span><span class="sxs-lookup"><span data-stu-id="62f30-114">Call the [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function when you want to modify the property data in a frame.</span></span>
-   <span data-ttu-id="62f30-115">Вызовите функцию [**аттачпропертинстанце**](attachpropertyinstance.md) , если не хотите изменять данные свойства в кадре.</span><span class="sxs-lookup"><span data-stu-id="62f30-115">Call the [**AttachPropertyInstance**](attachpropertyinstance.md) function when you do not want to modify the property data in a frame.</span></span>

> [!Note]  
> <span data-ttu-id="62f30-116">Рекомендуется использовать данные в том виде, в котором они существуют в записи.</span><span class="sxs-lookup"><span data-stu-id="62f30-116">It is recommended that you use the data as it exists in the capture.</span></span>

 

<span data-ttu-id="62f30-117">Следующая процедура определяет шаги, необходимые для реализации [**аттачпропертиес**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="62f30-117">The following procedure identifies the steps necessary to implement [**AttachProperties**](attachproperties.md).</span></span>

<span data-ttu-id="62f30-118">**Реализация Аттачпропертиес**</span><span class="sxs-lookup"><span data-stu-id="62f30-118">**To implement AttachProperties**</span></span>

1.  <span data-ttu-id="62f30-119">Определите, какие свойства существуют, и расположение свойства в данных.</span><span class="sxs-lookup"><span data-stu-id="62f30-119">Determine which properties exist, and the property location in the data.</span></span>
2.  <span data-ttu-id="62f30-120">Вызовите [**аттачпропертинстанцеекс**](attachpropertyinstanceex.md) для каждого свойства со значением, которое необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="62f30-120">Call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) for each property with a value that you want to modify.</span></span>
3.  <span data-ttu-id="62f30-121">Вызовите [**аттачпропертинстанце**](attachpropertyinstance.md) для каждого свойства со значением, которое не нужно изменять.</span><span class="sxs-lookup"><span data-stu-id="62f30-121">Call [**AttachPropertyInstance**](attachpropertyinstance.md) for each property with a value that you do not want to modify.</span></span> <span data-ttu-id="62f30-122">Как правило, это единственная функция, которую необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="62f30-122">Typically, this is the only function that you need to call.</span></span>

<span data-ttu-id="62f30-123">Ниже приведена базовая реализация [**аттачпропертиес**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="62f30-123">The following is a basic implementation of [**AttachProperties**](attachproperties.md).</span></span> <span data-ttu-id="62f30-124">Имейте в виду, что в примере не содержится код, определяющий, какие свойства существуют, или код для обнаружения свойств.</span><span class="sxs-lookup"><span data-stu-id="62f30-124">Be aware that the example does not include either the code to determine which properties exist, or the code to locate the properties.</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



