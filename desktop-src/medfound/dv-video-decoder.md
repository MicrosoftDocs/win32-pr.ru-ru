---
description: Видеодекодер Media Foundation DV — это Media Foundation преобразование, которое декодирует видео в форматах DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Видеодекодер DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808093"
---
# <a name="dv-video-decoder"></a>Видеодекодер DV

Видеодекодер Media Foundation DV — это [Media Foundation преобразование](media-foundation-transforms.md) , которое декодирует видео в форматах DV.

Декодер DV Video поддерживает следующие типы входных данных:



| Subtype                 | Описание                  |
|-------------------------|------------------------------|
| **Мфвидеоформат \_ DVC**  | Видео DVC/DV                 |
| **Мфвидеоформат \_ двхд** | HD-ДВКР (1125-60 или 1250-50) |
| **Мфвидеоформат \_ двсд** | SDL-ДВКР (525-60 или 625-50)  |
| **Мфвидеоформат \_ двсл** | SD-ДВКР (525-60 или 625-50)   |



 

Он поддерживает один тип выходных данных:



| Subtype             | Описание |
|---------------------|-------------|
| Мфвидеоформат \_ YUY2 | Видео YUY2  |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                             |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                |
| DLL<br/>                      | <dl> <dt>Mfdvdec.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Типы видеоклипов](video-media-types.md)
</dt> </dl>

 

 




