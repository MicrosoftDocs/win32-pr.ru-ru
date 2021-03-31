---
title: аутоконвертто
description: Задает автоматическое преобразование данного класса объектов в новый класс объектов.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- COM раздела реестра Аутоконвертто
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160f6591ed318ad7622e0bf3c0af5187f95d3be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887420"
---
# <a name="autoconvertto"></a>аутоконвертто

Задает автоматическое преобразование данного класса объектов в новый класс объектов.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** , указывающее идентификатор класса объекта, в который необходимо преобразовать заданный объект или класс объектов.

Этот ключ обычно используется для автоматического преобразования файлов, созданных в более старой версии приложения, в более новую версию приложения.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**оледоаутоконверт**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**олежетаутоконверт**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**олесетаутоконверт**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




