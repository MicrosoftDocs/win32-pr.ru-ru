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
ms.openlocfilehash: f7427a28752384f6c30e050458e5844dcaedd1a7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989147"
---
# <a name="jet_pfnrealloc-callback-function"></a>Функция обратного вызова JET_PFNREALLOC


_**Применимо к:** Windows | Windows Сервером_

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

Система может создать коды успеха или сбоя в результате вызова этой функции. сведения о том, как вернуть эти коды в виде значений hresult, см. в разделе [ошибки расширенного обработчика служба хранилища](./extensible-storage-engine-errors.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>Успех</p> | <p>Если был указан ранее выделенный блок памяти и был указан новый нулевой размер, этот блок освобождается и возвращается значение NULL. Если был указан ранее выделенный блок памяти и не был указан ненулевой размер, возвращается блок памяти с перераспределением. Если блок памяти не указан, возвращается только что выделенный блок памяти указанного размера.</p> | 
| <p>Failure</p> | <p>Будет возвращено значение NULL. Если был предоставлен ранее выделенный блок памяти, этот блок останется выделенным.</p> | 



### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жетенумератеколумнс](./jetenumeratecolumns-function.md)
