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
ms.openlocfilehash: 6a96d859faa80e3e2269981d206c96e780d05c37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135519"
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

Тип: **[**уиинфо**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo) \** _

Структура. Выделенная память, на которую указывает эта структура, будет освобождена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[_ *Уиинфо**](/windows/win32/api/ndattrib/ns-ndattrib-uiinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

