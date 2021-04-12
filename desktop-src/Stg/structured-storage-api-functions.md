---
title: Функции API структурированного хранилища
description: Некоторые функции API для структурированного хранилища представляют собой вспомогательные функции, выполняющие последовательность вызовов других функций API и методов интерфейса. Эти вспомогательные функции можно использовать в качестве коротких вырезанией.
ms.assetid: 99ac66bc-db73-4811-9a39-fc49bb90ada8
keywords:
- Структурированное хранилище Стрктд STG, основы, функции API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df87e8c5910c6da23ca518d05541a69e7070f8bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328760"
---
# <a name="structured-storage-api-functions"></a><span data-ttu-id="9a4dd-105">Функции API структурированного хранилища</span><span class="sxs-lookup"><span data-stu-id="9a4dd-105">Structured Storage API Functions</span></span>

<span data-ttu-id="9a4dd-106">Некоторые функции API для структурированного хранилища представляют собой вспомогательные функции, выполняющие последовательность вызовов других функций API и методов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-106">Some of the API functions for structured storage are helper functions that perform a sequence of calls to other API functions and interface methods.</span></span> <span data-ttu-id="9a4dd-107">Эти вспомогательные функции можно использовать в качестве коротких вырезанией.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-107">You can use these helper functions as short cuts.</span></span>

<span data-ttu-id="9a4dd-108">Другие функции API предоставляют доступ к реализации структурированных файлов в модели COM.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-108">Other API functions provide access to COM's implementation of structured storage, Compound Files.</span></span>

<span data-ttu-id="9a4dd-109">Еще один набор функций API позволяет преобразовывать объекты OLE 1 в структурированное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-109">Still another set of API functions enable you to convert OLE 1 objects to structured storage.</span></span> <span data-ttu-id="9a4dd-110">Эти функции можно использовать для определения того, относится ли класс объекта к OLE 1 и для преобразования объектов между OLE 1 и текущим форматом хранения COM.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-110">You can use these functions to determine whether an object class is from OLE 1 and to convert objects between OLE 1 and current COM storage formats.</span></span>

<span data-ttu-id="9a4dd-111">Наконец, существуют функции API для преобразования и эмуляции других объектов.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-111">Finally, there are API functions for converting and emulating other objects.</span></span> <span data-ttu-id="9a4dd-112">Эти функции предоставляют службы для одного серверного приложения для работы с данными из другого приложения.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-112">These functions provide services for one server application to work with data from another application.</span></span> <span data-ttu-id="9a4dd-113">Данные можно преобразовать в собственный формат серверного приложения, считывая данные из исходного формата, но записывая их в собственном формате приложения объекта.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-113">The data can be converted to the native format of the server application by reading the data from its original format but writing it in the native format of the object application.</span></span> <span data-ttu-id="9a4dd-114">Данные могут оставаться в исходном формате, в то время как серверное приложение считывает и записывает данные в исходном формате.</span><span class="sxs-lookup"><span data-stu-id="9a4dd-114">Or the data can remain in its original format while the server application both reads and writes the data in its original format.</span></span>

<span data-ttu-id="9a4dd-115">Дополнительные сведения см. в следующих разделах: [структурированные режимы доступа к хранилищу](structured-storage-access-modes.md).</span><span class="sxs-lookup"><span data-stu-id="9a4dd-115">For more information, see the following section [Structured Storage Access Modes](structured-storage-access-modes.md).</span></span>

 

 




