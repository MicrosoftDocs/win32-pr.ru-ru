---
description: Действие ExecuteAction инициирует последовательность выполнения с помощью свойства EXECUTEACTION, чтобы определить, какой тип установки необходимо выполнить.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Действие ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2970a0fb4e9297264071769ac7415cd2acf866b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497793"
---
# <a name="executeaction-action"></a>Действие ExecuteAction

Действие ExecuteAction инициирует последовательность выполнения с помощью свойства [**ExecuteAction**](executeaction.md) , чтобы определить, какой тип установки необходимо выполнить.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Это действие должно быть упорядочено после завершения всей сбора информации, необходимой для начала установки. Дополнительные действия могут быть упорядочены после действия ExecuteAction в [таблице инсталлуисекуенце](installuisequence-table.md)и в [таблице админуисекуенце](adminuisequence-table.md). Последовательность обычно начинается с действий по [*затратам*](c-gly.md) , например [действия костинитиализе](costinitialize-action.md), за которыми следуют действия пользовательского интерфейса, а затем действие ExecuteAction.

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

## <a name="remarks"></a>Комментарии

Действие ExecuteAction выполняется с системными привилегиями, если служба установщика включена. Действия верхнего уровня, такие как [действие установки](install-action.md), [действие объявления](advertise-action.md)и [Административное действие](admin-action.md) , включают внутреннюю логику, определяющую, требуется ли выполнение вызова действия ExecuteAction или последовательности выполнения или пользовательского интерфейса.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Таблица Инсталлуисекуенце](installuisequence-table.md)
</dt> <dt>

[Таблица Админуисекуенце](adminuisequence-table.md)
</dt> <dt>

[Действие Костинитиализе](costinitialize-action.md)
</dt> </dl>

 

 



