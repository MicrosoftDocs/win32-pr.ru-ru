---
title: ResourceLocator. Клеарселекторс, метод (Всмандисп. h)
description: Удаляет все селекторы из объекта ResourceLocator.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Клеарселекторс
- Служба удаленного управления Windows метода Клеарселекторс, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, метод Клеарселекторс
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137198"
---
# <a name="resourcelocatorclearselectors-method"></a>ResourceLocator. Клеарселекторс, метод

Удаляет все [*селекторы*](windows-remote-management-glossary.md) из объекта [**ResourceLocator**](resourcelocator.md) . Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Синтаксис


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="remarks"></a>Комментарии

**Ивсманресаурцелокатор:: клеарселекторс** — соответствующий метод C++.

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

 

 





