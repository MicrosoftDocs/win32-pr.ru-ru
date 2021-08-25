---
title: Session.Batсвойство Читемс (Всмандисп. h)
description: Задает и возвращает количество элементов в каждом пакете перечисления.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства батчитемс
- служба удаленного управления Windows свойства батчитемс, объект Session
- объект Session служба удаленного управления Windows, свойство батчитемс
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59e395eb27be2b922cf9d53e40f1d8cea0fc13a5dcf7b62b95ac606ec8f3f96f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795344"
---
# <a name="sessionbatchitems-property"></a>Session.Bat, свойство Читемс

Задает и возвращает количество элементов в каждом пакете перечисления. Это значение нельзя изменить во время перечисления. Поставщик ресурсов может установить ограничение.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Session.BatchItems As long
```



## <a name="property-value"></a>Значение свойства

Указывает максимальное количество элементов, возвращаемых для каждого базового сетевого вызова службы. Значение по умолчанию равно 20.

## <a name="remarks"></a>Remarks

Это функция оптимизации, которая управляет частотой сетевых вызовов между клиентом и сервером. В настоящее время он используется только для перечислений. Дополнительные сведения о перечислении ресурсов см. в разделе [**Enumerate**](session-enumerate.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сеанс**](session.md)
</dt> <dt>

[**Перечислить**](session-enumerate.md)
</dt> <dt>

[**Enumerator. ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





