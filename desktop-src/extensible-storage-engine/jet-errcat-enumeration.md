---
description: 'Дополнительные сведения: перечисление JET_ERRCAT'
title: Перечисление JET_ERRCAT (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264787"
---
# <a name="jet_errcat-enumeration"></a>Перечисление JET_ERRCAT

Категория ошибки. Иерархия выглядит следующим образом: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//неправильные проблемы ввода-вывода могут быть невременными. | |--JET_errcatResource | |--JET_errcatMemory//недостаточно памяти (все варианты) | |--JET_errcatQuota | |--JET_errcatDisk//недостаточно места на диске (все варианты) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//обычно вызвано неисправностью пользователя | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a>Члены

<table>
<thead>
<tr class="header">
<th></th>
<th>Имя участника</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Неизвестно</td>
<td>Неизвестная Категория.</td>
</tr>
<tr class="even">
<td></td>
<td>Ошибка</td>
<td>Универсальная Категория.</td>
</tr>
<tr class="odd">
<td></td>
<td>Операция</td>
<td>Ошибки, которые обычно происходят в любое время из-за неконтролируемых условий. Часто временные, но не всегда. Восстановление. возможно, повторная попытка или последующее уведомление оператора.</td>
</tr>
<tr class="even">
<td></td>
<td>Аварий</td>
<td>Эта ошибка сортировки возникает только в том случае, если в ESE обнаруживается ошибка, поэтому мы не можем продолжать работу в защищенном (часто транзакционном) способе, а не в поврежденных данных, которые вызовут ошибки этой категории. Восстановление. Перезапустите экземпляр или процесс. Если проблема сохраняется, сообщите оператору.</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>Ошибки O поступают из операционной системы и выходят за пределы элемента управления ESE. Такая ошибка может быть временной, возможно, невозможной. Восстановление. Повторите попытку. Если это не разрешено, обратитесь к оператору о проблемах с диском.</td>
</tr>
<tr class="even">
<td></td>
<td>Ресурс</td>
<td>Это категория, которая указывает на одно из многих потенциальных условий нехватки ресурсов.</td>
</tr>
<tr class="odd">
<td></td>
<td>Память</td>
<td>Состояние классической нехватки памяти. Восстановление: Подождите некоторое время и повторите попытку, освободите память или закройте окно.</td>
</tr>
<tr class="even">
<td></td>
<td>Quota</td>
<td>Некоторые &quot; специализированные &quot; ресурсы находятся в пулах определенного размера, что упрощает обнаружение утечек этих ресурсов. Восстановление. может потребоваться внести небольшие изменения в код. Для обнаружения этих условий в процессе разработки приложение должно иметь только отладочное действие, например утверждение. Для розничного кода рекомендуется рассматривать эту ошибку как ошибку категории памяти и либо повторить попытку, либо освободить память, либо завершить операцию.</td>
</tr>
<tr class="odd">
<td></td>
<td>Диск</td>
<td>Недостаточно дисковых условий. Восстановление. может повторить попытку позже в случае, если освободится больше места, или попросите оператора освободить место на диске.</td>
</tr>
<tr class="even">
<td></td>
<td>Данные</td>
<td>Ошибка, связанная с данными.</td>
</tr>
<tr class="odd">
<td></td>
<td>Искажен</td>
<td>Мой жесткий диск ATE мое домашнее задание. Проблемы с классическим повреждением, часто постоянные без корректирующих действий. Восстановление: восстановление из резервной копии, возможно, операция исправления служебной программы ESE (с сохранением только тех данных, которые остались или теряются). Кроме того, в случае восстановления (Жетинит), возможно, можно выполнить восстановление, добавив возможность потери данных.</td>
</tr>
<tr class="even">
<td></td>
<td>Несогласованные</td>
<td>Это похоже на повреждение в том, что база данных и (или) файлы журнала находятся в несогласованном состоянии и не могут быть выверены друг с другом. Часто это вызвано неисправностью приложения или администратора. Восстановление: восстановление из резервной копии, возможно, операция исправления служебной программы ESE (с сохранением только тех данных, которые остались или теряются). Кроме того, в случае восстановления (Жетинит), возможно, можно выполнить восстановление, добавив возможность потери данных.</td>
</tr>
<tr class="odd">
<td></td>
<td>Фрагментации</td>
<td>Это класс ошибок, в котором был запущен некоторый сохраненный внутренний ресурс. Восстановление. для ошибок базы данных автономная дефрагментация устранит проблему, для файлов журнала _сначала_ восстановите все подключенные базы данных до чистого завершения работы, а затем удалите все файлы журналов и контрольные точки.</td>
</tr>
<tr class="even">
<td></td>
<td>API</td>
<td>Контейнер для использования и состояния.</td>
</tr>
<tr class="odd">
<td></td>
<td>Использование</td>
<td>Классическая ошибка использования. Это означает, что код клиента не передает правильные аргументы в API JET. Вероятно, эта ошибка не исчезнет с повторным выполнением. Восстановление. как правило, код клиента должен утверждать () Этот класс ошибок не возвращается, поэтому проблемы могут быть перехвачены во время разработки. В розничной торговле приложение, скорее всего, будет иметь немало вариантов, но не сможет возвращать ошибку оператору.</td>
</tr>
<tr class="even">
<td></td>
<td>Состояние</td>
<td>Это классификация различных сигналов, которые API может возвращать для описания состояния базы данных, классический случай — JET_errRecordNotFound, который может возвращаться Жетсик (), если запрошенная запись не найдена. Восстановление: не очень важно, сильно зависит от API.</td>
</tr>
<tr class="odd">
<td></td>
<td>Устаревшие.</td>
<td>Ошибка распознана как допустимая ошибка, но она не должна возвращаться этой версией API.</td>
</tr>
<tr class="even">
<td></td>
<td>Макс.</td>
<td>Максимальное значение для перечисления. Его не следует использовать.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
