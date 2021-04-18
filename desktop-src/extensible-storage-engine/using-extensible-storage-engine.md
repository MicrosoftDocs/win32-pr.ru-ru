---
description: 'Дополнительные сведения о: использование расширенного подсистемы хранилища'
title: Использование расширенного подсистемы хранилища
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 636c3fa96692b8c48f9a175b5fa7d34c53314e1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711578"
---
# <a name="using-extensible-storage-engine"></a><span data-ttu-id="d744e-103">Использование расширенного подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="d744e-103">Using Extensible Storage Engine</span></span>


<span data-ttu-id="d744e-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d744e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="using-extensible-storage-engine"></a><span data-ttu-id="d744e-105">Использование расширенного подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="d744e-105">Using Extensible Storage Engine</span></span>

<span data-ttu-id="d744e-106">В этом разделе содержатся общие сведения об использовании следующих частей API ESE.</span><span class="sxs-lookup"><span data-stu-id="d744e-106">This section contains general information about how to use the following parts of the ESE API.</span></span>

  - [<span data-ttu-id="d744e-107">Столбцы</span><span class="sxs-lookup"><span data-stu-id="d744e-107">Columns</span></span>](./columns.md)

  - [<span data-ttu-id="d744e-108">Индексирование в таблице</span><span class="sxs-lookup"><span data-stu-id="d744e-108">Indexing in the Table</span></span>](./indexing-in-the-table.md)

  - [<span data-ttu-id="d744e-109">Создание баз данных</span><span class="sxs-lookup"><span data-stu-id="d744e-109">Creating Databases</span></span>](./creating-databases.md)

  - [<span data-ttu-id="d744e-110">Транзакции</span><span class="sxs-lookup"><span data-stu-id="d744e-110">Transactions</span></span>](./transactions.md)

  - [<span data-ttu-id="d744e-111">Ошибки ESE</span><span class="sxs-lookup"><span data-stu-id="d744e-111">ESE Errors</span></span>](./extensible-storage-engine-errors.md)

  - [<span data-ttu-id="d744e-112">Файлы ESE</span><span class="sxs-lookup"><span data-stu-id="d744e-112">ESE Files</span></span>](./extensible-storage-engine-files.md)

<span data-ttu-id="d744e-113">Исходные файлы программы должны включать заголовочный файл ESENT. h для доступа к прототипам функций и определения структур для API-интерфейса расширенного подсистемы хранилища.</span><span class="sxs-lookup"><span data-stu-id="d744e-113">Your program source files should include the esent.h header file to access function prototypes and structure definitions for the Extensible Storage Engine API.</span></span> <span data-ttu-id="d744e-114">Разработчики могут использовать файл библиотеки ESENT. lib для создания приложений, использующих API подсистемы расширенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="d744e-114">Developers can use the esent.lib library file to build applications that use the Extensible Storage Engine API.</span></span> <span data-ttu-id="d744e-115">Во время выполнения приложения связываются с esent.dll.</span><span class="sxs-lookup"><span data-stu-id="d744e-115">At runtime, applications link to the esent.dll.</span></span>
