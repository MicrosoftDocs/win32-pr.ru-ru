---
title: InprocHandler32
description: Указывает, использует ли приложение пользовательский обработчик.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- COM раздела реестра InprocHandler32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410724"
---
# <a name="inprochandler32"></a>InprocHandler32

Указывает, использует ли приложение пользовательский обработчик.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** , указывающее настраиваемый обработчик, используемый приложением. Если пользовательский обработчик не используется, для записи следует задать значение Ole32.dll.

Если контейнер выполняет поиск пользовательского обработчика в реестре, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**инпрочандлер**](inprochandler.md)
</dt> </dl>

 

 




