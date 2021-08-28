---
description: Дополнительные сведения о функции ЖетжетинстанцемисЦинфо
title: Функция ЖетжетинстанцемисЦинфо
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07167dc0f2cad5192dc30e9897541b6619086bfc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481350"
---
# <a name="jetgetinstancemiscinfo-function"></a>Функция ЖетжетинстанцемисЦинфо


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgetinstancemiscinfo-function"></a>Функция ЖетжетинстанцемисЦинфо

Функция **жетжетинстанцемисЦинфо** получает сведения об экземпляре, в то время как экземпляр находится в режиме «в сети».

**Windows vista: жетжетинстанцемисЦинфо** появился в Windows Vista.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Определяет экземпляр базы данных, который будет использоваться для вызова API.

*пвресулт*

Указатель на буфер, который будет принимать сведения. Тип буфера зависит от *инфолевел*. Вызывающий объект отвечает за правильное согласование буфера.

*кбмакс*

Размер буфера (в байтах), переданного в *пвресулт*.

*инфолевел*

Определяет, какой тип данных будет извлечен для экземпляра, заданного *экземпляром*. Формат данных, хранящихся в *пвресулт* , зависит от *инфолевел*.

Для использования с этим параметром доступны следующие параметры.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_InstanceMiscInfoLogSignature</p> | <p><em>пвресулт</em> интерпретируется как структура <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> последовательности журнала транзакций, связанной с этим экземпляром.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>Буфер слишком мал.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Указан недопустимый <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> или недопустимое значение <em>инфолевел</em> .</p> | 



#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
