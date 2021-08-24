---
description: Действие Унрегистерфонтс удаляет сведения о регистрации установленных шрифтов из системы.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Действие Унрегистерфонтс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ec15a7a431a03d678fb2fd8c39460ea40ebbcadf3efd0c24814c84e6042fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787004"
---
# <a name="unregisterfonts-action"></a>Действие Унрегистерфонтс

Действие Унрегистерфонтс удаляет сведения о регистрации установленных шрифтов из системы.

## <a name="sequence-restrictions"></a>Ограничения последовательности

Действие [ремовефилес](removefiles-action.md) должно быть вызвано после унрегистерфонтс.

## <a name="actiondata-messages"></a>Сообщения Актиондата



| Поле | Описание данных действия |
|-------|----------------------------|
| \[1\] | Файл шрифта.                 |



 

## <a name="remarks"></a>Remarks

Действие Унрегистерфонтс выполняется, если файл, указанный в \_ столбце file [таблицы Font](font-table.md) , относится к удаляемому компоненту.

 

 



