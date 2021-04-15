---
description: Приложение может распаковать один сжатый файл с помощью функций Лзопенфиле, Лзкопи и Лзклосе.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Распаковка одного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8da6ee4ee80e42d6ff70c3d9c50efdc572f97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683190"
---
# <a name="decompressing-a-single-file"></a><span data-ttu-id="d6f4e-103">Распаковка одного файла</span><span class="sxs-lookup"><span data-stu-id="d6f4e-103">Decompressing a Single File</span></span>

<span data-ttu-id="d6f4e-104">Приложение может распаковать один сжатый файл, выполнив следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="d6f4e-104">An application can decompress a single compressed file by performing the following tasks:</span></span>

1.  <span data-ttu-id="d6f4e-105">Откройте исходный файл, вызвав функцию [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .</span><span class="sxs-lookup"><span data-stu-id="d6f4e-105">Open the source file by calling the [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) function.</span></span>
2.  <span data-ttu-id="d6f4e-106">Откройте целевой файл, вызвав [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="d6f4e-106">Open the destination file by calling [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
3.  <span data-ttu-id="d6f4e-107">Скопируйте исходный файл в целевой файл, вызвав функцию [**лзкопи**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) и передав дескрипторы, возвращенные [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span><span class="sxs-lookup"><span data-stu-id="d6f4e-107">Copy the source file to the destination file by calling the [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) function and passing the handles returned by [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).</span></span>
4.  <span data-ttu-id="d6f4e-108">Закройте файлы, вызвав функцию [**лзклосе**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .</span><span class="sxs-lookup"><span data-stu-id="d6f4e-108">Close the files by calling the [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) function.</span></span>

 

 



