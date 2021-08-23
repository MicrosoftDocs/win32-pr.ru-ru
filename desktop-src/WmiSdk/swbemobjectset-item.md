---
description: Метод Item объекта SWbemObjectSet получает объект SWbemObject из коллекции.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Метод SWbemObjectSet. Item (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a0d357eda1098bd20e4ebc68f5b959b7ac5ffd4fb46788ffac99d1f18678d6a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857224"
---
# <a name="swbemobjectsetitem-method"></a>SWbemObjectSet. Item, метод

Метод **Item** объекта [**SWbemObjectSet**](swbemobjectset.md) получает объект [**SWbemObject**](swbemobject.md) из коллекции.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стробжектпас* 
</dt> <dd>

Обязательный. Относительный путь к объекту, который необходимо получить из коллекции. Пример: Win32 \_ LogicalDisk = "C:"

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения запрошенный объект [**SWbemObject**](swbemobject.md) возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Item** объект **Err** может содержать один из кодов ошибок, приведенных ниже.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Запрошенный элемент не найден.

</dd> </dl>

## <a name="remarks"></a>Remarks

Метод **Item** может потребовать много времени процессора, поскольку для возврата результата требуется полное перечисление по поставщику элементов набора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемобжектсет<br/>                                                         |



 

 




