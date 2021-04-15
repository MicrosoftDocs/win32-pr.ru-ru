---
title: Константы Direct2D
description: Direct2D определяет следующий список констант.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654583"
---
# <a name="direct2d-constants"></a>Константы Direct2D

Следующие константы объявляются в `d2d1effectauthor.h` `d2d1.h` `d2d1_1.h` `d2d1effects_2.h` файлах заголовков,, и.

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1)
Используется при упаковке входных элементов макета. Указывает, что элементы должны упаковываться непрерывно.

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)
Допуск по умолчанию для геометрических операций спрямления.

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)
Определяет недопустимый индекс свойства.

Эта константа возвращается из [**ID2D1Properties:: жетпропертиндекс**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) , чтобы указать, что указанное именованное свойство не имеет индекса в интерфейсе свойства.

Если передать эту константу в [**ID2D1Properties:: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) или [**ID2D1Properties:: жетвалуебинаме**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), то вызов завершается ошибкой, а выходной буфер заполняется нулем.

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX)
Процессу не используйте.

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0 f)
Число НИТС, которое используется для цветового пространства sRGB или scRGB для белого SDR, или значений с плавающей точкой 1,0 f. Это значение является константой только в том случае, если цветовое пространство использует освещенность, основанную на сцене, что относится к содержимому с большим динамическим диапазоном (HDR). Если цветовая область использует светимость, связанную с отображением, то на экране должны быть запрошены белые уровни SDR.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Минимальная версия клиента | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\] |
| Минимальная версия сервера | Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\] |
| Минимальный поддерживаемый телефон | Windows Phone 8,1 \[ Windows Phone silverlight 8,1 и среда выполнения Windows приложения \] Windows Phone 8,1 \[ Windows Phone silverlight 8,1 и среда выполнения Windows Apps\] |
| Header | d2d1effectauthor. h, D2D1. h, d2d1_1. h, d2d1effects_2. h |
