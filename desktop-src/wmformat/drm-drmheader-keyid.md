---
title: DRM_DRMHeader_KeyID
description: Атрибут DRM \_ дрмхеадер \_ KEYID содержит идентификатор ключа для файла.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID формат Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336343"
---
# <a name="drm_drmheader_keyid"></a>\_Дрмхеадер \_ KeyID DRM

Атрибут **DRM \_ дрмхеадер \_ KeyID** содержит идентификатор ключа для файла.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмдрм \_ дрмхеадер \_ KeyID

## <a name="data-type"></a>Тип данных

**\_Строка типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Этот атрибут имеется только в содержимом DRM версии 7. Его можно получить с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Чтобы задать идентификатор ключа для файла с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , необходимо использовать свойство [**\_ KeyID DRM**](drm-keyid.md) .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> </dl>

 

 




