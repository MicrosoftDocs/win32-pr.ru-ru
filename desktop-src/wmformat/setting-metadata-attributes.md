---
title: Задание атрибутов метаданных
description: Задание атрибутов метаданных
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media Format SDK, задание атрибутов метаданных
- Расширенный системный формат (ASF), установка атрибутов метаданных
- ASF (Расширенный системный формат), установка атрибутов метаданных
- метаданные, задание атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412553"
---
# <a name="setting-metadata-attributes"></a>Задание атрибутов метаданных

Атрибуты метаданных задаются с помощью метода [**IWMHeaderInfo3:: аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .

Всем атрибутам назначается язык из списка языков для файла. Доступ к списку языков можно получить с помощью интерфейса [**ивмлангуажелист**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) . Чтобы получить указатель на интерфейс **ивмлангуажелист** , вызовите метод **QueryInterface** для любого интерфейса объекта, из которого получен [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).

Вы можете добавить атрибуты с любым именем. Однако использование имен атрибутов, которые не являются стандартными именами, поддерживаемыми пакетом SDK для формата Windows Media, может усложнить поиск пользователями метаданных. Большинство воспроизводимых мультимедийных приложений будут проверять стандартные значения. Дополнительные сведения см. в разделе [пользовательские метаданные](custom-metadata.md).

Нельзя использовать потоковый номер 0xFFFF для глобального добавления атрибута. Каждому атрибуту необходимо назначить конкретный номер потока или поток 0 для атрибутов на уровне файла.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Работа с метаданными**](working-with-metadata.md)
</dt> </dl>

 

 




