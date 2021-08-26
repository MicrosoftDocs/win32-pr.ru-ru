---
title: Фиксированная сериализация буфера
description: Фиксированная сериализация буфера.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce58d3bdf92673c97ae8dc9fbbf8f366cb4a59a9e3ce114431de1581af30ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021214"
---
# <a name="fixed-buffer-serialization"></a>Фиксированная сериализация буфера

При использовании фиксированного стиля буфера укажите буфер, достаточно большой для размещения операций кодирования (маршалинга), выполненных с помощью этого маркера. При распаковке Вы предоставляете буфер, содержащий все данные для декодирования.

Фиксированный стиль буфера для сериализации использует следующие подпрограммы:

-   [**месенкодефикседбуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**месдекодебуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**месбуфферхандлересет**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Функция **месенкодефикседбуфферхандлекреате** выделяет память, необходимую для маркера кодирования, а затем инициализирует ее. Приложение может вызвать [**месбуфферхандлересет**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) для повторной инициализации обработчика или вызвать [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree) для освобождения памяти обработчика. Чтобы создать маркер декодирования, соответствующий фиксированному стилю, необходимо использовать [**месдекодебуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

Приложение вызывает [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree) для освобождения буфера кодирования или декодирования.

## <a name="examples-of-fixed-buffer-encoding"></a>Примеры фиксированной кодировки буфера

В следующем разделе приведен пример использования фиксированного стиля буфера для кодирования процедур.

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

Следующий фрагмент представляет часть приложения.

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

В следующем разделе приведен пример того, как использовать фиксированный формат буфера — для кодирования типов.

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

Следующий фрагмент представляет соответствующие фрагменты приложения.


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



 

 




