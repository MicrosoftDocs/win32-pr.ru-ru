---
title: Использование служб сериализации
description: MIDL создает заглушку сериализации для процедуры с помощью атрибутов \ Encoded \ и декодирования \.
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- Удаленный вызов процедур RPC, задачи, использование служб сериализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be20d513bdb74eca316b022dd8536e8988e32e93099981cc77830035048e55e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010633"
---
# <a name="using-serialization-services"></a>Использование служб сериализации

MIDL создает заглушку сериализации для процедуры с помощью \[ [**кодирования**](/windows/desktop/Midl/encode) \] и \[ [**декодирования**](/windows/desktop/Midl/decode)атрибутов \] . При вызове этой подпрограммы выполняется вызов сериализации вместо удаленного вызова. Аргументы процедуры маршалируются в буфер или расмаршалируются из буфера обычным способом. После этого вы получите полный контроль над буферами.

В отличие от этого, когда программа выполняет сериализацию типа (тип помечен атрибутами сериализации), MIDL создает подпрограммы для размера, кодирования и декодирования объектов этого типа. Для сериализации данных необходимо вызывать эти подпрограммы соответствующим образом. Сериализация типов является расширением Майкрософт и, таким образом, недоступна при компиляции в режиме DCE-Compatibility ([**/ОСФ**](/windows/desktop/Midl/-osf)). Используя \[ атрибуты [**кодирования**](/windows/desktop/Midl/encode) \] и \[ [**декодирования**](/windows/desktop/Midl/decode) в \] качестве атрибутов интерфейса, RPC применяет кодировку ко всем типам и подпрограммым, определенным в IDL-файле.

При использовании служб сериализации необходимо предоставить адекватные согласованные буферы. Начало буфера должно быть согласовано по адресу, который имеет кратное 8 или 8-байтовое согласованное. Для сериализации процедур каждый вызов процедуры должен выполнять упаковку или распаковку из места в буфере с согласованием в 8 байт. Для сериализации типов, изменения размера, кодировки и декодирования должны начинаться с позиции, которая соответствует 8 байтам.

Один из способов, позволяющих приложению обеспечить согласованность его буферов, — написать функцию [**\_ пользовательского \_ выделения MIDL**](/windows/desktop/Midl/midl-user-allocate-1) , чтобы создать согласованные буферы. В следующем образце кода показано, как это можно сделать.


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



В следующем примере показана соответствующая функция [**\_ \_ Free пользователя MIDL**](/windows/desktop/Midl/midl-user-free-1) .


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



 

 