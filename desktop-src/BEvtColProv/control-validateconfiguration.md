---
description: Проверьте правильность текста конфигурации, не настроив его как активный. Возвращает 1 при успешном выполнении, 0 при ошибке.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Метод Валидатеконфигуратион класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990344"
---
# <a name="validateconfiguration-method-of-the-control-class"></a>Метод Валидатеконфигуратион класса Control

Проверьте правильность текста конфигурации, не настроив его как активный. Возвращает 1 при успешном выполнении, 0 при ошибке.

## <a name="syntax"></a>Синтаксис


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Конфигурация* \[ окне\]
</dt> <dd>

Проверяемая конфигурация.

</dd> <dt>

*ErrorString* \[ заполняет\]
</dt> <dd>

Когда этот метод возвращает значение, если произошла ошибка, этот параметр содержит описание ошибки проверки для операции.

</dd> <dt>

*Варнингстринг* \[ заполняет\]
</dt> <dd>

При возврате из этого метода этот параметр содержит описание любых предупреждений проверки для операции.

Текстовая строка с предупреждениями.

</dd> <dt>

*Инфостринг* \[ заполняет\]
</dt> <dd>

При возврате из этого метода этот параметр содержит набор сведений о конфигурации.

</dd> <dt>

*ErrorType* \[ заполняет\]
</dt> <dd>

Если этот метод возвращает значение, если произошла ошибка проверки, этот параметр указывает тип ошибки.

Допустимые значения:

<dt>

0
</dt> <dd>

Отсутствует аргумент.

</dd> <dt>

1
</dt> <dd>

Недопустимый формат аргумента.

</dd> <dt>

2
</dt> <dd>

Недопустимый аргумент конфигурации.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

<dl> <dt>


</dt> <dd>

0

Сбой

</dd> <dt>


</dt> <dd>

1

Успешно

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                       |
| Пространство имен<br/>                | Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор<br/>                                              |
| MOF<br/>                      | <dl> <dt>Бутевентколлекторвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемента**](control.md)
</dt> </dl>

 

 




