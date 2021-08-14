---
description: Форматы расширений MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Форматы расширений MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a490c29c98b454b7d563e8af46131b040f123b9de2ef689ea5ede1a2ac100ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193960"
---
# <a name="mtp-extension-formats"></a>Форматы расширений MTP

Формат файла на устройстве можно описать с помощью значения GUID. Это значение задается \_ свойством "формат объекта WPD" \_ .

## <a name="vendor-extended-formats"></a>Поставщик — Расширенные форматы

Если производитель устройства поддерживает расширенный формат поставщика, его драйвер объединяет код формата поставщика (UINT16) с старшими 16 битами **\_ формата объекта WPD без \_ \_ указания** идентификатора GUID.

Например, если код, расширенный поставщиком, — 0xB001, то результирующий идентификатор GUID будет выглядеть так, как показано в следующем примере:


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поддержка расширений MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



