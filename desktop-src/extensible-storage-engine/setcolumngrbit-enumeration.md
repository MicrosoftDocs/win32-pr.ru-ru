---
description: Дополнительные сведения о перечислении Сетколумнгрбит
title: Перечисление Сетколумнгрбит
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497673"
---
# <a name="setcolumngrbit-enumeration"></a>Перечисление Сетколумнгрбит

Параметры для Жетсетколумн.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
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
<td>Нет</td>
<td>Параметры по умолчанию.</td>
</tr>
<tr class="even">
<td></td>
<td>аппендлв</td>
<td>Этот параметр используется для добавления данных в столбец типа JET_coltypLongText или JET_coltypLongBinary. Аналогичное поведение можно добиться, определив размер существующего длинного значения и указав Иблонгвалуе в псетинфо. Однако проще использовать этот грбит, так как знание размера существующего значения столбца не требуется.</td>
</tr>
<tr class="odd">
<td></td>
<td>оверврителв</td>
<td>Этот параметр используется для замены существующего длинного значения новыми предоставленными данными. При использовании этого параметра, как будто существующее длинное значение было установлено равным 0 (нулю), перед установкой новых данных.</td>
</tr>
<tr class="even">
<td></td>
<td>реверттодефаултвалуе</td>
<td>Этот параметр применим только к столбцам с тегами, разреженным или многозначным. Это приводит к тому, что столбец возвращает значение столбца по умолчанию при последующих операциях получения столбца. Все существующие значения столбцов удаляются.</td>
</tr>
<tr class="odd">
<td></td>
<td>сепарателв</td>
<td>Этот параметр используется для принудительного задания длинного значения, столбцов типа JET_coltyp. LongText или JET_coltyp. Лонгбинари, который будет храниться отдельно от оставшейся части данных записи. Обычно это происходит, когда размер длинного значения предотвращает сохранение его с помощью оставшихся данных записи. Однако этот параметр можно использовать для принудительного сохранения длинного значения. Обратите внимание, что значения long размером четыре байта меньше не могут быть разными. В таких случаях параметр игнорируется.</td>
</tr>
<tr class="even">
<td></td>
<td>сизелв</td>
<td>Этот параметр используется для интерпретации входного буфера в виде целого числа байтов, устанавливаемого в качестве длины длинного значения, описываемого значением columnid, и если оно предоставлено, порядковый номер в псетинфо- &gt; итагсекуенце. Если указанный размер больше значения существующего столбца, столбец будет расширен с помощью нулей. Если размер меньше значения существующего столбца, то значение будет обрезано.</td>
</tr>
<tr class="odd">
<td></td>
<td>уникуемултивалуес</td>
<td>Этот параметр используется, чтобы обеспечить уникальность всех значений в столбце с несколькими значениями. Этот параметр сравнивает данные исходного столбца без преобразований с другими существующими значениями столбцов, и при обнаружении дубликата возвращается ошибка. Если этот параметр задан, также нельзя указывать Аппендлв, Оверврителв и Сизелв.</td>
</tr>
<tr class="even">
<td></td>
<td>уникуенормализедмултивалуес</td>
<td>Этот параметр используется, чтобы обеспечить уникальность всех значений в столбце с несколькими значениями. Этот параметр сравнивает ключевое нормализованное преобразование данных столбца с другими аналогично преобразованными значениями столбцов, и при обнаружении дубликата возвращается ошибка. Если этот параметр задан, также нельзя указывать Аппендлв, Оверврителв и Сизелв.</td>
</tr>
<tr class="odd">
<td></td>
<td>зероленгс</td>
<td>Этот параметр используется для задания значения нулевой длины. Как правило, значение столбца устанавливается равным NULL путем передачи Кбмакс 0 (нуль). Однако для некоторых типов, например JET_coltyp. Текст, значение столбца может быть равно 0 (нулевой) длине, а не NULL, и этот параметр используется для различения длины, равной NULL, и 0 (нуль).</td>
</tr>
<tr class="even">
<td></td>
<td>интринсиклв</td>
<td>Попробуйте сохранить в записи столбцы длинных значений, даже если они превышают размер разделения по умолчанию.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[Compressed](./windows7grbits.compressed-field.md)

[Без сжатия](./windows7grbits.uncompressed-field.md)
