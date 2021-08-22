---
title: Свойство ResourceLocator. ResourceURI (Всмандисп. h)
description: Возвращает или задает URI ресурса в объекте ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- ResourceURI, свойство служба удаленного управления Windows
- ResourceURI, свойство служба удаленного управления Windows, объект ResourceLocator
- служба удаленного управления Windows объекта ResourceLocator, свойство ResourceURI
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
ms.openlocfilehash: 323240462dad32ba757897798b663b78b373ebb3ab3e60c3387dd7da8eef4c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642864"
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

## <a name="remarks"></a>Remarks

Ниже приведен пример правильного пути для [**resourceUri**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

Следующий путь не работает, так как он содержит ключ для конкретного экземпляра. Используйте метод [**ResourceLocator. аддселектор**](resourcelocator-addselector.md) , чтобы указать конкретный экземпляр.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**Ивсманресаурцелокатор:: resourceUri** — соответствующий метод C++.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





