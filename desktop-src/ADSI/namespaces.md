---
title: Пространства имен
description: Объекты, находящиеся в заданном пространстве имен, идентифицируются по уникальному имени.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- пространства имен ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410599"
---
# <a name="namespaces"></a><span data-ttu-id="62e47-104">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="62e47-104">Namespaces</span></span>

<span data-ttu-id="62e47-105">Объекты, находящиеся в заданном пространстве имен, идентифицируются по уникальному имени.</span><span class="sxs-lookup"><span data-stu-id="62e47-105">Objects that reside within a given namespace are identified by a unique name.</span></span> <span data-ttu-id="62e47-106">Например, файлы, хранящиеся на диске компьютера, находятся в пространстве имен файловой системы.</span><span class="sxs-lookup"><span data-stu-id="62e47-106">For example, files stored on a PC disk drive reside in the file system namespace.</span></span> <span data-ttu-id="62e47-107">Уникальное имя файла основано на том, где он хранится в пространстве имен файловой системы.</span><span class="sxs-lookup"><span data-stu-id="62e47-107">The unique name of a file is based on where it is stored in the file system namespace.</span></span> <span data-ttu-id="62e47-108">Пример:</span><span class="sxs-lookup"><span data-stu-id="62e47-108">For example:</span></span>


```C++
C:\public\documents\adsi\adsi_spec.doc
```



<span data-ttu-id="62e47-109">Пространства имен службы каталогов также определяют объекты, которые они содержат, с помощью уникальных имен, которые обычно основаны на расположении в каталоге, где находится объект.</span><span class="sxs-lookup"><span data-stu-id="62e47-109">Directory service namespaces also identify the objects they contain by unique names which are usually based on the location in the directory where the object can be found.</span></span> <span data-ttu-id="62e47-110">Например, в каталоге X. 500 заданный объект может иметь такое имя:</span><span class="sxs-lookup"><span data-stu-id="62e47-110">For example, in an X.500 directory, a given object might have a name like this:</span></span>


```C++
CN=John,OU=Marketing,O=Fabrikam
```



<span data-ttu-id="62e47-111">Разные службы каталогов используют разные формы для именования объектов, которые они содержат.</span><span class="sxs-lookup"><span data-stu-id="62e47-111">Different directory services use different forms for naming the objects they contain.</span></span> <span data-ttu-id="62e47-112">Это затрудняет работу с разными пространствами имен, особенно для разработчиков, учитывая все среды, в которых может выполняться код.</span><span class="sxs-lookup"><span data-stu-id="62e47-112">This makes dealing with different namespaces challenging, especially for developers, considering all of the different environments on which the code might be running.</span></span>

<span data-ttu-id="62e47-113">Целью Active Directory интерфейсов служб (ADSI) является предоставление инфраструктуры именования, которая обеспечивает доступ к пространствам имен разных поставщиков служб каталогов.</span><span class="sxs-lookup"><span data-stu-id="62e47-113">A goal of Active Directory Service Interfaces (ADSI) is to provide a naming framework that allows access to namespaces of different directory service providers.</span></span>

<span data-ttu-id="62e47-114">ADSI определяет соглашение об именовании, которое может однозначно идентифицировать объект в разнородной среде.</span><span class="sxs-lookup"><span data-stu-id="62e47-114">ADSI defines a naming convention that can uniquely identify an object in a heterogeneous environment.</span></span> <span data-ttu-id="62e47-115">Эти имена называются «ADsPath строки».</span><span class="sxs-lookup"><span data-stu-id="62e47-115">These names are called ADsPath strings.</span></span> <span data-ttu-id="62e47-116">ADsPath строк имеют несколько форм:</span><span class="sxs-lookup"><span data-stu-id="62e47-116">ADsPath strings take several forms:</span></span>


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



<span data-ttu-id="62e47-117">Дополнительные форматы ADsPath могут быть представлены различными поставщиками ADSI (например, поставщиком ADSI для сервера службы IIS, который поддерживает Адспасс).</span><span class="sxs-lookup"><span data-stu-id="62e47-117">Additional ADsPath formats can be introduced by different ADSI providers (such as the ADSI provider for the Internet Information Services server, which support the "IIS://" ADsPaths).</span></span>

 

 




