---
description: Метки времени обычно включаются, когда файл подписывается с помощью средства SignTool с параметром-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Добавление меток времени в ранее подписанные файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988f63e7b5c58f5d8346d074d3ec98d31dc87443670480f7ded2e72f2272275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880234"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Добавление меток времени в ранее подписанные файлы

Метки времени обычно включаются, когда файл подписывается с помощью средства SignTool с параметром **-t** . Кроме того, метки времени можно добавлять к файлам, которые были подписаны без отметки времени. Следующая команда добавляет отметку времени к ранее подписанному файлу:

**Метка времени SignTool-t HTTPS: \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> Файл, к которому отметок времени, должен быть ранее подписан.

 

Дополнительные сведения о SignTool см. в разделе [SignTool](signtool.md).

 

 



