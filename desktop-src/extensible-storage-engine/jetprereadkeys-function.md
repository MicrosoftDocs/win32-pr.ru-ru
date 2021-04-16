---
description: Дополнительные сведения о функции Жетпререадкэйс
title: Функция Жетпререадкэйс
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497409"
---
# <a name="jetprereadkeys-function"></a>Функция Жетпререадкэйс


_**Применимо к:** Windows | Windows Server_

## <a name="jetprereadkeys-function"></a>Функция Жетпререадкэйс

Функция **жетпререадкэйс** считывает значения ключей для повышения производительности очистки хранилища версий.

**Windows 7: функция пререадкэйс** появилась в Windows 7.

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Курсор, используемый для этого вызова.

*ргпвкэйс*

Массив указателей на ключи. Ключи можно создавать с помощью [жетмакекэй](./jetmakekey-function.md) или извлекать с помощью [жетжетбукмарк](./jetgetbookmark-function.md). Ключи должны быть отсортированы в порядке возрастания или убывания в зависимости от переданного грбит. Ключи можно сортировать с помощью memcmp.

*ргкбкэйс*

Массив длин ключей. Ргпвкэйс \[ n \] должен указывать на ключ длины ргкбкэйс \[ n\]

*ккэйс*

Количество ключей. Ргпвкэйс и Ргкбкэйс должны указывать на массив по крайней мере ккэйс элементов.

*пккэйспререад*

Возвращает число ключей, для которых фактически были выданы данные для чтения. Этот параметр может принимать значение NULL.

*грбит*

Это должен быть либо JET_bitPrereadForward, либо JET_bitPrereadBackward. Если грбит имеет JET_bitPrereadForward, ключи должны быть отсортированы в возрастающем порядке. Если грбит имеет JET_bitPrereadBackward, ключи должны быть отсортированы в порядке убывания.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

Ошибки ввода-вывода могут возвращаться вместе со следующими ошибками использования API:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Грбит не был ни JET_bitPrereadForward, ни JET_bitPrereadBackward.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Передан неверный размер ключа. Ключи не могут иметь значение 0 и не превышать максимальную длину ключа для таблицы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Передан недопустимый параметр. Это может быть вызвано значением NULL для обязательного параметра или может означать, что массив ключей не отсортирован должным образом.</p></td>
</tr>
</tbody>
</table>


**Жетпререадкэйс** проходит внутренние страницы сбалансированного дерева, чтобы определить, какие конечные страницы содержат ключи, указанные в Ргпвкэйс/ргкбкэйс. Список конечных страниц сортируется, а затем для диапазонов страниц выводятся данные для чтения. Число страниц, которые могут быть доступны для чтения, ограничено, поэтому возможно, что не все ключи могут быть считаны. В этом случае число ключей, фактически прочитанных в Пккэйспререад, будет возвращено.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows 7.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008 R2.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
</tbody>
</table>
