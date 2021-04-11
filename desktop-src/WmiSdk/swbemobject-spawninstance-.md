---
description: Используйте метод Спавнинстанце \_ объекта SWbemObject для создания нового экземпляра класса.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Метод SWbemObject.SpawnInstance_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272564"
---
# <a name="swbemobjectspawninstance_-method"></a>SWbemObject. Спавнинстанце, \_ метод

Используйте метод **спавнинстанце \_** объекта [**SWbemObject**](swbemobject.md) для создания нового экземпляра класса. Текущий объект должен быть определением класса, полученным от WMI с помощью метода, такого как [**SwbemServices. Get**](swbemservices-get.md) или [**SWbemServices.Exeккуери**](swbemservices-execquery.md). Затем используйте это определение класса для создания новых экземпляров. Создайте каждый новый экземпляр локально в процессе, а затем вызовите метод [**SWbemObject. \_**](swbemobject-put-.md) Create, чтобы создать экземпляр в WMI.

> [!Note]  
> Порождение экземпляра из экземпляра поддерживается, но возвращаемый экземпляр пуст.

 

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано и должно быть равно нулю, если указано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха этот вызов возвращает объект [**SWbemObject**](swbemobject.md) , содержащий новый экземпляр класса.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **спавнинстанце \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерринкомплетекласс** -2147749920 (0x80041020)
</dt> <dd>

Текущий объект не является допустимым определением класса и не может создавать новые экземпляры. Либо он неполон, либо он не был зарегистрирован в WMI с помощью [**SWbemObject. \_ постановки**](swbemobject-put-.md).

</dd> <dt>

**вбемерриллегалоператион** -2147749918 (0x8004101E)
</dt> <dd>

Возвращается, если этот метод используется в экземпляре, а не в классе.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | IID \_ исвбемобжект<br/>                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject. размещение\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServices. Get**](swbemservices-get.md)
</dt> </dl>

 

 




