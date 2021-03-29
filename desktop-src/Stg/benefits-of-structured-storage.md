---
title: Преимущества структурированного хранилища
description: COM предоставляет набор служб, которые совместно называют структурированным хранилищем.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Структурированное хранилище Стрктд STG, преимущества
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773745"
---
# <a name="benefits-of-structured-storage"></a><span data-ttu-id="75ae6-104">Преимущества структурированного хранилища</span><span class="sxs-lookup"><span data-stu-id="75ae6-104">Benefits of Structured Storage</span></span>

<span data-ttu-id="75ae6-105">COM предоставляет набор служб, которые совместно называют структурированным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="75ae6-105">COM provides a set of services collectively called structured storage.</span></span> <span data-ttu-id="75ae6-106">Преимущество этих служб заключается в снижении потерь производительности и издержек, связанных с хранением отдельных объектов в неструктурированном файле.</span><span class="sxs-lookup"><span data-stu-id="75ae6-106">Among the benefits of these services is the reduction of performance penalties and overhead associated with storing separate objects in a flat file.</span></span> <span data-ttu-id="75ae6-107">Вместо неструктурированного файла COM хранит отдельные объекты в одном структурированном файле, состоящем из двух основных элементов: объектов хранилища и объектов потока.</span><span class="sxs-lookup"><span data-stu-id="75ae6-107">Instead of a flat file, COM stores the separate objects in a single, structured file consisting of two main elements: storage objects and stream objects.</span></span> <span data-ttu-id="75ae6-108">Вместе они работают как файловая система в файле.</span><span class="sxs-lookup"><span data-stu-id="75ae6-108">Together, they function like a file system within a file.</span></span>

<span data-ttu-id="75ae6-109">Структурированное хранилище позволяет решить проблемы с производительностью, избавляя от необходимости полностью перезаписывать файл в хранилище при добавлении нового объекта в составной файл или при увеличении размера существующего объекта.</span><span class="sxs-lookup"><span data-stu-id="75ae6-109">Structured storage solves performance problems by eliminating the need to totally rewrite a file to storage whenever a new object is added to a compound file, or an existing object increases in size.</span></span> <span data-ttu-id="75ae6-110">Новые данные записываются в следующее доступное место в постоянном хранилище, а объект хранилища обновляет таблицу указателей, которую он поддерживает, чтобы отследить расположение объектов хранилища и объекты потока.</span><span class="sxs-lookup"><span data-stu-id="75ae6-110">The new data is written to the next available location in permanent storage, and the storage object updates the table of pointers it maintains to track the locations of its storage objects and stream objects.</span></span> <span data-ttu-id="75ae6-111">В то же время структурированное хранилище позволяет конечным пользователям взаимодействовать с составным файлом и управлять им, как если бы он был отдельным файлом, а не вложенной иерархией отдельных объектов.</span><span class="sxs-lookup"><span data-stu-id="75ae6-111">At the same time, structured storage enables end users to interact and manage a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

<span data-ttu-id="75ae6-112">Структурированное хранилище также имеет и другие преимущества:</span><span class="sxs-lookup"><span data-stu-id="75ae6-112">Structured storage also has other benefits:</span></span>

-   <span data-ttu-id="75ae6-113">**Добавочный доступ**.</span><span class="sxs-lookup"><span data-stu-id="75ae6-113">**Incremental access**.</span></span> <span data-ttu-id="75ae6-114">Если пользователю требуется доступ к объекту в составном файле, пользователь может загрузить и сохранить только этот объект, а не весь файл.</span><span class="sxs-lookup"><span data-stu-id="75ae6-114">If a user needs access to an object within a compound file, the user can load and save only that object, rather than the entire file.</span></span>
-   <span data-ttu-id="75ae6-115">**Множественное использование**.</span><span class="sxs-lookup"><span data-stu-id="75ae6-115">**Multiple use**.</span></span> <span data-ttu-id="75ae6-116">Несколько конечных пользователей или приложений могут одновременно считывать и записывать данные в один и тот же составной файл.</span><span class="sxs-lookup"><span data-stu-id="75ae6-116">More than one end user or application can concurrently read and write information in the same compound file.</span></span>
-   <span data-ttu-id="75ae6-117">**Обработка транзакций**.</span><span class="sxs-lookup"><span data-stu-id="75ae6-117">**Transaction processing**.</span></span> <span data-ttu-id="75ae6-118">Пользователи могут выполнять чтение или запись в составные файлы COM в режиме транзакций, где изменения, вносимые в файл, помещаются в буфер и затем могут быть зафиксированы в файле или отменены.</span><span class="sxs-lookup"><span data-stu-id="75ae6-118">Users can read or write to COM compound files in transacted mode, where changes made to the file are buffered and can subsequently either be committed to the file or reversed.</span></span>
-   <span data-ttu-id="75ae6-119">**Сохранение нехватки памяти**.</span><span class="sxs-lookup"><span data-stu-id="75ae6-119">**Low-memory saves**.</span></span> <span data-ttu-id="75ae6-120">Структурированное хранилище предоставляет средства для сохранения файлов в ситуациях нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="75ae6-120">Structured storage provides facilities for saving files in low-memory situations.</span></span>

 

 




