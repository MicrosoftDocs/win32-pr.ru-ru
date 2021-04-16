---
description: Восстановление активной конфигурации сборщика из файла резервной копии, выбранного по метке времени.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Метод Ресторефромтиме класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650464"
---
# <a name="restorefromtime-method-of-the-control-class"></a>Метод Ресторефромтиме класса Control

Восстановление активной конфигурации сборщика из файла резервной копии, выбранного по метке времени.

## <a name="syntax"></a>Синтаксис


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Таржеттиместамплов* \[ окне\]
</dt> <dd>

Восстановите файл резервной копии по этой метке времени. Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Таржеттиместамфигх* \[ окне\]
</dt> <dd>

Восстановите файл резервной копии по этой метке времени. Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Олдтиместамплов* \[ окне\]
</dt> <dd>

Метка времени, когда была задана предыдущая конфигурация. Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась). Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Олдтиместамфигх* \[ окне\]
</dt> <dd>

Метка времени, когда была задана предыдущая конфигурация. Если значение не равно 0, включает проверку атомарности: Новая конфигурация будет применена только в том случае, если метка времени старой конфигурации совпадает (т. е. конфигурация не изменилась). Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Невтиместамплов* \[ заполняет\]
</dt> <dd>

Метка времени, когда была задана новая конфигурация, если вызов завершился успешно. Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Невтиместамфигх* \[ заполняет\]
</dt> <dd>

Метка времени, когда была задана новая конфигурация, если вызов завершился успешно. Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Оригиналтиместамплов* \[ заполняет\]
</dt> <dd>

Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз. Это Младшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Оригиналтиместамфигх* \[ заполняет\]
</dt> <dd>

Исходная метка времени, когда Восстановленная конфигурация была задана в первый раз. Это старшая часть [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*ErrorString* \[ заполняет\]
</dt> <dd>

Текстовая строка с описанием ошибки.

</dd> <dt>

*Варнингстринг* \[ заполняет\]
</dt> <dd>

Текстовая строка с предупреждениями.

</dd> <dt>

*Инфостринг* \[ заполняет\]
</dt> <dd>

Текстовая строка со сведениями о конфигурации.

</dd> <dt>

*ErrorType* \[ заполняет\]
</dt> <dd>

Тип ошибки: Обратите внимание, что 0 или отсутствует указывает на успешное выполнение.

<dt>

0
</dt> <dd>

Успешно.

</dd> <dt>

1
</dt> <dd>

неправильный формат аргумента

</dd> <dt>

2
</dt> <dd>

неверное значение аргумента

</dd> <dt>

3
</dt> <dd>

Ошибка при открытии ресурса (сокет)

</dd> <dt>

4
</dt> <dd>

Ошибка сохраняемости (запись файла)

</dd> <dt>

5
</dt> <dd>

Ошибка атомарности (старая метка времени не совпадает)

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

 

