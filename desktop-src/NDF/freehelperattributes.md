---
title: Функция Фрихелператтрибутес (Ндаттрибутилс. h)
description: Освобождает память, выделенную внутри, в массив ВСПОМОГАТЕЛЬных \_ структур атрибутов.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- Фрихелператтрибутес функция NDF
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489879"
---
# <a name="freehelperattributes-function"></a>Функция Фрихелператтрибутес

Функция **фрихелператтрибутес** освобождает память, выделенную внутри, в массив [**вспомогательных структур \_ атрибутов**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) . Эта функция вызывает [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.

## <a name="syntax"></a>Синтаксис


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинфо* \[ окне\]
</dt> <dd>

Тип: **[**вспомогательный \_ атрибут**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _

Массив структур. Выделенная память, на которую указывают эти структуры, будет освобождена.

</dd> <dt>

_HelperAttributeCount * 
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ВСПОМОГАТЕЛЬный \_ атрибут**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

