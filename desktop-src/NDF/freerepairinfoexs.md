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
ms.openlocfilehash: b75d3d3ee8ba710b0b0ed4755e5ee01309f955bcc1658145dc1d42fe3b9e1ed8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802424"
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

Тип: **[ **репаиринфоекс**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\***

Массив структур. Выделенная память, на которую указывают эти структуры, будет освобождена.

</dd> <dt>

*репаиркаунт* 
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

[**репаиринфоекс**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

