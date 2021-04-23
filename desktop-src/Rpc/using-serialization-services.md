---
title: Использование служб сериализации
description: MIDL создает заглушку сериализации для процедуры с помощью атрибутов \ Encoded \ и декодирования \.
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- Удаленный вызов процедур RPC, задачи, использование служб сериализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317156a2da954e001b687cca12eb0c6df23ef4ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070576"
---
# <a name="using-serialization-services"></a><span data-ttu-id="8cc80-104">Использование служб сериализации</span><span class="sxs-lookup"><span data-stu-id="8cc80-104">Using Serialization Services</span></span>

<span data-ttu-id="8cc80-105">MIDL создает заглушку сериализации для процедуры с помощью \[ [**кодирования**](/windows/desktop/Midl/encode) \] и \[ [**декодирования**](/windows/desktop/Midl/decode)атрибутов \] .</span><span class="sxs-lookup"><span data-stu-id="8cc80-105">MIDL generates a serialization stub for the procedure with the attributes \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\].</span></span> <span data-ttu-id="8cc80-106">При вызове этой подпрограммы выполняется вызов сериализации вместо удаленного вызова.</span><span class="sxs-lookup"><span data-stu-id="8cc80-106">When you call this routine, you execute a serialization call instead of a remote call.</span></span> <span data-ttu-id="8cc80-107">Аргументы процедуры маршалируются в буфер или расмаршалируются из буфера обычным способом.</span><span class="sxs-lookup"><span data-stu-id="8cc80-107">The procedure arguments are marshaled to or unmarshaled from a buffer in the usual way.</span></span> <span data-ttu-id="8cc80-108">После этого вы получите полный контроль над буферами.</span><span class="sxs-lookup"><span data-stu-id="8cc80-108">You then have complete control of the buffers.</span></span>

<span data-ttu-id="8cc80-109">В отличие от этого, когда программа выполняет сериализацию типа (тип помечен атрибутами сериализации), MIDL создает подпрограммы для размера, кодирования и декодирования объектов этого типа.</span><span class="sxs-lookup"><span data-stu-id="8cc80-109">In contrast, when your program performs type serialization (a type is labeled with serialization attributes), MIDL generates routines to size, encode, and decode objects of that type.</span></span> <span data-ttu-id="8cc80-110">Для сериализации данных необходимо вызывать эти подпрограммы соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="8cc80-110">To serialize data, you must call these routines in the appropriate way.</span></span> <span data-ttu-id="8cc80-111">Сериализация типов является расширением Майкрософт и, таким образом, недоступна при компиляции в режиме DCE-Compatibility ([**/ОСФ**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="8cc80-111">Type serialization is a Microsoft extension and, as such, is not available when you compile in DCE-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="8cc80-112">Используя \[ атрибуты [**кодирования**](/windows/desktop/Midl/encode) \] и \[ [**декодирования**](/windows/desktop/Midl/decode) в \] качестве атрибутов интерфейса, RPC применяет кодировку ко всем типам и подпрограммым, определенным в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="8cc80-112">By using the \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\] attributes as interface attributes, RPC applies encoding to all the types and routines defined in the IDL file.</span></span>

<span data-ttu-id="8cc80-113">При использовании служб сериализации необходимо предоставить адекватные согласованные буферы.</span><span class="sxs-lookup"><span data-stu-id="8cc80-113">You must supply adequately aligned buffers when using serialization services.</span></span> <span data-ttu-id="8cc80-114">Начало буфера должно быть согласовано по адресу, который имеет кратное 8 или 8-байтовое согласованное.</span><span class="sxs-lookup"><span data-stu-id="8cc80-114">The beginning of the buffer must be aligned at an address that is a multiple of 8, or 8-byte aligned.</span></span> <span data-ttu-id="8cc80-115">Для сериализации процедур каждый вызов процедуры должен выполнять упаковку или распаковку из места в буфере с согласованием в 8 байт.</span><span class="sxs-lookup"><span data-stu-id="8cc80-115">For procedure serialization, each procedure call must marshal into or unmarshal from a buffer position that is 8-byte aligned.</span></span> <span data-ttu-id="8cc80-116">Для сериализации типов, изменения размера, кодировки и декодирования должны начинаться с позиции, которая соответствует 8 байтам.</span><span class="sxs-lookup"><span data-stu-id="8cc80-116">For type serialization, sizing, encoding, and decoding must start at a position that is 8-byte aligned.</span></span>

<span data-ttu-id="8cc80-117">Один из способов, позволяющих приложению обеспечить согласованность его буферов, — написать функцию [**\_ пользовательского \_ выделения MIDL**](/windows/desktop/Midl/midl-user-allocate-1) , чтобы создать согласованные буферы.</span><span class="sxs-lookup"><span data-stu-id="8cc80-117">One way for your application to ensure that its buffers are aligned is to write the [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) function such that it creates aligned buffers.</span></span> <span data-ttu-id="8cc80-118">В следующем образце кода показано, как это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="8cc80-118">The following code sample demonstrates how this can be done.</span></span>


```C++
#include <windows.h>

#define ALIGN_TO8(p)   (char *)((unsigned long)((char *)p + 7) & ~7)

void __RPC_FAR *__RPC_USER  MIDL_user_allocate(size_t sizeInBytes)
{
    unsigned char *pcAllocated;
    unsigned char *pcUserPtr;

    pcAllocated = (unsigned char *) malloc( sizeInBytes + 15 );
    pcUserPtr =  ALIGN_TO8( pcAllocated );
    if ( pcUserPtr == pcAllocated )
        pcUserPtr = pcAllocated + 8;

    *(pcUserPtr - 1) = pcUserPtr - pcAllocated;

    return( pcUserPtr );
}
```



<span data-ttu-id="8cc80-119">В следующем примере показана соответствующая функция [**\_ \_ Free пользователя MIDL**](/windows/desktop/Midl/midl-user-free-1) .</span><span class="sxs-lookup"><span data-stu-id="8cc80-119">The following example shows the corresponding [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) function.</span></span>


```C++
void __RPC_USER  MIDL_user_free(void __RPC_FAR *f)
{
    unsigned char * pcAllocated;
    unsigned char * pcUserPtr;

    pcUserPtr = (unsigned char *) f;
    pcAllocated = pcUserPtr - *(pcUserPtr - 1);

    free( pcAllocated );
}
```



 

 