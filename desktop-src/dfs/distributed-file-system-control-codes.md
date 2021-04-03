---
title: Коды управления распределенная файловая система
description: распределенная файловая система управляющих кодов DFS
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe054f87210c40da595dd731b263c485311729a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987640"
---
# <a name="distributed-file-system-control-codes"></a>Коды управления распределенная файловая система

Ниже приведены коды управления распределенная файловая система (DFS):

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

Код элемента управления [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) может получить те же сведения, что и функция [**нетдфсжетклиентинфо**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , но может обеспечить лучшую производительность в некоторых конфигурациях с высокой задержкой для серверов DFS. Не рекомендуется использовать управляющий код **FSCTL_DFS_GET_PKT_ENTRY_STATE** , если нет проблем с производительностью.

Чтобы выполнить эту операцию, вызовите функцию [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

</dd> </dl>