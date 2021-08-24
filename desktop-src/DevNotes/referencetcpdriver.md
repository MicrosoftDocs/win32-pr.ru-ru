---
description: Получает ссылку на объект драйвера TCP v4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: Функция Референцеткпдривер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 36329ecb695c6fcc011f7e1fe4f44a149fbeac48b0125c34330b9bde51342f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690844"
---
# <a name="referencetcpdriver-function"></a>Функция Референцеткпдривер

Получает ссылку на объект драйвера TCP v4.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдриверобжект* \[ заполняет\]
</dt> <dd>

Указатель на структуру **\_ объектов драйвера** . Дополнительные сведения см. в документации по WDK.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается успешно, возвращается **состояние \_ Success**. В случае сбоя он возвратит соответствующий код состояния.

## <a name="remarks"></a>Remarks

Эту функцию можно вызывать только из режима ядра. Вызывающий объект должен уменьшить число ссылок, вызвав функцию **обдереференцеобжект** после завершения работы с объектом.

Эта функция реализована в Дрвреф. lib, которая доступна для загрузки. см. раздел [библиотека API справочника по сетевым драйверам Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Дрвреф. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




