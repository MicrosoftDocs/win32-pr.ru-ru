---
title: Создание файла или обработчика потока
description: Создание файла или обработчика потока
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067839"
---
# <a name="creating-a-file-or-stream-handler"></a><span data-ttu-id="dbc16-103">Создание файла или обработчика потока</span><span class="sxs-lookup"><span data-stu-id="dbc16-103">Creating a File or Stream Handler</span></span>

<span data-ttu-id="dbc16-104">В приложении, написанном на языке C, обработчик файлов или потоков обычно создает функцию для каждого метода.</span><span class="sxs-lookup"><span data-stu-id="dbc16-104">In an application written in the C programming language, a file or stream handler usually creates a function for each method.</span></span> <span data-ttu-id="dbc16-105">Приложение обращается к этим функциям через массив указателей функций, создаваемых обработчиком потока.</span><span class="sxs-lookup"><span data-stu-id="dbc16-105">Your application accesses these functions through an array of function pointers the stream handler creates.</span></span> <span data-ttu-id="dbc16-106">Структура **иавистреамвтбл** содержит массив указателей функций.</span><span class="sxs-lookup"><span data-stu-id="dbc16-106">An **IAVIStreamVtbl** structure contains the array of function pointers.</span></span> <span data-ttu-id="dbc16-107">Обработчик потока может назначить любое имя, которое он хочет создать для методов.</span><span class="sxs-lookup"><span data-stu-id="dbc16-107">A stream handler can assign any name it wants to functions it creates for the methods.</span></span> <span data-ttu-id="dbc16-108">Расположение указателя функции в структуре подразумевает соответствие функции методу.</span><span class="sxs-lookup"><span data-stu-id="dbc16-108">The position of the function pointer in the structure implies the correspondence of the function to the method.</span></span> <span data-ttu-id="dbc16-109">Например, первый указатель функции в структуре соответствует методу **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="dbc16-109">For example, the first function pointer in the structure corresponds to the **QueryInterface** method.</span></span> <span data-ttu-id="dbc16-110">Обработчик потоков должен предоставлять все функции интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dbc16-110">Your stream handler must provide all the functions of an interface.</span></span>

 

 




