---
title: Файл WinNT ADsPath
description: В этом разделе содержатся примеры строк, используемых для файла WinNT ADsPath.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- Служба WinNT Service Provider ADSI, WinNT ADsPath
- ADsPath ADSI, WinNT, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986078"
---
# <a name="winnt-adspath"></a><span data-ttu-id="04fd0-105">Файл WinNT ADsPath</span><span class="sxs-lookup"><span data-stu-id="04fd0-105">WinNT ADsPath</span></span>

<span data-ttu-id="04fd0-106">Строка ADsPath для поставщика ADSI WinNT может быть одной из следующих форм:</span><span class="sxs-lookup"><span data-stu-id="04fd0-106">The ADsPath string for the ADSI WinNT provider can be one of the following forms:</span></span>


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



<span data-ttu-id="04fd0-107">Доменное имя может быть либо NETBIOS-именем, либо именем DNS.</span><span class="sxs-lookup"><span data-stu-id="04fd0-107">The domain name can be either a NETBIOS name or a DNS name.</span></span>

<span data-ttu-id="04fd0-108">Сервер — это имя определенного сервера в домене.</span><span class="sxs-lookup"><span data-stu-id="04fd0-108">The server is the name of a specific server within the domain.</span></span>

<span data-ttu-id="04fd0-109">Путь — это путь к объекту, например "printserver1/Printer2".</span><span class="sxs-lookup"><span data-stu-id="04fd0-109">The path is the path of on object, such as "printserver1/printer2".</span></span>

<span data-ttu-id="04fd0-110">Имя объекта — это имя определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="04fd0-110">The object name is the name of a specific object.</span></span>

<span data-ttu-id="04fd0-111">Класс объекта — это имя класса именованного объекта.</span><span class="sxs-lookup"><span data-stu-id="04fd0-111">The object class is the class name of the named object.</span></span> <span data-ttu-id="04fd0-112">Одним из примеров такого использования может быть «WinNT://MyServer/JeffSmith,user».</span><span class="sxs-lookup"><span data-stu-id="04fd0-112">One example of this usage would be "WinNT://MyServer/JeffSmith,user".</span></span> <span data-ttu-id="04fd0-113">Указание имени класса может повысить производительность операции привязки.</span><span class="sxs-lookup"><span data-stu-id="04fd0-113">Specifying a class name can improve the performance of the bind operation.</span></span>

 

 




