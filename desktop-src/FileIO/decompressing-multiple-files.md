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
# <a name="decompressing-multiple-files"></a>Распаковка нескольких файлов

Приложение может распаковать несколько файлов, выполнив следующие задачи:

1.  Откройте исходные файлы, вызвав функцию [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .
2.  Откройте файлы назначения, вызвав [**лзопенфиле**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Скопируйте исходные файлы в файлы назначения, вызвав функцию [**лзкопи**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .
4.  Закройте файлы, вызвав функцию [**лзклосе**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .

 

 



