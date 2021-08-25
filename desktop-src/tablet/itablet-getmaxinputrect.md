---
description: Извлекает прямоугольник, представляющий максимальную область ввода планшета.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: 'Метод Итаблет:: Жетмаксинпутрект'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 422c64a8f5f77b354f02ab9601f7a0c888669d61783afb636816efbdc2e13b27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883544"
---
# <a name="itabletgetmaxinputrect-method"></a>Метод Итаблет:: Жетмаксинпутрект

Извлекает прямоугольник, представляющий максимальную область ввода планшета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прЦинпут* \[ заполняет\]
</dt> <dd>

Указатель на прямоугольник, представляющий максимальную область ввода планшета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Итаблет**](itablet.md)
</dt> </dl>

 

 




