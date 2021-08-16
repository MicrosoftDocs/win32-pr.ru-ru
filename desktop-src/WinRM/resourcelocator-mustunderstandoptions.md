---
title: Свойство ResourceLocator. Мустундерстандоптионс (Всмандисп. h)
description: Возвращает или задает значение Мустундерстандоптионс для объекта ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства мустундерстандоптионс
- служба удаленного управления Windows свойства мустундерстандоптионс, объект ResourceLocator
- служба удаленного управления Windows объекта ResourceLocator, свойство мустундерстандоптионс
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a49c3af0372553c221dae902a5fdca0e026bb874f612b8e21f41e6a6870f7ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323742"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>ResourceLocator. Мустундерстандоптионс, свойство

Возвращает или задает значение **мустундерстандоптионс** для объекта [**ResourceLocator**](resourcelocator.md) . Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>Значение свойства

Указывает, что при **значении true** служба, которая реализует [протокол WS-Management](ws-management-protocol.md) , должна возвращать ошибку, если она не может обработать параметр.

## <a name="remarks"></a>Remarks

**Ивсманресаурцелокатор:: мустундерстандоптионс** — соответствующее свойство C++.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





