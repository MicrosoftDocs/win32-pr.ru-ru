---
title: Составные файлы
description: Несмотря на то, что можно реализовать собственные структурированные объекты хранения и интерфейсы, COM предоставляет стандартную реализацию, называемую составными файлами.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252888"
---
# <a name="compound-files"></a><span data-ttu-id="9c61a-103">Составные файлы</span><span class="sxs-lookup"><span data-stu-id="9c61a-103">Compound Files</span></span>

<span data-ttu-id="9c61a-104">Несмотря на то, что можно реализовать собственные структурированные объекты хранения и интерфейсы, COM предоставляет стандартную реализацию, называемую составными файлами.</span><span class="sxs-lookup"><span data-stu-id="9c61a-104">Although you can implement your own structured storage objects and interfaces, COM provides a standard implementation called Compound Files.</span></span> <span data-ttu-id="9c61a-105">Использование составных файлов позволяет сэкономить на написании кода собственной реализации структурированного хранилища и предоставляет несколько дополнительных преимуществ, полученных от применения к определенному стандарту.</span><span class="sxs-lookup"><span data-stu-id="9c61a-105">Using Compound Files saves you the work of coding your own implementation of structured storage and confers several additional benefits derived from adhering to a defined standard.</span></span> <span data-ttu-id="9c61a-106">К таким преимуществам относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="9c61a-106">These benefits include the following:</span></span>

-   <span data-ttu-id="9c61a-107">**Независимость от файловой системы и платформы**.</span><span class="sxs-lookup"><span data-stu-id="9c61a-107">**File-system and platform independence**.</span></span> <span data-ttu-id="9c61a-108">Поскольку реализация составных файлов COM выполняется поверх существующих неструктурированных систем, составные файлы, хранящиеся в файловой системе FAT, файловой системе NTFS или файловых системах Macintosh, могут быть открыты приложениями, использующими любую из других файловых систем.</span><span class="sxs-lookup"><span data-stu-id="9c61a-108">Because COM's Compound Files implementation runs on top of existing flat-file systems, compound files stored in the FAT file system, NTFS file system, or Macintosh file systems can be opened by applications using any one of the other file systems.</span></span>
-   <span data-ttu-id="9c61a-109">С **возможностью поиска**.</span><span class="sxs-lookup"><span data-stu-id="9c61a-109">**Searchable**.</span></span> <span data-ttu-id="9c61a-110">Поскольку отдельные объекты в составном файле сохраняются в стандартном формате и доступны с помощью стандартных интерфейсов COM и интерфейсов API, любая служебная программа браузера, использующая эти интерфейсы и API-интерфейсы, может содержать список объектов в файле, даже если данные внутри данного объекта могут быть в собственном формате.</span><span class="sxs-lookup"><span data-stu-id="9c61a-110">Because the separate objects in a compound file are saved in a standard format and can be accessed using standard COM interfaces and APIs, any browser utility using these interfaces and APIs can list the objects in the file, even though data within a given object may be in a proprietary format.</span></span>
-   <span data-ttu-id="9c61a-111">**Доступ к определенным внутренним данным**.</span><span class="sxs-lookup"><span data-stu-id="9c61a-111">**Access to certain internal data**.</span></span> <span data-ttu-id="9c61a-112">Поскольку реализация составных файлов предоставляет стандартные способы записи определенных типов данных, то, например, сводные данные, приложения могут считывать эти данные с помощью интерфейсов COM и интерфейсов API.</span><span class="sxs-lookup"><span data-stu-id="9c61a-112">Because the Compound Files implementation provides standard ways of writing certain types of data—summary information, for example—applications can read this data using COM interfaces and APIs.</span></span>

 

 




