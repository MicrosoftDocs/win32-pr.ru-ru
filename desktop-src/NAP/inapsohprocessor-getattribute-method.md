---
title: Метод Инапсохпроцессор-Attribute (Наппротокол. h)
description: Извлекает тип и значение атрибута с учетом расположения атрибута.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Метод OutAttribute NAP
- Метод OutAttribute NAP, интерфейс Инапсохпроцессор
- Инапсохпроцессор интерфейса NAP, метод InAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba1b86ca1eab51fdca382a758a9a65650af2249eb0d605c24274c84d1f95669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939571"
---
# <a name="inapsohprocessorgetattribute-method"></a>Метод Инапсохпроцессор:: OutAttribute

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Метод **инапсохпроцессор:: InAttribute** Извлекает тип и значение атрибута с учетом расположения атрибута.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*аттрибутелокатион* \[ окне\]
</dt> <dd>

Расположение (индекс) атрибута, тип и значение которого необходимо получить. Значение *аттрибутелокатион* возвращается при предыдущем вызове метода [**Инапсохпроцессор:: финднекстаттрибуте**](inapsohprocessor-findnextattribute-method.md).

</dd> <dt>

*тип* \[ заполняет\]
</dt> <dd>

Указатель на структуру [**сохаттрибутетипе**](sohattributetype-enum.md) , указывающую тип атрибута в *значении*.

</dd> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Указатель на указатель на структуру [**сохаттрибутевалуе**](sohattributevalue-union.md) , которая содержит значение атрибута в соответствии с определением *типа*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Также могут возвращаться другие коды ошибок, относящиеся к COM.



| Код возврата                                                                                     | Описание                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**С \_ ОК**</dt> </dl>           | Операция успешно завершена.<br/>                                    |
| <dl> <dt>**Д \_ ACCESSDENIED**</dt> </dl> | Ошибка разрешений, доступ запрещен.<br/>                       |
| <dl> <dt>**Д \_ OUTOFMEMORY**</dt> </dl>  | Не удалось выполнить операцию из – за пределов системных ресурсов.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Наппротокол. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Наппротокол. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**инапсохпроцессор**](inapsohprocessor.md)
</dt> </dl>

 

 





