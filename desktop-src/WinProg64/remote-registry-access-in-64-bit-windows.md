---
title: Удаленный доступ к реестру в 64-разрядной версии Windows
description: Перенаправитель реестра обеспечивает удаленный доступ к реестру в 64-разрядной системе Windows с помощью функции Регконнектрегистри.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- удаленный доступ к реестру 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691514"
---
# <a name="remote-registry-access-in-64-bit-windows"></a>Удаленный доступ к реестру в 64-разрядной версии Windows

Перенаправитель реестра обеспечивает удаленный доступ к реестру в 64-разрядной системе Windows с помощью функции [**регконнектрегистри**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .

Если клиент является 32-битным приложением, он обращается к представлению реестра по умолчанию в 32-битном сервере. Если клиент является 64-битным приложением, он обращается к представлению реестра с 64-битным реестром.

**Windows Server 2003:** Все клиенты получают доступ к 64-разрядному представлению реестра, если только приложение не использует \_ \_ флаг WOW64 32KEY. Такое поведение изменилось при использовании Windows Server 2003 с пакетом обновления 1 (SP1) и Windows XP Professional x64 Edition при условии, что клиент и сервер работают под управлением этих версий Windows.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Перенаправитель реестра](registry-redirector.md)
</dt> <dt>

[Отражение реестра](registry-reflection.md)
</dt> </dl>

 

 