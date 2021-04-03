---
description: Функция Креатенппинтерфаце использует большой двоичный объект, возвращенный из Finder, для создания НПП, который может использоваться приложением.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Функция Креатенппинтерфаце (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998787"
---
# <a name="createnppinterface-function"></a>Функция Креатенппинтерфаце

Функция **креатенппинтерфаце** использует большой двоичный объект, возвращенный из Finder, для создания НПП, который может использоваться приложением.

## <a name="syntax"></a>Синтаксис


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хблоб* \[ окне\]
</dt> <dd>

Обработчик для большого двоичного объекта, возвращенного из Finder.

</dd> <dt>

*IID* \[ в\]
</dt> <dd>

Идентификатор интерфейса, который вызывается из НПП (например,**ИРТК** или **иделайдк**).

</dd> <dt>

*ппвобжект* \[ заполняет\]
</dt> <dd>

Указатель на возвращаемый указатель на запрошенный интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.

Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Нпптулс. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




