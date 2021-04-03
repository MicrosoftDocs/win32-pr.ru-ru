---
description: Блок среды потока (заметки об отладке)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Блок среды потока (заметки об отладке)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895910"
---
# <a name="thread-environment-block-debugging-notes"></a>Блок среды потока (заметки об отладке)

Блок среды потока ([**Структура Теб**](/windows/win32/api/winternl/ns-winternl-teb)) содержит сведения о контексте для потока.

В следующих версиях Windows смещение 32-разрядного адреса ТЕБ в 64-бит ТЕБ равно 0. Это можно использовать для прямого доступа к 32-разрядному ТЕБ потока WOW64. Это может измениться в более поздних версиях Windows



|               |                        |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Структуры отладки](debugging-structures.md)
</dt> <dt>

[**\_Контекст WOW64**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
