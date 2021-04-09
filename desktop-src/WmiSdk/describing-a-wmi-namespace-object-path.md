---
description: Путь к объекту пространства имен описывает расположение определенного пространства имен на сервере. Путь к объекту пространства имен содержит элементы Server и Namespace и форматируется с использованием прямой или обратной косой черты.
ms.assetid: 6d8da19e-0914-4267-870e-c203176b895e
ms.tgt_platform: multiple
title: Описание пути к объекту пространства имен WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586104a1c193f1c229b0fbb27437d22e3686585b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080586"
---
# <a name="describing-a-wmi-namespace-object-path"></a><span data-ttu-id="79ac1-104">Описание пути к объекту пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="79ac1-104">Describing a WMI Namespace Object Path</span></span>

<span data-ttu-id="79ac1-105">Путь к объекту пространства имен описывает расположение определенного пространства имен на сервере.</span><span class="sxs-lookup"><span data-stu-id="79ac1-105">A namespace object path describes the location of a particular namespace on a server.</span></span> <span data-ttu-id="79ac1-106">Путь к объекту пространства имен содержит элементы Server и Namespace и форматируется с использованием прямой или обратной косой черты.</span><span class="sxs-lookup"><span data-stu-id="79ac1-106">A namespace object path contains server and namespace elements, and is formatted using either forward or backward slashes.</span></span>

<span data-ttu-id="79ac1-107">Элемент Server указывает сетевое имя компьютера, на котором размещается пространство имен, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="79ac1-107">The server element specifies the network name of the computer that is hosting the namespace, as shown in the following example.</span></span>

``` syntax
\\Server\Namespace
```

<span data-ttu-id="79ac1-108">\- или -</span><span class="sxs-lookup"><span data-stu-id="79ac1-108">\- or -</span></span>

``` syntax
//Server/Namespace
```

<span data-ttu-id="79ac1-109">Если сервер является локальным компьютером, используйте одну точку вместо имени сервера, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="79ac1-109">If the server is the local computer, use a single dot instead of the server name, as shown in the following example.</span></span>

``` syntax
\\.\Namespace
```

<span data-ttu-id="79ac1-110">Элемент namespace указывает любое допустимое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="79ac1-110">The namespace element specifies any valid namespace.</span></span> <span data-ttu-id="79ac1-111">Пространство имен представлено иерархической строкой, содержащей элементы, разделенные одинарными косыми чертами, такими как root \\ CIMV2.</span><span class="sxs-lookup"><span data-stu-id="79ac1-111">A namespace is represented with a hierarchical string containing elements delimited by single backslashes, such as root\\cimv2.</span></span> <span data-ttu-id="79ac1-112">Нельзя использовать косую черту в именах пространств имен.</span><span class="sxs-lookup"><span data-stu-id="79ac1-112">You cannot use forward slashes within namespace names.</span></span>

 

 



