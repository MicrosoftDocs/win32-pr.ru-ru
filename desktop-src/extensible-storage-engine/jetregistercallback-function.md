---
description: Дополнительные сведения о функции Жетрегистеркаллбакк
title: Функция JetRegisterCallback
TOCTitle: JetRegisterCallback Function
ms:assetid: 04c82fac-ffa2-477f-b4dd-59bbf1dde3c8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269175(v=EXCHG.10)
ms:contentKeyID: 32765478
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRegisterCallback
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a13415d8174a48e7e9f33d1459ca9a0a07271421101e65236f8f03263ea2a898
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849664"
---
# <a name="jetregistercallback-function"></a>Функция JetRegisterCallback


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetregistercallback-function"></a>Функция JetRegisterCallback

Функция **жетрегистеркаллбакк** позволяет приложению настроить ядро СУБД, чтобы выдать уведомления приложению о конкретных событиях. Эти уведомления связаны с определенной таблицей и остаются в силе только до тех пор, пока экземпляр, содержащий таблицу, не завершит работу с помощью [жеттерм](./jetterm-function.md).

**Windows xp: жетрегистеркаллбакк** появился в Windows XP.

```cpp
    JET_ERR JET_API JetRegisterCallback(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_CBTYP cbtyp,
      __in          JET_CALLBACK pCallback,
      __in          void* pvContext,
      __out         JET_HANDLE* phCallbackId
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*кбтип*

Битовая маска, состоящая из причин обратного вызова, для которых приложение хочет получать уведомления.

Чтобы создать эту битовую маску, можно просто или совместно использовать допустимые причины обратного вызова из перечисления [JET_CBTYP](./jet-cbtyp.md) .

*pCallback*

Указатель функции на функцию обратного вызова для приложения.

*пвконтекст*

Задает указатель контекста, который будет передан функции обратного вызова для приложения.

*фкаллбаккид*

Возвращает маркер, который впоследствии можно использовать для отмены регистрации данной функции обратного вызова с помощью [жетунрегистеркаллбакк](./jetunregistercallback-function.md).

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Эта ошибка будет возвращена <strong>жетрегистеркаллбакк</strong> в следующих случаях:</p>
<ul>
<li><p><em>кбтип</em> равен нулю,</p></li>
<li><p><em>пкаллбакк</em> имеет значение null.</p></li>
<li><p><em>фкаллбаккид</em> имеет значение null.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении указанный обратный вызов будет зарегистрирован для данной причины обратного вызова с таблицей, связанной с данным курсором. Изменение состояния базы данных не выполняется.

В случае сбоя обратный вызов не будет зарегистрирован. Изменение состояния базы данных не выполняется.

#### <a name="remarks"></a>Remarks

Этот метод предоставляет приложению возможность связать временные обратные вызовы с таблицей в базе данных. Если приложение желает связать сохраняемые обратные вызовы с таблицей в базе данных, необходимо передать обратный вызов для [JET_TABLECREATE](./jet-tablecreate-structure.md) с помощью [жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md).

#### <a name="requirements"></a>Требования

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
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows server 2008 или Windows server 2003.</p></td>
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


#### <a name="see-also"></a>См. также

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[жеттерм](./jetterm-function.md)  
[жетунрегистеркаллбакк](./jetunregistercallback-function.md)
