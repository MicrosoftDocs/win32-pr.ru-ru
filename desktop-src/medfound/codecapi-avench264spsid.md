---
description: Задает идентификатор набора параметров последовательности (SPS) в единице уровня абстракции сети SPS (NAL) потока битов H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: Свойство CODECAPI_AVEncH264SPSID (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143249"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**икодекапи**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

