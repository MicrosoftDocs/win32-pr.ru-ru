---
title: Session.Batсвойство Читемс (Всмандисп. h)
description: Задает и возвращает количество элементов в каждом пакете перечисления.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства Батчитемс
- Служба удаленного управления Windows свойства Батчитемс, объект Session
- Объект Session служба удаленного управления Windows, свойство Батчитемс
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
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710520"
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

## <a name="remarks"></a>Комментарии

Это функция оптимизации, которая управляет частотой сетевых вызовов между клиентом и сервером. В настоящее время он используется только для перечислений. Дополнительные сведения о перечислении ресурсов см. в разделе [**Enumerate**](session-enumerate.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Session**](session.md)
</dt> <dt>

[**Перечислить**](session-enumerate.md)
</dt> <dt>

[**Enumerator. ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





