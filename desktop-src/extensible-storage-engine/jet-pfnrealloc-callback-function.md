---
description: 'Дополнительные сведения: функция обратного вызова JET_PFNREALLOC'
title: Функция обратного вызова JET_PFNREALLOC
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272858"
---
# <a name="jet_pfnrealloc-callback-function"></a>Функция обратного вызова JET_PFNREALLOC


_**Применимо к:** Windows | Windows Server_

## <a name="jet_pfnrealloc-callback-function"></a>Функция обратного вызова JET_PFNREALLOC

Функция JET_PFNREALLOC представляет [собой совместимый с](/cpp/c-runtime-library/reference/realloc?view=vs-2019) перераспределением обратный вызов, используемый [жетенумератеколумнс](./jetenumeratecolumns-function.md) для выделения памяти для буферов вывода.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Параметры

*пвконтекст*

Указатель контекста, переданный в [жетенумератеколумнс](./jetenumeratecolumns-function.md). Этот указатель контекста можно использовать для передачи состояния из вызывающего объекта [жетенумератеколумнс](./jetenumeratecolumns-function.md) в реализацию этого обратного вызова.

*PV*

Если значение не равно NULL, указывает указатель на блок памяти, ранее выделенный этим обратным вызовом. Если значение равно NULL, выделяется новый блок памяти запрошенного размера.

*CB*

Новый размер блока памяти в байтах. Если этот параметр имеет значение 0 (ноль) и указан блок памяти, то этот блок памяти будет освобожден.

### <a name="return-value"></a>Возвращаемое значение

Система может создать коды успеха или сбоя в результате вызова этой функции. Сведения о том, как вернуть эти коды HRESULT, см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md).

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
<td><p>Успешно</p></td>
<td><p>Если был указан ранее выделенный блок памяти и был указан новый нулевой размер, этот блок освобождается и возвращается значение NULL. Если был указан ранее выделенный блок памяти и не был указан ненулевой размер, возвращается блок памяти с перераспределением. Если блок памяти не указан, возвращается только что выделенный блок памяти указанного размера.</p></td>
</tr>
<tr class="even">
<td><p>Failure</p></td>
<td><p>Будет возвращено значение NULL. Если был предоставлен ранее выделенный блок памяти, этот блок останется выделенным.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жетенумератеколумнс](./jetenumeratecolumns-function.md)
