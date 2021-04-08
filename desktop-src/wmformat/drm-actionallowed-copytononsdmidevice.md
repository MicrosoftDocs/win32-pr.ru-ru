---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: Атрибут DRM \_ актионалловед \_ копитононсдмидевице указывает, разрешено ли копирование содержимого на устройство, не поддерживающее SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice формат Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069596"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a>\_Актионалловед \_ копитононсдмидевице DRM

Атрибут **DRM \_ актионалловед \_ копитононсдмидевице** указывает, разрешено ли копирование содержимого на устройство, не поддерживающее SDMI.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмдрм \_ актионалловед \_ копитононсдмидевице

## <a name="data-type"></a>Тип данных

**\_bool типа \_ ВМТ**

## <a name="remarks"></a>Комментарии

Лицензии DRM для Windows Media 10 используют действие копирования для ограничения копирования на устройства. Чтобы определить, разрешено ли копирование, проверьте свойство [**\_ Актионалловед \_ Copy DRM**](drm-actionallowed-copy.md) .

Это свойство только для чтения, которое извлекается с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства DRM**](drm-properties.md)
</dt> </dl>

 

 




