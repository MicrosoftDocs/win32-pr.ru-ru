---
title: ResourceLocator. Аддоптион, метод (Всмандисп. h)
description: Добавляет дополнительные данные, необходимые для обработки запроса. Например, некоторым поставщикам WMI может потребоваться объект Ивбемконтекст или Свбемнамедвалуесет с информацией, зависящей от поставщика.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода аддоптион
- служба удаленного управления Windows метода аддоптион, объект ResourceLocator
- служба удаленного управления Windows объекта ResourceLocator, метод аддоптион
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c03e587c4884e6d9efc3b98bdd7b41b4204a783e153d9e59a400a4e4bc02a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112969"
---
# <a name="resourcelocatoraddoption-method"></a>ResourceLocator. Аддоптион, метод

Добавляет дополнительные данные, необходимые для обработки запроса. Например, некоторым поставщикам WMI может потребоваться объект [**ивбемконтекст**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) или [**свбемнамедвалуесет**](/windows/desktop/WmiSdk/swbemnamedvalueset) с информацией, зависящей от поставщика. Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Синтаксис


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*OptionName* \[ окне\]
</dt> <dd>

Имя (ключ) необязательного объекта данных.

</dd> <dt>

*OptionValue* \[ окне\]
</dt> <dd>

Значение, заданное для необязательного объекта данных.

</dd> <dt>

*мусткомпли* \[ окне\]
</dt> <dd>

Флаг, указывающий, что параметр должен быть обработан. Значение по умолчанию — **false** (0).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

**Ивсманресаурцелокатор:: аддоптион** — соответствующий метод C++.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

