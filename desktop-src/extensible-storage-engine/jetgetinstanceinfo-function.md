---
description: Дополнительные сведения о функции Жетжетинстанцеинфо
title: Функция Жетжетинстанцеинфо
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9dfc8bec0e6cee6e127dc99135d82db3ee3001ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478350"
---
# <a name="jetgetinstanceinfo-function"></a>Функция Жетжетинстанцеинфо


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgetinstanceinfo-function"></a>Функция Жетжетинстанцеинфо

Функция **жетжетинстанцеинфо** извлекает сведения о выполняемых экземплярах.

**Windows xp: жетжетинстанцеинфо** появился в Windows XP.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Параметры

*пЦинстанцеинфо*

Указатель на буфер, который получит количество элементов, хранящихся в *паинстанцеинфо*.

*паинстанцеинфо*

Указатель на буфер, который получит адрес первого элемента массива структур.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Эта ошибка будет возвращена <strong>жетжетинстанцеинфо</strong> в следующих случаях:</p><ul><li><p><em>пЦинстанцеинфо</em> или <em>паинстанцеинфо</em> имеют значение null.</p></li></ul> | 
| <p>JET_errOutOfMemory</p> | <p>Недостаточно памяти для обработки запроса.</p> | 



#### <a name="remarks"></a>Комментарии

Ядро СУБД выделит массив структур [JET_INSTANCE_INFO](./jet-instance-info-structure.md) . Вызывающий объект отвечает за освобождение этой памяти с помощью [жетфрибуффер](./jetfreebuffer-function.md).

Если активных экземпляров нет, **жетжетинстанцеинфо** возвратит JET_errSuccess, а *пЦинстанцеинфо* получит значение 0.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетжетинстанцеинфов</strong> (Юникод) и <strong>жетжетинстанцеинфоа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[жетфрибуффер](./jetfreebuffer-function.md)
