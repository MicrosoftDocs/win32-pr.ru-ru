---
title: Соглашения об именовании объектов хранилища
description: Объекты хранилища и потока называются в соответствии с набором соглашений.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Структурированное хранилище Стрктд STG, основы, соглашения об именовании объектов хранилища
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410689"
---
# <a name="storage-object-naming-conventions"></a><span data-ttu-id="b58cb-104">Соглашения об именовании объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="b58cb-104">Storage Object Naming Conventions</span></span>

<span data-ttu-id="b58cb-105">Объекты хранилища и потока называются в соответствии с набором соглашений.</span><span class="sxs-lookup"><span data-stu-id="b58cb-105">Storage and stream objects are named according to a set of conventions.</span></span>

<span data-ttu-id="b58cb-106">Имя корневого объекта хранилища — это фактическое имя файла в базовой файловой системе.</span><span class="sxs-lookup"><span data-stu-id="b58cb-106">The name of a root storage object is the actual name of the file in the underlying file system.</span></span> <span data-ttu-id="b58cb-107">Он соответствует правилам и ограничениям, которые накладывает файловая система.</span><span class="sxs-lookup"><span data-stu-id="b58cb-107">It conforms to the conventions and restrictions that the file system imposes.</span></span> <span data-ttu-id="b58cb-108">Строки имени файла, передаваемые методам и функциям, связанным с хранилищем, передаются в файловую систему с неинтерпретируемыми и без изменений.</span><span class="sxs-lookup"><span data-stu-id="b58cb-108">File name strings passed to storage-related methods and functions are passed on, uninterpreted and unchanged, to the file system.</span></span>

<span data-ttu-id="b58cb-109">Имя вложенного элемента, содержащегося в объекте хранилища, управляется реализацией конкретного объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="b58cb-109">The name of a nested element contained within a storage object is managed by the implementation of the particular storage object.</span></span> <span data-ttu-id="b58cb-110">Все реализации объектов хранилища должны поддерживать имена вложенных элементов 32 символов (включая знак завершения **null** ), хотя некоторые реализации могут поддерживать более длинные имена.</span><span class="sxs-lookup"><span data-stu-id="b58cb-110">All implementations of storage objects must support nested element names 32 characters in length (including the **NULL** terminator), although some implementations might support longer names.</span></span> <span data-ttu-id="b58cb-111">Выполняется ли преобразование регистра для объекта хранилища, определяется реализацией.</span><span class="sxs-lookup"><span data-stu-id="b58cb-111">Whether the storage object does any case conversion is implementation-defined.</span></span> <span data-ttu-id="b58cb-112">В результате приложения, определяющие имена элементов, должны выбирать имена, которые приемлемы независимо от того, выполняется преобразование регистра или нет.</span><span class="sxs-lookup"><span data-stu-id="b58cb-112">As a result, applications that define element names must choose names that are acceptable whether or not case conversion is performed.</span></span> <span data-ttu-id="b58cb-113">Реализация COM-реализации составных файлов поддерживает имена с максимальной длиной 32 символов и не выполняет преобразование регистра.</span><span class="sxs-lookup"><span data-stu-id="b58cb-113">The COM implementation of compound files supports names with a maximum length of 32 characters, and does not perform any case conversion.</span></span>

 

 




