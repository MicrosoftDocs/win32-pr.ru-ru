---
description: Приложение может распаковать несколько файлов с помощью функций Лзопенфиле, Лзкопи и Лзклосе.
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: Распаковка нескольких файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683187"
---
# <a name="decompressing-multiple-files"></a><span data-ttu-id="c7be5-103">Распаковка нескольких файлов</span><span class="sxs-lookup"><span data-stu-id="c7be5-103">Decompressing Multiple Files</span></span>

<span data-ttu-id="c7be5-104">Приложение может распаковать несколько файлов, выполнив следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="c7be5-104">An application can decompress multiple files by performing the following tasks:</span></span>

1.  <span data-ttu-id="c7be5-105">Откройте исходные файлы, вызвав функцию [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="c7be5-105">Open the source files by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="c7be5-106">Откройте файлы назначения, вызвав [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="c7be5-106">Open the destination files by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="c7be5-107">Скопируйте исходные файлы в файлы назначения, вызвав функцию [**лзкопи**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .</span><span class="sxs-lookup"><span data-stu-id="c7be5-107">Copy the source files to the destination files by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function.</span></span>
4.  <span data-ttu-id="c7be5-108">Закройте файлы, вызвав функцию [**лзклосе**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="c7be5-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



