---
description: Действие ExecuteAction инициирует последовательность выполнения с помощью свойства EXECUTEACTION, чтобы определить, какой тип установки необходимо выполнить.
ms.assetid: 61878317-ac87-4f6e-9375-12a78969e29e
title: Действие ExecuteAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20555af337f8774aec6c58769f2235da97ae763e044665e407a8dc29e75de750
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636891"
---
# <a name="executeaction-action"></a>Действие ExecuteAction

Действие ExecuteAction инициирует последовательность выполнения с помощью свойства [**ExecuteAction**](executeaction.md) , чтобы определить, какой тип установки необходимо выполнить.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Это действие должно быть упорядочено после завершения всей сбора информации, необходимой для начала установки. Дополнительные действия могут быть упорядочены после действия ExecuteAction в [таблице инсталлуисекуенце](installuisequence-table.md)и в [таблице админуисекуенце](adminuisequence-table.md). Последовательность обычно начинается с действий по [*затратам*](c-gly.md) , например [действия костинитиализе](costinitialize-action.md), за которыми следуют действия пользовательского интерфейса, а затем действие ExecuteAction.

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

## <a name="remarks"></a>Remarks

Действие ExecuteAction выполняется с системными привилегиями, если служба установщика включена. Действия верхнего уровня, такие как [действие установки](install-action.md), [действие объявления](advertise-action.md)и [Административное действие](admin-action.md) , включают внутреннюю логику, определяющую, требуется ли выполнение вызова действия ExecuteAction или последовательности выполнения или пользовательского интерфейса.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Таблица Инсталлуисекуенце](installuisequence-table.md)
</dt> <dt>

[Таблица Админуисекуенце](adminuisequence-table.md)
</dt> <dt>

[Действие Костинитиализе](costinitialize-action.md)
</dt> </dl>

 

 



