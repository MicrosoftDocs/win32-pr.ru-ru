---
title: Начало загрузки
description: Начало загрузки
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- Интернет-магазины проигрывателя Windows Media, диспетчер загрузки
- Интернет-магазины, диспетчер загрузки
- Тип 2 Интернет-магазинов, диспетчер загрузки
- Интернет-магазины проигрывателя Windows Media, запуск загрузки
- Интернет-магазины, запуск загрузки
- Тип 2 Интернет-магазинов, запуск загрузок
- Проигрыватель Windows Media, диспетчер загрузки
- Диспетчер загрузки проигрывателя Windows Media
- Диспетчер загрузки
- Запуск загрузок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec723bd504cc511c3ca43db90f3c613a8acefd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411333"
---
# <a name="starting-the-downloads"></a>Начало загрузки

Загрузка начинается при нажатии пользователем кнопки **загрузить**. Эта кнопка называется Бтндовнлоад в коде, а функция обработчика событий для события **OnClick** называется "OnClick".

При первом скачивании сначала создается пустой объект **довнлоадколлектион** , который назначается локальной переменной.


```C++
oDLC = g_oManager.createDownloadCollection();

```



Затем функция запускает каждый из пяти элементов, загружая и сохраняющая возвращенный объект **довнлоадитем** в массиве.


```C++
g_DLI[0] = oDLC.startDownload(g_sFiles[0], g_sDLType);
g_DLI[1] = oDLC.startDownload(g_sFiles[1], g_sDLType);
g_DLI[2] = oDLC.startDownload(g_sFiles[2], g_sDLType);
g_DLI[3] = oDLC.startDownload(g_sFiles[3], g_sDLType);
g_DLI[4] = oDLC.startDownload(g_sFiles[4], g_sDLType);

```



Затем код обновляет элементы пользовательского интерфейса со сведениями о загружаемой коллекции и ее элементах загрузки.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование диспетчера загрузки**](using-the-download-manager.md)
</dt> </dl>

 

 




