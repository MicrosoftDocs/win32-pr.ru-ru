---
title: Оптимизация составных файлов
description: Асинхронное хранилище позволяет приложениям точно разформатировать составные файлы, чтобы данные были доступны в том порядке, в котором они понадобятся приложениям.
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- Оптимизация составных файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb55d4d9ba7b264c1a0aac4252d879a7ba98b6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773736"
---
# <a name="compound-file-optimization"></a><span data-ttu-id="d4d9d-104">Оптимизация составных файлов</span><span class="sxs-lookup"><span data-stu-id="d4d9d-104">Compound File Optimization</span></span>

<span data-ttu-id="d4d9d-105">Асинхронное хранилище позволяет приложениям точно разформатировать составные файлы, чтобы данные были доступны в том порядке, в котором они понадобятся приложениям.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-105">Asynchronous storage enables applications to precisely layout compound files so that data is available in the order in which applications will require it.</span></span> <span data-ttu-id="d4d9d-106">Если приложению требуется только часть данных для вывода первой страницы информации, эти данные можно поместить в начало файла, даже если они логически находятся в конце потока.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-106">If an application requires only part of its data to display a first page of information, this data can be placed at the beginning of the file, even if it logically resides at the end of a stream.</span></span> <span data-ttu-id="d4d9d-107">Данные из разных потоков могут быть чередованием.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-107">Data from different streams can be interleaved.</span></span> <span data-ttu-id="d4d9d-108">Например, звуковые и видеоданные могут быть чередованием, чтобы последующие операции чтения получали оба одновременно, требования для мультимедийных приложений.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-108">Audio and video data, for example, can be interleaved so that subsequent read operations retrieve both simultaneously, a requirement for multimedia applications.</span></span>

<span data-ttu-id="d4d9d-109">Метод [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) можно использовать для размещения докфиле, что повышает производительность в большинстве сценариев.</span><span class="sxs-lookup"><span data-stu-id="d4d9d-109">[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) can be used to layout a docfile, thus improving performance in most scenarios.</span></span>

 

 




