---
title: DRM_HeaderSignPrivKey
description: Свойство DRM \_ хеадерсигнпривкэй содержит закрытый ключ, используемый для подписи заголовка ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey формат Windows Media
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788755"
---
# <a name="drm_headersignprivkey"></a>\_ХЕАДЕРСИГНПРИВКЭЙ DRM

Свойство **DRM \_ хеадерсигнпривкэй** содержит закрытый ключ, используемый для подписи заголовка ASF.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмдрм \_ хеадерсигнпривкэй

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Это свойство создается с помощью [**ивмдрмвритер:: женератесигнингкэйпаир**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair). Обеспечьте секрет ключа и поделитесь открытым ключом только со службой лицензирования. После установки этого ключа компонент DRM будет использовать его для подписи заголовка ASF-файла (а не заголовка DRM, который подписан с помощью значений объектов цифровых подписей, таких как DRM \_ ласигнатурепривкэй). Очевидно, **\_ хеадерсигнпривкэй DRM** не включается в заголовок файла.

Это свойство недоступно из объекта модуля чтения. Его можно задать из объекта модуля записи с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства DRM**](drm-properties.md)
</dt> </dl>

 

 




