---
description: Указывает число последовательных кадров B между кадрами I и P по умолчанию.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Свойство Авенкмпвдефаултбпиктурекаунт (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2026ddcb6a2b4ce813bd8ba2f6144f0c4a32344
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072285"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>Авенкмпвдефаултбпиктурекаунт, свойство

Указывает число последовательных кадров B между кадрами I и P по умолчанию.

Это свойство доступно для чтения и записи.

## <a name="data-type"></a>Тип данных

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенкмпвдефаултбпиктурекаунт**

## <a name="property-value"></a>Значение свойства

Это свойство имеет линейный Диапазон значений. Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Комментарии

До Windows 8 это свойство применяется к кодировщикам видео MPEG. Начиная с Windows 8, это свойство используется кодировщиками видео MPEG, WMV и H. 264.

Если кодировщик поддерживает это свойство, его можно использовать для управления структурой групп рисунков (GOP).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Приложения Windows 2000 Professional \[ классические приложения \| UWP\]<br/>                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows 2000 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства кодека API](codec-api-properties.md)
</dt> <dt>

[**Интерфейс Икодекапи**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




