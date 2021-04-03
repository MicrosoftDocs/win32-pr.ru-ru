---
title: Файл ACF
description: Файл ACF позволяет настраивать клиентский и (или) интерфейс RPC серверных приложений, не влияя на характеристики сети интерфейса.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987839"
---
# <a name="the-acf-file"></a><span data-ttu-id="44af2-103">Файл ACF</span><span class="sxs-lookup"><span data-stu-id="44af2-103">The ACF File</span></span>

<span data-ttu-id="44af2-104">Файл ACF позволяет настраивать клиентский и (или) интерфейс RPC серверных приложений, не влияя на характеристики сети интерфейса.</span><span class="sxs-lookup"><span data-stu-id="44af2-104">The ACF file enables you to customize your client and/or server applications' RPC interface without affecting the network characteristics of the interface.</span></span> <span data-ttu-id="44af2-105">Например, если клиентское приложение содержит сложную структуру данных, которая имеет значение только на локальном компьютере, можно указать в файле ACF, как данные в этой структуре могут быть представлены в независимой от компьютера форме для удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="44af2-105">For example, if your client application contains a complex data structure that only has meaning on the local machine, you can specify in the ACF file how the data in that structure can be represented in a machine-independent form for remote procedure calls.</span></span>

<span data-ttu-id="44af2-106">В этом руководстве показано другое использование файла ACF, в котором указывается тип маркера привязки, который представляет соединение между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="44af2-106">This tutorial demonstrates another use of the ACF file—specifying the type of binding handle that represents the connection between client and server.</span></span> <span data-ttu-id="44af2-107">Атрибут **\[** [**неявного \_ обработчика**](/windows/desktop/Midl/implicit-handle) **\]** в заголовке ACF позволяет клиентскому приложению выбрать сервер для удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="44af2-107">The **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]** attribute in the ACF header allows the client application to select a server for its remote procedure call.</span></span> <span data-ttu-id="44af2-108">ACF определяет маркер, который должен иметь тип « [**\_ t**](/windows/desktop/Midl/handle-t) » (примитивный тип данных MIDL).</span><span class="sxs-lookup"><span data-stu-id="44af2-108">The ACF defines the handle to be of the type [**handle\_t**](/windows/desktop/Midl/handle-t) (a MIDL primitive data type).</span></span> <span data-ttu-id="44af2-109">Компилятор MIDL поместит имя маркера привязки, указанное ACF, Hello \_ ифхандле в создаваемый им файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="44af2-109">The MIDL compiler will put the binding handle name that the ACF specified, hello\_IfHandle into the header file it generates.</span></span> <span data-ttu-id="44af2-110">Обратите внимание, что этот конкретный файл ACF имеет пустое тело.</span><span class="sxs-lookup"><span data-stu-id="44af2-110">Notice that this particular ACF file has an empty body.</span></span>

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

<span data-ttu-id="44af2-111">Компилятор MIDL имеет параметр [**/АПП \_ config**](/windows/desktop/Midl/-app-config), который позволяет включать в IDL определенные атрибуты ACF, например **неявные \_ маркеры**, а не создавать отдельные файлы ACF.</span><span class="sxs-lookup"><span data-stu-id="44af2-111">The MIDL compiler has an option, [**/app\_config**](/windows/desktop/Midl/-app-config), that lets you include certain ACF attributes, such as **implicit\_handle**, in the IDL file, rather than creating a separate ACF file.</span></span> <span data-ttu-id="44af2-112">Рассмотрите возможность использования этого параметра, если приложению не требуется много специальной конфигурации и если использование совместимость не является проблемой.</span><span class="sxs-lookup"><span data-stu-id="44af2-112">Consider using this option if your application doesn't require a lot of special configuration and if strict OSF compatibility is not an issue.</span></span>

 

 