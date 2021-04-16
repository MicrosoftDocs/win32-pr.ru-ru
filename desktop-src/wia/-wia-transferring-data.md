---
description: 'Дополнительные сведения: передача данных'
ms.assetid: 34871ff4-7eb0-451b-a62b-85b632af9a47
title: Передача данных
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05d94e9e09aad121720ca491864a23f3d2d38b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692417"
---
# <a name="transferring-data"></a>Передача данных

> [!Note]  
> Эта система сценариев была заменена на уровень автоматизации службы "получение образа Windows" (WIA). См. раздел [уровень службы "получение образа Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)".

 

Используйте метод [**передачи**](-wia-iwiadispatchitem-transfer.md) объекта [**Item**](-wia-item.md) для передачи изображения или звуковых данных с устройства в файл или в буфер обмена.

Передайте путь и имя файла в качестве первого параметра для сохранения данных на диск или передайте строку "Clipboard" для передачи элемента в буфер обмена.

 

 
