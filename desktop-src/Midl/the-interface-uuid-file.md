---
title: Файл UUID интерфейса
description: Файл UUID интерфейса собирает определения идентификаторов интерфейса из всех интерфейсов в обрабатываемом IDL-файле.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL и COM MIDL, интерфейсы, прокси-файлы UUID
- файл UUID интерфейса MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778992"
---
# <a name="the-interface-uuid-file"></a><span data-ttu-id="73fb5-105">Файл UUID интерфейса</span><span class="sxs-lookup"><span data-stu-id="73fb5-105">The Interface UUID File</span></span>

<span data-ttu-id="73fb5-106">Файл UUID интерфейса собирает определения идентификаторов интерфейса из всех интерфейсов в обрабатываемом IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="73fb5-106">The interface UUID file collects the definitions of the interface identifiers from all interfaces in the processed IDL file.</span></span> <span data-ttu-id="73fb5-107">Как и в файле заглушки, и в файле заголовка, замыкание входного потока определяется текущим IDL-файлом и включенными файлами.</span><span class="sxs-lookup"><span data-stu-id="73fb5-107">Similar to the stub file and the header file, the input stream closure is defined by the current IDL file and the included files.</span></span> <span data-ttu-id="73fb5-108">Например, для интерфейса IFace компилятор создает константу IID \_ IFace и инициализирует его с UUID интерфейса, указанным в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="73fb5-108">For example, for Interface IFace, the compiler generates a constant IID\_IFace and initializes it to the interface's UUID specified in the IDL file.</span></span> <span data-ttu-id="73fb5-109">Клиентские приложения и DLL прокси-сервера используют эту константу для обнаружения интерфейса.</span><span class="sxs-lookup"><span data-stu-id="73fb5-109">Client applications and the proxy DLL use this constant to identify the interface.</span></span>

<span data-ttu-id="73fb5-110">Имя по умолчанию для файла IID интерфейса, созданного из файла. idl — файл \_ i.c.</span><span class="sxs-lookup"><span data-stu-id="73fb5-110">The default name for an interface IID file generated from a file.idl is File\_i.c.</span></span> <span data-ttu-id="73fb5-111">Параметр компилятора [**/IID**](-iid.md) MIDL переопределяет имя файла UUID интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73fb5-111">The [**/iid**](-iid.md) MIDL compiler switch overrides the default name of the interface UUID file.</span></span>

 

 




