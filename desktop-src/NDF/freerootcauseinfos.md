---
title: Функция Фрируткаусеинфос (Ндаттрибутилс. h)
description: Освобождает память, выделенную внутреннему массиву структур Руткаусеинфо.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- Фрируткаусеинфос функция NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9cbd0386af86ebe5e1fdc5e6350cebfb305f44544f8822e0f2bde4d46cb55f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065244"
---
# <a name="freerootcauseinfos-function"></a>Функция Фрируткаусеинфос

Функция **фрируткаусеинфос** освобождает память, выделенную внутреннему массиву структур [**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) . Эта функция вызывает [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.

## <a name="syntax"></a>Синтаксис


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинфо* \[ окне\]
</dt> <dd>

Тип: **[ **руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

Массив структур. Выделенная память, на которую указывают эти структуры, будет освобождена.

</dd> <dt>

*руткаусекаунт* 
</dt> <dd>

Тип: **ulong**

Количество структур в массиве, на которое указывает *пинфо*.

</dd> <dt>

*бфрипоинтер* 
</dt> <dd>

Тип: **bool** .

Значение true, если массив структур также должен быть удален; в противном случае — значение false.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

