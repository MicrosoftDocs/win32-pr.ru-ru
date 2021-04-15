---
description: Windows использует указатель на файл для хранения прочитанных или записанных байтов.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Размещение указателя на файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6588a3d65e71c2180c4e9753e65cd94ed070d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683444"
---
# <a name="positioning-a-file-pointer"></a>Размещение указателя на файл

Когда приложение вызывает [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) для открытия файла в первый раз, Windows помещает [указатель файла](file-pointers.md) в начало файла. Так как байты считываются из файла или записываются в файл, Windows увеличивает указатель файла на число считанных или записанных байтов.

Приложение может поместить указатель файла в указанное смещение, вызвав [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).

Функция [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) может также использоваться для запроса текущей позиции указателя файла путем указания метода Move **файла \_ Current** и расстояния от нуля.

 

 



