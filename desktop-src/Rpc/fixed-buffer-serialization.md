---
title: Фиксированная сериализация буфера
description: Фиксированная сериализация буфера.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87e3cad0a272ccd493cf9088fedeb272f1206b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411028"
---
# <a name="fixed-buffer-serialization"></a><span data-ttu-id="74f4c-103">Фиксированная сериализация буфера</span><span class="sxs-lookup"><span data-stu-id="74f4c-103">Fixed Buffer Serialization</span></span>

<span data-ttu-id="74f4c-104">При использовании фиксированного стиля буфера укажите буфер, достаточно большой для размещения операций кодирования (маршалинга), выполненных с помощью этого маркера.</span><span class="sxs-lookup"><span data-stu-id="74f4c-104">When using the fixed buffer style, specify a buffer that is large enough to accommodate the encoding (marshalling) operations performed with the handle.</span></span> <span data-ttu-id="74f4c-105">При распаковке Вы предоставляете буфер, содержащий все данные для декодирования.</span><span class="sxs-lookup"><span data-stu-id="74f4c-105">When unmarshaling, you provide the buffer that contains all of the data to decode.</span></span>

<span data-ttu-id="74f4c-106">Фиксированный стиль буфера для сериализации использует следующие подпрограммы:</span><span class="sxs-lookup"><span data-stu-id="74f4c-106">The fixed buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="74f4c-107">**месенкодефикседбуфферхандлекреате**</span><span class="sxs-lookup"><span data-stu-id="74f4c-107">**MesEncodeFixedBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [<span data-ttu-id="74f4c-108">**месдекодебуфферхандлекреате**</span><span class="sxs-lookup"><span data-stu-id="74f4c-108">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="74f4c-109">**месбуфферхандлересет**</span><span class="sxs-lookup"><span data-stu-id="74f4c-109">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="74f4c-110">**мешандлефри**</span><span class="sxs-lookup"><span data-stu-id="74f4c-110">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="74f4c-111">Функция **месенкодефикседбуфферхандлекреате** выделяет память, необходимую для маркера кодирования, а затем инициализирует ее.</span><span class="sxs-lookup"><span data-stu-id="74f4c-111">The **MesEncodeFixedBufferHandleCreate** function allocates the memory needed for the encoding handle, and then initializes it.</span></span> <span data-ttu-id="74f4c-112">Приложение может вызвать [**месбуфферхандлересет**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) для повторной инициализации обработчика или вызвать [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree) для освобождения памяти обработчика.</span><span class="sxs-lookup"><span data-stu-id="74f4c-112">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle, or it can call [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="74f4c-113">Чтобы создать маркер декодирования, соответствующий фиксированному стилю, необходимо использовать [**месдекодебуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="74f4c-113">To create a decoding handle corresponding to the fixed style–encoding handle, you must use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

<span data-ttu-id="74f4c-114">Приложение вызывает [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree) для освобождения буфера кодирования или декодирования.</span><span class="sxs-lookup"><span data-stu-id="74f4c-114">The application calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the encoding or decoding buffer handle.</span></span>

## <a name="examples-of-fixed-buffer-encoding"></a><span data-ttu-id="74f4c-115">Примеры фиксированной кодировки буфера</span><span class="sxs-lookup"><span data-stu-id="74f4c-115">Examples of Fixed Buffer Encoding</span></span>

<span data-ttu-id="74f4c-116">В следующем разделе приведен пример использования фиксированного стиля буфера для кодирования процедур.</span><span class="sxs-lookup"><span data-stu-id="74f4c-116">The following section provides an example of how to use a fixed buffer style–serializing handle for procedure encoding.</span></span>

``` syntax
/*This is a fragment of the IDL file defining MooProc */

...
void __RPC_USER
MyProc( [in] handle_t Handle, [in,out] MyType * pMyObject,
        [in, out] ThisType * pThisObject);
...

/*This is an ACF file. MyProc is defined in the IDL file */

[
    explicit_handle
]
interface regress
{
    [ encode,decode ] MyProc();
}
```

<span data-ttu-id="74f4c-117">Следующий фрагмент представляет часть приложения.</span><span class="sxs-lookup"><span data-stu-id="74f4c-117">The following excerpt represents a part of an application.</span></span>

``` syntax
if (MesEncodeFixedBufferHandleCreate (
        Buffer, BufferSize, 
        pEncodedSize, &Handle) == RPC_S_OK)
{
    ...
    /* Manufacture a MyObject and a ThisObject */
    ...
    /* The serialization works from the beginning of the buffer because 
   the handle is in the initial state. The function MyProc does the    
   following when called with an encoding handle:
     - sizes all the parameters for marshalling,
     - marshalls into the buffer (and sets the internal state 
    appropriately) 
    */

    MyProc ( Handle, pMyObject, pThisObject );
    ...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK)
{

    /* The MooProc does the following for you when called with a decoding 
    handle:
     - unmarshalls the objects from the buffer into *pMooObject and 
       *pBarObject
*/

MyProc ( Handle, pMyObject, pThisObject);
...
MesHandleFree ( Handle );
}
```

<span data-ttu-id="74f4c-118">В следующем разделе приведен пример того, как использовать фиксированный формат буфера — для кодирования типов.</span><span class="sxs-lookup"><span data-stu-id="74f4c-118">The following section provides an example of how to use a fixed buffer style–serializing handle for type encoding.</span></span>

``` syntax
/* This is an ACF file. MyType is defined in the IDL file */

[    
    explicit_handle
]
interface regress
{
    typedef [ encode,decode ] MyType;
}
```

<span data-ttu-id="74f4c-119">Следующий фрагмент представляет соответствующие фрагменты приложения.</span><span class="sxs-lookup"><span data-stu-id="74f4c-119">The following excerpt represents the relevant application fragments.</span></span>


```C++
if (MesEncodeFixedBufferHandleCreate (Buffer, BufferSize, 
    pEncodedSize, &Handle) == RPC_S_OK)
{
    //...
    /* Manufacture a MyObject and a pMyObject */
    //...
    MyType_Encode ( Handle, pMyObject );
    //...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK )
{
    MooType_Decode (Handle, pMooObject);
    //...
    MesHandleFree ( Handle );
}
```



 

 




