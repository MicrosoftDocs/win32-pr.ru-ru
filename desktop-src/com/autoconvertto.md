---
title: аутоконвертто
description: Задает автоматическое преобразование данного класса объектов в новый класс объектов.
ms.assetid: e34b799b-0d23-4034-ba79-49e92ec4dea7
keywords:
- COM раздела реестра Аутоконвертто
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ea2b32445bb7107dcbfdc2aec8aee518fdd474674e76fdbd820265d06b6160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097054"
---
# <a name="autoconvertto"></a>аутоконвертто

Задает автоматическое преобразование данного класса объектов в новый класс объектов.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoConvertTo = value
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ SZ** , указывающее идентификатор класса объекта, в который необходимо преобразовать заданный объект или класс объектов.

Этот ключ обычно используется для автоматического преобразования файлов, созданных в более старой версии приложения, в более новую версию приложения.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**оледоаутоконверт**](/windows/desktop/api/Ole2/nf-ole2-oledoautoconvert)
</dt> <dt>

[**олежетаутоконверт**](/windows/desktop/api/Ole2/nf-ole2-olegetautoconvert)
</dt> <dt>

[**олесетаутоконверт**](/windows/desktop/api/Ole2/nf-ole2-olesetautoconvert)
</dt> </dl>

 

 




