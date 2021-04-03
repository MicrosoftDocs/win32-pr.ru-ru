---
title: Фиксированные массивы
description: Если интерфейс указывает массив с определенным количеством элементов в качестве параметра, используется фиксированный массив. При использовании MIDL вы определяете фиксированные массивы точно так же, как и в C. Укажите тип, имя и размер массива.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776967"
---
# <a name="fixed-arrays"></a><span data-ttu-id="5aca6-104">Фиксированные массивы</span><span class="sxs-lookup"><span data-stu-id="5aca6-104">Fixed Arrays</span></span>

<span data-ttu-id="5aca6-105">Если интерфейс указывает массив с определенным количеством элементов в качестве параметра, используется фиксированный массив.</span><span class="sxs-lookup"><span data-stu-id="5aca6-105">If your interface specifies an array with a specific number of elements as a parameter, it is using a fixed array.</span></span> <span data-ttu-id="5aca6-106">При использовании MIDL вы определяете фиксированные массивы точно так же, как и в C. Укажите тип, имя и размер массива.</span><span class="sxs-lookup"><span data-stu-id="5aca6-106">When using MIDL, you define fixed arrays in the same way you define them in C. You specify the array's type, name, and size.</span></span>

<span data-ttu-id="5aca6-107">В следующем примере показано, как определить фиксированный массив.</span><span class="sxs-lookup"><span data-stu-id="5aca6-107">The following example demonstrates how to define a fixed array.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="5aca6-108">Когда клиентская программа передает фиксированный массив в серверную программу, клиентская заглушка отправляет весь массив в заглушку сервера.</span><span class="sxs-lookup"><span data-stu-id="5aca6-108">When a client program passes a fixed array to a server program, the client stub sends the entire array to the server stub.</span></span> <span data-ttu-id="5aca6-109">Заглушка сервера выделяет память для массива и сохраняет данные массива, которые он получает по сети, в выделенную память.</span><span class="sxs-lookup"><span data-stu-id="5aca6-109">The server stub allocates memory for the array and stores the array data it receives across the network into the allocated memory.</span></span> <span data-ttu-id="5aca6-110">Затем он передает массив в удаленную процедуру на сервере.</span><span class="sxs-lookup"><span data-stu-id="5aca6-110">It then passes the array to the remote procedure on the server.</span></span> <span data-ttu-id="5aca6-111">Сервер может изменять данные в массиве.</span><span class="sxs-lookup"><span data-stu-id="5aca6-111">The server may modify the data in the array.</span></span>

<span data-ttu-id="5aca6-112">При завершении удаленной процедуры заглушка сервера отправляет содержимое массива обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="5aca6-112">When the remote procedure terminates, the server stub sends the contents of the array back to the client.</span></span> <span data-ttu-id="5aca6-113">Клиентская заглушка копирует полученные данные из серверной заглушки в исходный массив.</span><span class="sxs-lookup"><span data-stu-id="5aca6-113">The client stub copies the data it received from the server stub into the original array.</span></span> <span data-ttu-id="5aca6-114">Затем клиентская программа может использовать данные, как если бы они получали данные из локального вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="5aca6-114">The client program can then use the data as it would if it received the data from a local procedure call.</span></span>

 

 




