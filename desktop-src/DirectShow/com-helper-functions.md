---
description: Эти функции обеспечивают поддержку реализации интерфейса IUnknown в DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Вспомогательные функции COM (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680003"
---
# <a name="com-helper-functions"></a>Вспомогательные функции COM

Эти функции обеспечивают поддержку реализации интерфейса **IUnknown** в DirectShow.



| Функция                                               | Описание                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**ОБЪЯВЛЕНИЕ \_ IUnknown**](declare-iunknown.md)          | Объявляет три метода базового интерфейса для нового интерфейса. |
| [**GetInterface**](getinterface.md)                   | Извлекает указатель интерфейса на запрошенный клиент.               |
| [**инонделегатингункновн**](inondelegatingunknown.md) | Неделегированная версия интерфейса **IUnknown** .                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Загружает библиотеку DLL службы автоматизации (OleAut32.dll).                              |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Служебные функции](utility-functions.md)
</dt> </dl>

 

 




