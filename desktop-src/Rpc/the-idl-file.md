---
title: IDL-файл
description: IDL-файл состоит из одного или нескольких определений интерфейса, каждый из которых имеет заголовок и текст.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487809"
---
# <a name="the-idl-file"></a><span data-ttu-id="e7906-103">IDL-файл</span><span class="sxs-lookup"><span data-stu-id="e7906-103">The IDL File</span></span>

<span data-ttu-id="e7906-104">IDL-файл состоит из одного или нескольких определений интерфейса, каждый из которых имеет заголовок и текст.</span><span class="sxs-lookup"><span data-stu-id="e7906-104">The IDL file consists of one or more interface definitions, each of which has a header and a body.</span></span> <span data-ttu-id="e7906-105">Заголовок содержит сведения, относящиеся ко всему интерфейсу, например UUID.</span><span class="sxs-lookup"><span data-stu-id="e7906-105">The header contains information that applies to the entire interface, such as the UUID.</span></span> <span data-ttu-id="e7906-106">Эти сведения заключены в квадратные скобки, за которыми следует ключевое слово **Interface** и имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e7906-106">This information is enclosed in square brackets and is followed by the keyword **interface** and the interface name.</span></span> <span data-ttu-id="e7906-107">Текст содержит определения типов данных в стиле C и прототипы функций, дополненные атрибутами, описывающими передачу данных по сети.</span><span class="sxs-lookup"><span data-stu-id="e7906-107">The body contains C-style data type definitions and function prototypes, augmented with attributes that describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="e7906-108">В этом примере заголовок интерфейса содержит только UUID и номер версии.</span><span class="sxs-lookup"><span data-stu-id="e7906-108">In this example, the interface header contains only the UUID and the version number.</span></span> <span data-ttu-id="e7906-109">Номер версии гарантирует, что при наличии нескольких версий интерфейса RPC будут подключены только совместимые версии клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="e7906-109">The version number ensures that when there are multiple versions of an RPC interface, only compatible versions of the client and server will be connected.</span></span>

<span data-ttu-id="e7906-110">Тело интерфейса содержит прототип функции для **хеллопрок**.</span><span class="sxs-lookup"><span data-stu-id="e7906-110">The interface body contains the function prototype for **HelloProc**.</span></span> <span data-ttu-id="e7906-111">В этом прототипе параметр функции Псзстринг имеет атрибуты **\[** [**в**](/windows/desktop/Midl/in) **\]** и **\[** [**String**](/windows/desktop/Midl/string) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e7906-111">In this prototype, the function parameter pszString has the attributes **\[**[**in**](/windows/desktop/Midl/in)**\]** and **\[**[**string**](/windows/desktop/Midl/string)**\]**.</span></span> <span data-ttu-id="e7906-112">Атрибут **\[ in \]** сообщает библиотеке времени выполнения о том, что параметр передается только от клиента серверу.</span><span class="sxs-lookup"><span data-stu-id="e7906-112">The **\[in\]** attribute tells the run-time library that the parameter is passed only from the client to the server.</span></span> <span data-ttu-id="e7906-113">Атрибут **\[ String \]** указывает, что заглушка должна рассматривать параметр как строку символов в стиле C.</span><span class="sxs-lookup"><span data-stu-id="e7906-113">The **\[string\]** attribute specifies that the stub should treat the parameter as a C-style character string.</span></span>

<span data-ttu-id="e7906-114">Клиентское приложение должно иметь возможность завершить работу серверного приложения, поэтому интерфейс содержит прототип для другой удаленной функции (**Shutdown** ), который будет реализован далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="e7906-114">The client application should be able to shut down the server application, so the interface contains a prototype for another remote function,**Shutdown** , that will be implemented later in this tutorial.</span></span>

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 