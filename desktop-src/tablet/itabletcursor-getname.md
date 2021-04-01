---
description: Извлекает имя пера планшета.
ms.assetid: 94955c04-f699-428b-b4bf-53919b61b1ab
title: 'Метод Итаблеткурсор:: Name'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b9d984d5eb711c2344ba0f9fb2dbf410a7d49bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999426"
---
# <a name="itabletcursorgetname-method"></a>Метод Итаблеткурсор:: Name

Извлекает имя пера планшета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппвсзнаме* \[ заполняет\]
</dt> <dd>

Имя пера планшета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="remarks"></a>Комментарии

Он отвечает за освобождение памяти, возвращаемой этим методом, с помощью [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итаблеткурсор**](itabletcursor.md)
</dt> <dt>

[**Интерфейс Итаблеткурсорбуттон**](itabletcursorbutton.md)
</dt> </dl>

 

