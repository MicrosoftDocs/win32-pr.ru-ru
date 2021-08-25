---
description: Описывает схему разбивки на части для чтения или записи несмежных фрагментов данных за одну операцию.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Чтение или запись в файлы с помощью схемы Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc8a7ee9fcae2a54ac31c51a7c038e3d9442a6ccded2fc7dab916c7a6165a68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914484"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Чтение или запись в файлы с помощью схемы Scatter-Gather

Схема разбивки на части использует операционную систему для доставки в одной операции нескольких дискретных блоков данных (например, записей базы данных) из файла в отдельные несмежные буферы в памяти. Схема рассеивания также записывает данные из несмежных буферов за одну операцию.

Приложение может реализовать схему разбивки на области с помощью функций [**реадфилескаттер**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) и [**вритефилегасер**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) .

 

 



