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
ms.openlocfilehash: fa8558cd0d04258adf89cbacdd99952cf00c6d0aa5f24ee38cca2dceb4e5478f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084344"
---
# <a name="com-helper-functions"></a>Вспомогательные функции COM

Эти функции обеспечивают поддержку реализации интерфейса **IUnknown** в DirectShow.



| Функция                                               | Описание                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**ОБЪЯВЛЕНИЕ \_ IUnknown**](declare-iunknown.md)          | Объявляет три метода базового интерфейса для нового интерфейса. |
| [**GetInterface**](getinterface.md)                   | Извлекает указатель интерфейса на запрошенный клиент.               |
| [**инонделегатингункновн**](inondelegatingunknown.md) | Неделегированная версия интерфейса **IUnknown** .                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Загружает библиотеку DLL службы автоматизации (OleAut32.dll).                              |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>комбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Служебные функции](utility-functions.md)
</dt> </dl>

 

 




