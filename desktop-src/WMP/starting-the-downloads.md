---
title: Начало загрузки
description: Начало загрузки
ms.assetid: 0a830b11-f7e1-41da-a867-86f9ac361c0b
keywords:
- проигрыватель Windows Media интернет-магазинов, диспетчер загрузки
- Интернет-магазины, диспетчер загрузки
- Тип 2 Интернет-магазинов, диспетчер загрузки
- проигрыватель Windows Media интернет-магазинов, запуск загрузок
- Интернет-магазины, запуск загрузки
- Тип 2 Интернет-магазинов, запуск загрузок
- проигрыватель Windows Media, диспетчер загрузки
- проигрыватель Windows Media Диспетчер загрузки
- Диспетчер загрузки
- Запуск загрузок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d600bb037204b4dae1c07d8938e92eae2862460b94ef285567a8ca14144e72c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995074"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Использование диспетчера загрузки**](using-the-download-manager.md)
</dt> </dl>

 

 




