---
description: Метод Жетобжекттекст \_ объекта свбемластеррор Возвращает текстовое представление объекта в формате MOF-файл (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: Метод SWbemLastError.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998667"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a>Свбемластеррор. Жетобжекттекст, \_ метод

Метод **жетобжекттекст \_** объекта [**свбемластеррор**](swbemlasterror.md) Возвращает текстовое представление объекта в формате [MOF-файл (MOF)](managed-object-format--mof-.md) . Этот MOF-объект можно использовать для вывода содержимого объекта. Обратите внимание, что возвращаемый MOF-текст не содержит всех сведений об объекте, но достаточно информации для компилятора MOF, чтобы иметь возможность повторно создать исходный объект. Например, не будут найдены сведения о распространяемых квалификаторах или свойствах родительского класса.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ифлагс* \[ в необязательное\]
</dt> <dd>

Этот параметр зарезервирован и должен быть равен 0 (нулю), если он указан.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха этот метод возвращает строку, содержащую выходной текст.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **жетобжекттекст \_** объект **Err** может содержать один из кодов ошибок из следующего списка.

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

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМЛАСТЕРРОР CLSID<br/>                                                        |
| IID<br/>                      | IID \_ исвбемластеррор<br/>                                                         |



 

 




