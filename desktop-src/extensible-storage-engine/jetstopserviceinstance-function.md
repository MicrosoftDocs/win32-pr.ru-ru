---
description: Дополнительные сведения о функции Жетстопсервицеинстанце
title: Функция Жетстопсервицеинстанце
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74604ed5fb01e92638c0b139f5d29b95b551faef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482750"
---
# <a name="jetstopserviceinstance-function"></a>Функция Жетстопсервицеинстанце


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetstopserviceinstance-function"></a>Функция Жетстопсервицеинстанце

Функция **жетстопсервицеинстанце** готовит экземпляр к завершению.

**Windows xp:****жетстопсервицеинстанце** появился в Windows XP.  

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Выполняющийся экземпляр, используемый для вызова API.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Указанный параметр экземпляра имеет недопустимое значение (а не экземпляр, который сейчас выполняется).</p><p><strong>Windows XP:</strong>  это возвращаемое значение вводится в Windows XP.</p> | 



Если эта функция выполнена, она подготавливается к будущему завершению. Ниже приведены шаги, предпринимаемые для подготовки к завершению работы.

  - Останавливает оперативную дефрагментацию, если она запущена.

  - Запуск очистки хранилища версий.

  - Уменьшите глубину контрольной точки, начав с очистки «грязных» страниц в диспетчере буферов.

  - Предотвращение будущих вызовов большинства функций для этого экземпляра.

Если эта функция завершается ошибкой, не будет выполнен ни один из шагов подготовки к завершению работы экземпляра, поэтому изменение состояния экземпляра не выполняется.

#### <a name="remarks"></a>Комментарии

Эта функция сокращает объем работы, которую должен выполнить экземпляр при завершении, но не будет завершать экземпляр. В результате эта функция является просто оптимизацией и не является обязательной для использования. обратите внимание, что объем работы, выполненной в процессе подготовки, был меньше в Windows 2000 и Windows XP. После выполнения функции вызов функций, которые больше не разрешены, возвратит JET_errClientRequestToStopJetService. Функции, по-прежнему разрешенные после этого вызова: [жетроллбакк](./jetrollback-function.md), [жетклосетабле](./jetclosetable-function.md), [жетендсессион](./jetendsession-function.md), [жетклоседатабасе](./jetclosedatabase-function.md), [жетдетачдатабасе](./jetdetachdatabase-function.md) и [жетресетсессионконтекст](./jetresetsessioncontext-function.md).

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетклоседатабасе](./jetclosedatabase-function.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетдетачдатабасе](./jetdetachdatabase-function.md)  
[жетендсессион](./jetendsession-function.md)  
[жетресетсессионконтекст](./jetresetsessioncontext-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жеттерм](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
