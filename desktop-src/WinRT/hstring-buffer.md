---
description: Описатель изменяемого строкового буфера, который можно использовать для создания HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (HString. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692318"
---
# <a name="hstring_buffer"></a>\_БУФЕР HString

Описатель изменяемого строкового буфера, который можно использовать для создания [**HString**](hstring.md).


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Комментарии

**HString \_ BUFFER** представляет строковый буфер, который можно изменить перед преобразованием в неизменяемый [**HString**](hstring.md).

Вызовите функцию [**виндовспреаллокатестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) , чтобы создать **\_ буфер HString**. Вызовите [**виндовспромотестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) , чтобы преобразовать **\_ буфер HString** в неизменяемый [**HString**](hstring.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>HString. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**виндовспреаллокатестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**виндовспромотестрингбуффер**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
