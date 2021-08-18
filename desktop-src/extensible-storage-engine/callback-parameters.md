---
description: 'Дополнительные сведения: параметры обратного вызова'
title: Параметры обратного вызова
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
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
ms.openlocfilehash: a9c14940ee98d4f664914794cd4ff6185b78dd04f438b982179a7ab3c5eb6504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982814"
---
# <a name="callback-parameters"></a>Параметры обратного вызова


_**Применимо к:** Windows | Windows Сервером_

## <a name="callback-parameters"></a>Параметры обратного вызова

Этот раздел содержит параметры, используемые для обратных вызовов.

*JET_paramDisableCallbacks*  
65  

Этот параметр отключает все обратные вызовы ядра СУБД к функциям, предоставляемым приложением. В основном она предназначена для поддержки служебных программ ядра СУБД и не предназначена для использования в приложении.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>Неверно</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Логическое</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>False, true</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows XP и более поздних версий</p></td>
</tr>
</tbody>
</table>


*JET_paramEnablePersistedCallbacks*  
156  

Этот параметр позволяет использовать постоянные обратные вызовы в базе данных. в выпусках до Windows Vista использование постоянных обратных вызовов было включено по умолчанию. Теперь приложения должны явно разрешить использование постоянных обратных вызовов во время выполнения с помощью этого параметра. Если этот параметр не задан, то любая операция с базой данных, которая требует вызова обратного вызова, завершится с JET_errCallbackFailed. Этот параметр не влияет на обратные вызовы, указанные во время выполнения со следующими механизмами: JET_paramRuntimeCallback, [жетрегистеркаллбакк](./jetregistercallback-function.md)или явный параметр обратного вызова для Jet API. Можно создавать элементы схемы, содержащие постоянные обратные вызовы, даже если использование этих постоянных обратных вызовов запрещено. Если этот параметр имеет значение false, он переопределяет JET_paramDisableCallbacks.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>Неверно</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Логическое</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>False, true</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows Vista и более поздние версии</p></td>
</tr>
</tbody>
</table>


*JET_paramRuntimeCallback*  
73  

Этот параметр настраивает подсистему с помощью функции обратного вызова среды выполнения, реализующей интерфейс [JET_CALLBACK](./jet-callback-callback-function.md) . Этот обратный вызов можно вызвать по следующим причинам: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)или [JET_cbtypNull](./jet-cbtyp.md). Дополнительные сведения см. в разделе [жетсетлс](./jetsetls-function.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Значение по умолчанию:</p></td>
<td><p>NULL</p></td>
</tr>
<tr class="even">
<td><p>Тип:</p></td>
<td><p>Указатель функции (JET_API_PTR)</p></td>
</tr>
<tr class="odd">
<td><p>Допустимый диапазон:</p></td>
<td><p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p></td>
</tr>
<tr class="even">
<td><p>Область.</p></td>
<td><p>Экземпляр</p></td>
</tr>
<tr class="odd">
<td><p>Задать после <a href="gg269354(v=exchg.10).md">жеткреатеинстанце</a>:</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p>Задать после <a href="gg294068(v=exchg.10).md">жетинит</a>:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на физический макет:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на надежность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>Влияет на производительность:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p>Влияет на ресурсы:</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p>"Доступность":</p></td>
<td><p>Windows XP и более поздних версий</p></td>
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
</tbody>
</table>


### <a name="see-also"></a>См. также

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетинит](./jetinit-function.md)  
[жетсетлс](./jetsetls-function.md)
