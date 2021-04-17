---
description: Мфтраце — это средство для создания журналов трассировки для Media Foundation приложений.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: мфтраце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651655"
---
# <a name="mftrace"></a>мфтраце

Мфтраце — это средство для создания журналов трассировки для Media Foundation приложений.

## <a name="in-this-section"></a>Содержание раздела

-   [Использование Мфтраце](using-mftrace.md)
-   [Ключевые слова Мфтраце](mftrace-keywords.md)
-   [Файл конфигурации Мфтраце](mftrace-configuration-file.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия пакета SDK      | Пакет средств разработки программного обеспечения Microsoft Windows (SDK) для Windows 7 и платформа .NET Framework 4,0 |
| Минимальная операционная система | Windows Vista                                                                         |



 

Для Мфтраце требуются следующие библиотеки DLL, которые также предоставляются в пакете SDK.

-   detoured.dll
-   mfdetours.dll

Пакет SDK предоставляет как 32-разрядную, так и 64-разрядную версию Мфтраце. Мфтраце не поддерживает WOW64; для трассировки 32-разрядного процесса, выполняющегося в 64-разрядной версии Windows, используйте 32-bit Мфтраце.

пакет SDK-root на 32-разрядных системах: \Program Files\Windows Kits\10 SDK-root на 64 разрядной системе: \Program Files (x86) \Windows Kits\10 вы найдете мфтраце по адресу <SDK — root> \bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>См. также

<dl> <dt>

[Средства Media Foundation](media-foundation-tools.md)
</dt> </dl>

 

 



