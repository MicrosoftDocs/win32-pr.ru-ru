---
description: Извлекает параметры контекста по умолчанию для планшета.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: 'Метод Итаблет:: Жетдефаултконтекстсеттингс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 646756a924bd9b848f2141b796205f2cf2374140811b7dd87f8ffd64c69ee8d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119336264"
---
# <a name="itabletgetdefaultcontextsettings-method"></a>Метод Итаблет:: Жетдефаултконтекстсеттингс

Извлекает параметры контекста по умолчанию для планшета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппткс* \[ заполняет\]
</dt> <dd>

Параметры контекста по умолчанию для планшета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="remarks"></a>Remarks

Он отвечает за освобождение памяти, возвращаемой этим методом, с помощью [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

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

 

