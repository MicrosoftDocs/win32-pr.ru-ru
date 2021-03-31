---
title: Свойство ResourceLocator. ResourceURI (Всмандисп. h)
description: Возвращает или задает URI ресурса в объекте ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- ResourceURI, свойство служба удаленного управления Windows
- ResourceURI, свойство служба удаленного управления Windows, объект ResourceLocator
- Служба удаленного управления Windows объекта ResourceLocator, свойство ResourceURI
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491580"
---
# <a name="resourcelocatorresourceuri-property"></a>ResourceLocator. ResourceURI, свойство

Возвращает или задает [*URI ресурса*](windows-remote-management-glossary.md) в объекте [**ResourceLocator**](resourcelocator.md) . Можно предоставить объект [**ResourceLocator**](resourcelocator.md) вместо указания URI ресурса в операциях объекта [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>Значение свойства

Строка, идентифицирующая ресурс. При задании универсального кода ресурса (URI) для объекта [**RESOURCELOCATOR**](resourcelocator.md) URI должен содержать только путь.

## <a name="remarks"></a>Комментарии

Ниже приведен пример правильного пути для [**resourceUri**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

Следующий путь не работает, так как он содержит ключ для конкретного экземпляра. Используйте метод [**ResourceLocator. аддселектор**](resourcelocator-addselector.md) , чтобы указать конкретный экземпляр.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**Ивсманресаурцелокатор:: resourceUri** — соответствующий метод C++.

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

 

 





