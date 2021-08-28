---
description: Блок среды потока (заметки об отладке)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Блок среды потока (заметки об отладке)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f5c40b2a64eb868a7fd3ffb2052a3692db90f19d33357d4ef4f3113803bf52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655274"
---
# <a name="thread-environment-block-debugging-notes"></a>Блок среды потока (заметки об отладке)

Блок среды потока ([**Структура Теб**](/windows/win32/api/winternl/ns-winternl-teb)) содержит сведения о контексте для потока.

в следующих версиях Windows смещение 32-разрядного адреса теб в 64-bit теб равно 0. Это можно использовать для прямого доступа к 32-разрядному ТЕБ потока WOW64. Это может измениться в более поздних версиях Windows



|  Платформа     | Версия                |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Структуры отладки](debugging-structures.md)
</dt> <dt>

[**\_Контекст WOW64**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
