---
title: Функция Фриуиинфо (Ндаттрибутилс. h)
description: Освобождает выделенную память для внутренней структуры Уиинфо.
ms.assetid: 41d923fd-2fb3-406e-a5cf-f3ba475685f6
keywords:
- Фриуиинфо функция NDF
topic_type:
- apiref
api_name:
- FreeUiInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e2008ddabdb412c117a3cfac5f2eb5ebf1e722f5f3729fb7c8b2ee0c394c454
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939051"
---
# <a name="freeuiinfo-function"></a>Функция Фриуиинфо

Функция **фриуиинфо** освобождает выделенную для внутренней памяти память для структуры [**уиинфо**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) . Эта функция вызывает [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.

## <a name="syntax"></a>Синтаксис


```C++
VOID FreeUiInfo(
  _In_ UiInfo *pInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинфо* \[ окне\]
</dt> <dd>

Тип: **[ **уиинфо**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)\***

Структура. Выделенная память, на которую указывает эта структура, будет освобождена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**уиинфо**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

