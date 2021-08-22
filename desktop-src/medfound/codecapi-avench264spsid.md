---
description: Задает идентификатор набора параметров последовательности (SPS) в единице уровня абстракции сети SPS (NAL) потока битов H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: Свойство CODECAPI_AVEncH264SPSID (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da06e431a3747e676e3934ac9a261e1d0e1ec37e18bacf01f8a3e623c4257488
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664664"
---
# <a name="codecapi_avench264spsid-property"></a>КОДЕКАПИ \_ AVEncH264SPSID, свойство

Задает идентификатор набора параметров последовательности (SPS) в единице уровня абстракции сети SPS (NAL) потока битов H. 264.

## <a name="data-type"></a>Тип данных

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ AVEncH264SPSID**

## <a name="property-value"></a>Значение свойства

Указывает значение **\_ \_ \_ идентификатора набора параметров seq** в единице SPS NAL. Элемент синтаксиса **\_ \_ Set \_ параметра seq** определяет набор параметров последовательности. Полученный бит потока можно объединить с другими потоками-потоками для создания более длинного потока, содержащего несколько наборов параметров последовательности с разными идентификаторами SPS.

Допустимый диапазон — 0 31, как указано в спецификации H. 264/AVC.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**икодекапи**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

