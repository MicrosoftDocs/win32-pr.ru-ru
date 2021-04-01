---
title: Выбор файлов
description: Выбор файлов
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- Создание обложек, выбор файлов
- Обложки проигрывателя Windows Media, выбор файлов
- обложки, выбор файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258861"
---
# <a name="choosing-files"></a>Выбор файлов

Если вы хотите выбрать файл, можно использовать код, похожий на пример списка воспроизведения, но заменить следующие сведения в разделе ПЛАЙЕЛЕМЕНТ:


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



Эта строка будет использовать метод **Опендиалог** **темы** для определения **URL-адреса** проигрывателя. Его можно использовать для выбора файлов, отсутствующих в списках воспроизведения.

Аналогичный пример рабочего **опендиалог** см. в разделе примера пакета SDK.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Руководством по созданию обложки**](skin-creation-guide.md)
</dt> </dl>

 

 




