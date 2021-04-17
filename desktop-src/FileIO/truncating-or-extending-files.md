---
description: Приложение может усечь или расширить файл путем вызова SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Усечение или расширение файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684190"
---
# <a name="truncating-or-extending-files"></a>Усечение или расширение файлов

Приложение может усечь или расширить файл путем вызова [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile). Эта функция задает маркер конца файла для текущей позиции указателя файла.

Обратите внимание, что при расширении файла содержимое между старым и новым расположениями в конце файла не определяется.

 

 



