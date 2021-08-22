---
description: Метод Remove объекта Свбемкуалифиерсет удаляет именованный квалификатор из коллекции.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Метод Свбемкуалифиерсет. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f4ca62276e39822964d33b58345b4718354bfd63039ec42ab30ac5daf95f6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463614"
---
# <a name="swbemqualifiersetremove-method"></a>Свбемкуалифиерсет. Remove, метод

Метод **Remove** объекта [**свбемкуалифиерсет**](swbemqualifierset.md) удаляет именованный квалификатор из коллекции.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*strName* \[ окне\]
</dt> <dd>

Обязательный. Имя удаляемого квалификатора.

</dd> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Зарезервировано. Значение по умолчанию — 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **Remove** объект **Err** может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Недопустимый параметр *ифлагс* .

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемеррнотфаунд** -2147749890 (0x80041002)
</dt> <dd>

Указанный квалификатор не существует.

</dd> <dt>

**вбемерринвалидоператион** -2147749910 (0x80041016)
</dt> <dd>

Удаление этого квалификатора недопустимо.

</dd> </dl>

## <a name="remarks"></a>Remarks

Невозможно выполнить итерацию коллекции при удалении элементов, так как при удалении элемента из коллекции указатель коллекции перемещается к следующему элементу. Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМКУАЛИФИЕРСЕТ CLSID<br/>                                                     |
| IID<br/>                      | IID \_ исвбемкуалифиерсет<br/>                                                      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**свбемкуалифиерсет**](swbemqualifierset.md)
</dt> <dt>

[**Свбемкуалифиерсет. Add**](swbemqualifierset-add.md)
</dt> </dl>

 

 




