---
title: инпрочандлер
description: Указывает, использует ли приложение пользовательский обработчик.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- COM раздела реестра Инпрочандлер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c19089ece43496465351b44e9faa8793ba893
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411206"
---
# <a name="inprochandler"></a>инпрочандлер

Указывает, использует ли приложение пользовательский обработчик.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** , указывающее настраиваемый обработчик, используемый приложением. Если пользовательский обработчик не используется, для записи следует задать значение Ole32.dll.

Если контейнер выполняет поиск пользовательского обработчика в реестре, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




