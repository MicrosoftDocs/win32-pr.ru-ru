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
# <a name="decompressing-a-single-file"></a>Распаковка одного файла

Приложение может распаковать один сжатый файл, выполнив следующие задачи:

1.  Откройте исходный файл, вызвав функцию [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .
2.  Откройте целевой файл, вызвав [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Скопируйте исходный файл в целевой файл, вызвав функцию [**лзкопи**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) и передав дескрипторы, возвращенные [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
4.  Закройте файлы, вызвав функцию [**лзклосе**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .

 

 



