---
title: Создание кодов Four-Character
description: Создание кодов Four-Character
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- Ввод-вывод файлов мультимедиа, коды из четырех символов
- Ввод-вывод в файл, коды из четырех символов
- Ввод и вывод (I/O), коды из четырех символов
- Ввод-вывод (ввод и вывод), коды из четырех символов
- коды из четырех символов
- Функция Ммиострингтофауркк
- макрос Ммиофауркк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789991"
---
# <a name="generating-four-character-codes"></a>Создание кодов Four-Character

Для создания четырех кодов символов можно использовать макрос [**ммиофауркк**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) или функцию [**ммиострингтофауркк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) . В следующем примере используется **ммиофауркк** для создания кода с четырьмя символами для "Wave".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



В следующем примере используется [**ммиострингтофауркк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) для создания кода с четырьмя символами для "Wave".


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



Второй параметр в [**ммиострингтофауркк**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) указывает флаги для преобразования строки в код из четырех символов. При указании \_ флага MMIO **ммиострингтофауркк** преобразует все буквы в строке в верхний регистр. Это полезно, если необходимо указать код из четырех символов для идентификации пользовательской процедуры ввода-вывода, так как в четырех кодах символов, идентифицирующих имена файлов, должно быть задано все прописные буквы.

 

 