---
description: ICE84 проверяет таблицу Адвтексекутесекуенце, таблицу Админексекутесекуенце и таблицу Инсталлексекутесекуенце, чтобы убедиться, что следующие стандартные действия не были заданы с условиями в поле Condition.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347775"
---
# <a name="ice84"></a>ICE84

ICE84 проверяет таблицу [адвтексекутесекуенце](advtexecutesequence-table.md), [таблицу Админексекутесекуенце](adminexecutesequence-table.md)и таблицу [инсталлексекутесекуенце](installexecutesequence-table.md) , чтобы убедиться, что следующие [стандартные действия](standard-actions.md) не были заданы с условиями в поле Condition.

-   [Действие Костинитиализе](costinitialize-action.md)
-   [Действие Костфинализе](costfinalize-action.md)
-   [Действие Филекост](filecost-action.md)
-   [Действие Инсталлвалидате](installvalidate-action.md)
-   [Действие Инсталлинитиализе](installinitialize-action.md)
-   [Действие функции InstallFinalize](installfinalize-action.md)
-   [Действие Процесскомпонентс](processcomponents-action.md)
-   [Действие Публишфеатурес](publishfeatures-action.md)
-   [Действие Публишпродукт](publishproduct-action.md)
-   [Действие Регистерпродукт](registerproduct-action.md)
-   [Действие Унпублишфеатурес](unpublishfeatures-action.md)

При обнаружении условий ICE84 отправляет предупреждение.

## <a name="result"></a>Результат

ICE84 отправляет следующее предупреждение.



| ICE84, ошибка                                                             | Описание                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| Действие " \[ 1 \] ", найденное в таблице% s, является обязательным действием с условием. | Было создано обязательное действие с условием. |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



