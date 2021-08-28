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
ms.openlocfilehash: 24547a7970270943546e5fcfbc026ff24be144b0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986647"
---
# <a name="jetprereadkeys-function"></a>Функция Жетпререадкэйс


_**Применимо к:** Windows | Windows Сервером_

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

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).

Ошибки ввода-вывода могут возвращаться вместе со следующими ошибками использования API:


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errInvalidGrbit</p> | <p>Грбит не был ни JET_bitPrereadForward, ни JET_bitPrereadBackward.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Передан неверный размер ключа. Ключи не могут иметь значение 0 и не превышать максимальную длину ключа для таблицы.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Передан недопустимый параметр. Это может быть вызвано значением NULL для обязательного параметра или может означать, что массив ключей не отсортирован должным образом.</p> | 



**Жетпререадкэйс** проходит внутренние страницы сбалансированного дерева, чтобы определить, какие конечные страницы содержат ключи, указанные в Ргпвкэйс/ргкбкэйс. Список конечных страниц сортируется, а затем для диапазонов страниц выводятся данные для чтения. Число страниц, которые могут быть доступны для чтения, ограничено, поэтому возможно, что не все ключи могут быть считаны. В этом случае число ключей, фактически прочитанных в Пккэйспререад, будет возвращено.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows 7.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows Server 2008 R2.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 

