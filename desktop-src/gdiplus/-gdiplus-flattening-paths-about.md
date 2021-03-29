---
description: Объект GraphicsPath сохраняет последовательность линий и B&\# 233; кривые Безье.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Сведение путей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988183"
---
# <a name="flattening-paths"></a>Сведение путей

Объект [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) хранит последовательность линий и сплайнов Безье. К контуру можно добавить несколько типов кривых (эллипсы, дуги, фундаментальные сплайны), но каждая кривая преобразуется в кривую Безье, прежде чем она будет сохранена в пути. Сведение контура состоит из преобразования каждого сплайна Безье в контуре в последовательность прямых линий.

Чтобы выполнить сведение пути, вызовите метод [**GraphicsPath:: спрямления**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) объекта [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . Метод **GraphicsPath:: спрямления** получает аргумент спрямления, указывающий максимальное расстояние между плоским путем и исходным путем. На следующем рисунке показан путь до и после спрямления.

![Иллюстрация, показывающая последовательность Соединенных сплайнов Безье синим цветом и соответствующие линии в красном](images/aboutgdip02-art32a.png)

 

 



