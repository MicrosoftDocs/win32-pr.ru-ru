---
description: метод Подключение объекта Merge подключает модуль к дополнительному компоненту. Модуль уже должен быть объединен в базу данных или будет объединен в базу данных. Функция должна существовать до вызова этой функции.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: AutoMerge. метод Подключение (мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c28aafaac9f8224ea4f622b2e63f81d9dc458d72e98c6e22c348087794e9e7a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926674"
---
# <a name="mergeconnect-method"></a>AutoMerge. метод Подключение

метод **Подключение** объекта [**Merge**](merge-object.md) подключает модуль к дополнительному компоненту. Модуль уже должен быть объединен в базу данных или будет объединен в базу данных. Функция должна существовать до вызова этой функции.

Изменения, внесенные в базу данных, не сохраняются на диске, если метод [**клоседатабасе**](merge-closedatabase.md) не вызывается с параметром *бкоммит* , для которого задано значение **true**.

## <a name="syntax"></a>Синтаксис


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Компонент* 
</dt> <dd>

Имя компонента, уже существующего в базе данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Ошибки могут быть получены с помощью свойства [**Errors**](merge-errors.md) . Ошибки и информационные сообщения отправляются в текущий файл журнала.

### <a name="c"></a>C++

см. раздел функция [**Подключение**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Заголовок<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
