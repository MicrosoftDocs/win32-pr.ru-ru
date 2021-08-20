---
description: Функция GetFileSize получает размер файла.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Определение размера файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf4185d0bb695d73dc3afd03bb1ee7d6fe95cf606960fbdc41c4ce0b33b732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150617"
---
# <a name="determining-the-size-of-a-file"></a>Определение размера файла

Функция [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) получает размер файла.

Поскольку реализация файлов в файловой системе NTFS позволяет использовать несколько потоков в файле, любое приложение, которое записывает доступ к файлам, должно учитывать возможность того, что создатель файла может включать в него несколько потоков. Если в файле не проверяются несколько потоков, приложение может недооценивать общий размер файла, помимо других ошибок.

 

 



