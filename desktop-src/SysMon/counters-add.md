---
title: Метод Counters. Add
description: Добавляет экземпляр Каунтеритем в коллекцию.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Добавить метод Сисмон
- Метод Add Сисмон, класс Counters
- Класс счетчиков Сисмон, метод Add
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36d2b9bdc2edc9565b1eac5ebae335e5fbad80752f572c48c0f1b05c9668de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883402"
---
# <a name="countersadd-method"></a>Метод Counters. Add

Добавляет экземпляр [**каунтеритем**](counteritem.md) в коллекцию.

## <a name="syntax"></a>Синтаксис


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*путь к файлу* \[ окне\]
</dt> <dd>

Путь к счетчику. Путь может включать имя компьютера и должно включать имя объекта производительности, имя экземпляра объекта, если указанный объект производительности поддерживает несколько экземпляров, и имя счетчика. В этой спецификации пути регистр не учитывается.

Дополнительные сведения об указании пути счетчика см. в разделе [Указание пути счетчика](/windows/desktop/PerfCtrs/specifying-a-counter-path).

</dd> </dl>

## <a name="exceptions"></a>Исключения



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип исключения</th>
<th>Условие</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System. Runtime. InteropServices. COMException</strong></td>
<td>Это исключение может быть получено по одной из следующих причин:
<ul>
<li>Указанный объект производительности не найден на компьютере. Значение Err. Number — 0xC0000BB8.</li>
<li>Не удалось найти указанный счетчик. Значение Err. Number — 0xC0000BB9.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarks

Если в параметре *PathName* указан подстановочный знак, метод **Add** создает по одному объекту [**каунтеритем**](counteritem.md) для каждого развернутого пути. Метод **Add** возвращает указатель на первый добавленный **каунтеритем**.

Если подстановочный знак приведет к дублированию счетчика, то ошибка не будет передана и дубликаты не будут созданы. Если состояние ошибки возникает до создания всех счетчиков, отображается сообщение об ошибке и оставшиеся счетчики не создаются.

Количество счетчиков, которые можно добавить, не ограничено. Однако СИСМОН будет выграфике только первые счетчики 1 024 в коллекции. Количество счетчиков, которые СИСМОН будут отображаться в отчете, не ограничено.

Чтобы получить уведомление при добавлении счетчика, реализуйте событие [онкаунтераддед](systemmonitor-oncounteradded.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                            |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Сисмон. ocx</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**каунтеритем**](counteritem.md)
</dt> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**Системмонитор. Бровсекаунтерс**](systemmonitor-browsecounters.md)
</dt> </dl>

 

