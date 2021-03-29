---
description: Действие Ресолвесаурце определяет расположение источника и задает свойство SourceDir, если источник еще не был разрешен.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Действие Ресолвесаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664263"
---
# <a name="resolvesource-action"></a>Действие Ресолвесаурце

Действие Ресолвесаурце определяет расположение источника и задает свойство [**SourceDir**](sourcedir.md) , если источник еще не был разрешен.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие Ресолвесаурце должно следовать после [действия костинитиализе](costinitialize-action.md).

## <a name="actiondata-messages"></a>Сообщения Актиондата

Нет сообщений Актиондата.

## <a name="remarks"></a>Комментарии

Действие Ресолвесаурце должно быть вызвано до использования свойства [**SourceDir**](sourcedir.md) в любом выражении. Он также должен вызываться перед попыткой получить значение свойства **SourceDir** с помощью [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya). Действие Ресолвесаурце не должно выполняться, если источник недоступен, так как это может быть при удалении приложения.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Отказоустойчивость источника](source-resiliency.md)
</dt> </dl>

 

 



