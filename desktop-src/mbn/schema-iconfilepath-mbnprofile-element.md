---
description: Содержит путь к файлу значка для соединения.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Иконфилепас (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: ea662a7519a8705818ef502f5b797f437b0f89bee649d0bde18ce6f71b099d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035822"
---
# <a name="iconfilepath-mbnprofile-element"></a>Иконфилепас (Мбнпрофиле), элемент

Элемент **иконфилепас (мбнпрофиле)** содержит путь к файлу значка для соединения.

В пользовательском интерфейсе подключения операционной системы будет отображаться этот значок, когда соединение устанавливается с помощью этого элемента.

При передаче XML для создания профиля в методе [**креатеконнектионпрофиле**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) интерфейса [**имбнконнектионпрофилеманажер**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) этот путь должен указывать на исходное расположение файла значка. При успешном создании объекта [**имбнконнектионпрофиле**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) служба мобильной широкополосной связи скопирует файл значка в внутреннее хранилище, а путь к профилю будет изменен в соответствии с этим.

Файл значка должен иметь формат .bmp с размером 32X32 пикселя.

Этот элемент представляет собой строку длиной до 1024 символов, содержащую абсолютный путь к файлу.

Элемент является необязательным.

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

Элемент **иконфилепас** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Контекст определения элемента в схеме**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> <dt>

**Возможный непосредственный родительский элемент в экземпляре схемы**
</dt> <dt>

[**мбнпрофиле**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




