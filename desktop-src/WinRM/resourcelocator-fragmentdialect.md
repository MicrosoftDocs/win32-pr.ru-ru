---
title: Свойство ResourceLocator. Фрагментдиалект (Всмандисп. h)
description: Возвращает или задает диалект языка для диалекта фрагмента ресурса, когда ResourceLocator используется в операциях с объектами сеанса, таких как Session. Get, Session. Where или Session. Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства Фрагментдиалект
- Служба удаленного управления Windows свойства Фрагментдиалект, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, свойство Фрагментдиалект
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1fe42c2bbe15c75d5f38ea47119f9649e678931
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492675"
---
# <a name="resourcelocatorfragmentdialect-property"></a>ResourceLocator. Фрагментдиалект, свойство

Возвращает или задает диалект языка для *диалекта* [*фрагмента*](windows-remote-management-glossary.md) [*ресурса*](windows-remote-management-glossary.md) , когда [**ResourceLocator**](resourcelocator.md) используется в операциях с объектами [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md). Фрагмент представляет одно свойство или часть ресурса. Вместо указания URI ресурса в операциях с объектами [**сеанса**](session.md) можно предоставить объект [**ResourceLocator**](resourcelocator.md) . Диалект указывает, какой язык XML описывает фрагмент для службы, которая реализует [протокол WS-Management](ws-management-protocol.md) и получает запрос.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Значение свойства

XML-строка, идентифицирующая язык, используемый в свойстве [**фрагментпас**](resourcelocator-fragmentpath.md) . Строка диалекта по умолчанию имеет спецификацию XPath 1,0. Дополнительные сведения см. на веб-сайте [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Комментарии

[**Ивсманресаурцелокатор:: фрагментдиалект**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) — соответствующее свойство C++.

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

 

 





