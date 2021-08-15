---
title: Свойство WSMan. Error (Всмандисп. h)
description: возвращает дополнительные сведения об ошибке в потоке XML для предыдущего вызова метода WSMan, если службе служба удаленного управления Windows не удалось создать объект сеанса, объект ConnectionOptions или объект ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства ошибки
- служба удаленного управления Windows свойства ошибки, объект WSMan
- объект WSMan служба удаленного управления Windows, свойство Error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d72c99150d3c6ac95e91e6a9674ab6364e8ea46fabf3d58d50556e129933cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742199"
---
# <a name="wsmanerror-property"></a>WSMan. Error, свойство

возвращает дополнительные сведения об ошибке в потоке XML для предыдущего вызова метода [**WSMan**](wsman.md) , если службе служба удаленного управления Windows не удалось создать объект [**сеанса**](session.md) , объект [**ConnectionOptions**](connectionoptions.md) или объект [**ResourceLocator**](resourcelocator.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a>Значение свойства

XML-представление сведений об ошибке.

## <a name="requirements"></a>Requirements (Требования)



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

[**Ведущий**](wsman.md)
</dt> </dl>

 

 





