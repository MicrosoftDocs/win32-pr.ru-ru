---
description: Возвращает строку, содержащую идентификатор самонастраивающийся для устройства планшета.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: 'Метод Итаблет:: Жетплугандплайид'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2c7028e11a7a8ec6d1e6c79c461ce05f50dfe0b4b69108f0f1527b4fbd9ba3fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041914"
---
# <a name="itabletgetplugandplayid-method"></a>Метод Итаблет:: Жетплугандплайид

Возвращает строку, содержащую идентификатор самонастраивающийся для устройства планшета.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппвсзппид* \[ заполняет\]
</dt> <dd>

Указатель на строку, содержащую идентификатор самонастраивающийся для устройства планшета.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Итаблет**](itablet.md)
</dt> </dl>

 

