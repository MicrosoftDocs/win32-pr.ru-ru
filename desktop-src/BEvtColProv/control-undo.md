---
description: Восстановите активную конфигурацию сборщика из предыдущего файла резервной копии (определяется путем возврата из текущей исходной метки времени).
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Метод Undo класса Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: e46649473da31fac09c65fcecaf44e91eba049c7ddce089d7f3c5ba9de2f8e19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589044"
---
# <a name="undo-method-of-the-control-class"></a>Метод Undo класса Control

Восстановите активную конфигурацию сборщика из предыдущего файла резервной копии (определяется путем возврата из текущей исходной метки времени). Если конфигурация была только что установлена, это означает отмену этого изменения. Последовательные вызовы будут отменяться до более ранних и более ранних конфигураций. Возвращает 1 при успешном выполнении, 0 при ошибке.

## <a name="syntax"></a>Синтаксис


```mof
Uint32 Undo(
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                       |
| Пространство имен<br/>                | корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор<br/>                                              |
| MOF<br/>                      | <dl> <dt>Бутевентколлекторвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент**](control.md)
</dt> </dl>

 

