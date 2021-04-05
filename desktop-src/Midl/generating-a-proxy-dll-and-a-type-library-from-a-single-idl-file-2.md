---
title: Создание прокси-библиотеки DLL и библиотеки типов из одного файла IDL
description: Для создания прокси-заглушек и файлов заголовков для маршалирования кода и библиотеки типов можно использовать один файл IDL.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Язык MIDL MIDL, задачи, создание прокси-библиотеки DLL и библиотеки типов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81001bba7aeff416e765291d3e6660b705919a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068348"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a><span data-ttu-id="d5a84-104">Создание прокси-библиотеки DLL и библиотеки типов из одного файла IDL</span><span class="sxs-lookup"><span data-stu-id="d5a84-104">Generating a Proxy DLL and a Type Library from a Single IDL File</span></span>

<span data-ttu-id="d5a84-105">Для создания прокси-заглушек и файлов заголовков для маршалирования кода и библиотеки типов можно использовать один файл IDL.</span><span class="sxs-lookup"><span data-stu-id="d5a84-105">You can use a single IDL file to generate both the proxy stubs and header files for marshaling code, and a type library.</span></span> <span data-ttu-id="d5a84-106">Для этого необходимо определить интерфейс за пределами блока библиотеки и затем ссылаться на него из блока Library, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="d5a84-106">You do this by defining an interface outside the library block and then referencing that interface from inside the library block, as shown in this example:</span></span>

``` syntax
//file: AllKnown.idl

[
    object, uuid(. . .), <other interface attributes>
]
interface IKnown : IUnknown 
{
    import "unknwn.idl";
    <declarations, etc. for IKnown interface go here>
};

[
    <library attributes>
]
library KnownLibrary 
{

    //reference interface IKnown:
    interface IKnown;

    //or create a new class:
    [
        <coclass attributes>
    ] 
    coclass KnowMore 
    {
       interface IKnown;
    };
};
```

<span data-ttu-id="d5a84-107">Дополнительные сведения см. в разделе [маршалирование типов данных OLE](marshaling-ole-data-types.md) и [дополнительных файлов, необходимых для создания библиотеки типов](additional-files-required-to-generate-a-type-library-2.md).</span><span class="sxs-lookup"><span data-stu-id="d5a84-107">For more information, see [Marshaling OLE Data Types](marshaling-ole-data-types.md) and [Additional Files Required To Generate a Type Library](additional-files-required-to-generate-a-type-library-2.md).</span></span>

 

 




