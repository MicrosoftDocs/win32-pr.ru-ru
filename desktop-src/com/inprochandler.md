---
title: инпрочандлер
description: Инпрочандлер указывает, использует ли приложение настраиваемый обработчик в HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID разделе реестра.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- COM раздела реестра Инпрочандлер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404737"
---
# <a name="inprochandler"></a>инпрочандлер

Указывает, использует ли приложение пользовательский обработчик.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ SZ** , указывающее настраиваемый обработчик, используемый приложением. Если пользовательский обработчик не используется, для записи следует задать значение Ole32.dll.

Если контейнер выполняет поиск пользовательского обработчика в реестре, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




