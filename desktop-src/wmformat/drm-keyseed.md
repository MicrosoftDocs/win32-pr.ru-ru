---
title: DRM_KeySeed
description: Свойство DRM \_ кэйсид содержит начальное значение ключа, которое будет использоваться в сочетании с KeyID для создания ключа.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed формат Windows Media
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46766dc5754bde33c00af250f03a54caf3c12c607ec14da858ac638a70f79baf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658974"
---
# <a name="drm_keyseed"></a>\_КЭЙСИД DRM

Свойство **DRM \_ кэйсид** содержит начальное значение ключа, которое будет использоваться в сочетании с KeyID для создания ключа.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмдрм \_ кэйсид

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Remarks

Это свойство можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). Он недоступен для объекта Reader.

Начальное значение обычно используется для защиты нескольких файлов или наборов файлов, например всех файлов, выданных сервером лицензирования, или, возможно, всех файлов определенным исполнителем. Однако KeyID уникальны для каждого файла.

Начальное значение ключа должно оставаться секретом, который является общим только для создателя содержимого и распространителя лицензий. Это значение не хранится в заголовке DRM и не является ни необходимым, ни недоступным для приложений проигрывателя DRM.

Новое начальное значение ключа можно создать с помощью метода [**ивмдрмвритер:: женератекэйсид**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) или любых других подходящих средств.

## <a name="see-also"></a>См. также

<dl> <dt>

[**Свойства DRM**](drm-properties.md)
</dt> </dl>

 

 




