---
title: Функция Фрирепаиринфоексс (Ндаттрибутилс. h)
description: Освобождает память, выделенную внутреннему массиву структур Репаиринфоекс.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- Фрирепаиринфоексс функция NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534313"
---
# <a name="freerepairinfoexs-function"></a>Функция Фрирепаиринфоексс

Функция **фрирепаиринфоексс** освобождает память, выделенную внутреннему массиву структур [**репаиринфоекс**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) . Эта функция вызывает [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения памяти.

## <a name="syntax"></a>Синтаксис


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинфо* \[ окне\]
</dt> <dd>

Тип: **[**репаиринфоекс**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) \** _

Массив структур. Выделенная память, на которую указывают эти структуры, будет освобождена.

</dd> <dt>

_RepairCount * 
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

[**репаиринфоекс**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

