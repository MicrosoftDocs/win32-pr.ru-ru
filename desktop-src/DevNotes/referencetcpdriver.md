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
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649075"
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

## <a name="remarks"></a>Комментарии

Эту функцию можно вызывать только из режима ядра. Вызывающий объект должен уменьшить число ссылок, вызвав функцию **обдереференцеобжект** после завершения работы с объектом.

Эта функция реализована в Дрвреф. lib, которая доступна для загрузки. См. раздел [Библиотека API справочника по сетевым драйверам Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Дрвреф. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ReferenceTcpDriverV6**](referencetcpdriverv6.md)
</dt> </dl>

 

 




