---
title: DRM_Level
description: '\_уровень DRM — это атрибут лицензии, который задается пакетом SDK для Windows Media Format при создании локальной лицензии для файлов, защищенных с помощью DRM версии 1.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level формат Windows Media
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4767f839c5d21610e7e425aea4a20a52c3cb0d8658848f578a33ca403f4ad60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848689"
---
# <a name="drm_level"></a>\_Уровень DRM

**DRM \_ Level** — это атрибут лицензии, который задается пакетом SDK Windows Media Format при создании локальной лицензии для файлов, защищенных с помощью DRM версии 1. Он содержит уровень безопасности, который должен иметь вызывающее приложение для доступа к содержимому в файле. По умолчанию используется значение 150.

## <a name="global-constant"></a>Глобальная константа

\_уровень g всзвмдрм \_

## <a name="data-type"></a>Тип данных

**ВМТ, \_ тип \_ DWORD**

## <a name="remarks"></a>Remarks

Уровень безопасности DRM приложения определяется конкретной библиотекой вмстубдрм, на которую она ссылается во время компиляции. Дополнительные сведения об этих уровнях безопасности см. [в разделе получение требуемой библиотеки DRM](obtaining-the-required-drm-library.md). Используйте [**ивмхеадеринфо:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , чтобы задать это свойство при защите файлов ASF с помощью DRM версии 1.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства DRM**](drm-properties.md)
</dt> </dl>

 

 




