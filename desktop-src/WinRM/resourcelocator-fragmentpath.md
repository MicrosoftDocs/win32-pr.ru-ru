---
title: Свойство ResourceLocator. Фрагментпас (Всмандисп. h)
description: Возвращает или задает путь к фрагменту или свойству ресурса, когда ResourceLocator используется в операциях с объектами сеанса, таких как Session. Get, Session. Where или Session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства фрагментпас
- служба удаленного управления Windows свойства фрагментпас, объект ResourceLocator
- служба удаленного управления Windows объекта ResourceLocator, свойство фрагментпас
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f756d669ba79ce034a9562d6cae5d58653bc60e042344306fb18aa37edfdc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121634"
---
# <a name="resourcelocatorfragmentpath-property"></a>ResourceLocator. Фрагментпас, свойство

Возвращает или задает путь к [*фрагменту*](windows-remote-management-glossary.md) или свойству [*ресурса*](windows-remote-management-glossary.md) , когда [**ResourceLocator**](resourcelocator.md) используется в операциях с объектами [**сеанса**](session.md) , таких как [**Session. Get**](session-get.md), [**Session.**](session-put.md)WHERE или [**Session. Enumerate**](session-enumerate.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Значение свойства

Строка, идентифицирующая фрагмент или свойство ресурса. Например, если ресурс является диском, а запрошенным свойством является Manufacturer, строка может содержать `Diskdrive/Manufacturer` . В тексте фрагмента учитывается регистр. В этом случае нельзя использовать `diskdrive/manufacturer` .

## <a name="remarks"></a>Remarks

**Ивсманресаурцелокатор:: фрагментпас** — соответствующее свойство C++.

Можно указать один элемент свойства массива, указав индекс массива, как показано в следующем примере. Имейте в виду, что индексация массива начинается с 1, а не 0.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



Чтобы получить весь массив, укажите имя свойства массива, как показано в следующем примере.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



## <a name="requirements"></a>Требования



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

 

 





