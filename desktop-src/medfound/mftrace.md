---
description: Мфтраце — это средство для создания журналов трассировки для Media Foundation приложений.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: мфтраце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542ac9325b33fc8f1a76394d203dbf1d27919bd6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885227"
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
| Минимальная версия пакета SDK      | пакет средств разработки Microsoft Windows Software Development Kit (SDK) для Windows 7 и платформа .NET Framework 4,0 |
| Минимальная операционная система | Windows Vista                                                                         |



 

Для Мфтраце требуются следующие библиотеки DLL, которые также предоставляются в пакете SDK.

-   detoured.dll
-   mfdetours.dll

Пакет SDK предоставляет как 32-разрядную, так и 64-разрядную версию Мфтраце. Мфтраце не поддерживает WOW64; для трассировки 32-разрядного процесса, выполняемого на 64-разрядной Windows, используйте 32-bit версии мфтраце.

пакет sdk-root на 32-разрядных системах: \program files \ Windows Kits\10 sdk-root на 64 разрядной системе: \program files (x86) \ Windows Kits\10 вы найдете мфтраце в &lt; пакете sdk-root &gt; \bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Средства Media Foundation](media-foundation-tools.md)
</dt> </dl>

 

 



