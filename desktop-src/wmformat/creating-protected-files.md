---
title: Создание защищенных файлов
description: Создание защищенных файлов
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Пакет SDK для формата мультимедиа, создание защищенных файлов
- Windows Пакет SDK для формата мультимедиа, защищенные файлы
- Расширенный формат систем (ASF), создание защищенных файлов
- ASF (Расширенный системный формат), создание защищенных файлов
- Расширенный формат систем (ASF), защищенные файлы
- ASF (Расширенный системный формат), защищенные файлы
- Расширенный системный формат (ASF), Вмстубдрм. lib
- ASF (Расширенный системный формат), Вмстубдрм. lib
- Вмстубдрм. lib, создание защищенных файлов
- Вмстубдрм. lib, защищенные файлы
- Управление цифровыми правами (DRM), Вмстубдрм. lib
- DRM (Управление цифровыми правами), Вмстубдрм. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5be729f04f67e1a2e4319bcc8d267c798942293c2df2ee97dcc6a559af612aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809474"
---
# <a name="creating-protected-files"></a>Создание защищенных файлов

Чтобы создать защищенные цифровые файлы мультимедиа с помощью DRM версии 1 или DRM версии 7 и более поздних, свяжите с файлом Вмстубдрм. lib, полученным от Майкрософт, и создайте объект модуля записи. Для защиты версии 1 используйте интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , чтобы задать атрибуты DRM, которые нужно применить. В версиях 7 и более поздних используйте методы интерфейса [**ивмдрмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .

В следующих разделах подробно описано, как защитить файлы.

-   [Защита файлов с помощью DRM версии 1](protecting-files-with-drm-version-1.md)
-   [Защита файлов с помощью DRM версии 7 или более поздней](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> DRM не поддерживает версию этого пакета SDK на базе x64.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Список атрибутов DRM**](drm-attribute-list.md)
</dt> <dt>

[**Свойства DRM**](drm-properties.md)
</dt> <dt>

[**Версии DRM**](drm-versions.md)
</dt> <dt>

[**Включение поддержки DRM**](enabling-drm-support.md)
</dt> <dt>

[**Получение требуемой библиотеки DRM**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**Чтение защищенных файлов**](reading-protected-files.md)
</dt> </dl>

 

 




