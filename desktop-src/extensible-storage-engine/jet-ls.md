---
description: 'Дополнительные сведения: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38ddb306ee6fdcbd1eb792b2c29ca367adc0f4b88cc25dfcbdde22c2638258d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765050"
---
# <a name="jet_ls"></a>JET_LS


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_ls"></a>JET_LS

**JET_LS** тип данных содержит контекстный обработчик для локального хранилища (Ls). Этот маркер может быть связан с курсором или таблицей и может ссылаться на динамически выделенные ресурсы.

**Windows xp: JET_LS** введены в Windows xp.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Типы данных

JET_LS

Значение JET_LSNil указывает на недопустимый обработчик контекста.

### <a name="remarks"></a>Remarks

Обработчик контекста изначально связан с типом данных **JET_LS** с помощью [жетсетлс](./jetsetls-function.md). Маркер контекста можно извлечь из типа данных **JET_LS** с помощью [жетжетлс](./jetgetls-function.md).

Обработчик контекста может быть явно связан с типом данных **JET_LS** с помощью [жетжетлс](./jetgetls-function.md) с JET_bitLSReset. Кроме того, маркер контекста может быть неявно связан с типом данных **JET_LS** , когда базовый объект освобождается ядром СУБД в результате прямого или непрямого действия приложения. В неявном случае для приложения выдается обратный вызов времени выполнения, чтобы он мог очистить контекстный маркер. Дополнительные сведения о неявном разрыве связи с типом данных **JET_LS** см. в разделе [жетсетлс](./jetsetls-function.md).

С типом данных JET_LS связаны следующие флаги.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Термин</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Маркер контекста не связан с объектом.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSCursor</p></td>
<td><p>Задает или получает локальное хранилище, связанное с курсором таблицы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Задайте или получите локальное хранилище, связанное с таблицей.</p></td>
</tr>
<tr class="even">
<td><p>JET_LSNil</p></td>
<td><p>Недопустимый маркер контекста.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requirements (Требования)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista или Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>требуется Windows server 2008 или Windows server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также

[жетсетлс](./jetsetls-function.md)  
[жетжетлс](./jetgetls-function.md)
