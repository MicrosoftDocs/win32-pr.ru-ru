---
title: Создание прокси-библиотеки DLL и библиотеки типов из одного файла IDL
description: Для создания прокси-заглушек и файлов заголовков для маршалирования кода и библиотеки типов можно использовать один файл IDL.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Язык MIDL MIDL, задачи, создание прокси-библиотеки DLL и библиотеки типов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e7bf2694b791007b0f1da303525217cf55d75d574e083c6d1756bc2784d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384240"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>Создание прокси-библиотеки DLL и библиотеки типов из одного файла IDL

Для создания прокси-заглушек и файлов заголовков для маршалирования кода и библиотеки типов можно использовать один файл IDL. Для этого необходимо определить интерфейс за пределами блока библиотеки и затем ссылаться на него из блока Library, как показано в следующем примере:

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

Дополнительные сведения см. в разделе [маршалирование типов данных OLE](marshaling-ole-data-types.md) и [дополнительных файлов, необходимых для создания библиотеки типов](additional-files-required-to-generate-a-type-library-2.md).

 

 




