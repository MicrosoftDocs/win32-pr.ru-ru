---
description: Метод Item объекта Свбеммесодсет Возвращает именованный объект Свбеммесод из коллекции.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Метод Свбеммесодсет. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692699"
---
# <a name="swbemmethodsetitem-method"></a>Свбеммесодсет. Item, метод

Метод **Item** объекта [**свбеммесодсет**](swbemmethodset.md) Возвращает именованный объект [**свбеммесод**](swbemmethod.md) из коллекции.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*strName* \[ окне\]
</dt> <dd>

Обязательный. Имя извлекаемого метода.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано. Значение по умолчанию — 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения запрошенный объект [**свбеммесод**](swbemmethod.md) возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Item** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Недопустимый параметр *ифлагс* .

</dd> <dt>

**вбемеррфаилед** -2147749894
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Указанный метод не существует.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕММЕСОДСЕТ CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбеммесодсет<br/>                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбеммесодсет**](swbemmethodset.md)
</dt> <dt>

[**свбеммесод**](swbemmethod.md)
</dt> </dl>

 

 




